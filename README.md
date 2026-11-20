# RoofFlow Voice AI

Inbound AI voice receptionist and lead qualification automation for roofing businesses. Demo built with sample data.

A customer calls the business, the voice AI answers and gathers information, and n8n turns the call into a structured, prioritized CRM record with the right follow-up.

Built with Retell AI, n8n, Groq, GoHighLevel, Google Calendar, and Google Sheets.

## The Problem
Roofing inquiries often arrive by phone, where emergency leaks, estimate requests, and lower-intent questions enter the same queue. Manual notes and delayed handoffs can lose context, duplicate records, and slow the response that wins the job.

## How It Works
**Call → Understand → Prioritize → Record → Book → Follow Up**

1. A customer calls the business. Retell AI answers, responds naturally, assists the caller, and gathers information.
2. An n8n webhook receives the call data.
3. Groq extracts structured lead information using a fixed extraction schema. Captured: customer name, contact number, roofing inquiry, and an urgency indicator.
4. n8n applies deterministic urgency and intent scoring.
5. The contact and opportunity are upserted in GoHighLevel, which holds the CRM pipeline and follow-up tasks.
6. Appointment booking checks availability in Google Calendar before a booking is confirmed.
7. Follow-up tasks are created by route in GoHighLevel.
8. Every routed outcome is logged to Google Sheets, with CRM record IDs, as an audit trail.

See the [architecture diagram](docs/architecture.md).

## Follow-up Routing
| Lead type | Follow-up task |
|---|---|
| Emergency | Due within 5 minutes |
| Qualified | Due within 15 minutes |
| Nurture | Due in 1 day |

## Tools
| Tool | Role |
|---|---|
| Retell AI | Inbound voice AI that answers calls and gathers information |
| n8n | Webhook, orchestration, and urgency scoring |
| Groq | Structured information extraction |
| GoHighLevel | CRM, pipeline, and follow-up tasks |
| Google Calendar | Availability and booking |
| Google Sheets | Audit log |
| Webhooks | Communication between services |

## Reliability
- Fixed extraction schema
- Deterministic urgency rules
- Contact upsert to reduce duplicates
- Explicit routing branches
- Every routed outcome logged to Google Sheets

## Testing
The Emergency, Qualified, and Nurture routes were scenario-tested. Run-level execution records and raw data are not published, to protect customer information.

## Result
Turns roofing calls into structured, prioritized CRM actions, so urgent leaks are handled quickly, qualified leads are booked, and every follow-up is traceable. This is a demo built with sample data.

## Privacy and Security
This repository does not contain real customer data, phone numbers, emails, client or company names, credentials, live webhook URLs, account or workspace IDs, call transcripts, or workflow exports. Sample data is fictional.

## About the Builder
**Mars Atolba**, AI Automation Specialist in the Philippines.

[Portfolio](https://automateiv.vercel.app) · [GitHub](https://github.com/marsatolba6-gif) · [LinkedIn](https://www.linkedin.com/in/automatewithmars)
