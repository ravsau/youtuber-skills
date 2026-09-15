---
name: youtube-lane
description: "3 content lanes for a channel with buyer, engine, proof titles, and a kill test. Use when asked what to make or which niche to pick."
argument-hint: "[channel or niche] [3 videos you liked making] [your skills] [what you sell, if anything]"
---

# YouTube Lane

Input: the channel or niche, 3 videos you liked making, your skills, and what you sell if anything.
Output: 3 candidate lanes, scored, with one recommended lane and its 60-day kill test.

## Steps

1. Write the creator's edge in one line: what they can show that most channels in the niche cannot.
2. List 3 lanes where that edge meets a buyer with a repeated question. Name the buyer in 5 words.
3. For each lane, find 5 titles from other channels that did 3x their channel average. Note the format each used.
4. Set the engine per lane: search (the buyer types the question) or browse (the packaging wins the click).
5. Score each lane 1-5 on edge, demand, and sale path. Recommend the highest sum.
6. Write the kill test: 4 videos in 60 days, the one number to beat, and what happens on a miss.

## Rules

- A lane is a repeated buyer question, never a topic list.
- Every lane needs 5 outlier titles as proof. No proof, no lane.
- One lane at a time. The other two wait for the kill test result.
- The sale path can be "none yet". Say so instead of inventing one.

CRITICAL: never recommend a lane the creator cannot film with what they own today.

## Output format

```markdown
## Lanes for: [channel]

Edge: [one line]

| # | Lane | Buyer | Engine | Edge | Demand | Sale | Total |
|---|------|-------|--------|------|--------|------|-------|
| 1 | ... | ... | search | 4 | 5 | 3 | 12 |

### Pick: lane N
Proof (5 outlier titles): ...
Kill test: 4 videos by [date]. Beat [number]. On a miss: move to lane M.
```

## Example

Input: `local AI channel; liked: a 128GB Mac agent test, a token-cost breakdown, a Claude Code settings walkthrough; skills: cloud infra, cost math; sells: 1:1 setup calls`

| # | Lane | Buyer | Engine | Edge | Demand | Sale | Total |
|---|------|-------|--------|------|--------|------|-------|
| 1 | What does this AI setup cost to run | Solo dev picking a setup | search | 5 | 4 | 4 | 13 |
| 2 | Local vs cloud, tested on real work | Dev with a Mac deciding | browse | 4 | 5 | 3 | 12 |
| 3 | Coding agent config fixes | Dev whose agent misbehaves | search | 3 | 4 | 2 | 9 |

Pick: lane 1. Proof: 5 titles from 3 channels in the niche, each a cost number in the title, each 3x their average.
Kill test: 4 videos by day 60. Beat the channel's 30-day median views. On a miss: move to lane 2.
