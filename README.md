# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-11-09T19:27:00Z
- **Source Commit**: [`16541ca8882a4ee8b31ee380a5707d3dd2bf92ac`](https://github.com/keunwoochoi/seoulunderground.live/commit/16541ca8882a4ee8b31ee380a5707d3dd2bf92ac)
- **Branch**: `fix-slack-noti`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/19213342034)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Use CSS variable for secondary text color in admin list

Code review feedback: replaced hardcoded #666 color with var(--text-secondary)
for better theme consistency and maintainability. Applied to both datetime and
price elements in the admin event list.

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
