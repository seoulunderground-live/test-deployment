# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T04:21:58Z
- **Source Commit**: [`a52d59797f4df3ca970b691a0355aed0b0a02aad`](https://github.com/keunwoochoi/seoulunderground.live/commit/a52d59797f4df3ca970b691a0355aed0b0a02aad)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18962615990)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Fix data symlink: remove checked-out dir first

The issue: ln -sf ./data was creating a symlink INSIDE the existing
data/ directory (which git checked out with README.md and app.db),
not replacing it.

The fix: rm -rf ./data first, then create symlink. Now export script
will see data/seoul/jazz/gemini_analyzed/venues/ correctly.

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
