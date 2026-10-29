# Lead Funnel (Form → Clean → Check → Save → Thank-you → Email)

A complete lead-capture funnel for a coaching institute's **"Free 1:1 Answer Review"** offer, connected to a live landing page. Each lead is cleaned and checked **before** it is saved, so the team only gets leads they can actually contact.

## Flow
```
Landing page button
  → On form submission (n8n Form: Name, Phone, Email, Course)
  → clean data (Code): "+91 98765-43210" → "9876543210", email → lowercase, no spaces
  → check phone (IF): 10 digits?
      ├─ false → phone error page
      └─ true  → check email (IF): contains "@" AND "."?
                   ├─ false → email error page
                   └─ true  → Save Lead (Google Sheets)
                                → thank you page
                                → welcome email (Gmail)
```

## Why it's built this way
- **Clean first, check second.** People type phones as `+91 98765 43210` or `98765-43210`. Without cleaning, real leads get rejected.
- **One IF = one question.** Phone and email are checked separately, so the person sees exactly what to fix.
- **Save → page → email order.** The lead is saved first, the person sees "Thank you" instantly, and the email is sent last. If Gmail ever fails, the lead is still saved and the visitor never sees an error.
- **Status, next step and time saved with every lead** (`status = new`, `next_step = WhatsApp within 1hr`, `created_at` in India time), so the team knows what to do and how fast.

## Nodes used
n8n Form Trigger · Code (JavaScript) · IF (×2) · Form Ending (×3) · Google Sheets (Append Row) · Gmail

## Key code (clean data)
```javascript
let phone = String(d.Phone || '').replace(/\D/g, '');   // keep only digits
if (phone.length === 12 && phone.startsWith('91')) phone = phone.slice(2); // drop +91
```

## Setup
1. Import `workflow.json` into n8n.
2. Connect your Google Sheets and Gmail accounts.
3. In **Save Lead**, replace `YOUR_SHEET_ID`. Columns: `name, phone, course, status, next_step, created_at, Email`.
4. Publish the workflow and link the form's **Production URL** to your landing-page button.

## Lessons from debugging
- A changed sheet header (one cell renamed) breaks the Sheets node: never edit row 1.
- When a workflow uses Form Ending pages, **every** path must end on one, or the visitor sees "Problem submitting response".
- `{{ }}` must always be 2 open + 2 close braces.

*Test data only. Credentials, sheet IDs and email addresses removed.*
