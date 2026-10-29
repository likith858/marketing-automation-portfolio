# Lead Funnel (Form + 2 IF checks + Google Sheets)

A lead-capture funnel for a coaching institute's **"Free 1:1 Answer Review"** offer. It checks each lead **before** saving it, so the sales team only gets leads they can actually contact.

## Flow
```
On form submission
  → Check phone (IF): phone has 10 digits?
      ├─ false → Phone error page ("Please check your phone number")
      └─ true  → Check email (IF): email contains "@" AND "."?
                   ├─ false → Email error page ("Please check your email")
                   └─ true  → Save lead (Google Sheets)
```

## Why it's built this way
- **One IF = one question.** Phone and email are checked separately, so the person sees exactly what to fix.
- **Bad data never reaches the sheet.** A wrong number wastes a salesperson's call; a wrong email means no follow-up.
- **Status + next step saved with every lead** (`status = new`, `next_step = WhatsApp within 1 hour`, `created_at`), so the team knows what to do and how fast.

## Nodes used
n8n Form Trigger · IF (×2) · Form (Form Ending pages) · Google Sheets (Append Row)

## Setup
1. Import `workflow.json` into n8n.
2. In **Save lead (Google Sheets)**, connect your Google account and replace `YOUR_SHEET_ID` with your sheet. Columns: `name, phone, course, status, next_step, created_at, Email`.
3. Test with a wrong phone, a wrong email and a correct lead.

## Next version
Gmail welcome email + "Thank you" ending page after the sheet step, and timezone set to Asia/Kolkata.

*Test data only. Credentials and sheet IDs removed.*
