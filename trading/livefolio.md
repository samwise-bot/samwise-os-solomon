# LIVEFOLIO.md

ALGO_VERSION: v2026.02.27-livefolio-separation-fix

Purpose: **Livefolio stream only** (external strategy monitoring), separate from paper-trading sleeve.

## Stream Boundary
- This file tracks Livefolio monitoring state/notes only.
- Paper-trading positions and allocations are tracked in:
  - `reports/paper-trade-ledger.md`

## Current Status
- Livefolio monitoring remains enabled via cron jobs.
- No paper-trade positions should be recorded in this file.
