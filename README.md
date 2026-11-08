# IT Ticket Management Automation

I built this n8n workflow to organize incoming IT support requests, use AI to classify technical issues and set their priority, and monitor ticket deadlines based on SLA targets.

<img width="463" height="199" alt="image" src="https://github.com/user-attachments/assets/9db82c51-19f9-425b-a552-baf264f0f21b" />

## How it works

1. An employee submits a technical support request through a form with their name, email, and issue description.
2. Google Gemini analyzes the issue and assigns a category, priority, responsible team, and suggested first troubleshooting step.
3. JavaScript generates a ticket ID and calculates the SLA deadline based on priority: Critical (2 hours), High (8 hours), Medium (24 hours), or Low (72 hours).
4. The ticket is saved to Google Sheets, and email notifications are sent to the support team and the employee.
5. A scheduled check reviews open tickets. When a ticket passes its SLA deadline without being marked as breached, the workflow sends a Telegram alert and updates the ticket record.

## Main features

- IT support ticket submission form.
- AI-based issue classification (Hardware, Network, Account, or Software).
- Priority assignment and team routing.
- Suggested first troubleshooting step.
- Automatic ticket ID and SLA deadline calculation.
- Ticket tracking in Google Sheets.
- Email confirmations and Telegram SLA breach alerts.

## Technologies

n8n, Google Gemini, Google Sheets, Gmail, Telegram, JavaScript, AI Agent, and n8n Forms.

## Setup

Import [workflow.json](./workflow.json) into n8n, configure your Gemini, Google Sheets, Gmail, and Telegram credentials, then connect your ticket tracking sheet. Review the priority-to-SLA mapping, notification recipients, and ticket status fields before testing.
