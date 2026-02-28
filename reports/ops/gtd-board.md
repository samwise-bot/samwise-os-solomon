# GTD Task Board — Solomon CFO Ops (Week 1)

## Inbox
- [ ] Confirm preferred risk budget for crypto lane (default: observation-only week 1).
- [ ] Confirm KPI reporting format preference (compact vs full).

## Projects

### P1 — Async Research System v1
- [ ] Day 1: finalize folder schema and canonical state files
- [ ] Day 2: implement Macro/Fundamentals/News/Risk worker templates
- [ ] Day 3: implement orchestrator merge + confidence scoring
- [ ] Day 4: add CFO gates + pre-publish hard rule checks
- [ ] Day 5: publish standard premarket/post-close templates + KPI rollup
- [ ] Day 7: dry run + retro + lock SOP v1

### P2 — Company Research Skill Hardening
- [ ] Add filing cache index (`as_of`, `filing_date`, `last_full_read`)
- [ ] Add weekly-light/monthly-deep refresh routines
- [ ] Add evidence scorecard to output schema

### P3 — Portfolio Stream Separation Enforcement
- [ ] Keep Livefolio-only updates in `trading/livefolio.md`
- [ ] Keep paper sleeve in `reports/paper-trade-ledger.md`
- [ ] Add lint/checklist before report publish

### P4 — Crypto/BTC Research Lane (Phase 0)
- [ ] Create `reports/crypto/` and `state/crypto-risk.md`
- [ ] Define separate risk limits + budget namespace
- [ ] Build daily monitor template (price, regime, sentiment, flows)
- [ ] Build weekly deep-research template (thesis + risks + invalidation)

## Next Actions (Immediate)
- [ ] Apply SOP in next premarket run
- [ ] Start crypto lane as research-only unless explicitly authorized for execution
- [ ] Produce first weekly KPI card on Friday close

## Waiting For
- [ ] None

## Done
- [x] Company-research skill created and wired into cron prompts
- [x] Premarket cron moved to 6:15 AM PT
- [x] Stream separation corrected (Livefolio vs paper ledger)
