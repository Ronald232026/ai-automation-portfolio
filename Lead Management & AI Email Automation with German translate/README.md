# The Organized Habitat — Lead Management & AI Email Automation

## Project Overview

The Organized Habitat is a self-initiated portfolio project demonstrating how AI and workflow automation can be used to manage website leads, CRM records, email communication, and automated follow-up.

The project combines lead capture, CRM integration, AI-generated email responses, human approval, email delivery, marketing automation, and scheduled follow-up into one practical workflow.

The workflow was developed using n8n and connected with several business and marketing tools.

**This is a self-built portfolio project — not client or employer work.**

---

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
MailerLite
        ↓
Automated Follow-up
        ↓
   Google Sheets
```

---

## Follow-up Automation

A separate scheduled workflow is connected to the same lead tracking system.

It checks lead records in Google Sheets, evaluates follow-up conditions, generates personalized follow-up emails using an AI Agent with OpenRouter, sends the email, and updates the tracking information.

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

---

# Technologies Used

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

---

# Key Features

### Lead Capture

Website contact form submissions are received through an n8n webhook and processed automatically.

### CRM Integration

Contact information is sent to HubSpot CRM for lead management.

### Data Tracking

Lead information and workflow status are stored and tracked using Google Sheets.

### AI Email Generation

An AI Agent generates a professional acknowledgment email based on the submitted contact information.

### Human-in-the-Loop Approval

The initial AI-generated email is sent to Telegram for human review and approval before delivery.

### Automated Email Delivery

After approval, the email is sent automatically through Gmail.

### Automated Follow-up

A scheduled n8n workflow checks lead records, evaluates follow-up conditions, generates personalized follow-up messages using an AI Agent with OpenRouter, sends the email, and updates the lead status in Google Sheets.

### Marketing Automation

Newsletter and follow-up processes can be connected with MailerLite for additional marketing automation.

---

# Skills Demonstrated

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

---

# Project Purpose

This project was created as a self-initiated portfolio project to demonstrate practical skills in:

* AI automation
* Workflow automation
* CRM integration
* Email automation
* Lead management
* Follow-up automation
* Digital marketing

It demonstrates how different tools can be connected into a practical lead management and communication workflow.

**This is not client or employer work.**

---

# Project Websites

### The Organized Habitat

🌐 https://theorganizedhabitat.runable.site/

The website used as the example business environment for this automation project.

### Personal Portfolio

🌐 https://floresronaldjonjon.runable.site/

The portfolio website where this project and other AI automation projects are presented.

---

# Deutsche Version

## Projektübersicht

The Organized Habitat ist ein selbst entwickeltes Portfolio-Projekt, das zeigt, wie KI und Workflow-Automatisierung zur Verwaltung von Website-Leads, CRM-Daten, E-Mail-Kommunikation und automatisierten Follow-ups eingesetzt werden können.

Das Projekt kombiniert Lead-Erfassung, CRM-Integration, KI-generierte E-Mail-Antworten, menschliche Freigabe, E-Mail-Versand, Marketing-Automatisierung und zeitgesteuerte Follow-ups in einem praktischen Workflow.

Der Workflow wurde mit n8n entwickelt und mit verschiedenen Business- und Marketing-Tools verbunden.

**Dies ist ein selbst entwickeltes Portfolio-Projekt – kein Kunden- oder Arbeitgeberprojekt.**

---

## Haupt-Workflow

```text
Website-Kontaktformular
        ↓
      n8n
        ↓
    HubSpot CRM
        ↓
   Google Sheets
        ↓
      KI-Agent
        ↓
Menschliche Freigabe über Telegram
        ↓
     Gmail E-Mail
        ↓
MailerLite
        ↓
Automatisiertes Follow-up
        ↓
   Google Sheets
```

---

## Follow-up-Automatisierung

Ein separater zeitgesteuerter Workflow ist mit demselben Lead-Tracking-System verbunden.

Er prüft die Lead-Daten in Google Sheets, bewertet die Follow-up-Bedingungen, erstellt personalisierte Follow-up-E-Mails mit einem KI-Agenten und OpenRouter, versendet die E-Mail und aktualisiert anschließend die Tracking-Daten.

```text
Zeitplan-Trigger
        ↓
   Google Sheets abrufen
        ↓
       IF
        ↓
       IF
        ↓
