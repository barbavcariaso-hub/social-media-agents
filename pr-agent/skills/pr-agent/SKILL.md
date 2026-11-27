---
name: pr-agent
description: Edit video in Adobe Premiere Pro with the pr agent - cuts, silence removal, captions, motion graphics, 9:16 reframes, exports. Type /pr-agent followed by what you want.
argument-hint: <what to do in Premiere, e.g. "remove silences and make a 9:16 version">
context: fork
agent: pr
disable-model-invocation: true
---

Do this in Adobe Premiere Pro:

$ARGUMENTS

If nothing was asked above, check the connection to Premiere, list the open
project's sequences and any .mogrt templates you can find, then ask what to edit.
