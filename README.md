# 8digit Planner plugin

Official plugin for [8digit Planner](https://planner.8digitcreative.com). It connects Claude, Claude Code, ChatGPT and Codex to your Planner workspaces through Planner's remote MCP server and adds the Planner skill. 8digit Planner is a content calendar for creators, personal brands, studios and agencies who need a client or a teammate to approve posts before they go out. Upload finished photos and videos, plan posts, carousels, Stories and Reels, and get them reviewed with timestamped comments. Guest reviewers do not need a seat. From your AI assistant, say “plan my first post”: it lists your brands, uploads the files you choose, drafts and schedules posts and asks for approval when you want it. Built for people who manage content for a brand, their own personal brand or their clients.

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
