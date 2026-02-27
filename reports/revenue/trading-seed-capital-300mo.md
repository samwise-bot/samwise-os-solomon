# Revenue Architecture Update — Trading Contribution for $300/mo Target

Date: 2026-02-27
Assumption used: target = **$300/mo**, hard floor = **$100/mo** (per filename + directive context). If Ian confirms different values, recompute immediately.

## Executive Take
- Trading should fund a **reliable portion** of monthly goal, not the whole stack.
- Under current long-only, lower-turnover framework, target trading contribution should be **$90–$150/mo** in normal months.
- Seed capital to support that contribution with reasonable stability: **$6k–$10k**.
- Full $300/mo from trading alone is possible but less reliable unless capital is materially higher.

## Seed Capital by Trading Contribution
Formula: `Seed = Monthly Trading Contribution / Net Monthly Return Assumption`

| Scenario | Net Return Assumption (monthly, net of slippage) | Trading Contribution Goal | Seed Capital Needed | Risk / DD Profile |
|---|---:|---:|---:|---|
| Conservative | 1.0% | $90/mo | $9,000 | Lower variance, DD ~8–12% |
| Base | 1.8% | $120/mo | ~$6,700 | Moderate variance, DD ~12–18% |
| Aggressive | 3.0% | $150/mo | $5,000 | Higher variance, DD ~18–28% |

## If Trading Tries to Cover Full $300/mo Alone
- 1.0% net/mo: **$30,000** seed
- 1.8% net/mo: **~$16,700** seed
- 3.0% net/mo: **$10,000** seed

Interpretation: full-coverage is capital-intensive for reliability; blended revenue is better risk-adjusted.

## Recommended Blended Model (Primary Recommendation)
Target stack:
- **Trading sleeve:** $120/mo expected (40%)
- **Non-trading stream A (retainer/service/automation support):** $120/mo (40%)
- **Non-trading stream B (micro-product/affiliate/template/digital asset):** $60/mo (20%)
- **Total expected:** $300/mo

## Weak-Month Resilience Design (must stay >=$100)
1. Set **floor budget** from non-trading base streams first:
   - Keep at least **$100/mo contracted/recurring** outside trading.
2. Trading risk throttle:
   - If rolling 20-trade expectancy drops below threshold or DD breach triggers, cut risk by 30–50%.
3. Carry a 2-month reserve buffer:
   - Reserve target = **$200+** (2 x hard floor) to absorb one weak month.
4. Monthly rebalance rule:
   - If total run-rate < $250 for 2 consecutive months, increase non-trading allocation effort, not trading leverage.

## Constraints (Why this structure)
- Long-only + lower turnover means smoother operations but fewer independent bets.
- Trading income is path-dependent month to month.
- Non-trading streams reduce dependency on market regime and improve minimum-floor reliability.
- Tax-aware holding improves long-run drag but can delay realization timing.

## Recommendation
- **Keep trading as secondary contributor (30–50% of monthly goal) until 6–12 months live edge is proven.**
- Build guaranteed non-trading baseline to hard floor first, then scale trading contribution.

## Source Context
- `MEMORY.md` (long-only, lower turnover, stock-only, adaptive process control)
- `memory/non-negotiables.md`
- `trading/STATE.md`, `trading/ALGO_CHANGELOG.md`, `trading/livefolio.md`
- Note: `memory_search` returned no additional indexed snippets; this is scenario-based planning with explicit assumptions.
