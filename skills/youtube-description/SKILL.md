---
name: youtube-description
description: "Search-or-browse call, then a full YouTube description with title check, tags, and a fixed footer. Use before upload, or when views stall and the metadata needs an audit."
argument-hint: "[title] [transcript, notes or chapter list] [optional: surface (browse | search), CTR / retention, products and links for the footer]"
---

# YouTube Description

Input: title, transcript or notes, surface and metrics if known. Output: the surface call, the title check, one paste-ready description (head, body in the surface's shape, fixed footer), tags and 3 long-tail keywords.

Source: an audit of four MrBeast uploads and eight AI teaching channels (RESEARCH.md). MrBeast
runs one byte-identical footer, one objection paragraph per video, money on top, socials at the
bottom, no chapters. Teaching channels add chapters (5 of 8) and rarely fix the footer (3 of 8).

## Steps

1. Name the buyer query. Write the exact phrase a viewer types when they need this video. If no phrase exists, the surface is browse.
2. Pick the surface. Search: the query exists and the channel can beat the top 3 results. Browse: the topic is a want, not a need, and the viewer came from the feed or a Short.
3. Check the title. Search: keyword inside the first 40 characters. Browse: keep the packaging line as is. Never keep a keyword the video does not answer in the first two minutes.
4. Write the head: the one offer for this video (sponsor, product or booking), one line, `label → url`. Money above the fold.
5. Write the objection line: name the top comment before it exists (what was estimated, not measured, or skipped). Mandatory.
6. Write the body in the surface's shape (template below), then paste the fixed footer. Never edit the footer per video. Search body line 1 is keyword + claim, line 2 is what the viewer gets.
7. List 5-10 tags and 3 long-tail keywords with a low, medium, or high competition guess. Two minutes, no more.
8. If metrics were given, name the one problem: CTR under 4% is packaging, midpoint retention is editing, no session continuation is the end screen.
9. Check: one objection line, one comment question, zero subscribe requests, no hand-written CTA inside the body.

## Rules

- One surface per video. A video that tries to win both usually wins neither.
- Long-tail beats broad. "Claude Code weekly limit reset time" beats "Claude Code tips".
- The footer never changes. A changing footer reads as a pitch; a fixed one reads as the brand.
- Browse shape: no chapters, no question block. Search shape: chapters as micro-promises (a number, a comparison, a finding).
- One `?utm_source=<video_id>` on owned links only. Business email once, at the bottom. Zero to three hashtags.
- Every video ends with an end screen that names one specific next video. Label AI-generated content in the upload settings.

## Template

```text
Surface: [search | browse]. Buyer query: "[phrase]". Title: "[title]" ([chars] chars, keyword at char [n])

[HEAD] <offer label> → <url>?utm_source=<video_id>

[BODY, browse]                          [BODY, search]
<one premise line, restates the title>  <line 1: keyword + claim>
<objection line>                        <line 2: what the viewer gets>
<sources line, only if a number is quoted>  <objection line>
<one comment question>                  ▶ CHAPTERS  0:00 <micro-promise> ...
                                        ▶ QUESTIONS ANSWERED  <4-8 the video answers>
                                        ▶ LINKS AND SOURCES  <repo first>
                                        <one comment question>
                                        #tag #tag

[FOOTER, identical on every upload]
🎓 <product 1> → <url>?utm_source=<video_id>
🧪 <product 2> → <url>?utm_source=<video_id>
💻 Code → <repo url>
🐦 X → <url>    💼 LinkedIn → <url>
📧 Sponsorship inquiries: <email>

Tags: tag1, tag2, ...   Long-tail: "[phrase]" (low) | "[phrase]" (medium) | "[phrase]" (low)
Problem to fix first: [packaging | editing | end screen | none]
```

## Example

Input: `"$20 or $100 or $200 AI plan: here's how to decide"; chapters given; CTR 3.1%`

```text
Surface: search. Buyer query: "which claude plan should I buy". Title: keyword at char 0, kept.

📞 I'll help you make the $200 plan pay back, 55 min → https://example.io/meet?utm_source=abc123

I used $300 of tokens in one day on the $100 plan. This is the decision ladder: when $20 is enough, when $100 and $200 pay for themselves, and how limit resets change the math.
The token values per plan come from a third-party estimate, not from the vendor.

▶ CHAPTERS  0:00 $300 of tokens in one day, on a $100 plan | 1:35 The full ladder: 4x the limits for 2x the price
▶ QUESTIONS ANSWERED  Is the $100 plan worth it? When should you leave the $20 plan?
▶ LINKS AND SOURCES  Prompt pack: https://github.com/example/reset-prompts
Which plan are you on, and did it pay back? Tell me in the comments.
#codex #claudecode

🎓 All courses → https://learn.example.io/courses?utm_source=abc123
💻 Code from my videos → https://github.com/example
📧 Sponsorship inquiries: hello@example.io

Tags: claude plan, claude max plan, claude pro vs max, claude code limits, ai coding plan cost
Long-tail: "claude max plan worth it" (low) | "claude pro vs max" (medium) | "claude code weekly limit" (low)
Problem to fix first: packaging. CTR sits under 4%, so the thumbnail must show the price ladder.
```
