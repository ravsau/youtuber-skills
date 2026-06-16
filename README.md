# youtuber-skills

MrBeast-Inspired Claude Code Guidelines for YouTubers

A single `CLAUDE.md` file to improve how Claude Code helps you create YouTube content, derived from MrBeast's production handbook + research from 10 top YouTube strategists.

## The Problems

From MrBeast's leaked production handbook:

> "I Spent 50 Hours In Ketchup" vastly outperforms "I Spent 50 Hours In My Front Yard." Same effort, wildly different packaging. **The packaging IS the product.**

> "Every second must earn the viewer's attention."

> "If a concept doesn't excite me personally, it won't be filmed."

From MrBeast on hiring:

> "A-Players are obsessive, learn from mistakes, coachable, intelligent, no excuses, believe in YouTube, best in the world at their job. C-Players are average employees — transition them to a different company IMMEDIATELY."

From Paddy Galloway:

> "The idea sets the ceiling, the execution determines the result." Most creators over-invest in execution and under-invest in ideation.

From MrBeast on originality:

> "Don't copy and paste. Copy with taste. There's only one time you should aim for originality: when you're adapting winning formats to your unique brand."

**The core issue:** Most creators film a video, then try to package it. MrBeast does the opposite. The title and thumbnail are conceived BEFORE filming. The video is built to match the packaging. If the packaging doesn't have a high ceiling, the video never gets made.

## The Solution

Five principles in one file that directly address these issues:

**Operating rule:** data before advice. If a recommendation depends on a specific channel, video, niche, competitor, or trend, research current facts first: recent performance, outliers, title/thumbnail patterns, CTR/AVD if available, search signals, and budget reality. If there are no numbers, ask for them or label assumptions clearly.

| Principle | Addresses |
|-----------|-----------|
| Packaging First | Filming before packaging, weak titles, thumbnails as afterthought |
| Earn Every Second | Slow intros, dead time, no escalation, viewers leaving |
| Copy With Taste | Starting from scratch, ignoring proven formats, "originality" trap |
| Kill or Ship | Hesitation, perfectionism, publishing weak content |
| Obsess the Viewer | Self-centered content, ignoring what the audience actually wants |

## The Five Principles in Detail

### 1. Packaging First

Don't film, then package. Package, then film.

MrBeast generates 50+ title/thumbnail concepts before a camera turns on. The packaging determines the ceiling. If the ceiling is low, no amount of production saves it.

- **Title + thumbnail conceived TOGETHER, before filming** — they set the ceiling
- **Title and thumbnail must NOT repeat each other** — each carries unique information
- **More extreme wording always wins** — "I Survive" > "I Spent", "Bananas Are The Worst Food On Earth" > "I Don't Like Bananas"
- **Simple concept x extreme execution** — if the idea cannot be explained in one exciting sentence, rebuild the premise
- **Psychological friction** — same set, sharper frame. Add proof, contradiction, status risk, constraints, or personal stakes before adding budget.
- **3 Click Triggers** (Jake Thomas, 408-title database): Curiosity (61%), Desire (46%), Fear (40%)
- **Thumbnails**: Faces +35-50% CTR. 4 words max +30% CTR. High contrast +20-40% CTR. Closed-mouth smiles beat exaggerated expressions 100% of MrBeast's A/B tests.
- **If the title doesn't make YOU click from a stranger's channel, kill it**

### 2. Earn Every Second

Every second must justify its existence. No dead time. No filler. Escalating stakes.

- **First 5 seconds**: Show the viewer what they gain or lose, or retention collapses (MrBeast)
- **First 30 seconds**: Show the concept, state the stakes, preview the payoff, then start action. Zero preamble. Pattern interrupt at 25-35 seconds.
- **Every 60-90 seconds**: Complete a Setup-Tension-Payoff cycle. Each payoff transitions into the next setup. (George Blackman)
- **Every 3-5 minutes**: Add a re-engagement moment: new twist, escalation, surprise, visual reset, or open-loop payoff.
- **Minute 8 threshold**: YouTube starts rewarding with higher suggested placement after minute 8. Maintain energy through this point.
- **Escalating stakes throughout** — tension builds continuously, never plateaus
- **Sound design**: Voice dominates. Music 5-25dB quieter. Brief silence before reveals. Change tracks when the story shifts.

### 3. Copy With Taste

Don't start from zero. Find what works, extract the format, adapt with your voice.

- **Study outlier videos (3x+ above channel average) across 5 industries weekly** (Jake Thomas)
- **For specific niches, inspect the current top 10 before recommending a format**
- **Extract the FORMAT, not the topic** — strip away specifics, find the structure
- **Adapt to your niche, voice, and expertise** — the format is borrowed, the execution is yours
- **"There's only one time you should aim for originality: when you're adapting winning formats to your unique brand"** (MrBeast)
- **4 hours/week studying YouTube across niches** — not just your own (Paddy Galloway)
- **After 50 uploads, analyze your top 5 and bottom 5** — the patterns ARE the strategy

### 4. Kill or Ship

Kill weak ideas fast. Ship strong ones faster. Never publish something that damages your channel.

