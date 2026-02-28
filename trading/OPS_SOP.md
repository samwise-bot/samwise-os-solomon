# Solomon CFO Operating SOP (v1)

ALGO_VERSION: v2026.02.27-ops-v1

## 1) Operating Model
- Solomon-core = orchestrator (single writer for canonical portfolio state).
- Async specialist desks:
  1. Macro/Regime
  2. Fundamentals/EDGAR
  3. News/Sentiment
  4. Portfolio/Risk
  5. Execution Planner
  6. Ops/Bookkeeping
- Artifact bus: each desk writes structured output into dated markdown/json under `reports/` and `research/`.

## 2) Execution Rules
- Fan-out desks in parallel.
- Per-desk timeout + output quality checklist.
- Merge only if evidence threshold met (>=2 independent signals for thesis-critical claims).
- Reproducibility required: include timestamp, source links, model/run context in outputs.

## 3) Model Routing
- Tier A: retrieval/normalization/rendering.
- Tier B: thesis synthesis/reconciliation (default).
- Tier C: regime shifts, conflict resolution, post-mortem, high-impact portfolio decisions.
- Escalate to Tier C on drawdown breach, cross-desk conflict, major macro event week, concentration-risk breach.

## 4) Daily Cadence (Market Days)
- T-90m: macro regime + overnight risk scan
- T-60m: EDGAR/fundamentals deltas for held/watch names
- T-45m: sentiment/catalyst map
- T-30m: ranked candidates + no-trade list
- T-15m: CFO risk gate (liquidity, sizing, concentration, event risk)
- Publish: premarket report (ADD/SELL/HOLD/WATCHLIST)
- Post-close: attribution + RCCA + next-day priorities

## 5) Risk Guardrails
- Long-only (no shorting) for this sleeve.
- New names must be enterable today, else WATCHLIST.
- Hold unless thesis breaks (tax-aware lower turnover).
- Position/risk caps enforced before publish.
- Human-in-the-loop for live execution.
- Paper-trading and Livefolio streams remain separate.

## 6) Crypto/BTC Lane (Separate)
- Separate risk budget, separate reporting section, separate limits.
- Daily lightweight monitor + weekly deep-dive.
- No contamination of core equity sleeve constraints.

## 7) KPI Pack (Weekly)
- Decision quality: hit rate, avg win/loss, expectancy, thesis fidelity
- Risk: max drawdown, return volatility, concentration index, beta drift
- Ops: report timeliness, freshness SLA, agent turnaround p50/p95, evidence density
- Behavior: turnover vs target, % out-of-plan trades
