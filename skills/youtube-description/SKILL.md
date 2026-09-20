---
name: youtube-description
description: "A full YouTube description from a title, transcript or notes, in the shape the traffic surface needs (browse or search), with a fixed footer. Use after packaging, before upload."
argument-hint: "[title] [transcript, notes or chapter list] [optional: surface (browse | search), products and links for the footer]"
---

# YouTube Description

Input: title, transcript or notes, surface if known. Output: one paste-ready description: head, body in the surface's shape, fixed footer.

Source: an audit of four MrBeast uploads and eight AI teaching channels (RESEARCH.md). MrBeast
runs one byte-identical footer, one objection paragraph per video, money on top, socials at the
bottom, no chapters. Teaching channels add chapters (5 of 8) and rarely fix the footer (3 of 8).

## Steps

1. Pick the surface. Browse: the viewer came from the feed or a Short and does not read. Search: they typed a query and read.
2. Write the head: the one offer for this video (sponsor, product or booking), one line, `label → url`. Money above the fold.
3. Write the objection line: name the top comment before it exists (what was estimated, not measured, or skipped). Mandatory.
4. Write the body in the surface's shape (template below), then paste the fixed footer. Never edit the footer per video.
5. Check: one objection line, one comment question, zero subscribe requests, no hand-written CTA inside the body.

## Rules

- The footer never changes. A changing footer reads as a pitch; a fixed one reads as the brand.
- Browse shape: no chapters, no question block. Search shape: chapters as micro-promises (a number, a comparison, a finding).
- One `?utm_source=<video_id>` on owned links only. Business email once, at the bottom. Zero to three hashtags.

## Template

```text
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
```

## Example

Input: `"$20 or $100 or $200 AI plan: here's how to decide"; search; chapters given`

```text
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
```
