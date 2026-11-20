# RoofFlow: AI Voice and Lead Automation for Roofing

An AI-powered inbound voice and lead management automation designed to transform roofing customer inquiries into structured information, prioritized CRM records, and appointment bookings.

Built using **Retell AI, n8n, Groq, GoHighLevel, and Google Calendar**.

## The Problem

Roofing businesses receive customer inquiries ranging from emergency roof leaks to routine inspections and estimates.

Handling these calls manually can introduce delays in capturing customer information, identifying urgent requests, organizing leads, and scheduling appointments.

## The Solution

RoofFlow combines conversational Voice AI with workflow automation to streamline customer inquiries.

The system is designed to:

1. Answer inbound customer calls using Retell AI.
2. Assist customers through natural, context-aware conversations.
3. Collect relevant customer and roofing inquiry information.
4. Trigger n8n workflows through webhooks during the call and run post-call automation.
5. Extract structured information using Groq.
6. Qualify leads based on the urgency of their inquiries.
7. Record and organize leads in GoHighLevel CRM.
8. Check appointment availability and support AI-assisted booking.

## How It Works

**Inbound Call → AI Assistance → Data Extraction → Lead Qualification → CRM → Appointment Booking**

### 1. Inbound Voice AI

The customer initiates the call.

Retell AI answers and conducts a conversational interaction that adapts to the customer's inquiry.

The AI functions as a customer service assistant while gathering relevant information.

### 2. Data Collection and Extraction

The system captures:

- Customer name
- Contact number
- Customer inquiry or roofing concern
- Emergency or urgency indicator

An n8n webhook is triggered during the call.

Groq processes information using a predefined extraction prompt, converting conversational information into structured lead data.

Post-call automation is executed after the conversation ends.

### 3. Lead Qualification

Lead qualification depends on the urgency of the customer's inquiry.

GoHighLevel evaluates the lead's urgency and organizes the record within the CRM pipeline.

### 4. CRM Management

GoHighLevel serves as the CRM for organizing customer inquiries and tracking leads through the pipeline.

Urgency information helps distinguish emergency inquiries from non-emergency requests.

### 5. AI Appointment Booking

The AI checks appointment availability before confirming a booking.

Appointments can be arranged based on information provided during the customer call or through client email communication.

Google Calendar is part of the scheduling integration.

## Technology Stack

| Technology | Role |
|---|---|
| Retell AI | Inbound conversational Voice AI |
| n8n | Workflow orchestration and webhook automation |
| Groq | Structured information extraction |
| GoHighLevel | CRM, urgency qualification, and lead pipeline |
| Google Calendar | Appointment scheduling and availability |
| Webhooks | Communication between services |

## Architecture and Reliability

The workflow incorporates:

- A predefined Groq extraction prompt
- Structured customer data collection
- Urgency-based lead qualification
- CRM pipeline organization
- Event-driven n8n automation
- AI-assisted availability checking

Exact scoring thresholds, retry strategies, deduplication behavior, and execution-level performance metrics are not documented here.

## Validation Scenarios

The following scenarios describe intended behavior and should be validated against workflow execution records.

| Scenario | Expected behavior |
|---|---|
| Incoming customer call | Retell AI answers and assists the caller |
| Customer information collection | Name, contact number, inquiry, and urgency information are captured |
| Workflow execution | n8n receives webhook information and processes post-call automation |
| Emergency inquiry | Lead urgency is identified and represented in GoHighLevel |
| Non-emergency inquiry | Lead is organized in the appropriate CRM pipeline |
| Appointment request | AI checks availability before booking |
| CRM processing | Captured customer information is recorded for lead management |

These are functional scenarios, not claims of completed or passed tests.

## Outcome

RoofFlow demonstrates how conversational AI and workflow automation can connect customer service, lead qualification, CRM management, and appointment scheduling.

The system is designed to reduce manual information handling, improve the organization of roofing inquiries, and help businesses prioritize urgent customer needs.

Quantified performance outcomes are not published.

## Privacy and Security

This repository is intended for public technical documentation.

It does not contain:

- Real customer information
- Private phone numbers or email addresses
- Authentication credentials or API keys
- Production webhook URLs
- Live CRM account identifiers
- Private customer call transcripts

Workflow exports and execution records are not included.

## Future Documentation

- Verified scoring criteria
- Sanitized n8n workflow examples
- Integration-level error handling
- Validated test execution results
- Optional Google Sheets functionality

## About the Builder

**Mars Atolba**  
AI Automation Specialist | Philippines

[Portfolio](https://automateiv.vercel.app)  
[GitHub](https://github.com/marsatolba6-gif)
