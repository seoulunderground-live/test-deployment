# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T05:07:10Z
- **Source Commit**: [`5b2a8f0017b2d1c195e4a9b77c7418ef0ea571aa`](https://github.com/keunwoochoi/seoulunderground.live/commit/5b2a8f0017b2d1c195e4a9b77c7418ef0ea571aa)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18963303969)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Fix 'Next week' button showing same events as 'This week'

Issue: Next week button was showing the same events as this week because
the API was always sending fromDt=today, not fromDt=startOfNextWeek.

Fix:
- API mode: Use fromDate (calculated start of week) for specific weeks
- Static mode: Use fromDate for specific weeks, not always today
- Logic: weekFilter === null → today, weekFilter !== null → fromDate

Result:
- [All]: Shows all future events (from today onwards)
- [This week]: Shows today through end of week (today + 6 days)
- [Next week]: Shows start of next week through end (today + 7 to +13)

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
