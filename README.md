# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-11-01T03:28:06Z
- **Source Commit**: [`fb452a0d6b436a6ba5eb3ee5d32d663ecb7c722a`](https://github.com/keunwoochoi/seoulunderground.live/commit/fb452a0d6b436a6ba5eb3ee5d32d663ecb7c722a)
- **Branch**: `venue-tab`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18990037871)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: fix: export_static_json datetime type error

- Change _get_today_kst_start() to return datetime object instead of string
- crud.list_events expects datetime and calls .isoformat() on it
- Add tests to prevent regression of type errors in export functions

Fixes deployment error:
  AttributeError: 'str' object has no attribute 'isoformat'

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
