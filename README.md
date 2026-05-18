# NS Tester Pay Calculator

A single-file HTML pay calculator for Metro Trains NS Testing staff. Enter your fortnightly schedule manually and get an estimated pay breakdown instantly — no server, no install, runs entirely in the browser.

## Features

- **Manual schedule entry** — click any day badge to set shift type, click hours to edit
- **All shift types** — Weekday (130%), Sunday (200%), Project EX (200%), Overtime (200%), PH Worked (250%), Sick/Bonus/WLBP, Non-Roster PH Leave, Annual Leave, Day Off
- **Annual Leave** — split into base + penalty components matching payslip layout, including Annual Leave Loading (20%)
- **All pay grades** — VB8 through VZL, with correct base rates and allowances across all pay periods from Jul-23 to Jan-27; VB8–VZJ use Testing Allowance (A078), VZK–VZL use Senior Testing Allowance (A077)
- **Automatic overtime split** — Weekday and Sunday shifts over 9.5h automatically split at the normal rate for the first 9.5h and overtime rate (200%) for any excess, excluded from super
- **E Grade Electrical Allowance (A440)** — applied to all physically worked and annual leave hours
- **Pay period aware** — rates update automatically based on today's date, including the 1% rise from Jan-26
- **Reset button** — restore the schedule to the default template in one click
- **Pre-tax deductions** — enter salary sacrifice, car lease, purchased leave etc. to adjust taxable income
- **Tax estimate** — PAYG calculated using ATO 2025–26 resident individual rates (Stage 3) + 2% Medicare levy
- **Super estimate** — 12% SG on eligible earnings (excludes OT and PH Worked per SGC rules)
- **Annual estimate** — projects your fortnightly result × 26 to give a yearly gross, tax, net and super figure

## Usage

1. Open `index.html` in any modern browser (or visit the GitHub Pages URL)
2. Select your pay grade
3. Click badges to set each day's shift type; click hours to adjust if needed
4. Optionally enter pre-tax deductions

## Notes

- All figures are estimates only — for reference purposes, not payroll advice
- Tax is annualised from fortnightly taxable income using ATO 2025–26 rates
- Overtime and PH Worked shifts are excluded from the super base per SGC rules; Annual Leave Loading is included
- Annual estimate assumes 26 identical fortnights — useful as a ballpark only

