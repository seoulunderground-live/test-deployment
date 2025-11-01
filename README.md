# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-11-01T04:04:11Z
- **Source Commit**: [`44bfd747a0f84408d141d39a9c6fd1ef97130469`](https://github.com/keunwoochoi/seoulunderground.live/commit/44bfd747a0f84408d141d39a9c6fd1ef97130469)
- **Branch**: `venue-tab`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18991050758)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: fix: stop creating placeholder venues in database

Changed event import behavior:
- No longer creates placeholder venues when events reference unknown handles
- Unknown venues are logged to venue_candidates.csv for manual review
- Events will have venue_id=None if venue not in database

This keeps the venue database clean - only venues from venue_handles.txt
that have been properly enriched should be in the database.

Manually deleted 5 existing placeholder venues from local database.

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
