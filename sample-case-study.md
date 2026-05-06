# Sample Case Study

This is a synthetic case study for demonstrating the organism's reasoning before it has a real customer. It must be labeled as synthetic anywhere public.

## Workflow

A small agency receives website inquiry emails. Each inquiry needs to be reviewed, categorized, answered, and copied into a lead spreadsheet.

## Current Process

1. Read inbound email.
2. Decide whether it is a serious lead.
3. Extract name, company, budget, timeline, and requested service.
4. Draft a reply.
5. Copy details into a spreadsheet.
6. Flag urgent or high-value leads.

## Diagnostic Score

| Factor | Score | Notes |
| --- | ---: | --- |
| Repetition | 8 | Happens many times per week |
| Time cost | 6 | Short per item, meaningful in aggregate |
| Rule clarity | 7 | Lead categories can be defined |
| Error risk | 5 | Customer-visible replies require review |

Automation readiness: strong candidate for assisted workflow, not full autopilot.

## Recommended Improvement

Start with a human-reviewed AI drafting and extraction process.

Do:

- Generate a structured lead summary.
- Suggest category and priority.
- Draft a reply for review.
- Produce spreadsheet-ready fields.

Do not:

- Send replies automatically.
- Reject leads automatically.
- Make pricing commitments without human approval.

## Prompt Pack

### Lead Extraction Prompt

You are reviewing an inbound website inquiry for a small agency. Extract the following fields as JSON:

- name
- company
- email
- requested_service
- budget
- timeline
- urgency
- lead_quality
- missing_information
- recommended_next_step

If a field is not present, use `unknown`. Do not invent details.

### Reply Draft Prompt

Write a concise reply to this inquiry. Thank the sender, acknowledge their requested service, ask for any missing information, and suggest a short discovery call if the lead appears qualified. Do not quote prices. Keep the tone professional and direct.

## SOP

1. Paste the inquiry into the extraction prompt.
2. Review the JSON fields.
3. Copy approved fields into the lead spreadsheet.
4. Paste the inquiry into the reply draft prompt.
5. Edit the reply manually.
6. Send only after human review.

## Expected Value

The agency preserves human judgment while reducing repetitive reading, copying, and first-draft writing.

## Risk Controls

- Human review before sending.
- No automatic pricing.
- No automatic rejection.
- Missing fields are marked `unknown`.

## Prototype Direction

A lightweight version could be built as:

- A spreadsheet with paste-in inquiry field and generated output columns.
- A local script that converts inquiry text to structured JSON.
- A form that stores inbound leads and drafts responses for review.
