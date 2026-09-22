---
name: youtube-connect
description: "Connect a YouTube channel so the other skills read real numbers instead of pasted ones. Sets up read-only Google API access with the browser, then pulls views, impressions, CTR, average view duration, the retention curve, and comments. Use when asked to connect YouTube, pull metrics, or get the retention curve."
argument-hint: "[setup | pull VIDEO_ID | pull --recent 20 | comments VIDEO_ID]"
---

# YouTube Connect

Input: a Google account that owns the channel. For a pull, a video ID or a count of recent uploads.
Output: read-only API access saved once, then a `metrics/<VIDEO_ID>.json` per video that the other skills read.

This skill ships no code. The agent writes one short script in the user's own folder when needed, shows it, and runs it. Both scopes are read-only. Nothing in this flow can edit, upload, or delete a video.

## Step 1: Google Cloud setup (browser, once)

Drive the Cloud Console with a browser or computer-use tool. Stop at any Google sign-in page and ask the user to sign in. Never type a password. Without a browser tool, give this list as text.

1. Open `console.cloud.google.com/projectcreate`. Name the project `youtube-skills`. Create it and select it.
2. Open `console.cloud.google.com/apis/library`. Enable **YouTube Data API v3** and **YouTube Analytics API**.
3. Open `console.cloud.google.com/auth/overview`. Audience **External**. App name `youtube-skills`. The user's email as both contacts. Save.
4. Open `console.cloud.google.com/auth/audience`. Add the user's email under Test users. Keep the app in Testing. Do not publish it.
5. Open `console.cloud.google.com/auth/clients`. Create a client of type **Desktop app**. Download the JSON.
6. Save the download as `~/.youtube-skills/client_secret.json`.

Confirm with a screenshot of the Clients page. Print the saved path.

## Step 2: Authorize (terminal, once)

Write `youtube_auth.py` in the user's folder with these facts. Show it before you run it.

- Packages: `google-api-python-client`, `google-auth-oauthlib`.
- Scopes: `https://www.googleapis.com/auth/youtube.readonly` and `https://www.googleapis.com/auth/yt-analytics.readonly`.
- Flow: `InstalledAppFlow.from_client_secrets_file(...).run_local_server(port=0, prompt="consent")`.
- Save the token as `~/.youtube-skills/token.json` with mode 600. Refresh it with `Request()` on later runs.
- Print the channel from `youtube.channels().list(part="snippet,statistics,contentDetails", mine=True)`.

The user picks the account or brand channel in the chooser and clicks **Allow**. Google shows an "unverified app" screen for Testing apps. Tell the user to click **Continue**. If the printed channel is wrong, delete the token and run again.

## Step 3: Pull (terminal, any time)

Write `youtube_pull.py` in the same folder. Every call uses `ids="channel==<CHANNEL_ID>"`, `startDate` = publish date, `endDate` = today, `filters="video==<VIDEO_ID>"`.

| Want | API | Call |
|------|-----|------|
| Recent uploads | Data v3 | `playlistItems.list` on `contentDetails.relatedPlaylists.uploads` |
| Title, duration, publish date | Data v3 | `videos.list(part="snippet,contentDetails,statistics")` |
| Views, AVD, AVD %, subs, likes, comments, shares | Analytics v2 | `metrics="views,averageViewDuration,averageViewPercentage,subscribersGained,likes,comments,shares"` |
| Impressions, CTR, traffic split | Analytics v2 | `metrics="views,impressions,impressionsClickThroughRate"`, `dimensions="insightTrafficSourceType"` |
| Retention curve, 101 points | Analytics v2 | `metrics="audienceWatchRatio,relativeRetentionPerformance"`, `dimensions="elapsedVideoTimeRatio"`, `sort="elapsedVideoTimeRatio"` |
| Comments | Data v3 | `commentThreads.list(part="snippet", videoId=..., order="relevance", maxResults=100)` |

Write `~/.youtube-skills/metrics/<VIDEO_ID>.json` with: title, duration, publish date, window, views, impressions, CTR, AVD, AVD %, subscribers gained, likes, comments, shares, traffic sources, the curve, and `retention` with watch ratio at 0:30, 25%, 50%, 75%, end, plus the 3 steepest non-overlapping 5-point drops as timestamps. Write `channel.json` with the channel name, subscribers, median views, and one row per video. Print a 4-line summary per video.

## Hand off

- `youtube-retention`: reads `retention` and `curve`. No paste needed.
- `youtube-channel-audit`: reads `channel.json`. Median and outliers come from real views.
- `youtube-description`: reads `traffic_sources` to make the search-vs-browse call.
- `youtube-comments-to-ideas`: reads the fetched comments.

## Rules

- Analytics data exists only for channels the signed-in account owns. Competitor numbers still come from public Data API fields or a paste.
- Impressions, CTR, and the curve return no rows for videos under 48 hours old or with very few views. Say "not returned". Never write zero.
- Data API quota is 10,000 units per day. Twenty videos with comments cost about 60 units. Analytics calls cost no Data API quota.
- Keep the token and client secret under the home directory. Never inside a repo. Add `client_secret.json` and `token.json` to `.gitignore` if the user moves them.
- Mark every number with its window. Studio may differ by a few percent from the API for the last 2 days.

## Common errors

| Error | Fix |
|-------|-----|
| `access_denied`, "app has not completed verification" | The email is not a test user. Redo Step 1, item 4. |
| `invalid_client` | Wrong client type. Redo Step 1, item 5 with type Desktop app. |
| `accessNotConfigured` | An API is not enabled. Redo Step 1, item 2. |
| `insufficientPermissions` on a curve query | The token has one scope only. Delete the token and redo Step 2. |
| Wrong channel printed | The user picked the personal account. Delete the token and pick the brand account. |

## Example

Input: `pull dQw4w9WgXcQ`

Output:

```
Saved ~/.youtube-skills/metrics/dQw4w9WgXcQ.json
"MLX vs GGUF on the Same Mac"  9:12  published 2026-08-30  window 2026-08-30..2026-09-21
views 4,210  impressions 61,300  CTR 5.4%  AVD 2:34 (28%)  subs +41
retention: 0:30 62%  25% 41%  50% 30%  75% 22%  end 14%
cliffs: 0:04-0:31 (-38 pts)  6:40-7:05 (-6 pts)  8:50-9:12 (-5 pts)
```
