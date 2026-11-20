# RoofFlow — AI Voice and Lead Automation for Roofing

RoofFlow is an inbound AI voice receptionist and lead qualification automation for roofing businesses.

## The Problem

Roofing inquiries often arrive by phone, where emergency leaks, estimate requests, and lower-intent questions enter the same queue. Manual notes and delayed handoffs can lose context, duplicate records, and slow the response that wins the job.

## The Workflow

**Inbound Call → Understand → Prioritize → Record → Book → Follow Up**

## How It Works

- A customer calls the business. Retell AI answers, responds naturally, assists the caller, and gathers information.
- An n8n webhook receives the call data.
- Groq extracts structured lead information using a fixed extraction schema. Captured: customer name, contact number, roofing inquiry, and an urgency indicator.
- n8n applies deterministic urgency and intent scoring. Urgency is detected by n8n, NOT by GoHighLevel.
- The contact and opportunity are upserted in GoHighLevel, which holds the CRM pipeline and follow-up tasks.
- Appointment booking checks availability in Google Calendar before a booking is confirmed.
- Follow-up tasks are created by route in GoHighLevel: Emergency within 5 minutes, Qualified within 15 minutes, Nurture within 1 day.
- Every routed outcome is logged to Google Sheets, with CRM record IDs, as an audit trail.

## Tools

Retell AI (inbound voice AI) · n8n (webhook, orchestration, urgency scoring) · Groq (structured extraction) · GoHighLevel (CRM, pipeline, follow-up tasks) · Google Calendar (availability and booking) · Google Sheets (audit log) · Webhooks

## Reliability

Fixed extraction schema · Deterministic urgency rules · Contact upsert to reduce duplicates · Explicit routing branches · Every routed outcome logged to Google Sheets

## Testing

The Emergency, Qualified, and Nurture routes were scenario-tested. Run-level execution records and raw data are not published, to protect customer information.

## Result

Turns roofing calls into structured, prioritized CRM actions, so urgent leaks are handled quickly, qualified leads are booked, and every follow-up is traceable.

## Not Published

Real customer data, phone numbers, emails, client or company names, credentials, live webhook URLs, account or workspace IDs, call transcripts, and workflow exports. Sample data is fictional.

## Builder

Mars Atolba — AI Automation Specialist, independent, based in the Philippines.

[Portfolio](https://automateiv.vercel.app) · [GitHub](https://github.com/marsatolba6-gif) · [LinkedIn](https://www.linkedin.com/in/automatewithmars/)
