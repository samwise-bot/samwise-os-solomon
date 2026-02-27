# ERRORS.md

## [ERR-20260227-001] reporting-consistency

**Logged**: 2026-02-27T00:50:00-08:00
**Priority**: high
**Status**: in_progress
**Area**: config

### Summary
Executive report flagged contradiction on source-of-truth root.

### Error
Initial report claimed workspace-solomon as canonical root while active cron payloads still targeted legacy `/home/bot/.openclaw/workspace/ops/solomon`.

### Context
- Operation: end-to-end process health reporting
- Trigger: red-team rejection from Samwise
- Environment: OpenClaw cron jobs

### Suggested Fix
Patch all swing jobs to workspace-solomon paths and verify on next run cycle.

### Metadata
- Reproducible: yes
- Related Files: reports/ops-status-2026-02-27.md, reports/ops-status-2026-02-27-v2.md

---
