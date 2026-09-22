---
name: youtube-shorts
description: "Shorts, long-form, or both for a topic, with a small calendar. Use when deciding format or planning a week of uploads."
argument-hint: "[topic or video idea] [optional: channel goal, current subs, upload capacity per week]"
---

# YouTube Shorts

Input: a topic or video idea, plus the channel goal and weekly upload capacity if known.
Output: one format call with the reason, the slices to cut, and a one-week calendar.

## Steps

1. State the viewer's job. A need with depth is long-form. A single tip or a reaction is a Short.
2. Score the topic on the trade-off table below. Pick the column that wins on the channel's current goal.
3. If long-form, list 3-6 moments that stand alone as Shorts.
4. If Shorts only, set the length, the first-second hook, and the hashtags. Write the hook in reverse (Jenny Hoyos): open on the payoff, then show how you got there. The opening line must hold both a "but" and a "then"; rewrite until it does.
5. Fill the one-week calendar within the upload capacity.

## Trade-off

| Factor | Shorts | Long-form |
|--------|--------|-----------|
| Role | Discovery | Revenue and authority |
| Audience | Cold, browsing | Warm, subscribed |
| Retention target | Loops above 100% | Above half at midpoint |
| Evergreen value | Low | High |
| Production | Low effort, high volume | High effort, fewer uploads |

## Rules

- Shorts: new niche, topic test before a long video, best moment of a long video, a tip under 60 seconds.
- Long-form: needs depth, needs ad revenue, builds authority, needs watch hours.
- Both is the default when capacity allows. Long-form first, then cut the Shorts from it.
- A Short opens on the payoff in the first second. No greeting, no context.
- Shorts rank on audio, hashtags, and loop rate. Title and description matter less.
- Swipe-away in the first 2 seconds is the filter. Target 90%+ retention; under 70% means the hook, not the topic, failed.
- Any vertical or square upload of 3 minutes or less is a Short by YouTube's rule. Cut to 2:59 or shoot horizontal if you want long-form treatment.

## Output format

```markdown
## Format: [topic]

Call: [Shorts | Long-form | Both]. Why: one line.
Long-form: [length] min, evergreen [high | medium | low]
Shorts to cut: 1. ... 2. ... 3. ...
Short spec: [length]s, hook "[first line]", hashtags #a #b #c

| Day | Format | Angle |
|-----|--------|-------|
| Mon | Long-form | ... |
| Wed | Short | ... |
```

## Example

Input: `MLX vs GGUF on the same Mac, which format is faster; goal: subscribers; capacity 1 long + 3 Shorts a week`

Call: Both. Why: the benchmark needs the full run, and the single number is a Short.
Long-form: 9 min, evergreen high
Shorts to cut: 1. the final tok/s number side by side 2. the one setting that changed the result
Short spec: 30s, hook "Same Mac, same model, but one file format ran 2x faster, then I found the one setting behind it", hashtags #mlx #gguf #localai

| Day | Format | Angle |
|-----|--------|-------|
| Mon | Long-form | MLX vs GGUF, full benchmark |
| Tue | Short | the final number |
| Thu | Short | the one setting |

CRITICAL: Never post a Short that promises a result the long-form video does not show.
