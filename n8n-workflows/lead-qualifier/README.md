# Lead Qualifier

**What it does:** a coaching-institute enquiry form sorts each lead into Hot (budget 20,000 or more) or Cold, saves it to Google Sheets with a timestamp, and emails the lead a personalised welcome message (different text for Hot and Cold).

**Flow:** Form Trigger (or Manual Trigger + test data) > IF budget >= 20000 > Hot Lead / Cold Lead > Google Sheets: append row > Gmail: welcome email

**Business value:** counsellors see Hot leads first and call within an hour; every lead gets an instant reply instead of waiting.

**To run:** import `workflow.json` into n8n, connect your Google Sheets and Gmail credentials, create a sheet with columns `name, phone, course, budget, status, next_step, created_at, Email`, and replace `YOUR_GOOGLE_SHEET_ID`.
