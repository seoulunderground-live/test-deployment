# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T04:57:59Z
- **Source Commit**: [`6eaf526814b1e78cbc3e9d882744548cc196a46f`](https://github.com/keunwoochoi/seoulunderground.live/commit/6eaf526814b1e78cbc3e9d882744548cc196a46f)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18963156152)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Refactor week navigation: URL-based relative weeks + 'All' = all future events

Changes:
- [All] button now means 'all future events' (default, no URL param)
- [This week] uses ?week=0 (relative to current week)
- [Next week] uses ?week=1 (relative to current week)
- Removed showAllEvents state, replaced with weekFilter (null | 0 | 1 | ...)
- URL params: No 'week' param = all future, 'week=N' = specific week
- Simplified updateUrlParams to only handle week and query
- Disabled keyboard shortcuts (h/l/t) - use buttons instead

Benefits:
- URLs are always valid relative to opening time
- 'All' button is now default (shows all future events)
- Cleaner state management (single weekFilter instead of multiple booleans)

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
