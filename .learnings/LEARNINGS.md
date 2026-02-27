# LEARNINGS.md

## [LRN-20260227-001] best_practice

**Logged**: 2026-02-27T00:49:00-08:00
**Priority**: high
**Status**: pending
**Area**: config

### Summary
Enforce a single persistence root for trading automation to prevent continuity drift.

### Details
Trading cron jobs were configured with legacy output paths in another workspace root, while executive reporting assumed workspace-solomon as source of truth. This creates audit ambiguity and inconsistent state.

### Suggested Action
Add a pre-run path assertion in trading jobs: fail job if any write target is outside `/home/bot/.openclaw/workspace-solomon`.

### Metadata
- Source: error
- Related Files: reports/ops-status-2026-02-27-v2.md, trading/livefolio.md
- Tags: continuity, root-cause, cron
- Pattern-Key: harden.single_source_of_truth
- Recurrence-Count: 1
- First-Seen: 2026-02-27
- Last-Seen: 2026-02-27

---

## [LRN-20260227-002] best_practice

**Logged**: 2026-02-27T00:49:30-08:00
**Priority**: medium
**Status**: pending
**Area**: docs

### Summary
Launch-stage scorecards must include process KPIs when realized PnL metrics are sparse.

### Details
A KPI section with only N/A values is low utility during pre-fill lifecycle. Must include interim process-health metrics (actionability completeness, rule compliance, slippage policy coverage, trigger-hit ratio).

### Suggested Action
Standardize report template with mandatory Lifecycle + Interim Process KPI block.

### Metadata
- Source: user_feedback
- Related Files: reports/ops-status-2026-02-27-v2.md
- Tags: reporting, kpi, launch-stage
- Pattern-Key: simplify.lifecycle_kpi_template
- Recurrence-Count: 1
- First-Seen: 2026-02-27
- Last-Seen: 2026-02-27

---
