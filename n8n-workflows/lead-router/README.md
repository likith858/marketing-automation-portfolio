# Lead Router (IF node)

Checks every new lead **before** it reaches the sales team, and blocks leads that can't be contacted.

## What it does
1. **Test leads (Code):** creates 5 sample leads for a UPSC coaching institute (one has no phone number)
2. **Has phone? (IF):** checks if the phone field is not empty
   - **true:** 4 valid leads continue
   - **false:** 1 lead goes to the reject path
3. **Mark rejected (Edit Fields):** adds `status = "Rejected: no phone"` while keeping the lead's name and course

## Why it matters
Leads with no phone number waste the team's time. Marking them (instead of deleting) means the business can still follow up by email and recover the lead.

## Nodes used
Manual Trigger · Code · IF · Edit Fields

## Next version
Switch node to route valid leads by course (Foundation / Mains / Test Series / other) + Merge node to save them in one place.

*Test data only. All names and phone numbers are fake.*
