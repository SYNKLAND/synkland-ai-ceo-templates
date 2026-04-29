# SYNKLAND AI-CEO Templates

> Prompt templates for running your one-person business as a hierarchical AI organization.

A set of MIT-licensed prompts that turn Claude / ChatGPT into a structured C-suite for your solo business or side project.

**Live demo / waitlist**: https://synkland.pages.dev
**Architecture writeup**: https://zenn.dev/synk/articles/d29140703b0dcf
**V2-F (AI Monthly Review, Stage 1 LP)**: https://synkland.pages.dev/v2/

> Failure is publicized here. Every venture launched under SYNKLAND has its post-mortem auto-published if it fails — see `/post-mortems/` (populated as ventures retire).

---

## Why this exists

Single-LLM workflows break after week 3:

- Context drifts between conversations
- You become the bottleneck for every decision
- Marketing advice contaminates accounting questions

The fix: organize AI as a **hierarchical organization** with clear roles, dedicated state files, and a single human approval point.

```
                ┌────────────┐
human approval ─→  │   AI-CEO   │  strategy, prioritization
                └─────┬──────┘
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼
   AI-CMO         AI-Writer       AI-CFO
   marketing      content         finance
```

## Repository layout

```
prompts/
├── ai_ceo.md        # top-level strategy + delegation
├── ai_cmo.md        # marketing, growth, channel ranking
├── ai_writer.md     # content drafting (blog, social, email)
└── ai_cfo.md        # cash flow, accruals, runway

examples/
├── state/
│   ├── roadmap.md   # owned by CEO
│   ├── marketing.md # owned by CMO
│   └── kpi.md       # shared
└── workflow_example.md

LICENSE
```

## Quick start

1. Clone the repo
2. Pick a role (start with `ai_ceo.md`)
3. Open Claude / ChatGPT and paste the prompt
4. Provide your `state/` files as context (or attach them)
5. Issue a single command, e.g. *"What is the highest-leverage task for this week?"*
6. Approve / reject the AI's recommendation — that's your only job

## Design principles

1. **One state file per role** — no shared mutable scratchpad
2. **Read-before-write** — every prompt begins with a state-load step
3. **One human gate per cycle** — Approve / Confirm / Publish, never partial edits
4. **BYOK by default** — never hardcode API keys; always pull from local secret store

## Compatible models

Tested with:

- Claude Sonnet 4.5 / 4.6
- GPT-4o / GPT-5
- Gemini 2.5 Pro

Should work with any model that supports >50k context.

## Contributing

Issues and PRs welcome. Especially needed:

- Translations (English, Japanese, Chinese, Spanish)
- Additional roles (AI-CTO, AI-COO, AI-Legal)
- Real-world state-file examples from your own business

## License

MIT — see `LICENSE`.

## About SYNKLAND

SYNKLAND is building an AI-CEO operating system for solo founders and indie developers. Zero-cost, BYOK, privacy-first. Join the waitlist: https://synkland.pages.dev
