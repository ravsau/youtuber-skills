---
name: youtube-comments-to-ideas
description: "5 video ideas from pasted comments, each tied to the comment that proves demand. Use when asked what viewers want next."
argument-hint: "[pasted comments, or a video URL if the agent can fetch comments]"
---

# YouTube Comments to Ideas

Input: pasted comments from one or more videos. A video URL works if the agent can fetch comments.
Data source: if `youtube-connect` is set up, fetch the comments with the Data API. Else ask the user to paste them.
Output: 5 video ideas, each with the quoted comment, the buyer, a working title, and a demand count.

## Steps

1. Read every comment. Drop praise, spam, and replies to other viewers.
2. Group the rest by the question or complaint under them. Count comments per group.
3. Keep the 5 largest groups that the creator can answer with a demo.
4. For each group, quote the clearest comment and write one title that answers it.
5. Rank by count, then by how well the title packages.

## Rules

- One idea per group. Never split one question into two videos.
- The title must answer the comment, not restate it.
- Quote the comment word for word. Trim, never paraphrase.
- Say "1 comment" when demand is one comment. Do not round up.

CRITICAL: an idea with no quoted comment is a guess and does not belong in the output.

## Output format

```markdown
## Ideas from [N] comments

| # | Idea title | Count | Buyer | Proof comment |
|---|-----------|-------|-------|---------------|
| 1 | ... | 7 | ... | "..." |

### Do first: #N
Why: one line.
```

## Example

Input: `42 comments from "I Ran 12 Coding Agents on One Mac. It Broke at 9"`

| # | Idea title | Count | Buyer | Proof comment |
|---|-----------|-------|-------|---------------|
| 1 | The Setting That Got Me From 9 Agents to 11 | 9 | Dev with a 128GB Mac | "what did you change to get past 9, mine dies at 6" |
| 2 | 64GB Mac, Same Test: Where It Breaks | 6 | Dev deciding on RAM | "would love to see this on 64gb before I buy" |
| 3 | Do Agents Break the Same Way on Linux? | 4 | Linux dev | "is this a macOS memory thing or would a linux box do the same" |
| 4 | One Agent, 12 Tabs: Is It Cheaper? | 3 | Cost-aware dev | "why not one agent with 12 worktrees, what does that cost" |
| 5 | Swap vs RAM: What Actually Slowed It Down | 1 | Curious viewer | "was it swap or cpu, activity monitor looked odd" |

Do first: #1. Nine viewers asked the same question, and the answer is a 5-minute demo.
