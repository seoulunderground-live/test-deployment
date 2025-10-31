# Seoul Underground Live - TEST DEPLOYMENT

⚠️ **This is a TEST/STAGING environment** ⚠️

## Build Information

- **Environment**: TEST
- **Build Time**: 2025-10-31T05:14:37Z
- **Source Commit**: [`0bc68e58859a0d0c19d07bf8c4db4a503ac855bf`](https://github.com/keunwoochoi/seoulunderground.live/commit/0bc68e58859a0d0c19d07bf8c4db4a503ac855bf)
- **Branch**: `korean-jazz`
- **Workflow Run**: [View logs](https://github.com/keunwoochoi/seoulunderground.live/actions/runs/18963434265)

## Commit Details

- **Author**: Keunwoo Choi <gnuchoi+github@gmail.com>
- **Message**: Add [Today] and [Tomorrow] buttons to date filters

Changes:
- Added 5 date filter buttons: [All] [Today] [Tomorrow] [This week] [Next week]
- Added dayFilter state (null | 0 | 1) for day-level filtering
- Added 'tomorrow' translation (Tomorrow / 내일)
- URL params: ?day=0 (today), ?day=1 (tomorrow), ?week=0, ?week=1
- Day and week filters are mutually exclusive

Fix:
- Use undefined (not null) for unmodified params in button onClick
- This prevents one handler from clearing another's param

Result:
- [All]: All future events (no URL param)
- [Today]: ?day=0 (shows only today's events)
- [Tomorrow]: ?day=1 (shows only tomorrow's events)
- [This week]: ?week=0 (shows this week)
- [Next week]: ?week=1 (shows next week)

## Deployment URLs

- **Test Site**: https://test.seoulunderground.live
- **Production Site**: https://seoulunderground.live

## Data Snapshot

The static JSON files in `/api/` were exported from the local backend at build time.
Events shown are from the crawler's database as of the build timestamp above.

---

*This README is auto-generated during deployment. Do not edit manually.*
