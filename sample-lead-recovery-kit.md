# Sample Lead Recovery Kit

This is a synthetic sample. It shows the shape of a Veridian delivery without using real customer data.

## Lead Tracker Fields

| Field | Purpose |
| --- | --- |
| Lead received | Date the inquiry arrived |
| Source | Website form, email, referral, ad, social DM |
| Contact | Name or company, sanitized if needed |
| Need | What the lead appears to want |
| Owner | Person responsible for the next reply |
| Status | New, replied, waiting, booked, not fit, closed |
| Next step | The smallest concrete action |
| Follow-up due | Date/time when silence becomes a leak |
| Risk note | Privacy, payment, legal, deadline, or customer-visible concern |
| Last touched | Most recent human action |

## Status Rules

| Status | Rule |
| --- | --- |
| New | No reply has been sent yet |
| Replied | First useful response has been sent |
| Waiting | Lead owes information or a decision |
| Booked | Meeting, call, or work is scheduled |
| Not fit | Lead is outside the offer or risk boundary |
| Closed | Won, lost, referred, or intentionally ended |

## Weekly Leak Report

1. Count new leads received.
2. Count leads still marked `New`.
3. Count leads past `Follow-up due`.
4. Count leads with no clear owner.
5. List the three highest-value stuck leads.
6. Choose one process fix for next week.

## Follow-Up Templates

### New Inquiry

Thanks for reaching out. I have this noted and will review the details. The next useful step is:

`[one concrete next step]`

### Waiting On Customer

Quick follow-up. I am waiting on:

`[missing information]`

Once I have that, I can:

`[next action]`

### Not A Fit

Thanks for the details. This does not look like a safe fit for this offer because:

`[reason]`

The better next step is:

`[referral, manual review, or qualified professional]`

## Automation Decision

Do not automate the whole lead process first. Start by making the leak visible. Automate only the smallest repeatable step after the tracker shows which delay happens often enough to matter.
