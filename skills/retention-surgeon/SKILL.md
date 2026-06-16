---
name: retention-surgeon
description: "Diagnose retention problems using benchmarks, identify which of the 4 curve shapes you have, recommend cutting patterns, and fix the first 30 seconds. Use when a video underperforms or when editing."
argument-hint: "[paste retention data, or describe the video and its performance]"
---

# Retention Surgeon

Diagnose and fix retention for: **$ARGUMENTS**

## Step 1: Identify the Retention Curve Shape

### The 4 Shapes

1. **The Cliff** — Steep early drop (>30% lost in first 30 seconds)
   - Diagnosis: Failed hook. Title/thumbnail promise doesn't match opening.
   - Fix: Rewrite first 30 seconds. Deliver on the promise IMMEDIATELY.

2. **Gradual Decline** — Steady drop throughout
   - Diagnosis: Natural attrition. Healthy if above 40% at midpoint.
   - Fix: Add pattern interrupts every 20-30 seconds. More Setup-Tension-Payoff cycles.

3. **The Bump** — Spike at a specific point (people rewatching a segment)
   - Diagnosis: You have a rewatch-worthy moment. Extract it as a Short/clip.
   - Fix: Study what made that moment work. Replicate the structure.

4. **Flat Line** — Consistent engagement throughout
   - Diagnosis: Ideal. Rare. Your content is holding.
   - Fix: Nothing. Study this video and replicate.

## Step 2: Benchmark Against Standards

### By Video Length
| Length | Good | Great | Problem |
|--------|------|-------|---------|
| Under 5 min | 50% | 60%+ | Below 40% |
| 5-15 min | 40% | 50%+ | Below 30% |
| 15-30 min | 30% | 40%+ | Below 25% |
| Over 30 min | 25% | 35%+ | Below 20% |
| Shorts | 70% | 90%+ | Below 50% |

### By Content Type
- Tutorials: 45-55% (viewers skip to relevant parts — expect dips)
- Thought leadership: 35-50%
- Product demos: Bimodal curves typical
- Interviews/Podcasts: 25-35%

### Beast-Style Segment Targets

Use these as aggressive targets for highly packaged browse content:

| Time | Target | Strategy |
|------|--------|----------|
| 0-1 min | 90%+ retention | Perfect hook, no wasted setup |
| 1-3 min | 80%+ retention | First escalation and clear reason to stay |
| 3-6 min | 65%+ retention | Twist, reveal, or upgrade every 3 minutes |
| 6 min+ | 50%+ retention | Keep stair-stepping toward the peak moment |
| Final 30 sec | Hold or redirect | CTA, payoff, or next-video bridge |

### Engagement Ratios
- Like-to-view: 4-8% (long-form), 3-6% (Shorts)
- Return viewer rate: Above 10% = building an audience

## Step 3: First 30 Seconds Audit

The first 30 seconds are make-or-break. Check:

- [ ] Does it deliver on the title's promise within 5 seconds?
- [ ] Is there ZERO preamble before the value starts?
- [ ] Does it introduce specific value the viewer will get?
- [ ] Is there a pattern interrupt at 25-35 seconds?
- [ ] Does it establish purpose ("By the end, you'll know...")?
- [ ] MrBeast test: Does the viewer see what they gain or lose in first 5 seconds?
- [ ] Does it show the best visual proof, final result, or biggest problem before explaining background?
- [ ] Is action underway by 15-30 seconds?

If any box is unchecked, rewrite the opening.

## Step 4: Recommend a Cutting Pattern

### 5 Proven Patterns (AIR Media-Tech)

**1. Progressive Rhythm** — Best for: educational, explainer
- Min 0-3: Tight pacing, frequent visual changes
- Min 3-7: Stabilize, fewer cuts, more B-roll
- After min 8: Mix calm with energy bursts
- Used by: Veritasium, Ali Abdaal

**2. Contrast Pattern** — Best for: commentary, essay
- Simple pacing (15-25 sec/cut) most of the time
- Every 2-3 min: burst of 5-10 quick cuts
- Return to calm. Mimics conversation rhythm.
- Used by: Ryan Trahan, Drew Gooden

**3. Narrative Loop** — Best for: challenge, story, MrBeast-style
- Open with hook/question
- Every 2-3 min, remind viewers of core premise
- Smoother transitions, ambient bridges
- Used by: MrBeast, YesTheory

**4. Hybrid Tempo** — Best for: tutorial with energy
- Fast mode: micro-cuts every 10-15 sec with zooms/graphics
- Slow mode: holds up to 40 sec during examples
- Used by: Better Ideas, Think Media

**5. Anchor Pattern** — Best for: personal, documentary
- Edit at emotional beats, not time intervals
- Hold shots through full statements before cutting
- Ambient sound guides pacing
- Used by: Nathaniel Drew, Johnny Harris

## Step 5: The Minute 8 Threshold

YouTube starts rewarding with higher suggested placement after minute 8. If your video is 8+ minutes:
- Maintain high energy through minute 8
- Place a strong payoff or reveal just past the 8-minute mark
- This triggers algorithmic momentum for suggested placement

## Step 5.5: Re-Engagement Moments

If the curve drops every few minutes, add a re-engagement moment every 3-5 minutes:
- New rule or constraint
- New visual environment
- Unexpected failure
- Bigger prize, cost, timer, or consequence
- Open loop payoff followed by a new open loop

## Step 6: Sound Design Check

- [ ] Voice dominates, music 5-25dB quieter
- [ ] Calm segments: -20 to -25dB music
- [ ] Energetic sequences: -8 to -12dB music
- [ ] Music track changes when story shifts
- [ ] Brief silence before major reveals
- [ ] Heavy transitions reserved for BIG moments only

## Output Format

```markdown
## Retention Diagnosis: "[Video Title]"

### Curve Shape: [Cliff / Gradual / Bump / Flat]
**Current retention**: [X]% average
**Benchmark**: [Good/Below/Great] for [length] [content type]

### Problem Areas
1. [Timestamp] — [what's happening] — [why viewers leave here]
2. [Timestamp] — [what's happening] — [why viewers leave here]

### Recommended Cutting Pattern: [Pattern Name]
**Why**: [reason this pattern fits this video]

### Fix List (priority order)
1. **First 30 seconds**: [specific rewrite]
2. **[Timestamp]**: [specific fix]
3. **[Timestamp]**: [specific fix]

### Opportunities
- **Rewatch spike at [timestamp]**: Extract as Short
- **Minute 8 checkpoint**: [is energy maintained? what to add?]

### Sound Design Notes
- [any sound issues identified]
```
