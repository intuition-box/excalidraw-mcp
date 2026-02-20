# Excalidraw MCP

Local MCP server that streams hand-drawn Excalidraw diagrams with smooth viewport camera control and interactive fullscreen editing.

This project is maintained at:
`https://github.com/intuition-box/excalidraw-mcp`

This repository is intended for local usage only with the Claude Code Desktop app.

![Demo](docs/demo.gif)

## Install (Local Only, Claude Code Desktop App)

```bash
git clone https://github.com/intuition-box/excalidraw-mcp.git
cd excalidraw-mcp
pnpm install
pnpm run build
```

## Configure Claude Code Desktop App

1. From the repo root, run:

```bash
realpath dist/index.js
```

2. Copy the output path and paste it into the first `args` value below.
2. Update `~/Library/Application Support/Claude/claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "excalidraw": {
      "command": "node",
      "args": ["/absolute/path/from-realpath", "--stdio"],
      "env": {
        "OBSIDIAN_VAULT_PATH": "/absolute/path/to/your/Obsidian/vault"
      }
    }
  }
}
```

Then restart the Claude Code Desktop app.

## Usage

Example prompts:
- "Draw a cute cat using excalidraw"
- "Draw an architecture diagram showing a user connecting to an API server which talks to a database"

## Contributing

PRs welcome.

## Credits

Built with [Excalidraw](https://github.com/excalidraw/excalidraw), a virtual whiteboard for sketching hand-drawn diagrams.

## License

MIT
