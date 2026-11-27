# SkillLedger changelog

## v5.1.0 (header, recovery, Access panel, Excel import)
- Header redone: on desktop one clean row (Home, Dashboard, Register, Add training, People, Reports, More). On phones only the logo and a menu button show; language and Sign out moved inside the menu, which scrolls if it is long.
- Wrong passcode: after 5 tries the form locks with a live countdown ("Try again in 27 seconds"), buttons disabled, and the lock survives a page reload.
- Forgot the Owner passcode: a recovery key is made at first setup (shown once) and can be made later in Access. "Forgot the passcode?" on the sign-in page takes the key and sets a new passcode. Without a key, the only way is clearing site data and restoring a backup file (explained on the page).
- Passcode history: dates of when passcodes were made, changed or reset (Owner and accounts). Old passcodes can never be shown because they are stored scrambled; this is explained in Access.
- Access panel split into collapsible sections: System state, People accounts, Access codes, Owner passcode and recovery, Passcode history, Logins, Recent activity.
- People can be added one by one, by CSV, or by Excel (.xlsx, first sheet). Training nominees can be chosen by department, section, team, search, or by typing employee IDs.
- Storage meter in Settings; clear messages when the browser is full.

## v5.0.0 (Phase 5: ID and passcode accounts, portals, trainer feedback, report periods)
- Passcode boxes everywhere (setup, login, change passcode, ID login) have a Show/Hide button. Wrong-passcode messages are clearer, and the Welcome screen now explains what it means if it appears again (the browser did not keep the data).
- Sign in with ID and passcode. Owner makes accounts on the Access page for HR Manager, HR Executive, Head, Line manager, Employee and Trainer; passcodes are random, stored hashed, shown once. One click creates accounts for all employees or all trainers, with a CSV to hand out; New passcode, Revoke and Delete per account. Five wrong tries lock the form for 30 seconds.
- Employee page: own trainings, attendance, results, the questions with their own answers (Review answers) and the trainer's notes about them. Line manager and Head: own team or department, plus own learning when an employee is linked. A route guard stops an employee or trainer from opening other pages by typing the address (fixed: an employee could open Team view of themselves).
- Trainer portal: only trainings where the facilitator name matches; participant feedback, comments and assessment results, never costs. Per-participant note and rating (employee sees it), and a report as text and/or files (Excel, CSV, PDF, Word, text; 500 KB each; CSV and text shown as text). HR reads and downloads them in the Training File.
- Reports period: All time, Financial year, Calendar year, One month, Month to month; the chosen period is shown under the table and applies to every export. New report: L&D scorecard by department (coverage, hours per employee, cost per employee, cost per hour, attendance, pass rate).
- Demo now opens on a real login page listing fictional demo accounts; one tap fills and signs in. Role switcher replaced by Sign out so the demo behaves like the full version.
- Assessment results keep each person's answers (older results show no review). Manual chapter 17 added (EN/BN), chapters 12 updated.
- Honest limits: IDs and passcodes are checked inside the browser (casual security, not server security); an account works only in the browser holding the data; uploaded files are stored, not read (except CSV/text); HR Manager and HR Executive have the same permissions (title only); only the Owner creates accounts. Bangla text is mine and needs your review.

## v4.0.0 (Phase 4: import, merge, follow-up, Lumi)
- Import and tools page: CSV import with template download and a preview before anything changes. Employees, trainings, attendance and assessment results (paper or offline exams). Problem rows are listed and skipped; duplicates are caught.
- Merge from another device (optional sync without a server): export a sync pack (no passcodes), merge on another device; newer training copies win, people and codes are not overwritten, code clashes get a new code. Every change now stamps the training's updated time automatically.
- Follow-up kit per training: messages in English or Bangla (reminder, personal assessment links, absent, thank-you and feedback, below pass mark), who needs a follow-up, print.
- AI helper prompts (improvement ideas, draft questions, short report paragraph): ready-to-paste text with no names. Nothing is sent anywhere. Paste questions adds assessment questions from text.
- Custom Lumi: Owner can rename Lumi, pick a colour and set a welcome line on Home.
- Manual chapter 16 (EN/BN). Demo: sample buttons replace file picking, so visitors can try every importer without entering their own data.
- Honest limits: sync is by file, not live; no direct AI connection (prompts are pasted by you); import is CSV only; trainings import expects English values (In-house/External, Domestic/International).

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
