# SkillLedger changelog

## v3.0.0 (Phase 3: roles, assessments, portal)
- Roles by access code (Access page): HR, Head of department, Line manager, Employee, Viewer, plus the Owner. HR edits trainings, people, attendance and assessments but cannot open Access. Heads and managers see only their department/team in Team view. Employees see only their own learning in My learning. Codes can be revoked or expire.
- Assessments per training: multiple-choice questions with marks, pass mark (default 60%), grace period. Window opens at the training start and closes at end + grace, in the training time zone.
- One-time assessment links per nominee (copy, copy all, CSV export, replace/new link for another attempt). The link page works without signing in, scores on submit, shows pass/fail and cannot be reused.
- HR can enter marks by hand. Full exam history per person (People history, My learning) with attempts. Questions lock once results exist.
- Reports: separate Assessments section (by training, employee, department). Excel register export gains an Assessments sheet.
- Existing data upgrades automatically. English and Bangla; manual chapters 13-15.
- Demo build: a View as switcher shows each role; fictional access codes are listed on the Access page.
- Honest limits: roles and links are enforced inside this browser, so they keep ordinary users in their lane but are not server security; a link only works in the browser that holds the data (a server comes later); no email/SMS.

## v2.0.0 (Phase 2: people, attendance, cost)
- People page: employee directory (ID, name, designation, department, section, team, home time zone, active). Add/edit/delete; an employee nominated anywhere cannot be deleted (mark inactive instead). Per-person history. CSV export. 40 fictional employees in the test data.
- Nominees on the training form (search, department/team filters, overlap warning, "use as registered participants").
- Training File per training: attendance (Present/Absent, bulk buttons, only from the start date), check-in code, KPIs, print/PDF and CSV.
- Check-in page: employee ID + training code, valid from start to end date, works on this device only.
- Cost sharing: total cost split equally among nominees; absent people still carry their share; manual shares with automatic split of the rest (cannot exceed the total; cents are exact).
- Reports: by training, trainer, employee, team, section, department; all time or financial year; totals; CSV, Excel, PDF. Excel register export gains Employees and Nominations sheets.
- Existing v1 data is upgraded automatically (empty directory, no nominees). English and Bangla, manual chapters 10-12 added.
- Demo build: same code, fictional data, demo date 9 Dec 2026 so a training is running for the check-in demo.
- Known limits: data in this browser only; check-in and passcodes are checked in the browser (casual security); no email/SMS; assessment links, employee portal and roles come in Phase 3.

## v1.1.0
- Added a demo build for public pages. It has the same screens and features as the full build; only the data differs (12 fictional records, typing locked, examples to enter, nothing stored). Built from the same source, so the full build is unchanged.
- Watermark "SIJ - SkillLedger" (author initials) shown faintly on every screen, including the login screen, and restored automatically if removed or hidden.
- Watermark and copyright line added to PDF/Word reports, the Excel Summary sheet, the last row of the CSV export and the JSON backup.
- Honest limit: the watermark is part of the page code. It deters casual reuse and shows origin; it cannot stop someone who edits the source.

## v1.0.0 (Phase 1: rubric core)
- 15-field training form with validation (whole-number participants >= 0, cost >= 0, feedback 1-5 with at most 1 decimal, rejected outside the scale, only after the end date).
- Duration: auto = (to - from) x days; manual override shows "Manual" with a reset button. Time zone per training and "Ends next day (+1)" tick instead of a midnight rule.
- Automatic status: Upcoming / Completed / Pending Feedback.
- Register: search, sort, filters, totals, detail view; mobile card layout.
- Dashboard: KPIs, 5 clickable charts (month, mix, facilitator with low line, cost vs score, low/pending), views, customize, financial-year filter, insights.
- Improvement tracker with low scores highlighted.
- Export: Excel, CSV, Word, PDF (print), JSON backup; restore.
- Access: Owner passcode, viewer codes, lock states, login log, activity log.
- Settings, themes (Mist/Sand/Dusk), English/Bangla, in-app manual with PDF, Terms.
- 12 fictional test records. Locked copyright footer.
- Known limits: data in this browser only; passcodes checked in the browser (casual security); no sync; Locked freezes everyone including the Owner.
