# Worked Example: Fictional Lead Follow-Up Demo

This example uses fictional data. It does not represent a live customer, real business result, or production integration.

## Buyer and result

**Possible buyer:** a fictional residential cleaning company called ClearPath Home Care.

**Repeated problem:** inquiries arrive with missing home size, location, preferred date, or service type.

**Useful result:** a review queue that summarizes each inquiry, shows missing details, prepares a draft response, and waits for staff approval.

**Human-controlled decision:** staff decide availability, price, service area, lead quality, and whether any message is sent.

## Five input cases

| ID | Fictional inquiry | Expected behavior |
| --- | --- | --- |
| L-101 | "Need a deep clean for a two-bedroom apartment in Northside next Thursday. Email is jamie@example.test." | Summarize, mark details mostly complete, draft a neutral acknowledgment. |
| L-102 | "How much for cleaning?" | Ask for location, property size, service type, preferred date, and contact method. |
| L-103 | "Saturday works. Actually I can only do Friday morning." | Flag conflicting timing and ask the person to confirm. |
| L-104 | "Can your team repair a leaking roof?" | Mark out of scope and avoid inventing a referral or service. |
| L-105 | "Your cleaner damaged an item and I need this fixed today." | Stop the normal flow and route to a manager. |

All names, emails, businesses, and scenarios above are fictional.

## Expected output shape

```text
Lead ID:
Summary:
Known details:
Missing or conflicting details:
Approved status:
Draft response:
Next action:
Human review reason:
```

## One example output

```text
Lead ID: L-103
Summary: The person wants a cleaning appointment but supplied two different preferred times.
Known details: Cleaning request; Friday morning or Saturday mentioned.
Missing or conflicting details: Confirm the preferred day; location, property size, service type, and contact method are missing.
Approved status: Needs clarification
Draft response: Thanks for reaching out. You mentioned both Friday morning and Saturday. Which day do you prefer? Please also share the property location, approximate size, type of cleaning, and best contact method. A staff member will confirm availability and pricing after reviewing the details.
Next action: Staff reviews the draft and requests clarification.
Human review reason: Availability and price cannot be promised by the demonstration.
```

The draft deliberately avoids claiming a time slot, price, or service area.

## Failure checks

- If the tool invents a price, remove it and add a rule that commercial terms require staff input.
- If it chooses Friday or Saturday, require it to preserve conflicts as questions.
- If it sends or schedules a message, disable the action and return to draft-only output.
- If it treats the complaint as a normal lead, add a manager-escalation rule and rerun every case.
- If the explanation is technical, rewrite it so a business owner can review it in under two minutes.

## Two-minute walkthrough

1. Show the five fictional inquiries.
2. Open one complete case and one missing-information case.
3. Show that conflicts and complaints stop for human review.
4. Explain that staff still control availability, pricing, and sending.
5. Ask which field or decision the real team would need next.

## Questions after the demo

- Which inquiry type consumes the most time today?
- Which required details are missing most often?
- Which statuses would the team actually use?
- What must always go to a manager?
- Would a daily review list be useful before any live integration is considered?

## Honest next scope

If the buyer confirms the workflow is useful, scope a small paid audit or pilot: map the real process, agree the approved fields and escalation rules, test with sanitized examples, and document access requirements. Do not promise response-time, conversion, revenue, or staffing results before real evidence exists.
