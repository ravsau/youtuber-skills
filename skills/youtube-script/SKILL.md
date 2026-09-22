---
name: youtube-script
description: "Hook plus setup-tension-payoff script from a packaged title. Use when asked to script, open, or write the talking points for a video."
argument-hint: "[title] [key points or the number the video proves] [optional: target length]"
---

# YouTube Script

Input: a title, the key points, and if given, the target length in minutes.
Output: a timed script with a hook, one segment per key point, an end screen, and a b-roll list.

## Steps

1. Write the hook in three parts. Target: who this is for and why now, in up to 3 sentences. Transformation: the one measurable outcome, 1 sentence. Stakes: one bold claim or question, 1 sentence.
2. Place a pattern interrupt at 0:25 (cut, zoom, graphic, or music change) and name it.
3. Split the key points into segments of 60-90 seconds. Each segment has a setup (10-15 s), a tension build (40-60 s), and a payoff (10-15 s).
4. End each payoff with the next segment's setup, so there is no gap.
5. Place re-engagement beats on the MrBeast minute map: the first spectacle at 3:00, the second at 6:00, then one every 3-5 minutes after. Each beat is a new constraint, a failure, a reveal, or a format change. Minutes 3-6 run fast scene changes; after 6:00 the back half needs its own payoff, not a summary.
6. Write the end screen: one next video and the exact line that points to it.

## Rules

- The first 5 seconds show what the viewer gains or loses. No greeting, no channel intro.
- State the payoff of the title inside the first 30 seconds.
- Do not open with "today we will talk about". Show the result instead.
- Never say "this is complicated" or "bear with me" in the hook.
- Banned words: imagine, streamline, realm, game-changer, unlock, discover, skyrocket, revolutionize.
- Every segment ends with something the viewer did not have at its start.

## Output format

```markdown
## Script: "[title]"  ([N] min)

### Hook (0:00-0:30)
Target: ...
Transformation: ...
Stakes: ...
Interrupt at 0:25: ...

### Segment 1: [name] (0:30-2:00)
Setup: ...
Tension: ...
Payoff: ...

[one block per segment]

### End screen
Next video: ...
Line: "..."

### B-roll and overlays
- ...
```

## Example

Input: `Claude Code Read My Rules and Ignored Them; points: the rule it skipped, why the file loads late, the one-line fix; 6 min`

Hook. Target: You wrote an AGENTS.md. You told the agent to never touch the tests folder. It touched the tests folder. Transformation: In six minutes you will see why the file loads late and the one line that makes it hold. Stakes: The file is not broken. Your order of operations is. Interrupt at 0:25: cut to the diff where the test file changes.

Segment 1, The skip (0:30-2:00). Setup: replay the exact prompt. Tension: watch the agent read the file, then edit tests anyway. Payoff: the log line shows the rule was loaded after the plan was made.

CRITICAL: Every segment payoff must be true on screen. If the video cannot show it, cut the segment.
