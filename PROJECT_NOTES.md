# English Worksheets Project — Carlton's Notes
_Last updated: 2026-07-07_

---

## Infrastructure

| Item | Value |
|------|-------|
| GitHub repo | https://github.com/carlton-title/english-worksheets |
| Live site | https://carlton-title.github.io/english-worksheets/ |
| Supabase project ID | smtgkffnptwjlgccsrti |
| Supabase anon key | eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InNtdGdrZmZucHR3amxnY2NzcnRpIiwicm9sZSI6ImFub24iLCJpYXQiOjE3ODI1NDAxODIsImV4cCI6MjA5ODExNjE4Mn0.F2wlmHBtCPEqfZFiutSwtpH79TPe5GbJh1p3y6rm4qs |
| Teacher password | Carlton2026! |
| Google Apps Script URL | https://script.google.com/macros/s/AKfycbzlLebeREf4qvWfqVi70nmYN2SqAE94d_8P5BlfIHg_7LSZFAjudkXkiAuidUtZX-ay/exec |

---

## Files in GitHub Repo

| File | Description | Status |
|------|-------------|--------|
| worksheet4_m3_a1.html | WS4 for M3 sections 2, 4, 6 | ⚠️ NEEDS RE-UPLOAD (old version on GitHub) |
| teacher.html | Teacher dashboard | ✅ Current |
| W4M3A1Q1.png – W4M3A1Q10.png | Question images for WS4 M3 | ✅ Uploaded |

---

## CRITICAL: Pending Upload

**worksheet4_m3_a1.html** in the outputs folder is the CORRECT version. The file currently on GitHub is old and missing:
- Kyle removed from M3/2, M3/4, M3/6 student arrays
- Correct image filenames (W4M3A1Q*.png, not WS4M3A1Q*.png)
- Test mode (`?testmode=true`) functionality
- Emoji fix on Kyle's dropdown option

Carlton must upload the correct file from the outputs folder to GitHub to replace the old one.

---

## Worksheet 4 M3 (A1) — worksheet4_m3_a1.html

### Features
- **Score recording**: `submitToSheet()` sends to Google Apps Script → Google Sheet
- **Anti-cheating**: `applySeededOrder(studentId)` shuffles questions AND answer choices per student using their ID as RNG seed
- **Kyle (Test Student, ID 54565)**:
  - Hidden from all student dropdowns by default
  - Visible only via `?testmode=true` URL parameter
  - Gets fixed (original) question/answer order for consistent testing
  - Unlimited attempts (no 3-attempt lock)
- **Test mode URL**: https://carlton-title.github.io/english-worksheets/worksheet4_m3_a1.html?testmode=true
- **Image naming**: W4M3A1Q1.png through W4M3A1Q10.png

### Student Sections
- M3/2: ~36 students (Kyle REMOVED)
- M3/4: ~38 students (Kyle REMOVED)
- M3/6: ~39 students (Kyle REMOVED)

---

## Teacher Dashboard — teacher.html

### Features
- Login with password (Carlton2026!)
- Search student by name/ID + select worksheet
- Shows all attempts with score and pass/fail status
- **"🖨️ Download PDF Copy"** button per attempt → prints full report with:
  - Student info (name, ID, section, date)
  - Score and pass/fail
  - Full Q&A table (student answer vs correct answer, colour-coded)
- **🧪 Test Mode card**: Links to open each worksheet with `?testmode=true`

---

## Supabase Tables

| Table | Purpose |
|-------|---------|
| students | All student records; Kyle has is_test=true |
| worksheet_submissions | Detailed per-attempt records (answers JSON, score, timestamp) |

---

## Next: Worksheet 4 M4 — worksheet4_m4_a1.html

### To Do
1. Identify M4 sections (which sections? M4/1–M4/13 or subset?)
2. Pull M4 student list from Supabase (already inserted in Task 9)
3. Create worksheet4_m4_a1.html — same structure as M3 version:
   - Same 10 questions (Comparative Information)
   - Same anti-cheating seeded shuffle
   - Same test mode / Kyle handling
   - Same score submission to Google Sheet
   - Image filenames: W4M4A1Q1.png – W4M4A1Q10.png (to be confirmed)
4. Add M4 test mode link to teacher.html Test Mode card
5. Upload to GitHub

### Key difference from M3
- Different student data (M4 sections)
- Different image filenames (probably W4M4A1Q*.png)
- Same logic/features

---

## Task History

| # | Task | Status |
|---|------|--------|
| 1 | Create worksheet4_m3_a1.html | ✅ Done |
| 2 | Add WS4 column to Google Sheet | ✅ Done |
| 3 | Add Namo (37755, M3/6) to Sheet + Supabase | ✅ Done |
| 4 | Create Supabase submissions table | ✅ Done |
| 5 | Update worksheet to save answers to Supabase | ✅ Done |
| 6 | Build teacher.html | ✅ Done |
| 7 | Push files to GitHub | ✅ Done |
| 8 | Create Supabase students table | ✅ Done |
| 9 | Insert M4/1–M4/13 into Supabase | ✅ Done |
| 10 | Rewrite teacher.html to query Supabase | ✅ Done |
| 11 | Verify login/search on live site | 🔄 In progress |
| 12 | Update transferred students in Supabase | ✅ Done |
| 13 | Add is_test flag for Kyle in Supabase | ✅ Done |
| 14 | Remove Kyle from WS4 dropdown; add testmode | ✅ Done (needs re-upload) |
| 15 | Add Test Mode section to teacher dashboard | ✅ Done |
