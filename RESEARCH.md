# Research Sources

This repo is built from deep research across 10+ top YouTube creators and strategists.

## Primary Sources

### Creators & Strategists
- **MrBeast** — Production handbook (leaked 2024), A/B testing methodology, "every second earns its place"
- **Jake Thomas (Creator Hooks)** — 408-title database, 3 Click Triggers (Curiosity 61%, Desire 46%, Fear 40%), IMPACT framework
- **George Blackman** — MrBeast's former scriptwriter. Target-Transformation-Stakes hook, Setup-Tension-Payoff body, 5-step scriptwriting system
- **Paddy Galloway** — YouTube strategist. 12-month growth system, CCN framework, 280% avg first-year viewership increase for clients
- **Ali Abdaal** — HIVE framework, Part-Time YouTuber Academy (73% completion rate, 3,000+ students)
- **Roberto Blake** — Big Creator Energy framework, One Tribe/One Theme/Five Topics, platform ownership strategy
- **Colin & Samir** — Revenue diversification, creator economy economics, "leave AdSense out of budgeting"
- **Derral Eves** — "The YouTube Formula" author, Squatty Potty case ($45M from one 4-min video), 54 billion total views generated
- **Film Booth** — 4-beat storytelling structure (Cold Open, Intro, Concept in Action, Golden Moment)
- **vidIQ / Think Media / Sean Cannell** — SEO, algorithm mechanics, search-first strategy

### Research & Data
- **AIR Media-Tech** — 5 cutting patterns for retention editing
- **ThumbnailTest** — Thumbnail psychology research (0.05-second decision, face CTR data)
- **YouTube Creator Academy** — Official algorithm documentation and best practices
- **alchaincyf/mrbeast-skill** — MIT-licensed Chinese-language MrBeast perspective skill used as an additional framework reference for data-first workflow, CTR x AVD, simple concept x extreme execution, stair-stepping, and failure-mode checklists

### Description Audit (2026-09-20)
Pulled with yt-dlp, read in full. Basis for the `youtube-description` skill.
- **MrBeast**, 4 uploads: v9QtM6qnG50 (Sep 19, 21.5M views at read), gTKS8SAwUzE (Sep 5, 107.9M),
  Qtl8lJwbd4g (Aug 22, 108.3M), Af6i6ChAVTw (Aug 8, 115.4M). Findings: one footer byte-identical
  across all four (sister channels, merch, Viewstats, business email, music credit, socials,
  hiring); sponsor blocks first, one plain sentence + link + code + legal text; one paragraph per
  video that answers the top objection (gear recovered, officers off duty, trees replanted);
  two of four open with a lowercase premise line; zero chapters, zero tags, zero hashtags.
- **AI teaching lane**, 2 most recent uploads each from nateherk, bycloudAI, matthew_berman,
  edward.donner, houseofel-ai, JulianGoldieSEO, samwitteveenai, AIJasonZ. Findings: sponsor
  block first on 5 of 8; chapters on 5 of 8; a footer identical across both uploads on 3 of 8
  (nateherk, bycloudAI, JulianGoldieSEO); newsletter on 3 of 8; community link on 4 of 8;
  a comment question on almost none; no channel writes a long body paragraph.

## Source URLs

- [MrBeast Production Handbook (Simon Willison)](https://simonwillison.net/2024/Sep/15/how-to-succeed-in-mrbeast-production/)
- [MrBeast Internal Guide (Tubefilter)](https://www.tubefilter.com/2024/09/17/mrbeast-internal-production-guide-leaked-key-points/)
- [MrBeast 362M Formula (Hook Point)](https://hookpoint.com/blog/mrbeast-s-362m-content-formula-revealed/)
- [Paddy Galloway Growth Process (Passionfruit)](https://passionfru.it/paddy-galloways-how-to-grow-youtube-71562/)
- [Paddy Galloway YouTube Guide (Marketing Examined)](https://www.marketingexamined.com/blog/paddy-galloway-youtube-guide)
- [George Blackman Scriptwriting (Substack)](https://writewithai.substack.com/p/write-a-killer-youtube-script-like)
- [Jake Thomas / Creator Hooks (Creator Science)](https://podcast.creatorscience.com/jake-thomas/)
- [Jake Thomas Title Masterclass](https://engagevideomarketing.com/podcasts/a-youtube-titles-masterclass-with-jake-thomas/)
- [Roberto Blake Creator Economy](https://www.lightscameralive.com/blog/roberto-blake-creator-economy-tips)
- [Derral Eves YouTube Formula (Summary)](https://summaries.com/blog/the-youtube-formula)
- [Colin & Samir Creator Economy](https://lilys.ai/en/notes/creator-economy-20260108/colin-samir-creator-economy-youtube-economics)
- [YouTube Algorithm 2026 (vidIQ)](https://vidiq.com/blog/post/understanding-youtube-algorithm/)
- [Algorithm Updates (OutlierKit)](https://outlierkit.com/resources/youtube-algorithm-updates/)
- [Retention Benchmarks 2026 (Humble&Brag)](https://humbleandbrag.com/blog/youtube-audience-retention-benchmarks)
- [Retention Cutting Patterns (AIR Media-Tech)](https://air.io/en/youtube-hacks/advanced-retention-editing-cutting-patterns-that-keep-viewers-past-minute-8)
- [Thumbnail Psychology (ThumbnailTest)](https://thumbnailtest.com/guides/psychology-of-youtube-thumbnails/)
- [Shorts vs Long-Form 2026 (Mediacube)](https://mediacube.io/en-US/blog/youtube-shorts-vs-long-videos)
- [Title Best Practices 2026 (Humble&Brag)](https://humbleandbrag.com/blog/youtube-title-best-practices)
- [YouTube SEO 2026 (vidIQ)](https://vidiq.com/blog/post/how-to-rank-number-one-youtube-keyword-research/)
- [alchaincyf/mrbeast-skill](https://github.com/alchaincyf/mrbeast-skill)

## How Skills Were Built

Each skill maps to a topic area from the research:

| Skill | Primary Sources |
|-------|----------------|
| title-formula | Jake Thomas, MrBeast |
| thumbnail-psychology | ThumbnailTest, MrBeast, Derral Eves |
| mrbeast-packaging | MrBeast Production Handbook |
| script-hook-framework | George Blackman, Ali Abdaal, Film Booth |
| retention-surgeon | AIR Media-Tech, MrBeast, retention research |
| algorithm-2026 | vidIQ, OutlierKit, YouTube Creator Academy |
| shorts-strategy | Mediacube, vidIQ, YouTube internal data |
| youtube-description | Description Audit 2026-09-20 (MrBeast x4, AI teaching lane x8) |
| seo-discovery | vidIQ, Think Media |
| monetization-stack | Colin & Samir, Roberto Blake, Ali Abdaal, Derral Eves |
| production-ops | MrBeast Handbook, Paddy Galloway |
| outlier-hunter | MrBeast, Jake Thomas, Paddy Galloway |
| virality-gate | Composite from all sources |
