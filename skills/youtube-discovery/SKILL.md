---
name: youtube-discovery
description: "Search-or-browse call plus title, description, and tag changes for a video or channel. Use when views stall or before upload."
argument-hint: "[video title + topic, or channel name + 'audit'] [optional: CTR, retention, current traffic source]"
---

# YouTube Discovery

Input: a video title and topic, or a channel name, plus any metrics the user has.
Output: one surface to win on, the title/description/tags to use, and 3 long-tail keywords.

## Steps

1. Name the buyer query. Write the exact phrase a viewer types when they need this video. If no phrase exists, the surface is browse.
2. Pick the surface. Search when the query exists and the channel can answer it better than the top 3 results. Browse when the topic is a want, not a need.
3. Rewrite the title. Search: keyword inside the first 40 characters. Browse: the packaging line from the packaging skill.
4. Write the first three description lines: line 1 keyword + claim, line 2 what the viewer gets, line 3 the second keyword. The full body and footer come from the youtube-description skill, in this surface's shape.
5. List 5-10 tags and 3 long-tail keywords with a low, medium, or high competition guess.
6. If metrics were given, name the one problem: CTR is a packaging problem, midpoint retention is an editing problem, no session continuation is an end-screen problem.

## Rules

- One surface per video. A video that tries to win both usually wins neither.
- Long-tail beats broad. "Claude Code weekly limit reset time" beats "Claude Code tips".
- Tags help topic matching only. Never spend more than two minutes on them.
- Every video ends with an end screen that names one specific next video.
- Label AI-generated content in the upload settings.

## Output format

```markdown
## Discovery: "[title]"

Surface: [search | browse]. Why: one line.
Buyer query: "[phrase]"

Title: "[rewritten title]" ([chars] chars, keyword at char [n])
Description, first 3 lines:
1. ...
2. ...
3. ...
Tags: tag1, tag2, ...
Long-tail: "[phrase]" (low) | "[phrase]" (medium) | "[phrase]" (low)
Problem to fix first: [packaging | editing | end screen | none]
```

## Example

Input: `"Claude Code Weekly Limit Reset: Exact Time and What to Do Before It"; CTR 3.1%, midpoint retention 58%`

Surface: search. Why: viewers type this the moment they hit the wall.
Buyer query: "claude code weekly limit reset time"

Title: "Claude Code Weekly Limit Reset Time (And What to Do Before It)" (61 chars, keyword at char 0)
Description, first 3 lines:
1. Claude Code weekly limit reset time, shown from the usage panel.
2. What to finish before the reset and what to leave for after.
3. Works on Pro and Max plans, checked this week.
Tags: claude code, claude code weekly limit, claude code usage limit, claude code reset, anthropic claude plans
Long-tail: "claude code limit reset time" (low) | "claude code usage limit explained" (medium) | "claude code max plan limit" (low)
Problem to fix first: packaging. CTR sits under 4%, so the thumbnail must show the reset clock.

CRITICAL: Never put a keyword in the title that the video does not answer inside the first two minutes.
