# LIVEFOLIO.md

ALGO_VERSION: v2026.02.27-intraday-r3
Lifecycle Stage: Paper launch (T+0, conditional orders staged)
Start Date: 2026-02-27
Benchmark: VOO

## Executed Paper Orders (Today)
Status: **LLY filled, META still conditional**

| Ticket | Type | Entry | Stop | Target | Shares | Allocation | Notional | Status |
|---|---|---:|---:|---:|---:|---:|---:|---|
| LLY | Buy | 1024.76 | 983.30 | 1103.40 | 0.053671 | 55.04% | $55.00 | FILLED |
| META | Buy | 643.08 | 635.80 | 701.60 | 0.069976 | 45.00% | $45.00 | FILLED |

Fill confirmation source: user-provided broker screenshots at 06:46 PT (LLY avg cost 1024.76; META avg cost 643.08).

## Allocation Plan (Current)
- Starting capital: **$100.00**
- Filled exposure: **$100.00**
- Cash unallocated: **$0.00**
- Conditional reserve: **$0.00**

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
