# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T04:13:03Z
- **Source Commit**: [`b98be62957f3e3b519887b0a04a331488ff4002d`](https://github.com/keunwoochoi/seoulunderground.live/commit/b98be62957f3e3b519887b0a04a331488ff4002d)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18962479007)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Symlink data directory in workflow for venue export

The workflow runs in its own checkout directory which doesn't have
the gitignored data files. Symlink from actual dev workspace so the
export script can access venue/musician analyzed data.

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
