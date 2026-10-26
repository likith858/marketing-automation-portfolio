# Daily Lead Summary

**What it does:** every morning at 9 AM (Asia/Kolkata), reads the leads sheet, keeps only today's leads, removes duplicate submissions by phone number, and builds a one-line summary: total, Hot, Cold and who to call first.

**Flow:** Schedule Trigger > Google Sheets: get rows > Code (filter, dedupe, count) > Edit Fields: summary

**Example output:** "Leads for 22 Oct 2026: 3 total, 2 Hot, 1 Cold. Call first: Ravi (9876543210), Arjun (9988776655)"

**Business value:** the owner knows each morning how many enquiries came in and which ones to call first.

**Next step:** a Gmail node to email the summary to the owner.
