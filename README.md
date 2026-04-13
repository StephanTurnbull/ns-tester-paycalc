# NS Tester Pay Calculator

A single-file HTML pay calculator for Metro Trains NS Testing staff. Upload your two weekly timesheet PDFs and get an estimated fortnightly pay breakdown instantly — no server, no install, runs entirely in the browser.

## Features

- **PDF parsing** — drop in your Metro Trains weekly timesheet PDFs and shift types are detected automatically
- **All shift types** — Weekday (130%), Sunday (200%), Project EX (200%), Overtime (200%), PH Worked (250%), Sick/Bonus/WLBP, Non-Roster PH Leave, Annual Leave, Day Off
- **Annual Leave** — auto-detected via `ANNUALEV` work order; split into base + penalty components matching payslip layout, including Annual Leave Loading (20%)
- **All pay grades** — VB8 through VZL, with correct base rates and Testing Allowance (A078) across all pay periods from Jul-23 to Jan-27
- **Senior Testing Allowance (A077)** — automatically applied for VZO and VZJ grades
- **E Grade Electrical Allowance (A440)** — applied to all physically worked and annual leave hours
- **Pay period aware** — rates update automatically based on today's date, including the 1% rise from Jan-26
- **Editable schedule** — click any day badge to cycle through shift types if the auto-detection needs correcting
- **Pre-tax deductions** — enter salary sacrifice, car lease, purchased leave etc. to adjust taxable income
- **Tax estimate** — PAYG calculated using ATO 2025–26 resident individual rates (Stage 3) + 2% Medicare levy
- **Super estimate** — 12% SG on eligible earnings (excludes OT and PH Worked per SGC rules)
- **Annual estimate** — projects your fortnightly result × 26 to give a yearly gross, tax, net and super figure

## Usage

1. Open `pay-calculator.html` in any modern browser
2. Select your pay grade
3. Drop in your two weekly timesheet PDFs
4. Review the detected schedule and correct any badges if needed
5. Optionally enter pre-tax deductions

## Notes

- All figures are estimates only — for reference purposes, not payroll advice
- Tax is annualised from fortnightly taxable income using ATO 2025–26 rates
- Overtime and PH Worked shifts are excluded from the super base per SGC rules
- Annual estimate assumes 26 identical fortnights — useful as a ballpark only

## Known Limitations / To Do

**Calculations to verify**
- [ ] Confirm whether Annual Leave Loading should be included or excluded from the super base
- [ ] Confirm whether Testing Allowance (A078) pays out on sick/bonus leave days (currently included)

**Usability**
- [ ] Per-shift hour editing — all shifts are locked to 9.5h; no way to handle partial shifts without editing the source
- [ ] PDF parser is heuristic — counts shift types but doesn't know which day each falls on, so unusual rosters (e.g. annual leave on a Sunday) may need manual badge correction; consider adding a visible warning when shifts are auto-assigned
- [ ] Print / export — no way to save a result for your own records without screenshotting
