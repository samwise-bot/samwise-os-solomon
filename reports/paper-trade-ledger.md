# Paper Trade Ledger

ALGO_VERSION: v2026.03.03-rcca-r2
MANDATE: $100 seed, long-only, pure stocks (no ETFs in portfolio)

## Starting Capital
- Initial paper capital: $100.00

## Position Ledger

| Date | Ticker | Side | Qty (sh) | Fill | Slippage Rule | Gross Cash Flow | Reason | Status |
|---|---|---:|---:|---:|---|---:|---|---|
| 2026-02-27 | LLY | BUY | 0.053671 | 1024.76 | +0.00% (baseline carry) | -55.00 | Entry from prior session | OPEN |
| 2026-02-27 | META | BUY | 0.069976 | 643.08 | +0.00% (baseline carry) | -45.00 | Entry from prior session | CLOSED 2026-03-02 |
| 2026-03-02 | META | SELL (stop) | 0.069976 | 634.53 | -0.20% adverse vs stop (conservative) | +44.40 | Stop breach (low 634.50 < 635.80 stop) | FILLED |

## 2026-03-02 Open/Close Decisions (RCCA before metrics)

| Decision | R (Reality) | C (Cause) | C (Counterfactual) | A (Action) |
|---|---|---|---|---|
| OPEN: Hold LLY | Open 1045.98, above invalidation 983.30 | Thesis not invalidated | If open below invalidation, de-risk immediately | HOLD through open |
| OPEN: Monitor META stop | Open 637.16, tight to stop 635.80 | Name entered with narrow invalidation buffer | With wider ATR-aware stop/size, forced exit probability drops | Keep stop discipline; no override |
| CLOSE: Execute META stop exit | Intraday low 634.50 breached stop | Stop-loss condition satisfied | Ignoring stop would violate risk contract | SELL filled at 634.53 with -0.20% adverse slippage |
| CLOSE: Hold LLY | Close 1017.97, still above 983.30 | Drawdown but no invalidation | Premature exit cuts upside without rule trigger | HOLD overnight |

## 2026-03-03 Open/Close Decisions (RCCA before metrics)

| Decision | R (Reality) | C (Cause) | C (Counterfactual) | A (Action) |
|---|---|---|---|---|
| OPEN: Hold LLY | Open 1011.33, above invalidation 983.30 | No thesis-break gap; risk level unchanged | If open had gapped below 983.30, force exit at open with conservative slippage | HOLD through open |
| CLOSE: Hold LLY | Low 995.07 > stop 983.30; close 1007.73 | Stop never triggered; rule set favors trend continuation until invalidation | Exiting on non-trigger weakness increases churn and degrades expectancy | HOLD overnight, no fill |

## Simulated Fills (Conservative Slippage)
- 2026-03-03: No fills. Existing LLY stop was not touched (session low 995.07 > 983.30).

## Equity Curve vs VOO (baseline = 100 on 2026-02-27 fills)

| Date | Portfolio Equity | Portfolio Return | VOO Return (reference only) | Alpha vs VOO |
|---|---:|---:|---:|---:|
| 2026-02-27 close | 101.82 | +1.82% | +0.00% | +1.82% |
| 2026-03-02 close | 99.04 | -0.96% | +0.03% | -0.99% |
| 2026-03-03 close | 98.48 | -1.52% | -0.86% | -0.66% |

## Metrics (as of 2026-03-03 close)
- Daily return: **-0.56%** (vs 2026-03-02 close equity)
- Total return: **-1.52%** (since $100 start)
- Max drawdown: **-3.28%** (peak 101.82 -> 98.48)
- Win rate (closed trades): **0.0%** (0/1)
- Expectancy (closed trades): **-$0.60/trade** (META realized)

## Risk / Exposure Snapshot
- Open positions: LLY only
- Position value: $54.08 (54.91% of equity)
- Cash: $44.40 (45.09% of equity)
- No ETF holdings in portfolio (VOO used only as benchmark)

## 1% Process Improvement Logged (company-research loop)
- Improvement: add a **"research freshness TTL" gate** to each ticker thesis card (max 48h since last catalyst/filing verification) so stale theses are auto-downgraded before open decisions.

## Concrete Self-Iteration for Tomorrow
- Add a one-line `THESIS_FRESHNESS_HOURS` field to pre-open decision rows and auto-mark any position >48h stale as `REVALIDATE_REQUIRED` before allowing HOLD/ADD outcomes.
