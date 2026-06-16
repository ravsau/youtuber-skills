---
name: virality-gate
description: "Pre-publish quality gate with 8 checks every video must pass. Kill weak videos before they hurt your channel. Based on MrBeast, Paddy Galloway, and algorithm research. Use before publishing any video."
argument-hint: "[video title, or describe the video you're about to publish]"
---

# Virality Gate — Pre-Publish Quality Check

Evaluate: **$ARGUMENTS**

## The Stakes

In the 2026 algorithm, your channel is evaluated as a WHOLE. One weak video doesn't just flop — it signals to the algorithm that your channel is inconsistent. Kill weak videos before they go live.

"The idea sets the ceiling, the execution determines the result." (Paddy Galloway)

If the ceiling is low, no amount of execution saves it.

## Pre-Check: Is This Data-Dependent?

Before scoring, decide whether the answer needs research.

- **Specific channel/video/niche/trend**: inspect data first. Look at current competitors, outliers, title/thumbnail patterns, search/trend signals, and any available CTR/AVD/retention numbers.
- **Pure framework question**: score directly using the gates.
- **Mixed question**: get the facts for the specific case, then apply the gates.

If the user asks "will this work?" with no numbers, request or assume explicit targets: CTR, AVD, 30-second retention, completion rate, subscriber conversion, and budget.

## The 8 Gates

Every video must pass ALL 8. Any gate failed = fix it or kill it.

### Gate 1: Title Click Trigger
Does the title use at least one of Jake Thomas's 3 triggers?
- [ ] **Curiosity**: Creates an information void
- [ ] **Desire**: Promises something the viewer wants
- [ ] **Fear**: Warns about a mistake or loss

Score: Does the title make YOU want to click from a stranger's channel? Be honest.

**FAIL criteria**: Title is descriptive but not compelling. "How to Set Up AWS Bedrock" = weak. "AWS Bedrock Costs 90% Less Than You Think (Here's How)" = pass.

### Gate 2: Thumbnail-Title Synergy
- [ ] Title and thumbnail carry DIFFERENT information
- [ ] Together they create a curiosity gap
- [ ] Thumbnail has max 3 visual elements
- [ ] Text on thumbnail is 4 words or fewer
- [ ] Designed for dark mode (60-70% of viewers)
- [ ] Face with emotion visible (if applicable)

**FAIL criteria**: Thumbnail repeats the title, or is text-heavy, or has no clear focal point.

### Gate 3: First 5 Seconds
- [ ] Viewer sees what they gain or lose within 5 seconds
- [ ] Zero preamble before value starts
- [ ] Matches the promise of title + thumbnail
- [ ] Specific enough to hold attention

**FAIL criteria**: Opens with "Hey guys, welcome to my channel" or any filler before the hook.

### Gate 4: Satisfaction Delivery
The 2026 algorithm weights satisfaction above watch time.
- [ ] Video delivers on the title's promise (not clickbait)
- [ ] Viewer would rate this "worth watching" in a post-video survey
- [ ] Viewer would watch another video after this (session contribution)
- [ ] Content is genuinely useful/entertaining, not padded

**FAIL criteria**: Title promises X, video delivers Y. Or video is padded to hit a length target.

### Gate 5: Retention Architecture
- [ ] Mini-payoffs every 60-90 seconds
- [ ] Pattern interrupts every 20-30 seconds (visual changes, cuts, graphics)
- [ ] Stakes escalate throughout
- [ ] Re-engagement moment every 3-5 minutes
- [ ] No segment where a viewer would reasonably leave
- [ ] If 8+ minutes: energy maintained through minute 8 threshold

**FAIL criteria**: Long stretches without payoffs, flat energy, or obvious "skip to" sections.

### Gate 6: "Would Someone Subscribe?"
- [ ] This video demonstrates YOUR unique expertise or voice
- [ ] A new viewer watching this would think "I want more from this person"
- [ ] It's not generic content anyone could make
- [ ] It fits your channel's niche consistency (algorithm judges channels holistically)

**FAIL criteria**: Video is interchangeable with 50 other channels' content.

### Gate 7: Format Validation
- [ ] This format has proven demand (outlier in your niche or adjacent niche)
- [ ] Length matches topic (short high-retention > long low-retention)
- [ ] Format is right for the platform surface (search vs browse vs suggested)

**FAIL criteria**: Untested format with no evidence of demand.

### Gate 8: Personal Excitement
MrBeast rule: "If a concept doesn't excite me personally, it won't be filmed."
- [ ] You are genuinely excited about this video
- [ ] You would watch this video yourself
- [ ] This represents your best work right now

**FAIL criteria**: You're publishing because "I need to upload something" not because the video is good.

## Scoring

| Gate | Status | Notes |
|------|--------|-------|
| 1. Title Click Trigger | PASS/FAIL | |
| 2. Thumbnail-Title Synergy | PASS/FAIL | |
| 3. First 5 Seconds | PASS/FAIL | |
| 4. Satisfaction Delivery | PASS/FAIL | |
| 5. Retention Architecture | PASS/FAIL | |
| 6. "Would Someone Subscribe?" | PASS/FAIL | |
| 7. Format Validation | PASS/FAIL | |
| 8. Personal Excitement | PASS/FAIL | |

## Verdict

- **8/8 PASS**: Ship it.
- **6-7 PASS**: Fix the failed gates, then re-evaluate.
- **5 or fewer PASS**: Kill it. The ceiling is too low. Spend the time on a better idea.

## Failure Modes to Catch

- Vague advice: rewrite into commands. Not "make the title stronger"; say "move the number into the first 4 words and cut filler words."
- Budget mismatch: do not prescribe a giant production plan to a solo creator. Preserve the tension, shrink the execution.
- Case-study padding: every example must prove a principle and produce a next action.
- False encouragement: if the data says the ceiling is low, say so and repackage or kill it.
- Platform mismatch: YouTube logic does not transfer unchanged to Shorts, TikTok, Bilibili, newsletters, or podcasts.

## Output Format

```markdown
## Virality Gate: "[Video Title]"

### Results
| # | Gate | Status | Issue | Fix |
|---|------|--------|-------|-----|
| 1 | Title Click Trigger | [P/F] | [if F, what's wrong] | [specific fix] |
| 2 | Thumbnail Synergy | [P/F] | | |
| 3 | First 5 Seconds | [P/F] | | |
| 4 | Satisfaction Delivery | [P/F] | | |
| 5 | Retention Architecture | [P/F] | | |
| 6 | Subscribe Worthiness | [P/F] | | |
| 7 | Format Validation | [P/F] | | |
| 8 | Personal Excitement | [P/F] | | |

### Verdict: [SHIP / FIX / KILL]
**Score**: [X]/8

### If FIX:
[Specific changes needed, in priority order]

### If KILL:
[Why this video isn't worth the channel damage. What to make instead.]
```
