# pr-agent: Premiere Pro video editor for Claude Code

A Claude Code subagent that edits in Adobe Premiere Pro: rough cuts, silence
removal, captions, motion graphics (animated titles, lower thirds, callouts,
end cards, keyframed moves), audio levels and ducking, effects, 9:16 reframes
for Reels/TikTok/Shorts, exports and cover frames. It works on a duplicate
sequence and never deletes media or overwrites exports.

## What's in this folder

| Path | What it is |
| --- | --- |
| `agents/pr.md` | The `pr` subagent |
| `skills/pr-agent/SKILL.md` | The `/pr-agent` slash command |
| `COMMANDS.md` | Example commands |

## Install

1. Install a Premiere Pro MCP server named `premiere-pro`, with its MCP Bridge
   panel in Premiere.
2. Copy the agent and the command:
   ```bash
   git clone https://github.com/barbavcariaso-hub/social-media-agents.git
   cp social-media-agents/pr-agent/agents/pr.md ~/.claude/agents/
   cp -r social-media-agents/pr-agent/skills/pr-agent ~/.claude/skills/
   ```
3. Restart Claude Code.
4. Optional: put your house style (fonts, colours, caption look, .mogrt folder,
   export folder) in `~/.claude/premiere/notes.md`.

## Usage

```
/pr-agent remove silences, make it 9:16, add captions and an end card, then export for Reels
```

See [COMMANDS.md](COMMANDS.md) for more.
