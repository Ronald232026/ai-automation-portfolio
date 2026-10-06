# AI Portfolio Assistant — n8n, OpenRouter & Simple Memory

## English Version

### Overview

This project is a self-built **AI Portfolio Assistant** integrated into my personal portfolio website.

The assistant allows website visitors to ask questions about my:

* Skills
* Projects
* AI automation experience
* Digital marketing knowledge
* Tools and technologies
* Background
* Availability

Visitors can interact with the assistant through the website chat interface.

The workflow uses **n8n**, an **AI Agent**, **OpenRouter Chat Model**, and **Simple Memory** to maintain conversation context across multiple questions.

This is a self-initiated portfolio and learning project, not a paid client or production system.

---

## Workflow

```text
Webhook
   ↓
AI Agent
   ├── OpenRouter Chat Model
   └── Simple Memory
   ↓
Edit Fields
   ↓
Respond to Webhook
```

---

## How It Works

### 1. Webhook

The workflow starts when the portfolio website sends a visitor's message to the n8n webhook.

The webhook connects the portfolio website with the n8n AI workflow.

The request can contain information such as:

* User message
* Conversation history
* Session ID
* Language
* Voice/text mode

---

### 2. AI Agent

The AI Agent processes the visitor's question and generates the response.

The agent is configured to answer questions about the portfolio owner, projects, skills, tools, and automation experience.

The AI Agent uses the **OpenRouter Chat Model** as its language model.

The assistant is instructed to provide accurate and honest information and avoid inventing experience, clients, results, or qualifications.

---

### 3. OpenRouter Chat Model

OpenRouter provides the language model used by the AI Agent.

It allows the workflow to send the visitor's question to an AI model and receive a generated response.

---

### 4. Simple Memory

The **Simple Memory** node maintains conversation context.

This allows visitors to ask follow-up questions without repeating the previous question.

Example:

```text
Visitor:
What automation projects have you built?

AI:
I have built several self-initiated automation projects using
n8n, Notion, Firecrawl, Hugging Face, Make.com and other tools.

Visitor:
Which one uses Hugging Face?

AI:
The AI Image Generation Automation project uses Hugging Face
to generate images...
```

The memory helps the AI understand that the second question is related to the previous conversation.

---

### 5. Edit Fields

After the AI Agent generates the response, the **Edit Fields** node prepares the output.

The workflow formats the AI response into the structure expected by the portfolio website.

Example:

```json
{
  "reply": "AI-generated response"
}
```

---

### 6. Respond to Webhook

The final node sends the AI response back to the portfolio website.

The website then displays the response inside the AI Assistant chat interface.

---

## Complete Data Flow

```text
Portfolio Website
       ↓
    Webhook
       ↓
   AI Agent
       ↓
OpenRouter Chat Model
       ↓
 Simple Memory
       ↓
   AI Response
       ↓
 Edit Fields
       ↓
Respond to Webhook
       ↓
Portfolio Website
       ↓
Visitor sees the answer
```

---

## Key Features

* AI-powered portfolio assistant
* Website-to-n8n webhook integration
* OpenRouter language model
* Conversation memory
* Follow-up question support
* Structured webhook response
* Portfolio and project information
* English/German conversation support
* Designed for a junior AI automation portfolio
* Can be extended with voice functionality

---

## Technologies

* n8n
* OpenRouter
* AI Agent
* Simple Memory
* Webhooks
* HTTP / API integration
* JSON
* Workflow Automation
* Conversational AI
* Portfolio Website

---

## Skills Demonstrated

This project demonstrates practical experience with:

* n8n workflow automation
* AI Agent configuration
* OpenRouter integration
* Conversational AI
* Conversation memory
* Webhook integration
* API-based communication
* JSON data handling
* Website-to-automation integration
* AI portfolio assistant development
* Multi-language AI interaction

---

## Use Case

The main purpose of this project is to provide visitors with an interactive way to learn about my portfolio.

Visitors can ask questions such as:

```text
What AI automation projects have you built?

What tools do you use?

Do you have experience with n8n?

Tell me about your Hugging Face project.

What digital marketing skills do you have?

Who is Ronald?

How can I contact you?
```

The AI assistant responds based on the information configured for the portfolio.

---

## Project Architecture

```text
                 Personal Portfolio Website
                           │
                           │
                           ▼
                       Webhook
                           │
                           ▼
                      ┌─────────┐
                      │ AI Agent│
                      └────┬────┘
                           │
              ┌────────────┴────────────┐
              │                         │
              ▼                         ▼
     OpenRouter Chat Model       Simple Memory
              │                         │
              └────────────┬────────────┘
                           │
                           ▼
                      Edit Fields
                           │
                           ▼
                 Respond to Webhook
                           │
                           ▼
                 Portfolio Website
```

