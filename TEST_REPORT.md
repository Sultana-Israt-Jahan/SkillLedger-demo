# SkillLedger v1 test report (automated, Chromium)
Totals on seed data: 12 trainings, 100 h, 248 participants, 1,128,000 BDT, average feedback 4.0 (3.95 rounded half-up), 6 done / 2 pending / 4 upcoming at fixed date 2026-11-22.

| Area | Result |
|---|---|
| SHA-256 vector "abc" | pass |
| Duration: 20:00-00:00 +1 = 4 h; without tick = error; 00:00-00:00 = error; 09:30-16:00 x2 days = 13 h; end<start error; tick not needed error | pass |
| Validation: participants decimal/negative/text rejected, 0 ok; cost -1 rejected, 0 ok; score 0, 6, 4.55 rejected, 4.5 ok | pass |
| Add, edit, persist after reload, manual override and reset, delete, lock blocks form | pass |
| Search/type/status filters (after fixing a bug found in testing) | pass |
| Export CSV, XLSX (opens in openpyxl, 3 sheets), Word, JSON; restore backup | pass |
| Viewer read-only, wrong code/passcode refused, login log shows viewer name, Private blocks viewers | pass |
| No horizontal scroll at 390/768/1024/1440 on all 9 pages (one overflow found and fixed) | pass |
| Text contrast >= 4.5 in Mist, Sand, Dusk (main and muted text) | pass |
| Bangla: all UI strings translated | pass (wording needs your review) |
| Copyright footer restored when edited | pass |

Bugs found and fixed during testing: register search box not filtering; Improvements overflow on phone; averages like 3.95 rounding down; form error list lacking field names.
Not tested: real Excel/Word/Safari/Firefox; real print-to-PDF dialog; screen-reader use.
