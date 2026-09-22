---
name: youtube-virality-gate
description: "8-gate pre-publish check with a SHIP, FIX, or KILL verdict. Use before uploading or when asked if a video is ready."
argument-hint: "[title + thumbnail description + first 30 seconds, or a link to the script]"
---

# YouTube Virality Gate

Input: the title, the thumbnail description, the first 30 seconds, and the video length.
Output: 8 gate results, a verdict, and the fix list in priority order.

## Steps

1. Read the packaging and the opening. Ask for any missing piece before scoring.
2. Score each gate PASS or FAIL. Write the fix on every FAIL as a command.
3. Count passes and give the verdict: 8 = SHIP, 6-7 = FIX, 5 or fewer = KILL.

## Gates

| # | Gate | Passes when | Fails like |
|---|------|-------------|------------|
| 1 | Title trigger | The title opens a gap, promises a gain, or warns of a loss | "How to Set Up a Local Model" |
| 2 | Thumbnail adds | The thumbnail shows something the title does not say | Thumbnail text repeats the title |
| 3 | First 5 seconds | The viewer sees the gain or loss before any greeting | "Hey everyone, welcome back" |
| 4 | Promise kept | The video delivers exactly what the title claims | Title says "tested", video only explains |
| 5 | Retention shape | A payoff lands every 60-90 seconds and stakes rise | A 4-minute setup section with no result |
| 6 | Only you | A viewer could not get this from 50 other channels | Generic tool overview with no numbers |
| 7 | Format proven | The format has an outlier in this or an adjacent niche | Untested format, no reference |
| 8 | Creator wants it | The creator would watch it and is proud of it | "I need to upload something" |

## Rules

- One fix per failed gate, written as a command with the exact change.
- Do not soften a KILL. A low ceiling costs more than a skipped upload.
- Shorts use gates 1-4 and 6 only. Shorts verdict: 5 = SHIP, 4 = FIX, 3 or fewer = KILL.

## Output format

```markdown
## Gate: "[title]"

| # | Gate | Result | Fix |
|---|------|--------|-----|
| 1 | Title trigger | PASS | |
| 2 | Thumbnail adds | FAIL | Replace the title text with the failing memory bar |

Verdict: FIX (6/8)
Do first: ...
```

## Example

Input: `title "Running 9 Agents on a Mac Studio", thumbnail: Mac Studio with the text "9 agents", opens on the frozen terminal, 11 minutes`

| # | Gate | Result | Fix |
|---|------|--------|-----|
| 1 | Title trigger | FAIL | Add the outcome: "I Ran 9 Agents on One Mac. It Broke at 7" |
| 2 | Thumbnail adds | FAIL | Drop "9 agents". Show the red memory bar and the wince |
| 3 | First 5 seconds | PASS | |
| 4 | Promise kept | PASS | |
| 5 | Retention shape | PASS | |
| 6 | Only you | PASS | |
| 7 | Format proven | PASS | |
| 8 | Creator wants it | PASS | |

Verdict: FIX (6/8)
Do first: the title. It moves the ceiling more than the thumbnail.

CRITICAL: a verdict without a fix line for every FAIL is incomplete.
