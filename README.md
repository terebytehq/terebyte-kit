# Terebyte for AI agents

Give an AI a room in your encrypted Terebyte vault: it sees that room and nothing else.

Terebyte is end-to-end encrypted cloud storage. This MCP server lets an assistant or an agent work in one room a
member opens to it: list, read and write files, make a Sealed Link, and use the room's board. The member pairs it with
a 6-character code and chooses what it may do and for how long. Everything is encrypted and decrypted on the computer
it runs on; Terebyte's servers see only sealed bytes.

The server is the `terebyte` package on npm ([source and docs](https://terebyte.com/developers/mcp-server)); this
repository holds the listings that run it.

## Claude, ChatGPT, Cursor, Claude Code

From kit 0.1.2, the fastest way: [terebyte.com/connect](https://terebyte.com/connect), or on your computer:

```
npx terebyte connect claude      # or chatgpt, cursor, claude-code
```

Until then: `npx terebyte bridge` shows your connector's address to add as a custom connector.

## Gemini CLI

```
gemini extensions install https://github.com/terebytehq/terebyte-kit
```

## Claude Code plugin

```
/plugin marketplace add terebytehq/terebyte-kit
/plugin install terebyte@terebyte
```

## Any MCP client (stdio)

```json
{ "mcpServers": { "terebyte": { "command": "npx", "args": ["-y", "terebyte", "mcp"] } } }
```

The first call shows a 6-character code. In Terebyte, open **Rooms → Connect an agent**, type it, and approve the door:
the room, what it may do, and for how long. Nothing you keep reaches the agent until you do.

Privacy: [terebyte.com/privacy](https://terebyte.com/privacy). Help: support@terebyte.com. License: Apache-2.0.
