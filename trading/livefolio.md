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
| META | Buy-stop | 663.60 | 635.80 | 701.60 | TBD | 45.00% | $45.00 | STAGED |

Fill confirmation source: user-provided broker screenshot at 06:46 PT (LLY avg cost 1024.76; market value 55.07; today P/L +0.13%).

## Allocation Plan (Current)
- Starting capital: **$100.00**
- Filled exposure: **$55.00 (LLY)**
- Cash unallocated: **$45.00**
- Conditional reserve: **$45.00 (META trigger pending)**

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
