# Website Contact & AI Email Approval Automation — n8n, HubSpot & OpenRouter

## English Version

### Overview

This project is a self-built **Website Contact and AI Email Automation workflow** created with n8n.

It connects a website contact form with **HubSpot**, a database, an **AI Agent using OpenRouter**, **Telegram human approval**, and email.

When a visitor submits the contact form, the workflow receives the data through a webhook, stores the contact in HubSpot, creates a database record, generates an AI-assisted email response, sends the proposed response to Telegram for human approval, and then sends the email after approval.

The workflow is designed with a **human-in-the-loop approval step** so that AI-generated responses are reviewed before being sent.

This is a self-initiated portfolio and learning project, not a paid client or production system.

---

## Workflow

```text id="8x2h1p"
Website Contact Form
        ↓
Webhook
        ↓
Edit Fields
        ↓
HubSpot Contact
        ↓
Create Database
        ↓
AI Agent
   └── OpenRouter Chat Model
        ↓
Edit Fields
        ↓
Send Message for Approval
        ↓
Telegram
        ↓
Human Approval
        ↓
Send Email
```

---

## How It Works

### 1. Website Contact Form

A visitor submits the contact form on the website.

The submitted information can include:

* Name
* Email
* Message
* Other contact information configured in the form

The website sends the submitted information to the n8n webhook.

---

### 2. Webhook

The **Webhook** node receives the contact form submission.

It acts as the connection between the website and the n8n automation workflow.

---

### 3. Edit Fields

The first **Edit Fields** node prepares and organizes the incoming contact information.

This allows the workflow to map the submitted information into the required fields for the following nodes.

---

### 4. HubSpot Contact

The workflow creates or processes the contact in **HubSpot CRM**.

This provides a structured place to store contact information and can support future lead-management workflows.

---

### 5. Create Database

A database record is created to store information related to the contact submission.

This provides a separate record of the inquiry and its processing status.

---

### 6. AI Agent

The **AI Agent** analyzes the contact message and prepares a suggested email response.

The AI Agent uses the **OpenRouter Chat Model**.

The purpose is to help generate a relevant and professional response based on the visitor's message.

The AI-generated response is treated as a draft and is not automatically sent without review.

---

### 7. Edit Fields

The second **Edit Fields** node prepares the AI-generated response and the recipient information for the approval step and email delivery.

---

### 8. Telegram Human Approval

The proposed AI-generated email is sent to **Telegram** for human review.

The human can review the suggested response before the email is sent.

This creates a **human-in-the-loop** process.

```text id="9v2qkf"
AI generates draft
       ↓
Telegram
       ↓
Human reviews
       ↓
Approve
       ↓
Send Email
```

---

### 9. Send Email

After the response has been reviewed and approved, the workflow sends the email to the contact.

This provides an additional safety and quality-control step before communicating with the visitor.

---

## Complete Data Flow

```text id="h7n3cq"
Website Contact Form
        ↓
      Webhook
        ↓
    Edit Fields
        ↓
   HubSpot Contact
        ↓
   Create Database
        ↓
      AI Agent
        ↓
OpenRouter Chat Model
        ↓
    Edit Fields
        ↓
Telegram Approval
        ↓
  Human Review
        ↓
    Send Email
        ↓
      Contact
```

---

## Key Features

* Website contact form integration
* n8n workflow automation
* Webhook-based data processing
* HubSpot CRM integration
* Database record creation
* AI-generated email drafts
* OpenRouter integration
* Telegram human approval
* Human-in-the-loop workflow
* Automated email delivery after approval
* Structured contact management

---

## Technologies

* n8n
* HubSpot
* OpenRouter
* AI Agent
* Telegram
* Email
* Webhooks
* APIs
* Database
* JSON
* Workflow Automation
* AI-assisted Email Automation
* Human-in-the-Loop Automation

---

## Skills Demonstrated

This project demonstrates practical experience with:

* n8n workflow automation
* Webhook integration
* HubSpot CRM integration
* Contact data management
* AI Agent configuration
* OpenRouter integration
* AI-assisted email generation
* Telegram integration
* Human approval workflows
* Email automation
* Data transformation
* Multi-step workflow design
* Lead management automation
* AI and CRM integration

---

## Use Case

This workflow can be used for contact forms and lead-management processes where an organization wants to:

1. Receive a website inquiry.
2. Store the contact in a CRM.
3. Record the inquiry in a database.
4. Use AI to create a suggested response.
5. Send the response to a human for review.
6. Approve the response.
7. Send the approved email to the contact.

This approach combines **automation with human oversight**.

---

## Human-in-the-Loop Design

A key part of this project is the approval step.

Instead of allowing the AI to automatically send every generated response, the workflow sends the proposed email to Telegram first.

```text id="c6q8um"
Contact Form
     ↓
     AI
     ↓
Draft Email
     ↓
Telegram
     ↓
Human Review
     ↓
Approved?
   ↙     ↘
 Yes      No
  ↓        ↓
Email    Review/
         Change
```

