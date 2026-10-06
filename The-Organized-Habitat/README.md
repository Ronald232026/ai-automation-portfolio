# The Organized Habitat — Lead Management & AI Email Automation

## Project Overview

The Organized Habitat is a self-initiated portfolio project demonstrating how AI and workflow automation can be used to manage website leads, CRM records, email communication, and marketing follow-up.

The workflow was developed using n8n and connected with several business and marketing tools.

## Main Workflow

```text
Website Contact Form
        ↓
      n8n
        ↓
    HubSpot CRM
        ↓
   Google Sheets
        ↓
      AI Agent
        ↓
Telegram Human Approval
        ↓
     Gmail Email
        ↓
MailerLite / Follow-up
```

## Follow-up Automation

A separate scheduled workflow checks the lead tracking data and sends follow-up emails when the defined conditions are met.

```text
Schedule Trigger
        ↓
   Get Google Sheets
        ↓
       IF
        ↓
       IF
        ↓
AI Agent – OpenRouter
        ↓
   Edit Fields
        ↓
    Send Email
        ↓
Update Google Sheets
```

### Follow-up Process

1. A Schedule Trigger starts the workflow automatically.
2. Lead records are retrieved from Google Sheets.
3. IF conditions check whether a lead is ready for follow-up.
4. A second IF condition checks additional follow-up requirements.
5. An AI Agent using OpenRouter generates the follow-up message.
6. Edit Fields prepares the email data.
7. The email is sent automatically.
8. Google Sheets is updated with the follow-up status and tracking information.

## Technologies Used

* n8n
* AI / LLM
* OpenRouter
* HubSpot CRM
* Google Sheets
* MailerLite
* Gmail
* Telegram
* Webhooks
* APIs

## Key Features

### Lead Capture

Website contact form submissions are received through an n8n webhook.

### CRM Integration

Contact information is sent to HubSpot CRM for lead management.

### Data Tracking

Contact information and workflow status are tracked using Google Sheets.

### AI Email Generation

An AI workflow generates a professional acknowledgment email based on the submitted contact information.

### Human-in-the-Loop Approval

The generated email is sent to Telegram for review before it is delivered.

### Automated Email Delivery

After approval, the email is sent automatically through Gmail.

### Automated Follow-up

A scheduled n8n workflow checks lead records, evaluates follow-up conditions, generates personalized follow-up messages using an AI Agent with OpenRouter, sends the email, and updates the lead status in Google Sheets.

### Marketing Automation

Newsletter and follow-up processes can be connected with MailerLite.

## Skills Demonstrated

* Workflow automation
* AI integration
* AI Agents
* OpenRouter integration
* CRM automation
* Email automation
* Follow-up automation
* Human-in-the-loop workflows
* Webhook integration
* API integration
* Marketing automation
* Lead management
* Data tracking

## Project Purpose

This project was created as a self-initiated portfolio project to demonstrate practical skills in AI automation, workflow automation, CRM integration, email automation, and digital marketing.

It is not client or employer work.

## Portfolio

🌐 https://floresronaldjonjon.runable.site
