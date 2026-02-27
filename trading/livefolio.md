# LIVEFOLIO.md

ALGO_VERSION: v2026.02.27-intraday-r3
Lifecycle Stage: Paper launch (T+0, conditional orders staged)
Start Date: 2026-02-27
Benchmark: VOO

## Executed Paper Orders (Today)
Status: **Conditional entries placed (not yet marked filled)**

| Ticket | Type | Trigger / Entry | Stop | Target | Allocation | Notional Reserved | Status |
|---|---|---:|---:|---:|---:|---:|---|
| LLY | Buy-stop | 1033.00 | 983.30 | 1103.40 | 55% | $55.00 | STAGED |
| META | Buy-stop | 663.60 | 635.80 | 701.60 | 45% | $45.00 | STAGED |

Execution policy:
- If trigger prints intraday, mark fill at trigger (or next traded price in paper model) with conservative slippage.
- If neither trigger prints by close, both remain watchlist and no fill is recorded.

## Allocation Plan (Current)
- Cash available: **$100.00**
- Reserved for staged entries: **$100.00**
- Filled exposure: **$0.00**

## REMOVE / SELL
- None (no active filled positions).

## Active Watchlist (Ranked)
| Ticker | Trigger | Stop / Invalidation | Target | Action |
|---|---:|---|---:|---|
| NVDA | 185.80–186.70 reclaim | 177.20 / close < 177.20 | 201.10 | WATCHLIST |
| AMZN | 210.00–213.90 reclaim | 199.80 / close < 199.80 | 225.00 | WATCHLIST |
| BAC | 52.14 reclaim | 49.16 / close < 49.16 | 57.53 | WATCHLIST |

## Slippage/Execution Assumptions
- Trigger entries via buy-stop simulation.
- If open gap > +2% above trigger: cut planned allocation by 50%.
- Fractional shares allowed in $100 sleeve.

## Performance Snapshot
- Portfolio return since start: 0.00% (no fills yet)
- VOO return since start baseline: 0.00%
- Relative alpha: 0.00%
