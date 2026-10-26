# Marketing + Automation Portfolio

Performance marketing and n8n automation projects for local businesses (coaching institutes, gyms, home services), built while following a structured 6-month learning plan.

## Automation projects (n8n)

| Project | What it does | Key nodes |
|---|---|---|
| [Lead Qualifier](n8n-workflows/lead-qualifier) | Sorts form leads into Hot/Cold by budget, saves them to Google Sheets and sends a personalised welcome email | Form Trigger, IF, Edit Fields, Google Sheets, Gmail |
| [Daily Lead Summary](n8n-workflows/daily-lead-summary) | Every morning at 9 AM: reads the leads sheet, removes duplicates, counts Hot/Cold and lists who to call first | Schedule Trigger, Google Sheets, Code, Edit Fields |
| [Objection Auto-Reply](n8n-workflows/objection-auto-reply) | Sends the right reply for 4 common objections (price, time, trust, delay) | Form Trigger, Switch, Edit Fields, Merge |
| [Expressions practice](n8n-workflows/expressions-practice) | Cleans names, formats dates and builds personalised messages with n8n expressions | Code, Edit Fields |
| [JSON practice](n8n-workflows/json-practice) | Reads nested objects and arrays from JSON data | Manual Trigger, Edit Fields |

## Marketing samples

[`/marketing`](marketing): customer research (voice of customer), competitor analysis, ad angles, hooks, ad copy, landing-page copy, CTAs, follow-up sequences and creative concepts.

## Notes

- All data in these workflows is test data. Credentials and sheet IDs are removed; add your own to run them.
- Business samples are prepared for practice or pitches. Offers and figures in [brackets] are placeholders, not the businesses' real claims.

**Tools:** n8n · Google Sheets · Gmail · Meta Ad Library · Canva
