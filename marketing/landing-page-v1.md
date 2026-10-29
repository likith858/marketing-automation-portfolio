# Landing Page v1: Free 1:1 Mains Answer Review (Sample Work)

A one-page lead-capture site built on Google Sites for a UPSC coaching institute. The button opens an n8n form ([lead-funnel workflow](../n8n-workflows/lead-funnel/)), so every visitor who books goes straight into the lead sheet and gets a welcome email.

> Business name is a sample. Anything in [brackets] is a placeholder to confirm with a real client.

## Page plan (top to bottom)

| Block | Copy | Why it's there |
|---|---|---|
| 1. Headline | **Know exactly why your Mains answer lost marks** | Leads with the result the aspirant wants |
| 2. Sub-headline | Get one answer checked by a mentor, free. Know exactly what to fix. | Says the offer in one line: what, who, cost |
| 3. CTA button (above the fold) | **Book my free review** | Ready visitors can act in 3 seconds without scrolling |
| 4. Benefits | ✅ A mentor checks your answer line by line<br>✅ Small batch, so you get personal attention<br>✅ Evening batch for working aspirants | Benefits, not features: what changes for them |
| 5. Proof | [Student result to be added] | Real proof only; never invented |
| 6. FAQs | **Is it really free?** Yes. One answer, checked by a mentor, no payment.<br>**How long does it take?** About 10 minutes on a call, plus written feedback. | Removes the 2 doubts that stop people booking |
| 7. Second CTA (next version) | **Book my free review** | Visitors who read to the end are the most interested |

## Design choices
- **Hero image:** a hand writing an answer on paper, which matches *written* Mains answers (not an OMR/MCQ sheet).
- **Mobile first:** checked in phone preview; headline and button visible without scrolling.
- **Message match:** the ad hook "Stuck below 70 in mocks?" should be echoed on the page (e.g. in the sub-headline), so ad clicks feel they're in the right place.

## Headline options for A/B testing (one variable at a time)
| Version | Headline |
|---|---|
| A | Stuck below 70 in Mains mocks? |
| B | Writing answers daily, but marks not moving? |
| C (live) | Know exactly why your Mains answer lost marks |
| D | One answer. One mentor. Free feedback. |

## End-to-end test (passed)
Landing page → button → form → phone/email checks → Google Sheet row → thank-you page → welcome email ✅
