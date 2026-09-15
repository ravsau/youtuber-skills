# Examples: same prompt, without and with the skill

Invented topics. No numbers here are real channel data.

## youtube-packaging

Prompt: `package this: how many coding agents a 128GB Mac can run at once before it breaks`

Without:

> Title: "How Many AI Agents Can a 128GB Mac Run? (Tested)"
> Thumbnail: Mac Studio, the text "128GB vs AI Agents", a robot icon.

With:

> #1 "I Ran 12 Coding Agents on One Mac. It Broke at 9" (48 chars). Thumbnail: creator wincing beside a Mac Studio, Activity Monitor memory bar pinned red. Text: "agent 9". Click 5, Deliver 4.
> #2 "128GB of RAM Is Not Enough for This" (36 chars). Thumbnail: nine terminal windows tiled, one frozen cursor. Text: "$4,000 Mac". Click 4, Deliver 4.
> Pick: #1. Image prompt: photo-realistic 16:9, Activity Monitor pinned red, text "agent 9", no extra text, no logos, no watermark.

What changed: the title answers with a number and a failure. The thumbnail shows the break instead of repeating "128GB".

Prompt: `package this: Claude Code skipped my AGENTS.md rules until I added one line`

Without:

> Title: "Why Claude Code Ignores Your AGENTS.md File (And How to Fix It)"
> Thumbnail: Claude logo, a file icon, the text "AGENTS.md not working?".

With:

> #1 "Claude Code Read My Rules and Ignored Them" (42 chars). Thumbnail: split terminal, left the rule, right the agent doing the opposite; creator with a flat stare. Text: "one line fixes it". Click 5, Deliver 5.
> Rejected: "The AGENTS.md Line Nobody Adds" ("Nobody" construction).

What changed: the contradiction is the title. The how-to frame and the "Nobody" title are dropped by rule.

## youtube-script

Prompt: `script the open for "I Ran 12 Coding Agents on One Mac. It Broke at 9"`

Without:

> "Hey everyone, welcome back. Today I want to talk about running multiple AI agents on a Mac. I have been testing this for a while and..."

With:

> 0:00 [screen: Activity Monitor, memory pressure red] "Agent nine is where this Mac gave up. Twelve were supposed to run."
> 0:06 "If you are about to buy a 128GB Mac for agents, this is the number you need before you pay."
> 0:14 "Here is the setup, the moment it broke, and the one setting that got me to eleven."
> 0:25 [pattern interrupt: cut to the terminal grid]

What changed: the failure is on screen in the first second. The promise and the stakes land before 15 seconds.

## youtube-virality-gate

Prompt: `gate this: "Local LLM Setup Tutorial 2026", 22 min screen recording, no test result in the video`

Without:

> "Looks good! Here are some tips to improve engagement..."

With:

> Gate 1 Packaging: FAIL. "Setup Tutorial" names the topic, gives no reason to click.
> Gate 3 Payoff: FAIL. No measured result, so the viewer has nothing to wait for.
> Gate 6 Length: FIX. 22 minutes for a setup with no result; cut to the first working run.
> Verdict: KILL until the video proves one thing. Re-gate as "It Took 4 Tries to Run Qwen on a Mac. Here Is the One That Worked".

What changed: a verdict with a reason per gate, and a re-package that gives the video a ceiling.
