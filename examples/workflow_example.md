# Workflow example: weekly Monday review

This is a realistic 30-minute workflow showing how the four prompts coordinate on a Monday morning.

## 09:00 — Open AI-CEO

You: paste `ai_ceo.md` + your `state/roadmap.md` + `state/shared/kpi.md` + `state/shared/brand.md`.

You: *"It's Monday. What's the highest-leverage task this week?"*

AI-CEO: returns ranked options + one recommendation + "Decision needed: Approve recommendation."

You: Approve.

## 09:10 — Delegate to AI-CMO

You: paste `ai_cmo.md` + your `state/marketing.md` + the approved CEO recommendation.

You: *"Design the experiment to execute the CEO's #1 recommendation this week."*

AI-CMO: returns funnel snapshot + proposed experiment with falsifiable success criterion.

You: Approve or reject. If approved, AI-CMO outputs the state file diff for `marketing.md`.

## 09:20 — AI-Writer drafts the asset

You: paste `ai_writer.md` + your `state/content.md` + the approved experiment.

You: *"Draft the launch tweet for the experiment."*

AI-Writer: returns one publish-ready tweet ≤ 280 chars + 1 alt headline.

You: Publish.

## 09:25 — AI-CFO sanity check (optional, monthly)

If the experiment costs anything, paste `ai_cfo.md` + `state/finance.md` + experiment cost.

AI-CFO: confirms whether spend is within budget + updates runway.

## 09:30 — Done

You committed one decision per role. Your only output was Approve / Reject / Publish. The AIs handled the rest.

---

## What this is NOT

- **Not autonomous**: nothing happens without your Approve gate
- **Not multi-tasking**: one thing per role per cycle
- **Not memory-resident**: every cycle re-reads state files (no drift)
- **Not opinion-free**: each AI has strong refusals built in (anti-patterns)

The whole point is that the AIs do the analysis and you do the deciding.
