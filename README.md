# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T04:43:45Z
- **Source Commit**: [`1dfd7ad4d1dcfbe9fcc4690c385733dfc7ecb36f`](https://github.com/keunwoochoi/seoulunderground.live/commit/1dfd7ad4d1dcfbe9fcc4690c385733dfc7ecb36f)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18962949772)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Stop tracking data/app.db and data/README.md

These files should never have been in git:
- data/app.db: SQLite database (changes constantly, large)
- data/README.md: Local documentation only

Changes:
1. Untrack both files: git rm --cached
2. Simplify .gitignore: data/** (all excluded)
3. Fix .gitignore: frontend/public/api/ (was *.json, missed subdirs)
4. Move data docs to main README.md
5. Remove rm -rf from workflows (git won't create data/ anymore)

Workflow symlink now works cleanly without removing anything first.

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
