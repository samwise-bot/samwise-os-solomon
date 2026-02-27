# Revenue Architecture Update — Trading Contribution for $300+/mo Target

Date: 2026-02-27
Policy baseline (corrected): **target >= $300/mo**, **hard floor >= $200/mo**.

## Executive Take
- Trading should contribute a reliable slice, not carry full revenue.
- Recommended trading contribution: **$100–$150/mo** under current long-only, lower-turnover framework.
- Seed capital to support that range with reasonable stability: **$7k–$12k**.
- Floor reliability (>=$200 in weak months) should come primarily from non-trading recurring streams.

## Seed Capital by Trading Contribution
Formula: `Seed = monthly trading contribution / net monthly return assumption`

| Scenario | Net Monthly Return (after slippage) | Trading Contribution Goal | Seed Needed | Risk / DD |
|---|---:|---:|---:|---|
| Conservative | 1.0% | $100 | $10,000 | DD ~8–12% |
| Base | 1.8% | $120 | ~$6,700 | DD ~12–18% |
| Aggressive | 3.0% | $150 | $5,000 | DD ~18–28% |

## If Trading Tries to Cover Full $300 Alone
- 1.0%: **$30,000**
- 1.8%: **~$16,700**
- 3.0%: **$10,000**

Conclusion: possible, but less reliable than blended model.

## Recommended Blended Model (for >=$300 target, >=$200 floor)
- **Trading:** $100–$150 expected (variable)
- **Non-trading recurring A:** $120 baseline
- **Non-trading recurring B:** $80 baseline
- **Expected total:** $300–$350+
- **Hard-floor design:** Non-trading baseline alone set to **>=$200/mo**.

## Weak-Month Resilience Design (must keep >=$200)
1. **Baseline-first rule:** lock non-trading recurring commitments at **$200+** before scaling risk.
2. **Trading drawdown throttle:** if expectancy or DD trigger trips, cut risk 30–50% immediately.
3. **Reserve buffer:** maintain at least **$400** (2 months of floor gap coverage for execution slippage/variance).
4. **Escalation rule:** if 2-month rolling total < $260, shift effort to non-trading acquisition, not leverage.

## Constraints (Why)
- Long-only + lower turnover = fewer independent bets; month-to-month variability persists.
- Income realization timing is path-dependent.
- Tax-aware holds improve long-run drag but can defer realized gains.
- Non-trading recurring revenue stabilizes floor reliability.

## Recommendation
Trading remains **secondary contributor** until 6–12 months of live audited expectancy confirms stability.

## Source Context
- `MEMORY.md`
- `memory/non-negotiables.md`
- `trading/STATE.md`
- `trading/ALGO_CHANGELOG.md`
- `trading/livefolio.md`
