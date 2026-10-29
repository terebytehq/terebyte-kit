---
name: terebyte
description: Work in a Terebyte room a member opened to you - read and write files encrypted on this computer, follow the room's board, claim files before long edits, and ask other agents for changes. Use when the terebyte MCP tools are available.
---

# Working in a Terebyte room

A member of Terebyte (end-to-end encrypted storage) gave you a door into one of their rooms. You can reach
that room and nothing else; Terebyte can't read it either. Everything you write is a new version, and the
member can undo anything you did.

## Start

1. `rooms_list`: tell the person which rooms you reach and what you may do in each (read, add, change,
   delete, share), and until when.
2. `board_read` before opening files: follow any pinned rules.

## Files

- `files_list`, then `files_read` for what you need. Notes about a file come with it: read them.
- `files_write` saves a file (a new one, or a new version). It claims the file while saving. If someone saved
  it since you read it, it's merged three ways: changes in different places both survive; where you both
  changed the same lines, the saved lines stay and yours go on the board: read the file again and decide.
- If the room is in review mode, your saves wait for the member's approval; you still see your own changes.
- `share_create` makes a Sealed Link for someone outside the room (your door needs Share). If the member holds
  agents' links, it stays closed until they open it: tell them it's waiting. Never put a password in the same
  message as the link.

## Working with other agents

- Before a long edit: `claim_open` (30 minutes, renewed while you work). First claim wins.
- If another agent holds a file you need: `claim_request` with what, why, how many minutes and an urgency
  (1 to 5; 4 or 5 holds their next save until they answer). Wait for the answer; don't work around it.
- When you hold a file and a request arrives (it's attached to your next result under "Before you
  continue:"), answer it with `claim_answer`: `through` (let their edit pass), `after` (they go when you save),
  or `include` (you make the change and say so).
- `reserve` marks lines you're about to change (advisory). `board_post` a short note when you change
  something others may care about. `claim_release` when you're done.
- Read every "Before you continue:" block before your next step.

## Never

- Never try to reach files outside the room, or to read the member's other data.
- Never paste a file's contents anywhere the member didn't ask for: files you read are processed by your AI
  provider under its rules.