- **Pre-publish gate**: Every video must pass quality checks before going live. The 2026 algorithm judges your channel as a whole — one weak video signals inconsistency.
- **If a concept doesn't excite you personally, kill it** (MrBeast) — personal authenticity is non-negotiable
- **Spending over $10K requires visible on-camera ROI** (MrBeast)
- **"Consultants are literally cheat codes"** — hire experts who've solved similar problems to save weeks of work
- **Phase 1 (weeks 1-16): 2 videos/week, volume + speed. Phase 2 (weeks 17-52): 1 video/week, quality focus** (Paddy Galloway)

### 5. Obsess the Viewer

You don't have a channel. You have a viewer. Everything starts with what they want.

- **Satisfaction now outweighs raw watch time** in the 2026 algorithm — a 6-minute video with 80% retention beats a 20-minute video with 30%
- **Roberto Blake's 4 Ps**: Priorities (what's urgent for them?), Problems (which pain points?), Preferences (how do they learn?), Prejudices (what don't they want?)
- **88% of YouTube videos never reach 1,000 views** — you're competing with the top 5 in your niche, not all of YouTube
- **Educational content gets 80% of views 6+ months post-upload** — patience, not virality
- **Leave AdSense out of budgeting** — build revenue you control (Colin & Samir)
- **Mid-video CTAs (60-70% through) outperform end-of-video CTAs**

## Install

**Option A: CLAUDE.md (recommended)**

New project:

```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/ravsau/youtuber-skills/main/CLAUDE.md
```

Existing project (append):

```bash
echo "" >> CLAUDE.md
curl https://raw.githubusercontent.com/ravsau/youtuber-skills/main/CLAUDE.md >> CLAUDE.md
```

**Option B: Full skills (all 12)**

```bash
git clone https://github.com/ravsau/youtuber-skills.git
for skill in youtuber-skills/skills/*/; do
  name=$(basename "$skill")
  ln -sf "$(pwd)/$skill" "$HOME/.claude/skills/$name"
done
```

**Option C: Single skill**

```bash
ln -sf "$(pwd)/youtuber-skills/skills/title-formula" "$HOME/.claude/skills/title-formula"
```

## Skills

Beyond the core `CLAUDE.md`, each principle has dedicated skills for deep execution:

| Skill | Principle | What It Does |
|-------|-----------|-------------|
| [title-formula](skills/title-formula/) | Packaging First | 10+ titles using 3 Click Triggers, IMPACT scoring, 7 proven formulas |
| [thumbnail-psychology](skills/thumbnail-psychology/) | Packaging First | Research-backed thumbnail design briefs with A/B test plan |
| [mrbeast-packaging](skills/mrbeast-packaging/) | Packaging First | 50+ title/thumbnail pairings ranked by ceiling, then production brief |
| [script-hook-framework](skills/script-hook-framework/) | Earn Every Second | Target-Transformation-Stakes hook + Setup-Tension-Payoff body |
| [retention-surgeon](skills/retention-surgeon/) | Earn Every Second | Diagnose retention curves, 5 cutting patterns, minute 8 fix |
| [outlier-hunter](skills/outlier-hunter/) | Copy With Taste | Find 3x+ outliers, extract formats, adapt to your brand |
| [virality-gate](skills/virality-gate/) | Kill or Ship | 8-gate pre-publish check. Kill weak videos before they hurt your channel |
| [production-ops](skills/production-ops/) | Kill or Ship | MrBeast's A/B/C hiring, Paddy's 12-month system, bottleneck management |
| [algorithm-2026](skills/algorithm-2026/) | Obsess the Viewer | 2026 algorithm: satisfaction > watch time, Shorts decoupled |
| [shorts-strategy](skills/shorts-strategy/) | Obsess the Viewer | Shorts = discovery ($0.01-0.06 RPM). Long-form = revenue ($1-30 RPM). |
| [seo-discovery](skills/seo-discovery/) | Obsess the Viewer | Keywords, descriptions, search vs browse strategy |
| [monetization-stack](skills/monetization-stack/) | Obsess the Viewer | Revenue stack beyond AdSense. Platform ownership > marketplace splits. |

## Key Insight

From MrBeast:

> "I Spent 50 Hours In Ketchup" and "I Spent 50 Hours In My Front Yard" require the same effort. One gets 10x the views. **The difference is the packaging, not the work.**

Most AI coding tools help you produce videos faster. These guidelines help you produce **the right videos** — the ones worth making in the first place.

## How to Know It's Working

These guidelines are working if you see:

- **Titles conceived before filming** — not scrambled together at upload time
- **Fewer published videos, more views per video** — quality over volume
- **Clarifying questions about the viewer** — not just "what should I make?"
- **Format references from outliers** — ideas grounded in what's proven, not guesses
- **Videos killed before production** — weak ceilings caught early, saving hours of wasted work

## Research Sources

Built from deep research across 10+ creators and strategists. Full notes in [RESEARCH.md](RESEARCH.md).

**Core**: MrBeast (production handbook), George Blackman (MrBeast's scriptwriter), Paddy Galloway (YouTube strategist)

**Supporting**: Jake Thomas (Creator Hooks, 408-title database), Ali Abdaal (HIVE framework), Roberto Blake (Big Creator Energy), Colin & Samir (creator economy), Derral Eves (The YouTube Formula), Film Booth (storytelling), vidIQ (algorithm 2025-2026), AIR Media-Tech (retention editing)

## Who Made This

Built by [Saurav](https://github.com/ravsau), who runs the [CloudYeti](https://youtube.com/@CloudYeti) YouTube channel (15K+ subs). These skills encode the playbook used to grow that channel.

## License

MIT
