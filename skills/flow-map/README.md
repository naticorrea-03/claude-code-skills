# flow-map

Audit your whole automation system (cloud agent routines, crons, LaunchAgents, no-code automations) and render it as one dark, interactive, single-file HTML data-flow map. Four columns: Sources → Agents/routines → Stores → Outbox. Hover any node to isolate its flows. Includes a Schedule tab and a Changed tab so the map explains its own history.

## Setup (2 minutes)

1. Copy this folder to your skills directory (Claude Code: `~/.claude/skills/flow-map/`).
2. That's it. No accounts, no API keys. Output is a local HTML file that works from a double-click.

## Run

Say `/flow-map` or "map my data flows". The agent will:

1. Ask what's in scope.
2. Enumerate your live schedulers (cron, LaunchAgents, cloud routines, CI crons) and read their actual configs.
3. Interview you once, multiple-choice, about what discovery can't see (Zapier, webhooks, recently retired things).
4. Fill `template.html`'s data block and hand you the finished map.

## Design principle

The map only shows what the agent can prove is running. Docs and memory are leads, not evidence. Anything unverifiable is drawn with an explicit "not verified" flag instead of being silently trusted.