---

## Project Website

Personal Portfolio:

https://floresronaldjonjon.runable.site/

The AI Portfolio Assistant is available as part of my personal portfolio website.

---

## Project Purpose

This project was created as a **self-initiated portfolio project** to demonstrate practical skills in:

* AI automation
* n8n
* Conversational AI
* API integration
* Webhook-based communication
* Memory-enabled AI workflows
* Digital marketing automation

It is intended as a demonstration and learning project rather than a commercial production system.

---

## Future Improvements

Possible future improvements include:

* Voice input
* Browser-based voice output
* More advanced conversation memory
* Knowledge-base integration
* Retrieval-Augmented Generation (RAG)
* Analytics for visitor questions
* Improved multilingual support
* More detailed project knowledge
* Lead qualification
* Contact form integration
* Calendar / appointment integration
* Additional AI automation capabilities

---

# KI-Portfolio-Assistent — n8n, OpenRouter & Simple Memory

## Deutsche Version

### Überblick

Dieses Projekt ist ein selbst entwickelter **KI-Portfolio-Assistent**, der in meine persönliche Portfolio-Website integriert ist.

Der Assistent ermöglicht es Website-Besuchern, Fragen zu folgenden Themen zu stellen:

* Fähigkeiten
* Projekte
* KI-Automatisierung
* Kenntnisse im Digital Marketing
* Tools und Technologien
* Beruflicher Hintergrund
* Verfügbarkeit

Besucher können über die Chat-Oberfläche der Website mit dem Assistenten interagieren.

Der Workflow verwendet **n8n**, einen **AI Agent**, das **OpenRouter Chat Model** und **Simple Memory**, um den Gesprächskontext über mehrere Fragen hinweg zu erhalten.

Dieses Projekt ist ein selbstständiges Portfolio- und Lernprojekt und kein bezahltes Kunden- oder Produktionsprojekt.

---

## Workflow

```text
Webhook
   ↓
AI Agent
   ├── OpenRouter Chat Model
   └── Simple Memory
   ↓
Edit Fields
   ↓
Respond to Webhook
```

---

## Funktionsweise

### 1. Webhook

Der Workflow startet, wenn die Portfolio-Website die Nachricht eines Besuchers an den n8n-Webhook sendet.

Der Webhook verbindet die Portfolio-Website mit dem n8n-KI-Workflow.

Die Anfrage kann Informationen enthalten wie:

* Nachricht des Besuchers
* Gesprächskontext
* Session-ID
* Sprache
* Sprach-/Textmodus

---

### 2. AI Agent

Der AI Agent verarbeitet die Frage des Besuchers und erstellt eine Antwort.

Der Agent ist darauf ausgelegt, Fragen über den Portfolio-Inhaber, Projekte, Fähigkeiten, Tools und Automatisierungserfahrungen zu beantworten.

Als Sprachmodell wird das **OpenRouter Chat Model** verwendet.

Der Assistent soll ehrlich und auf Basis der vorhandenen Portfolio-Informationen antworten und keine Erfahrungen, Kunden, Ergebnisse oder Qualifikationen erfinden.

---

### 3. OpenRouter Chat Model

OpenRouter stellt das Sprachmodell für den AI Agent bereit.

Die Frage des Besuchers wird an das KI-Modell gesendet und die generierte Antwort wird an den Workflow zurückgegeben.

---

### 4. Simple Memory

Der **Simple Memory** Node speichert den Gesprächskontext.

Dadurch können Besucher Folgefragen stellen, ohne die vorherige Frage erneut erklären zu müssen.

Beispiel:

```text
Besucher:
Welche Automatisierungsprojekte hast du entwickelt?

KI:
Ich habe mehrere selbstständige Automatisierungsprojekte
mit n8n, Notion, Firecrawl, Hugging Face, Make.com
und weiteren Tools entwickelt.

Besucher:
Welches davon verwendet Hugging Face?

KI:
Das Projekt AI Image Generation Automation verwendet
Hugging Face zur Generierung von Bildern...
```

Die Memory-Funktion hilft dem KI-Assistenten zu erkennen, dass die zweite Frage mit der vorherigen Unterhaltung zusammenhängt.

---

### 5. Edit Fields

Nachdem der AI Agent eine Antwort erstellt hat, bereitet der **Edit Fields** Node die Ausgabe vor.

Die Antwort wird in das Format gebracht, das von der Portfolio-Website erwartet wird.

