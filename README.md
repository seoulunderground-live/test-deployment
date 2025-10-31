# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T04:00:08Z
- **Source Commit**: [`26ee040d2a3053dade34e3519bff6f9bc090be87`](https://github.com/keunwoochoi/seoulunderground.live/commit/26ee040d2a3053dade34e3519bff6f9bc090be87)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18962258584)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Add .gitignore and data/** to workflow triggers

Workflow now triggers on:
- .gitignore changes (affects what data gets exported)
- data/** changes (venue/musician analyzed data)

This ensures deployment runs when data structure or gitignore patterns change.

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
