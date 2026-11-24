# SkillLedger changelog

## v1.1.0
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
