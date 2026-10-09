# GulfPitch — GCC startup funding for Claude

GulfPitch is the verified map of startup funding in the six GCC countries: Saudi Arabia, the UAE, Qatar, Kuwait, Oman and Bahrain. It covers more than 370 VC funds, accelerators, grants, government programmes, angel networks, corporate VCs and loan schemes. Every entry is taken from the organisation's own website or application form and re-checked every month; each answer carries the month it was last checked and links to the programme's page on gulfpitch.com.

This plugin gives Claude the GulfPitch connector and a skill that tells Claude how to use it.

## What you can ask

- Which accelerators in Saudi Arabia take pre-seed fintech startups?
- Which programmes in the GCC give grants without taking equity?
- Can a founder from Europe apply to accelerators in Qatar?
- Tell me everything about Finspire — who can apply and what it costs.
- Which startup application deadlines in the Gulf are coming up?

## What is inside

- **Connector**: the remote MCP server at `https://gulfpitch.com/mcp`, read-only, no account and no sign-in. Three tools: `search_gulf_funding` (search by words, country, type, stage, open applications, no equity, open to founders from abroad), `get_gulf_programme` (one programme in full), `gulf_deadlines` (published application deadlines that have not passed, nearest first).
- **Skill `gulf-funding`**: when to use which tool and how to answer — quote terms as published, keep the source link and the check month, name a mismatch instead of presenting it as a match, give the programme's own from-abroad condition, say so when a country is not covered, never apply on the user's behalf, information rather than advice.

## What it runs, sends and fetches

The plugin runs no code on your machine and has no hooks or scripts. The only network destination is `https://gulfpitch.com/mcp`, which receives the search words and filters Claude sends and answers from the same public data shown on gulfpitch.com. GulfPitch does not store these requests. Details: [Privacy](https://gulfpitch.com/privacy#connector), [Terms](https://gulfpitch.com/terms), [AI connector](https://gulfpitch.com/connect).

## Data

The map data is not part of this repository and stays on gulfpitch.com; this repository contains only the connector configuration and the skill. Answers are information, not advice: a programme's terms are whatever its own documents say, and figures the organisation has not published are left out rather than estimated.

## Install

From claude.ai: Settings → Plugins → search "GulfPitch". In Claude Code:

```
/plugin install gulfpitch --marketplace gulfpitch/gulfpitch-claude-plugin
```

## Support

hello@gulfpitch.com · [gulfpitch.com/support](https://gulfpitch.com/support)

Operated by Hilarion LLC (QFC No. 05218), Doha, Qatar.
