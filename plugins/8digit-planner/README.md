# 8digit Planner

Plan and review social media content in [8digit Creative Content Planner](https://planner.8digitcreative.com) from Claude, Claude Code, ChatGPT or Codex. Your assistant can read your content calendar, upload finished images and videos, prepare posts, carousels and Library folders, and handle approvals you explicitly ask for. Publishing to social networks stays manual.

## What this plugin contains

- **A remote MCP server connection** (`.mcp.json` for Claude, `mcp.json` for the portable plugin format): one server at `https://planner.8digitcreative.com/mcp`, using Streamable HTTP with OAuth sign-in. No local program is installed or executed by this plugin.
- **The Planner skill** (`skills/planner/SKILL.md`): plain-text instructions that tell the assistant how to use the tools safely, for example to confirm the post before withdrawing an approval, deleting a post or marking it published.
- **Manifests** (`.claude-plugin/plugin.json`, `.codex-plugin/plugin.json`, `plugin.json`): name, version, description and license only.

## What it sends and where

The assistant sends tool requests over HTTPS only to `planner.8digitcreative.com`: workspace, brand and post identifiers, titles, captions, dates, folder names and the files you choose to upload. Sign-in happens in your browser on the Planner site with Google or email; the plugin never handles passwords, tokens or API keys. The server runs each request with your current Planner permissions, only in the workspaces and brands you selected when connecting. Private files and Guest access are never available to apps.

## Install

- **Claude Code:** `claude plugin marketplace add 8digit/8digit-planner-plugin`, then `claude plugin install 8digit-planner@8digit`. Run `/mcp`, choose 8digit-planner and Authenticate.
- **Codex:** `codex plugin marketplace add 8digit/8digit-planner-plugin`, then `codex plugin add 8digit-planner@8digit`, and sign in when asked.
- **Claude and ChatGPT:** add the connection URL above as a custom connector or plugin, or install 8digit Planner from their directories where it is listed.

The full guide, including a setup prompt you can paste into any of these apps, is at <https://planner.8digitcreative.com/connect-ai>.

## Permissions

You choose workspaces and brands during sign-in. Withdrawing approvals, deleting posts (Library files are kept) and marking posts as published are optional actions that stay off until you allow them. Manage or revoke a connection anytime in Planner → Account → Apps & connections.

## Support

[planner.8digitcreative.com/support](https://planner.8digitcreative.com/support) · [Privacy](https://planner.8digitcreative.com/privacy) · [Terms](https://planner.8digitcreative.com/terms)

Released under the MIT License by 8digit Creative LLC. The license covers the files in this plugin; the Planner service has its own terms.
