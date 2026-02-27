# Trading Seed Capital Analysis for $100/month Goal

Date: 2026-02-27
Framework: Long-only, lower-turnover swing sleeve (macro + filings + fundamentals + sentiment)

## Executive Answer
- **Can this framework sustainably target $100/month?** Yes, but only with adequate capital, disciplined risk limits, and acceptance of uneven monthly outcomes.
- **Practical base-case seed capital:** **$5,000–$8,000**.
- **Conservative seed capital:** **~$10,000+** for higher reliability and lower pressure.
- **Recommendation:** Treat trading as **secondary path** to the $100/month goal until at least 6–12 months of live audited edge is proven.

## Core Assumptions
1. Net monthly return assumptions are **after** slippage/fees, before taxes.
2. Lower-turnover approach reduces churn/tax drag but lowers trade frequency.
3. Long-only means downside beta to market regime; no short-side hedge alpha.
4. Position risk discipline remains intact (no leverage creep to force income).

## Scenario Table (Target = $100/month)
| Scenario | Net Monthly Return Assumption | Approx. Max DD Range | Confidence Band (12M average monthly return) | Required Starting Capital for $100/mo | Notes |
|---|---:|---:|---:|---:|---|
| Conservative | 1.0% | 8–12% | 0.2%–1.5% | **$10,000** | Most robust for low-noise execution; tolerates weak months better |
| Base | 2.0% | 12–18% | 0.5%–3.0% | **$5,000** | Reasonable if process edge persists and discipline holds |
| Aggressive | 4.0% | 20–30% | 0%–6% | **$2,500** | Least reliable; return path volatility high, risk of behavioral errors |

Formula used: `Required Capital = $100 / monthly return assumption`.

## Sustainability Constraints (Why)
- **Regime dependency:** Long-only swing performance degrades in choppy/down macro phases.
- **Variance clustering:** Small books see lumpy PnL; monthly target becomes path-dependent.
- **Execution friction:** Slippage + imperfect fills materially affect small-capital expectancy.
- **Tax-aware hold bias:** Good for drag reduction, but can delay profit realization timing.
- **Opportunity pacing:** Lower turnover means fewer independent bets; confidence requires longer sample.

## Practical Capital Guidance
- **Minimum experimental capital:** $2,500 (aggressive, unstable monthly consistency).
- **Operational minimum:** $5,000 (base-case viability).
- **Preferred reliability band:** $8,000–$12,000 (better chance of stable $100/month without overtrading).

## Decision: Primary vs Secondary Path to $100/month
**Recommendation: Secondary path (for now).**
- Promote to primary only if all are true:
  1) 6+ months live data,
  2) positive expectancy net of slippage,
  3) max drawdown within pre-set tolerance,
  4) consistent rule adherence with no leverage drift.

## Immediate Implementation Notes
- Keep reporting lifecycle-aware (process KPIs + performance KPIs).
- Continue $100 paper-to-live calibration before increasing capital.
- Re-estimate required seed quarterly using realized return distribution, not static assumptions.

## Sources / Context
- Workspace memory and directives in `MEMORY.md` (long-only, lower-turnover, stock-only, explicit risk policy).
- Current rule docs: `memory/non-negotiables.md`, `trading/STATE.md`, `trading/ALGO_CHANGELOG.md`, `trading/livefolio.md`.
- Note: `memory_search` returned no additional indexed snippets; assumptions above are explicitly scenario-based.
