Here's the longer, more detailed version — structured like a proper README:

---

# Invoice Automation — Google Sheets → Zoho Books → Google Drive

## Overview
An end-to-end invoicing automation built on **Make.com**, designed to eliminate manual invoice creation for small business/agency operations. The scenario pulls order data from Google Sheets, generates corresponding invoices in Zoho Books, and archives the output in Google Drive — all without manual intervention.

## How It Works
1. **Trigger:** New or updated row detected in a Google Sheet (sales/order data)
2. **Process:** Data is validated and mapped to Zoho Books' invoice fields (customer, line items, amounts, dates)
3. **Create:** An invoice is generated automatically in Zoho Books
4. **Archive:** The generated invoice is saved/exported into a structured Google Drive folder for record-keeping

```
Google Sheets → Make.com Scenario → Zoho Books (Invoice Created) → Google Drive (Archived)
```

## Tech Stack
- **Automation platform:** Make.com (blueprint-based scenario)
- **Data source:** Google Sheets API
- **Invoicing:** Zoho Books API
- **Storage:** Google Drive API

## Testing
- Built and stress-tested using a **200-row synthetic sales dataset**, designed to mirror real-world invoice volume and edge cases (missing fields, duplicate entries, formatting inconsistencies)

## Known Issues / Status
🚧 **In active development.** Six bugs have been identified in the current blueprint logic, primarily around:
- Field mapping mismatches between Sheets and Zoho Books
- Data formatting inconsistencies (dates, currency)
- Module error handling on edge-case rows

These are being debugged and resolved iteratively.

## Setup (for reference/reuse)
1. Import `blueprint.json` into Make.com
2. Connect your Google Sheets, Zoho Books, and Google Drive accounts
3. Update field mappings to match your own sheet structure
4. Test with a small sample before running on live data

## Future Improvements
- Add error notifications (email/Slack alert on failed runs)
- Support multi-currency invoices
- Add a dashboard to track automation run history
