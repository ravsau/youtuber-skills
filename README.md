# youtuber-skills

Claude Code skills for YouTube creators. Package before you film, script the hook, gate the upload.

[![skills.sh](https://skills.sh/b/ravsau/youtuber-skills)](https://skills.sh/ravsau/youtuber-skills)

```bash
npx skills add ravsau/youtuber-skills --skill youtube-packaging
```

## Same prompt, with and without the skill

Prompt: `package this: how many coding agents a 128GB Mac can run at once before it breaks`

Without:

> Title: "How Many AI Agents Can a 128GB Mac Run? (Tested)"
> Thumbnail: Mac Studio, the text "128GB vs AI Agents", a robot icon.

With `youtube-packaging`:

> #1 "I Ran 12 Coding Agents on One Mac. It Broke at 9" (48 chars)
> Thumbnail: creator wincing beside a Mac Studio, Activity Monitor memory bar pinned red. Text: "agent 9".
> Click 5, Deliver 4. Image prompt ready to paste.

The title answers the question with a number and a failure. The thumbnail shows the break instead of repeating "128GB". More pairs in [EXAMPLES.md](EXAMPLES.md).

## Skills

| Skill | Give it | Get back |
|-------|---------|----------|
| [youtube-lane](skills/youtube-lane/) | channel, 3 videos you liked, what you sell | 3 lanes with buyer, engine, proof titles, 60-day kill test |
| [youtube-comments-to-ideas](skills/youtube-comments-to-ideas/) | pasted comments | 5 ideas, each tied to the comment that proves demand |
| [youtube-packaging](skills/youtube-packaging/) | a topic | 5 title + thumbnail pairs, scored, with image prompts |
| [youtube-script](skills/youtube-script/) | a packaged title | hook + setup-tension-payoff script |
| [youtube-retention](skills/youtube-retention/) | a retention curve | timestamped fix list |
| [youtube-edit-list](skills/youtube-edit-list/) | a transcript, optional retention drops | edit decision list, chapters, end frame |
| [youtube-outliers](skills/youtube-outliers/) | a niche or channel | 3x outlier videos, their format, 3 adaptations |
| [youtube-virality-gate](skills/youtube-virality-gate/) | a finished video plan | 8 gates, SHIP / FIX / KILL |
| [youtube-description](skills/youtube-description/) | title + transcript, optional metrics | search vs browse call, title check, paste-ready description, tags |
| [youtube-shorts](skills/youtube-shorts/) | a topic | Shorts / long-form / both, with a calendar |
| [youtube-monetization](skills/youtube-monetization/) | niche, subs, revenue | ranked revenue stack, 90-day plan |
| [youtube-channel-audit](skills/youtube-channel-audit/) | last 10-20 uploads, channel page | top-20% publish bar, outlier variable, page fixes |

Every skill is under 90 lines: input, output, steps, template, one example.

## Install

All skills:

```bash
npx skills add ravsau/youtuber-skills
```

One skill:

```bash
npx skills add ravsau/youtuber-skills --skill youtube-script
```

Guidelines only, as a `CLAUDE.md` (the five principles the skills are built on):

```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/ravsau/youtuber-skills/main/CLAUDE.md
```

Manual, without npx:

```bash
git clone https://github.com/ravsau/youtuber-skills.git
ln -sf "$(pwd)/youtuber-skills/skills/youtube-packaging" ~/.claude/skills/youtube-packaging
```

## The five principles

1. **Packaging first.** Title and thumbnail before filming. They set the ceiling.
2. **Earn every second.** Stakes in 5 seconds, payoff cycles every 60-90 seconds.
3. **Copy with taste.** Take the format from outliers, keep your own topic and voice.
4. **Kill or ship.** Gate every upload. Kill weak ceilings before production.
5. **Obsess the viewer.** Satisfaction beats watch time.

Sources and quotes: [RESEARCH.md](RESEARCH.md). Derived from MrBeast's production handbook, George Blackman, Paddy Galloway, Jake Thomas, Ali Abdaal, Roberto Blake, Colin & Samir, Derral Eves, Film Booth, vidIQ.

## Who made this

[Saurav](https://github.com/ravsau), who runs [CloudYeti](https://youtube.com/@CloudYeti) on YouTube.

MIT
