---
name: youtube-edit-list
description: "Edit decision list from a transcript, with an optional retention curve: cuts, holds, state changes, caption chunks, chapters, and the end frame. Use when handing a rough cut to an editor or re-cutting a video that lost viewers."
argument-hint: "[timestamped transcript or rough-cut notes] [optional: retention drops from youtube-retention, target length, cutting pattern]"
---

# YouTube Edit List

Input: a timestamped transcript or rough-cut notes, plus the retention drops and cutting pattern if the video is a re-cut.
Data source: if `~/.youtube-skills/metrics/<VIDEO_ID>.json` exists (see `youtube-connect`), take the drops from its `retention.cliffs`.
Output: an edit decision list an editor can execute without watching the whole file, chapters, and the end frame.

## Steps

1. Mark the first cut. Speech or the payoff frame starts by 0:02.5. Everything before it is removed. Name the first on-screen change and its timestamp.
2. Walk the transcript in order. At every span of 8 seconds with no change of state (cut, zoom, graphic, b-roll, text, music), write one. At every span under 3 seconds with more than one change, remove one. Change of state means the viewer sees something new, not a jump cut on the same frame.
3. Apply the cutting pattern from youtube-retention if given. Otherwise pick it from the video type: tutorial is hybrid tempo, explainer is progressive rhythm, commentary is contrast.
4. If retention drops were given, treat each drop timestamp as a hard cut point: remove or move the span the retention skill named. The fix list from that skill becomes rows in this list.
5. Write the chapters. One per segment payoff, worded as a micro-promise with a number, a comparison, or a finding. Never "Intro" or "Outro".
6. Set the caption chunks: 1-5 words per screen, break on the spoken pause, keep the filler words that carry rhythm.
7. Mark the end frame. The video ends on the payoff or the pointer to the next video. No outro, no logo hold.

## Rules

- Every row names a timestamp, an action, and what the viewer sees after it. A row without a timestamp is a note, not an edit.
- Remove, do not speed up. A 1.3x segment still reads as slow.
- Hold up to 40 seconds only during a live example the viewer is reading. Hold nothing else past 15 seconds.
- Keep the mistake if it is the story. Cut it if it is only a stumble.
- Retention drops outrank pattern rules. When they conflict, the drop wins.

## Actions

| Action | Means |
|--------|-------|
| CUT | Remove the span |
| MOVE | Place the span at a new timestamp |
| B-ROLL | Cover the span with named footage or a screen |
| GFX | Add text, a number, a diagram, or a callout |
| ZOOM | Punch in on the named region |
| HOLD | Keep the span uncut, state why |

## Output format

```markdown
## Edit list: "[title]"  (rough [N] min, target [N] min)
Pattern: [name]. First change: [m:ss], [what].

| Time | Action | Detail | Viewer sees |
|------|--------|--------|-------------|
| 0:00-0:04 | CUT | greeting | opens on the two numbers side by side |
| ... | ... | ... | ... |

### Chapters
0:00 [micro-promise] | m:ss [micro-promise] | ...

### Captions
[N] words per screen, break on pauses. Style: [one line].

### End frame: [m:ss], [payoff or next-video pointer]. Nothing after it.
```

## Example

Input: `MLX vs GGUF transcript, 11:20 rough; retention drops: 0:00-0:30 explains MLX before any number, 7:30 summary; pattern hybrid tempo; target 9:00`

Pattern: hybrid tempo. First change: 0:02, the two tok/s numbers appear side by side.

| Time | Action | Detail | Viewer sees |
|------|--------|--------|-------------|
| 0:00-0:28 | CUT | MLX definition | the result first, definition moves to 1:10 as GFX |
| 0:02 | GFX | "MLX 48 tok/s vs GGUF 24 tok/s" | the gap the title promised |
| 3:10-3:48 | HOLD | live quant setting change | the setting flips, number changes on screen |
| 6:40 | ZOOM | terminal output | the line that doubled the speed |
| 7:30-8:05 | MOVE | summary to 8:10 | payoff lands after the 8-minute mark |

Chapters: 0:00 2x faster on the same Mac | 1:10 What MLX changes | 3:10 The one setting | 6:40 Why it doubled | 8:10 Which to pick
End frame: 8:55, side-by-side numbers with the next-video card. Nothing after it.

CRITICAL: Never add a row the transcript cannot support. If the footage does not exist, write "SHOOT: [what]" instead of B-ROLL.