This helps demonstrate how AI can be integrated into business workflows while keeping a human involved in the final communication step.

---

## Project Purpose

This project was created as a **self-initiated portfolio project** to demonstrate practical skills in:

* AI automation
* CRM automation
* n8n
* HubSpot
* OpenRouter
* Telegram workflows
* Email automation
* Human-in-the-loop AI
* Lead management

It is intended as a demonstration and learning project rather than a commercial production system.

---

## Project Website

Personal Portfolio:

https://floresronaldjonjon.runable.site/

The contact automation concept is demonstrated through my personal portfolio and automation projects.

---

## Future Improvements

Possible future improvements include:

* Approval buttons directly inside Telegram
* Separate approve/reject actions
* Email response templates
* Lead scoring
* Automatic lead categorization
* Follow-up reminders
* CRM pipeline management
* Email status tracking
* Duplicate contact detection
* Error notifications
* Automated follow-up sequences
* Analytics and reporting
* Integration with additional CRM platforms

---

# Website-Kontakt & KI-E-Mail-Freigabe-Automatisierung

## Deutsche Version

### Überblick

Dieses Projekt ist ein selbst entwickelter **Website-Kontakt- und KI-E-Mail-Automatisierungsworkflow** mit n8n.

Der Workflow verbindet ein Website-Kontaktformular mit **HubSpot**, einer Datenbank, einem **AI Agent mit OpenRouter**, **Telegram zur menschlichen Freigabe** und E-Mail.

Wenn ein Besucher das Kontaktformular absendet, empfängt der Workflow die Daten über einen Webhook, speichert den Kontakt in HubSpot, erstellt einen Datenbankeintrag, erstellt mit KI einen E-Mail-Entwurf, sendet diesen zur Prüfung an Telegram und versendet die E-Mail nach der Freigabe.

Der Workflow verwendet bewusst einen **Human-in-the-Loop-Freigabeschritt**, damit KI-generierte Antworten vor dem Versand geprüft werden können.

Dieses Projekt ist ein selbstständiges Portfolio- und Lernprojekt und kein bezahltes Kunden- oder Produktionsprojekt.

---

## Workflow

```text id="m2f5rx"
Website-Kontaktformular
        ↓
Webhook
        ↓
Edit Fields
        ↓
HubSpot Kontakt
        ↓
Datenbank erstellen
        ↓
AI Agent
   └── OpenRouter Chat Model
        ↓
Edit Fields
        ↓
Nachricht zur Freigabe senden
        ↓
Telegram
        ↓
Menschliche Freigabe
        ↓
E-Mail senden
```

---

## Funktionsweise

### 1. Website-Kontaktformular

Ein Besucher füllt das Kontaktformular der Website aus.

Die übermittelten Informationen können beispielsweise enthalten:

* Name
* E-Mail-Adresse
* Nachricht
* Weitere im Formular konfigurierte Kontaktinformationen

Die Website sendet die Daten an den n8n-Webhook.

---

### 2. Webhook

Der **Webhook** empfängt die Kontaktformular-Daten.

Er stellt die Verbindung zwischen der Website und dem n8n-Automatisierungsworkflow her.

---

### 3. Edit Fields

Der erste **Edit Fields** Node bereitet die eingehenden Kontaktdaten auf.

Dadurch können die Informationen für die nachfolgenden Workflow-Schritte strukturiert und zugeordnet werden.

---

### 4. HubSpot Kontakt

Der Workflow erstellt oder verarbeitet den Kontakt in **HubSpot CRM**.

Dadurch können Kontaktdaten strukturiert gespeichert und für weitere Lead-Management-Workflows verwendet werden.

---

### 5. Datenbank erstellen

Für die Kontaktanfrage wird ein Datenbankeintrag erstellt.

Dadurch kann die Anfrage zusätzlich dokumentiert und ihr Bearbeitungsstatus verfolgt werden.

---

### 6. AI Agent

Der **AI Agent** analysiert die Nachricht des Besuchers und erstellt einen vorgeschlagenen E-Mail-Entwurf.

Als Sprachmodell wird das **OpenRouter Chat Model** verwendet.

Die KI erstellt dabei einen Antwortvorschlag, der anschließend von einem Menschen geprüft wird.

Die KI-Antwort wird also nicht ohne Prüfung automatisch versendet.

---

### 7. Edit Fields

Der zweite **Edit Fields** Node bereitet die KI-Antwort und die Empfängerinformationen für die Freigabe und den E-Mail-Versand vor.

---

### 8. Telegram – Menschliche Freigabe

Der vorgeschlagene E-Mail-Entwurf wird zur Prüfung an **Telegram** gesendet.

Der Mensch kann die Antwort überprüfen, bevor sie an den Besucher gesendet wird.

Damit entsteht ein **Human-in-the-Loop-Workflow**.

```text id="k8r4nv"
KI erstellt Entwurf
       ↓
Telegram
       ↓
Mensch prüft
       ↓
Freigabe
       ↓
E-Mail senden
```

---

### 9. E-Mail senden

