# Social media agents for Claude Code

Two Claude Code subagents that run your Instagram and Facebook. They write the
drafts. You post them.

Looking for the Premiere Pro video editor (`/pr-agent`)? It has its own repo:
[premiere-pro-agent](https://github.com/barbavcariaso-hub/premiere-pro-agent).

| Agent | What it does |
| --- | --- |
| `instagram` | Reels, captions, carousels, stories, weekly plans, profile fixes, comments, replies, DMs, repurposing, viral research, insight audits. Sends each request to the right `ig-*` skill and runs them in order when a job needs more than one. |
| `facebook` | Page posts, group posts, Reel captions, comment and Messenger replies, weekly plans, Page bio fixes, reposting Instagram content for Facebook, and Page insights via Windsor.ai. |

## Install

1. Install the Instagram skills the agents depend on:
   ```
   /plugin marketplace add Jakeschincariol/instagram-agent-skill
   /plugin install instagram-agent
   ```
2. Copy the agents:
   ```bash
   git clone https://github.com/barbavcariaso-hub/social-media-agents.git
   cp social-media-agents/agents/*.md ~/.claude/agents/
   ```
3. Restart Claude Code, then set up your voice file. Paste 3 of your own posts
   and say "write my voice.md from these". It's saved to
   `~/.claude/instagram/voice.md`, and both agents read it.
4. Optional: connect Facebook Organic in Windsor.ai so the Facebook agent can
   read your Page insights.

## Usage

```
use the instagram agent to plan my week
facebook agent: turn my last reel into a Page post
```

## Rules the agents follow

- They never post, send, comment or DM. You paste the final copy yourself.
- All copy goes through the `ig-human` humanizer, which strips out writing that sounds like AI.
- Drafts and plans are saved to `~/.claude/instagram/` and `~/.claude/facebook/`.