KI-Agent – OpenRouter
        ↓
   Edit Fields
        ↓
    E-Mail senden
        ↓
Google Sheets aktualisieren
```

### Follow-up-Prozess

1. Ein Zeitplan-Trigger startet den Workflow automatisch.
2. Lead-Daten werden aus Google Sheets abgerufen.
3. IF-Bedingungen prüfen, ob ein Lead für ein Follow-up bereit ist.
4. Eine zweite IF-Bedingung prüft zusätzliche Follow-up-Anforderungen.
5. Ein KI-Agent mit OpenRouter erstellt die Follow-up-Nachricht.
6. Edit Fields bereitet die E-Mail-Daten vor.
7. Die E-Mail wird automatisch versendet.
8. Google Sheets wird mit dem Follow-up-Status und den Tracking-Daten aktualisiert.

---

# Verwendete Technologien

* n8n
* KI / LLM
* OpenRouter
* HubSpot CRM
* Google Sheets
* MailerLite
* Gmail
* Telegram
* Webhooks
* APIs

---

# Hauptfunktionen

### Lead-Erfassung

Anfragen aus dem Website-Kontaktformular werden über einen n8n-Webhook empfangen und automatisch verarbeitet.

### CRM-Integration

Die Kontaktdaten werden zur Lead-Verwaltung an HubSpot CRM übertragen.

### Daten-Tracking

Lead-Daten und Workflow-Status werden mit Google Sheets gespeichert und verfolgt.

### KI-E-Mail-Generierung

Ein KI-Agent erstellt auf Basis der übermittelten Kontaktdaten eine professionelle Antwort-E-Mail.

### Human-in-the-Loop-Freigabe

Die erste KI-generierte E-Mail wird zur Überprüfung und Freigabe an Telegram gesendet.

### Automatischer E-Mail-Versand

Nach der Freigabe wird die E-Mail automatisch über Gmail versendet.

### Automatisiertes Follow-up

Ein zeitgesteuerter n8n-Workflow prüft Lead-Daten, bewertet Follow-up-Bedingungen, erstellt personalisierte Follow-up-Nachrichten mit einem KI-Agenten und OpenRouter, versendet die E-Mail und aktualisiert den Lead-Status in Google Sheets.

### Marketing-Automatisierung

Newsletter- und Follow-up-Prozesse können mit MailerLite für zusätzliche Marketing-Automatisierung verbunden werden.

---

# Gezeigte Fähigkeiten

* Workflow-Automatisierung
* KI-Integration
* KI-Agenten
* OpenRouter-Integration
* CRM-Automatisierung
* E-Mail-Automatisierung
* Follow-up-Automatisierung
* Human-in-the-Loop-Workflows
* Webhook-Integration
* API-Integration
* Marketing-Automatisierung
* Lead-Management
* Daten-Tracking

---

# Projektziel

Dieses Projekt wurde als selbst entwickeltes Portfolio-Projekt erstellt, um praktische Kenntnisse in folgenden Bereichen zu demonstrieren:

* KI-Automatisierung
* Workflow-Automatisierung
* CRM-Integration
* E-Mail-Automatisierung
* Lead-Management
* Follow-up-Automatisierung
* Digitales Marketing

Das Projekt zeigt, wie verschiedene Tools zu einem praktischen Lead-Management- und Kommunikations-Workflow verbunden werden können.

**Dies ist kein Kunden- oder Arbeitgeberprojekt.**

---

# Projekt-Websites

### The Organized Habitat

🌐 https://theorganizedhabitat.runable.site/

Die Website dient als Beispielumgebung für dieses Automatisierungsprojekt.

### Persönliches Portfolio

🌐 https://floresronaldjonjon.runable.site/

Die Portfolio-Website, auf der dieses Projekt und weitere KI-Automatisierungsprojekte präsentiert werden.