Nach der Prüfung und Freigabe wird die E-Mail an den Kontakt gesendet.

Dadurch bleibt ein zusätzlicher Kontrollschritt zwischen KI-Generierung und Kommunikation mit dem Besucher bestehen.

---

## Kompletter Datenfluss

```text id="7m3c2a"
Website-Kontaktformular
        ↓
      Webhook
        ↓
    Edit Fields
        ↓
   HubSpot Kontakt
        ↓
   Datenbank erstellen
        ↓
      AI Agent
        ↓
OpenRouter Chat Model
        ↓
    Edit Fields
        ↓
Telegram-Freigabe
        ↓
Menschliche Prüfung
        ↓
    E-Mail senden
        ↓
      Kontakt
```

---

## Hauptfunktionen

* Integration eines Website-Kontaktformulars
* n8n Workflow Automation
* Webhook-basierte Datenverarbeitung
* HubSpot CRM Integration
* Erstellung von Datenbankeinträgen
* KI-generierte E-Mail-Entwürfe
* OpenRouter Integration
* Telegram-Freigabe
* Human-in-the-Loop Workflow
* Automatischer E-Mail-Versand nach Freigabe
* Strukturiertes Kontaktmanagement

---

## Technologien

* n8n
* HubSpot
* OpenRouter
* AI Agent
* Telegram
* E-Mail
* Webhooks
* APIs
* Datenbank
* JSON
* Workflow Automation
* KI-gestützte E-Mail-Automatisierung
* Human-in-the-Loop Automation

---

## Gezeigte Fähigkeiten

Dieses Projekt zeigt praktische Kenntnisse in:

* n8n Workflow Automation
* Webhook Integration
* HubSpot CRM Integration
* Kontakt- und Datenverwaltung
* AI Agent Konfiguration
* OpenRouter Integration
* KI-gestützte E-Mail-Erstellung
* Telegram Integration
* Human Approval Workflows
* E-Mail-Automatisierung
* Datenverarbeitung
* Mehrstufigem Workflow Design
* Lead Management Automation
* Integration von KI und CRM

---

## Anwendungsfall

Der Workflow kann für Kontaktformulare und Lead-Management-Prozesse eingesetzt werden, bei denen ein Unternehmen:

1. Eine Website-Anfrage empfängt.
2. Den Kontakt in einem CRM speichert.
3. Die Anfrage in einer Datenbank dokumentiert.
4. Mit KI einen Antwortvorschlag erstellt.
5. Die Antwort zur menschlichen Prüfung sendet.
6. Die Antwort freigibt.
7. Die freigegebene E-Mail an den Kontakt sendet.

Damit werden **Automatisierung und menschliche Kontrolle** miteinander kombiniert.

---

## Human-in-the-Loop Design

Ein wichtiger Bestandteil dieses Projekts ist der Freigabeschritt.

Die KI darf die generierte Antwort nicht direkt versenden. Stattdessen wird der E-Mail-Entwurf zuerst an Telegram gesendet.

```text id="n8b3yk"
Kontaktformular
     ↓
     KI
     ↓
E-Mail-Entwurf
     ↓
Telegram
     ↓
Menschliche Prüfung
     ↓
Freigegeben?
   ↙       ↘
 Ja        Nein
 ↓          ↓
E-Mail    Prüfen/
          Ändern
```

Dies zeigt, wie KI in Geschäftsprozesse integriert werden kann, während die endgültige Kommunikation weiterhin von einem Menschen kontrolliert wird.

---

## Projektzweck

Dieses Projekt wurde als **selbstständiges Portfolio- und Lernprojekt** entwickelt, um praktische Kenntnisse in folgenden Bereichen zu demonstrieren:

* KI-Automatisierung
* CRM-Automatisierung
* n8n
* HubSpot
* OpenRouter
* Telegram-Workflows
* E-Mail-Automatisierung
* Human-in-the-Loop KI
* Lead Management

Das Projekt dient als Demonstrations- und Lernprojekt und ist kein kommerzielles Produktionssystem.

---

## Projekt-Website

Persönliche Portfolio-Website:

https://floresronaldjonjon.runable.site/

Das Kontakt-Automatisierungskonzept wird über meine persönliche Portfolio-Website und meine Automatisierungsprojekte demonstriert.

---

## Zukünftige Verbesserungen

Mögliche zukünftige Erweiterungen:

* Approve-/Reject-Buttons direkt in Telegram
* Separate Freigabe- und Ablehnungsaktionen
* E-Mail-Antwortvorlagen
* Lead Scoring
* Automatische Lead-Kategorisierung
* Follow-up-Erinnerungen
* CRM-Pipeline-Management
* E-Mail-Status-Tracking
* Erkennung doppelter Kontakte
* Fehlerbenachrichtigungen
* Automatische Follow-up-Sequenzen
* Analytics und Reporting
* Integration weiterer CRM-Plattformen

---

## Author / Autor

**Ronald Flores**

Junior AI Automation & Digital Marketing Professional

Portfolio:

https://floresronaldjonjon.runable.site/
