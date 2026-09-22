---
name: youtube-channel-audit
description: "Channel-page and upload-history audit with a top-20% publish bar, views per subscriber, and one fix per surface. Use when growth stalls, before a relaunch, or when asked to audit a channel."
argument-hint: "[channel name or URL] [last 10-20 uploads: title, views, date] [optional: subs, banner text, trailer title, playlists, bio]"
---

# YouTube Channel Audit

Input: the channel, its last 10-20 uploads with views and dates, and the channel page elements if known.
Output: the publish bar, the outlier variable to test next, one fix per channel surface, and a 30-day order of work.

## Steps

1. Compute the baseline. Median views of the last 10-20 uploads, not the mean. Mark every video above 3x median as an outlier and every video under 0.5x as a miss.
2. Set the publish bar. Galloway's rule: never publish a video you would not rank in the channel's top 20%. Name the view count that marks the top 20% today. Every future packaging pick is judged against it.
3. Isolate the outlier variable. For each outlier, name the one thing that differs from the baseline: topic, title shape, thumbnail type, format, or timing. If two variables differ, the test is invalid; say so. Pick the single variable to repeat next.
4. Compute views per subscriber for the last 10 uploads (views divided by subs at upload). Under 0.1 means the channel is fed by subscribers only. Above 1.0 means browse or search is carrying it. State which.
5. Audit the channel page, one line each: banner (says who it is for and what they get), trailer (an outlier, not the newest upload), bio (buyer question in the first line), playlists (one per lane, outlier first), links (one offer at the top).
6. Write the 30-day order: the one variable to test, the one page fix, the one upload to remove or unlist if it drags the median.

## Rules

- Median beats mean. One viral video hides nine misses in a mean.
- One variable per test. A new topic with a new thumbnail style proves nothing.
- The trailer is the best proof the channel has, not the latest video.
- A miss is only worth unlisting if it is under 0.3x median and older than 90 days. Do not delete; unlist.
- Mark every number that comes from an estimate, not from Studio or a supplied export.

## Output format

```markdown
## Audit: [channel]

Baseline: median [N] views over [K] uploads. Top-20% bar: [N] views.
Outliers: "[title]" [Nx], variable: [topic | title | thumbnail | format | timing]
Misses: "[title]" [0.Nx], "[title]" [0.Nx]
Views per subscriber: [0.NN]. Fed by: [subscribers | browse | search]

| Surface | Now | Fix |
|---------|-----|-----|
| Banner | ... | ... |
| Trailer | ... | ... |
| Bio | ... | ... |
| Playlists | ... | ... |
| Links | ... | ... |

### 30 days
1. Test: repeat [variable] in the next upload. Pass if it clears [N] views in 7 days.
2. Page: [one fix]
3. Clean: unlist "[title]" | none
```

## Example

Input: `CloudYeti; 12 uploads, median 4,100 views; "I Ran 12 Coding Agents on One Mac" 31,000; "Kubernetes Basics Part 3" 900; 41,000 subs; trailer is the newest upload`

Baseline: median 4,100 views over 12 uploads. Top-20% bar: 9,500 views.
Outliers: "I Ran 12 Coding Agents on One Mac" 7.6x, variable: format (a live limit test, the rest are explainers).
Misses: "Kubernetes Basics Part 3" 0.2x.
Views per subscriber: 0.10. Fed by: subscribers.

Trailer: newest upload, 3,200 views. Fix: swap to the 12-agents video.
30 days: 1. Test: one more live limit test, same thumbnail style, new topic. Pass if it clears 9,500 in 7 days. 2. Page: trailer swap. 3. Clean: unlist "Kubernetes Basics Part 3", 0.2x and 14 months old.

CRITICAL: Never recommend a page change before the publish bar is set. The page follows the videos, not the other way.
