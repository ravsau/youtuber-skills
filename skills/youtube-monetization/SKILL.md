---
name: youtube-monetization
description: "Ranked revenue stack and 90-day plan from niche, subs, and current revenue. Use when asked how to make money from a channel."
argument-hint: "[niche] [subscriber count] [current revenue sources with monthly amounts, or 'none']"
---

# YouTube Monetization

Input: the niche, the subscriber count, and each current revenue source with its monthly amount.
Output: a control table for current revenue, a ranked stack of 3-5 streams, and a 90-day plan.

## Steps

1. Name the one audience the channel serves and the one change it promises them.
2. Rate each current source on control: low (ad revenue), medium (brand deals), high (own products, services, list).
3. Pick 3-5 streams the audience already pays for elsewhere. Rank by control first, then by time to first dollar.
4. For each stream write why it fits, what must exist first, and when it earns.
5. Write the 90-day plan. Month 1 ships one stream, month 2 measures it, month 3 adds the next.

## Rules

- Treat ad revenue as a bonus. Never plan around it.
- Prefer a platform where the creator keeps most of the revenue over a marketplace split.
- Under 1K subscribers, sell a service or a small product before ad eligibility.
- Every stream must map to a topic the channel already covers.
- Give each potential amount as a range and mark it as an estimate.

## Output format

```markdown
## Monetization Stack: [channel or niche]

| Source | Monthly | Control |
|--------|---------|---------|
| ... | $... | low / medium / high |

### Stack (ranked)
1. **[stream]**: $[low]-[high]/mo estimate. Why: ... Needs: ... Earns from: ...
2. ...

### 90-day plan
| Month | Ship | Measure |
|-------|------|---------|
| 1 | ... | ... |
| 2 | ... | ... |
| 3 | ... | ... |
```

## Example

Input: `local AI on Mac tutorials; 9K subs; AdSense $180/mo, one affiliate link $40/mo`

| Source | Monthly | Control |
|--------|---------|---------|
| AdSense | $180 | low |
| Affiliate (RAM upgrade kit) | $40 | medium |

1. **Setup call, 45 minutes**: $600-1,200/mo estimate. Why: comments ask "will this run on my machine". Needs: a booking page and one demo video that ends on it. Earns from: week 2.
2. **Paid hardware buying guide (PDF)**: $200-500/mo estimate. Why: the tier-map videos already drive the question. Needs: one page per RAM tier. Earns from: month 2.
3. **Tool sponsor, one slot per video**: $300-800/mo estimate. Why: every video names an inference tool. Needs: a one-page media kit. Earns from: month 3.

| Month | Ship | Measure |
|-------|------|---------|
| 1 | Booking page, CTA in the next 4 videos | Calls booked per 1K views |
| 2 | Buying guide, linked from the tier-map video | Sales per 1K views |
| 3 | Media kit sent to 5 tools | Replies and one signed slot |

CRITICAL: never present an estimate as a result the channel has earned.
