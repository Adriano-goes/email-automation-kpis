##  Summary
![Power BI Dashboard Screenshot](PowerBI_Screenshot.png)

- Google Form writes new leads to Google Sheets.
- Make watches the sheet, sends emails via Gmail, and logs outcomes (Sent / Failed) to an `Automation_Log` sheet.
- Power BI visualizes KPIs: totals, average/day, success & failure rate, unique recipients, daily trend, and a color-coded event log.

##  Tech Stack
Power BI · DAX · Make (Integromat) · Google Sheets · Gmail API

##  Dashboard Highlights
- **Total emails, Avg/day, Unique recipients**
- **Success Rate % vs Failure Rate %**
- **Emails sent by day** (line)
- **EmailLog** table with conditional formatting
- **Last updated** timestamp

##  How It Works

1. Google Form ➝ `Leads_DB` (Google Sheets)
2. Make scenario:
   - **Watch new rows** ➝ **Gmail: Send** ➝ **Add Row (Automation_Log)**
   - Error route logs failures with `error_message`
   - (Optional) Router validates email format before sending
3. Power BI connects to `Automation_Log` (CSV/Sheet) and computes KPIs with DAX

##  Contents

- `PowerBI_Report.pbix` — the report
- `PowerBI_Screenshot.png` — preview
- `Make_Scenario.png` — automation diagram
- `sample_data.csv` — example log data

##  Notes
- Demo data is synthetic; remove/replace any personal identifiers.

**Author:** Adriano Goes • v1.0 • 2025
