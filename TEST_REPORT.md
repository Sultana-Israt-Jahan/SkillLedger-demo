# SkillLedger v5.0 test report

Tested in headless Chromium (desktop and 390 px phone width). Not tested: real phones, Safari, Firefox, two devices, screen readers, Excel/Word opening exports.

| Area | Result |
|---|---|
| Earlier suites (t1 18 checks, t2, t3, t4, t6–t13) | all pass; t5 (phase-1 demo) retired because the demo now opens on a login page |
| New: demo login for 6 roles + wrong passcode + Show/Hide (t14) | 22 pass |
| New: route guards, trainer isolation, no horizontal scroll on phone, bulk accounts + CSV, passcode not stored in clear, 30 s lockout, persistence (t15) | 34 pass |
| Reports: month, range, year, FY, scorecard | pass |
| Bangla keys missing at runtime across the new pages | none |

Private-version login: could not be reproduced (setup, reload, login, and opening v4 over v1.1 data all worked). Likely causes are a typo in a hidden passcode, the 30-second lock after 5 wrong tries, or a phone/file viewer that does not keep browser data between opens. v5 adds Show/Hide, clearer messages and a Welcome-screen hint.

Known limits: security is browser-side only; files over 500 KB are refused; uploaded Excel/PDF/Word are stored, not read.

## v5.1 additions
- t16 (recovery key shown once, wrong key refused, reset works, new passcode works, countdown ticks and survives reload, Access sections, passcode history, hashes only in storage): 11 pass.
- Excel (.xlsx) import of employees through the Import page: 2 rows read and applied (file made with openpyxl; Excel itself not tested).
- t14 22 pass, t15 34 pass after the header change. t3 has one known false alarm (a person's name passing through the translator).
- Capacity (headless Chromium, synthetic data): 2,000 employees + 1,000 trainings with 20 nominees each = 1.4 MB, pages open in 0.07 to 0.4 s. 5,000 employees + 3,000 trainings = 4.1 MB, People page takes about 3 s and the browser limit of about 5 MB is close. Practical advice: up to about 3,000 employees and 2,000 trainings; beyond that a server database is needed.