Beispiel:

```json
{
  "reply": "KI-generierte Antwort"
}
```

---

### 6. Respond to Webhook

Der letzte Node sendet die KI-Antwort zurück an die Portfolio-Website.

Die Website zeigt die Antwort anschließend in der AI-Assistant-Chat-Oberfläche an.

---

## Kompletter Datenfluss

```text
Portfolio-Website
       ↓
    Webhook
       ↓
   AI Agent
       ↓
OpenRouter Chat Model
       ↓
 Simple Memory
       ↓
   KI-Antwort
       ↓
 Edit Fields
       ↓
Respond to Webhook
       ↓
Portfolio-Website
       ↓
Besucher sieht die Antwort
```

---

## Hauptfunktionen

* KI-gestützter Portfolio-Assistent
* Webhook-Integration zwischen Website und n8n
* OpenRouter Sprachmodell
* Conversation Memory
* Unterstützung für Folgefragen
* Strukturierte Webhook-Antwort
* Portfolio- und Projektinformationen
* Unterstützung für Deutsch und Englisch
* Für ein Junior-AI-Automation-Portfolio entwickelt
* Erweiterbar um Sprachfunktionen

---

## Technologien

* n8n
* OpenRouter
* AI Agent
* Simple Memory
* Webhooks
* HTTP / API Integration
* JSON
* Workflow Automation
* Conversational AI
* Portfolio Website

---

## Gezeigte Fähigkeiten

Dieses Projekt zeigt praktische Kenntnisse in:

* n8n Workflow Automation
* Konfiguration von AI Agents
* OpenRouter Integration
* Conversational AI
* Conversation Memory
* Webhook Integration
* API-basierter Kommunikation
* JSON-Datenverarbeitung
* Website- und Workflow-Integration
* Entwicklung eines KI-Portfolio-Assistenten
* Mehrsprachiger KI-Interaktion

---

## Anwendungsfall

Das Hauptziel dieses Projekts ist es, Website-Besuchern eine interaktive Möglichkeit zu geben, mehr über mein Portfolio zu erfahren.

Besucher können beispielsweise fragen:

```text
Welche KI-Automatisierungsprojekte hast du entwickelt?

Welche Tools verwendest du?

Hast du Erfahrung mit n8n?

Erzähl mir etwas über dein Hugging-Face-Projekt.

Welche Digital-Marketing-Kenntnisse hast du?

Wer ist Ronald?

Wie kann ich Ronald kontaktieren?
```

Der KI-Assistent antwortet auf Basis der für das Portfolio hinterlegten Informationen.

---

## Projekt-Architektur

```text
                 Persönliche Portfolio-Website
                              │
                              │
                              ▼
                          Webhook
                              │
                              ▼
                         ┌─────────┐
                         │ AI Agent│
                         └────┬────┘
                              │
                 ┌────────────┴────────────┐
                 │                         │
                 ▼                         ▼
        OpenRouter Chat Model       Simple Memory
                 │                         │
                 └────────────┬────────────┘
                              │
                              ▼
                         Edit Fields
                              │
                              ▼
                    Respond to Webhook
                              │
                              ▼
                    Portfolio-Website
```

---

## Projekt-Website

Persönliche Portfolio-Website:

https://floresronaldjonjon.runable.site/

Der AI Portfolio Assistant ist als Teil meiner persönlichen Portfolio-Website verfügbar.

---

## Projektzweck

Dieses Projekt wurde als **selbstständiges Portfolio- und Lernprojekt** entwickelt, um praktische Kenntnisse in folgenden Bereichen zu demonstrieren:

* KI-Automatisierung
* n8n
* Conversational AI
* API-Integration
* Webhook-basierte Kommunikation
* KI-Workflows mit Conversation Memory
* Digital Marketing Automation

Das Projekt dient als Demonstration und Lernprojekt und ist kein kommerzielles Produktionssystem.

---

## Zukünftige Verbesserungen

Mögliche zukünftige Erweiterungen:

* Spracheingabe
* Browser-basierte Sprachausgabe
* Erweiterte Conversation Memory
* Integration einer Knowledge Base
* Retrieval-Augmented Generation (RAG)
* Analytics für Besucherfragen
* Verbesserte Mehrsprachigkeit
* Detaillierteres Projektwissen
* Lead Qualification
* Kontaktformular-Integration
* Kalender-/Termin-Integration
* Weitere KI-Automatisierungen

---

## Author / Autor

**Ronald Flores**

Junior AI Automation & Digital Marketing Professional

Portfolio:

https://floresronaldjonjon.runable.site/
