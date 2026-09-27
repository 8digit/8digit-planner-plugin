# 8digit Planner plugin

Official plugin for [8digit Creative Content Planner](https://planner.8digitcreative.com). It connects Claude Code, Codex, Claude and ChatGPT to your Planner workspaces through Planner's remote MCP server and adds the Planner skill. Plan the content calendar, upload finished images and videos, prepare posts and carousels, and handle approvals you ask for. Publishing to social networks stays manual.

This repository is also a plugin marketplace named `8digit` for Claude Code and Codex.

## Install

**Claude Code**

```sh
claude plugin marketplace add 8digit/8digit-planner-plugin
claude plugin install 8digit-planner@8digit
```

Then run `/mcp`, choose `8digit-planner` and Authenticate.

**Codex**

```sh
codex plugin marketplace add 8digit/8digit-planner-plugin
codex plugin add 8digit-planner@8digit
```

**Claude (web, desktop, Cowork) and ChatGPT:** add `https://planner.8digitcreative.com/mcp` as a custom connector or plugin, or install 8digit Planner from their directories where it is listed. Step-by-step guide and a setup prompt: <https://planner.8digitcreative.com/connect-ai>.

## Contents

| Path | Purpose |
| --- | --- |
| `plugins/8digit-planner/` | The plugin: MCP connection, Planner skill, manifests, README and license |
| `.claude-plugin/marketplace.json` | Claude Code marketplace |
| `.agents/plugins/marketplace.json` | Codex marketplace |

The plugin contains configuration and instructions only. It installs and runs no local code; every request goes over HTTPS to `planner.8digitcreative.com` with your own sign-in and permissions. See the [plugin README](plugins/8digit-planner/README.md) for exactly what it sends.

## License

MIT, © 2026 8digit Creative LLC. The license covers the files in this repository; the Planner service itself is governed by its [terms](https://planner.8digitcreative.com/terms).
