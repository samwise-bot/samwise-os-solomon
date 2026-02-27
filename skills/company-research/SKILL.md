---
name: company-research
description: Fast, source-cited equity company research for swing-trade decisions. Use for any stock analysis/report generation where you must: (1) pull and interpret 10-K/10-Q and quarterly statements, (2) synthesize fundamentals and management guidance, (3) assess current market/industry/news context, (4) retrieve recent price/volume/relative-strength and macro overlays, and (5) produce actionable entry/exit-ready outputs. Apply by default in all stock research subagent workflows.
---

Execute this workflow for every stock-analysis task.

## Non-negotiables
- Use stock-only mandate constraints from workspace memory.
- Prefer primary sources first (SEC filings, company releases, official data).
- Cite sources inline (URL + what was extracted).
- If a value cannot be verified from source, label it `UNVERIFIED`.
- Keep output decision-ready: thesis, trigger, stop, target, invalidation, risks.

## Parallel Research Pipeline (required)
Run these tracks in parallel when possible, then merge:

1. **Filings/Statements Track**
   - Pull latest 10-K/10-Q and most recent 8-K earnings release.
   - Extract: revenue growth/quality, gross/operating margin trend, FCF/CFO quality, debt/liquidity, guidance language changes, segment momentum, risk-factor deltas.
   - Use `references/filings-checklist.md`.

2. **Fundamentals Synthesis Track**
   - Convert raw filing metrics into a compact scorecard.
   - Identify what improved, worsened, and what must be true for thesis continuation.
   - Use `references/output-schema.md`.

3. **Market + Industry Context Track**
   - Pull past day/week catalysts: earnings revisions, analyst actions, product/company news, peer and sector context.
   - Separate hard facts from narrative.

4. **Price + Macro Track**
   - Pull current price context and past day/week regime data.
   - Include trend state, liquidity, volatility, and relative strength vs SPY.
   - Overlay tactical macro (rates, dollar, oil, vol).

5. **Final Integrator Track**
   - Resolve conflicts across tracks (primary-source evidence wins).
   - Output one action category: `ENTER TODAY`, `HOLD`, `SELL`, or `WATCHLIST`.
   - Include confidence (0-100) and top 3 disconfirming risks.

## Source Priority
Use `references/source-priority.md` and prefer top-priority sources first. If a source fails, use next fallback and mark fallback in output.

## Required Output Contract
Follow `references/output-schema.md` exactly.

## Daily 1% Improvement Loop (required)
After each major report:
1. Run mini-RCCA on each trade call quality (thesis, timing, risk, execution).
2. Log one concrete improvement to prompts/process in daily memory.
3. If same correction repeats 3 times, propose permanent rule promotion.
Use `references/improvement-loop.md`.

## Enforcement for subagents
For stock-research subagent prompts, explicitly include:
- "Apply the `company-research` skill workflow and output schema."
- "Run tracks in parallel, then integrate with source-cited evidence."
- "Return only actionable classification with explicit thresholds."
