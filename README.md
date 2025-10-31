# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T05:24:29Z
- **Source Commit**: [`32c92e4701fd22204784cb3c41700f91d0203626`](https://github.com/keunwoochoi/seoulunderground.live/commit/32c92e4701fd22204784cb3c41700f91d0203626)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18963599363)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Refactor date filter: use discriminated union for type safety

Major improvements:
1. Replaced dayFilter/weekFilter with single DateFilter discriminated union
2. Centralized date range calculation in calculateDateRange()
3. Centralized URL parsing/generation in helper functions
4. Eliminated repeated logic (dayFilter === null && weekFilter === null)
5. Added explicit comment about 'this week' definition (starts from today)

Benefits:
- Type safe: impossible to have invalid filter states
- Single source of truth for filter logic
- Easier to add new filters (e.g., 'this weekend', 'next month')
- Reduced code duplication (4x repeated condition → 1 function)
- Cleaner state management (1 filter vs 2 nullable ints)

No functional changes - all buttons work the same as before.

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
