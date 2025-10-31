# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T05:01:40Z
- **Source Commit**: [`f1b0f50d0f8d6aef1acae2b895eba432b350c8ef`](https://github.com/keunwoochoi/seoulunderground.live/commit/f1b0f50d0f8d6aef1acae2b895eba432b350c8ef)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18963207100)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Fix 'All' button to show only future events, not past events

Issue: 'All' button was showing all events including past ones.

Fix:
- Always filter from today onwards in both API and static modes
- API mode: Always send fromDt=today, only add toDt for specific weeks
- Static mode: Always filter d >= today first, then apply toDate for weeks
- Result: 'All' button shows future events only, as intended

This ensures 'All' (전체) truly means 'all future events'.

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
