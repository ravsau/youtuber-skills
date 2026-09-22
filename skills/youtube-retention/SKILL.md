---
name: youtube-retention
description: "Timestamped fix list from a retention curve. Use when a video loses viewers and you paste the curve or the drop points."
argument-hint: "[paste the retention curve points, or describe the video and its average view duration]"
---

# YouTube Retention

Input: retention curve points or a description of the video and its average view duration.
Output: the curve shape, the problem timestamps, one cutting pattern, and a fix list in priority order.

## Steps

1. Name the curve shape. Cliff: most of the loss is in the first 30 seconds. Gradual: steady loss. Bump: a spike where viewers rewatch. Flat: holds all the way.
2. Compare the average retention with the benchmark table below and label it good, great, or a problem.
3. Audit the first 30 seconds: promise delivered by 0:05, no preamble, action started by 0:15, an interrupt at 0:25.
4. Mark each timestamp where the curve drops faster than the segments around it. Write what happens on screen there.
5. Pick one cutting pattern from the table below for the re-edit.
6. If the video runs past 8 minutes, place a payoff just after 8:00.

## Benchmarks (average retention)

| Length | Good | Great | Problem |
|--------|------|-------|---------|
| Under 5 min | 50% | 60% | Under 40% |
| 5-15 min | 40% | 50% | Under 30% |
| 15-30 min | 30% | 40% | Under 25% |
| Over 30 min | 25% | 35% | Under 20% |
| Shorts | 70% | 90% | Under 50% |

## Cutting patterns

| Pattern | Fits | Rule |
|---------|------|------|
| Progressive rhythm | Explainer | Fast cuts to 3:00, then slower with b-roll, then bursts after 8:00 |
| Contrast | Commentary | Calm 15-25 s cuts, a burst of 5-10 quick cuts every 2-3 min |
| Narrative loop | Challenge, story | Restate the premise every 2-3 min |
| Hybrid tempo | Tutorial | Cuts every 10-15 s while explaining, holds up to 40 s during examples |
| Anchor | Personal, documentary | Cut on emotional beats, hold through full statements |

## Output format

```markdown
## Retention: "[title]"
Shape: [cliff / gradual / bump / flat]. Average: [X]%, [good / great / problem] for [length].

### Drops
1. [m:ss] what happens on screen, why viewers leave
2. ...

### Pattern: [name]. Why: one line.

### Fix list
1. First 30 seconds: [rewrite]
2. [m:ss]: [fix]
3. ...

### Rewatch spike: [m:ss or none]. Clip it as a Short: [yes / no]

Hand the drops and the pattern to youtube-edit-list for the cut rows.
```

## Example

Input: `9-minute video, "MLX vs GGUF on the Same Mac"; 28% average; loses 38% by 0:30, flat to 6:00, bump at 6:40, slow fade after`

Shape: cliff, then a bump. 28% is a problem for 5-15 min (under 30%). Drops: 0:00-0:30, the creator explains what MLX is before showing a number. Pattern: hybrid tempo, it is a tutorial. Fix list: 1. open on the two tok/s numbers side by side, then explain. 2. 6:40 has the rewatch spike where the quant setting flips, clip it as a Short. 3. Move the 7:30 summary to 8:10.

CRITICAL: Every fix names a timestamp and one on-screen change. A fix without a timestamp is not a fix.
