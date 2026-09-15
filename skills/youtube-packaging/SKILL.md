---
name: youtube-packaging
description: "5 title + thumbnail pairs with paste-ready image prompts from a topic. Use before recording or when asked to package a video."
argument-hint: "[topic or rough title] [optional: niche, who is on camera, one data point the video proves]"
---

# YouTube Packaging

Input: a topic, and if given, the niche, who is on camera, and the one number the video proves.
Output: 5 title + thumbnail pairs, one image prompt per pair, one recommended pick.

## Steps

1. Write the video's one-sentence promise: who watches, what they get, what it costs them today.
2. Draft 5 titles. Use at least one of each: curiosity gap, fear or warning, specific result with a number.
3. For each title, write a thumbnail that adds new information. If the title states the claim, the thumbnail shows proof, scale, or consequence. Never repeat the title words in the thumbnail.
4. Write the image prompt for each thumbnail (rules below).
5. Score each pair 1-5 on click and 1-5 on deliverable. Recommend the highest sum. Reject any pair the video cannot deliver.

CRITICAL: never output a title the video cannot deliver.

## Title rules

- 45-55 characters. Put the payload in the first 40.
- Plain words. Active voice. One number or one named thing.
- No "Nobody Tells You", no "Ultimate Guide", no exclamation mark.

## Thumbnail rules

- Max 3 elements: one face or subject, one object or proof, one text block of at most 4 words.
- Text is not in the title.
- Must read at 168x94 px on a dark background.

## Image prompt rules

Write the prompt for a photo-realistic 16:9 thumbnail generator. Include, in this order: subject and expression, the one object or proof element, the text block with exact words and placement, background and two colors, framing. Add "no extra text, no logos, no watermark".

## Output format

```markdown
## Packaging: [topic]

| # | Title | Chars | Thumbnail (what it shows) | Text on image | Click | Deliver |
|---|-------|-------|---------------------------|---------------|-------|---------|
| 1 | ... | 48 | ... | "..." | 4 | 5 |

### Pick: #N
Why: one line.

### Image prompts
**#1:** [prompt]
**#2:** [prompt]
...
```

## Example

Input: `how many coding agents a 128GB Mac can run at once before it breaks; solo dev on camera; local AI niche`

| # | Title | Chars | Thumbnail | Text | Click | Deliver |
|---|-------|-------|-----------|------|-------|---------|
| 1 | I Ran 12 Coding Agents on One Mac. It Broke at 9 | 48 | Creator, wince, beside a Mac Studio; Activity Monitor with memory bar pinned red | "agent 9" | 5 | 4 |
| 2 | 128GB of RAM Is Not Enough for This | 36 | Nine terminal windows tiled on a screen, one shows a frozen cursor, creator points at it | "$4,000 Mac" | 4 | 4 |

Pick: #1. The title gives the count, the thumbnail shows the moment it failed, and the video can show both.

**#1 prompt:** Photo-realistic 16:9 YouTube thumbnail. A man in his 30s, wincing, one hand on a Mac Studio on a desk; a large monitor behind him shows Activity Monitor with the memory pressure bar pinned red. Text block bottom-left in thick white sans-serif with black outline: "agent 9". Background dark charcoal with a red rim light on the monitor edge. Medium close-up, subject on the left third, monitor fills the right. No extra text, no logos, no watermark.
