# AI Content Idea to Notion Automation

## Project Overview

This is a self-built portfolio automation project that demonstrates how content ideas can be transformed into structured content using AI and workflow automation.

The workflow starts with a content idea stored in Google Sheets. n8n retrieves the idea, sends it to an AI Agent using an OpenRouter chat model, generates structured content, processes the result with a JavaScript Code node, and creates a new data page in Notion.

The generated content is stored in a predefined Notion database with dedicated columns for organizing the content.

**This is a self-built portfolio project — not client or employer work.**

---

## Workflow

```text
Schedule Trigger
        ↓
Google Sheets – Get Row
        ↓
AI Agent
        ↓
OpenRouter Chat Model
        ↓
Structured Output
        ↓
Code – JavaScript
        ↓
Notion – Create Data Page
```

---

## How It Works

### 1. Schedule Trigger

The workflow starts automatically using a Schedule Trigger.

The trigger can be configured to run on a regular schedule and check Google Sheets for new content ideas.

### 2. Google Sheets – Get Row

Google Sheets is used as the starting point for content ideas.

A content idea is entered into the spreadsheet, and n8n retrieves the relevant row when the workflow runs.

Example:

```text
Content Idea
↓
"Home organization tips for small apartments"
```

The idea is then passed to the AI workflow.

### 3. AI Agent

The AI Agent receives the content idea and generates the requested content based on the workflow instructions.

The goal is to transform a simple idea into useful, structured content that can later be used for content marketing and Pinterest-related workflows.

### 4. OpenRouter Chat Model

The AI Agent uses an OpenRouter chat model to process the content idea and generate the required content.

This allows the workflow to use an AI language model as part of the automated content creation process.

### 5. Structured Output

The AI Agent uses Structured Output so that the generated information follows a predefined format.

This makes the AI response easier to process automatically in the following workflow steps.

Example content fields can include:

```text
Title
Description
Content
Keywords
Pinterest-related information
```

The exact fields depend on the structure defined in the workflow.

### 6. Code – JavaScript

The generated AI output is processed through a JavaScript Code node.

The Code node prepares and formats the data so that it matches the required Notion database properties.

This creates a consistent structure before the content is sent to Notion.

### 7. Notion – Create Data Page

The final step creates a new data page in the predefined Notion database.

The generated content is mapped into the corresponding Notion columns.

This allows the content ideas and AI-generated content to be stored and organized for later use.

---

## Example Workflow

```text
Content Idea in Google Sheets
            ↓
      Schedule Trigger
            ↓
     Get Google Sheets Row
            ↓
          AI Agent
            ↓
   OpenRouter Chat Model
            ↓
     Structured Output
            ↓
      JavaScript Code
            ↓
     Notion Data Page
```

---

## Content Pipeline

The workflow transforms a simple idea into organized content:

```text
Content Idea
     ↓
Google Sheets
     ↓
AI Processing
     ↓
Structured Content
     ↓
JavaScript Formatting
     ↓
Notion Database
```

This creates a reusable foundation for a future Pinterest content automation workflow.

---

## Technologies Used

* n8n
* Google Sheets
* AI Agent
* OpenRouter
* Structured Output
* JavaScript
* Notion
* APIs
* Workflow Automation

---

## Skills Demonstrated

* Workflow automation
* AI content generation
* AI Agent integration
* OpenRouter integration
* Structured AI output
* Google Sheets automation
* JavaScript data processing
* Notion database automation
* Content organization
* Multi-step n8n workflows
* Content marketing automation

---

## Project Purpose

This project was created as a self-initiated portfolio project to demonstrate how AI can transform simple content ideas into structured and organized content through workflow automation.

The project also serves as a foundation for future Pinterest content automation, where the generated content can be further processed and prepared for Pinterest publishing.

**This is not client or employer work.**

---

## Future Improvements

* Generate Pinterest-ready titles and descriptions
* Add automatic keyword generation
* Add Pinterest image generation
* Connect the workflow to a Pinterest publishing workflow
* Add content approval before publishing
* Add automated scheduling
* Add content performance tracking
* Connect the workflow with additional marketing platforms

---

## Project Websites

### The Organized Habitat

🌐 https://theorganizedhabitat.runable.site/

The website used as an example environment for content automation projects.

### Personal Portfolio

🌐 https://floresronaldjonjon.runable.site/

The portfolio website where this project and other AI automation projects are presented.

---

# Deutsche Version

# KI-Content-Idee zu Notion-Automatisierung

## Projektübersicht

Dies ist ein selbst entwickeltes Portfolio-Automatisierungsprojekt, das zeigt, wie Content-Ideen mithilfe von KI und Workflow-Automatisierung in strukturierte Inhalte umgewandelt werden können.

Der Workflow beginnt mit einer Content-Idee in Google Sheets. n8n ruft die Idee ab, übergibt sie an einen KI-Agenten mit einem OpenRouter-Chat-Modell, erstellt strukturierte Inhalte, verarbeitet das Ergebnis mit einem JavaScript-Code-Node und erstellt anschließend eine neue Daten-Seite in Notion.

Die generierten Inhalte werden in einer vorbereiteten Notion-Datenbank mit definierten Spalten gespeichert und organisiert.

**Dies ist ein selbst entwickeltes Portfolio-Projekt – kein Kunden- oder Arbeitgeberprojekt.**

---

## Workflow

```text
Zeitplan-Trigger
        ↓
Google Sheets – Zeile abrufen
        ↓
KI-Agent
        ↓
OpenRouter-Chat-Modell
        ↓
Strukturierter Output
        ↓
Code – JavaScript
        ↓
Notion – Daten-Seite erstellen
```

---

## Funktionsweise

### 1. Zeitplan-Trigger

Der Workflow startet automatisch über einen Schedule Trigger.

Der Trigger kann so eingestellt werden, dass er regelmäßig ausgeführt wird und Google Sheets auf neue Content-Ideen prüft.

### 2. Google Sheets – Zeile abrufen

Google Sheets dient als Ausgangspunkt für die Content-Ideen.

Eine Content-Idee wird in die Tabelle eingetragen und n8n ruft die entsprechende Zeile beim Start des Workflows ab.

Beispiel:

```text
Content-Idee
↓
„Tipps zur Organisation kleiner Wohnungen“
```

Die Idee wird anschließend an den KI-Workflow übergeben.

### 3. KI-Agent

Der KI-Agent erhält die Content-Idee und erstellt daraus Inhalte entsprechend den definierten Workflow-Anweisungen.

Das Ziel ist, eine einfache Idee in nützliche und strukturierte Inhalte umzuwandeln, die später für Content-Marketing- und Pinterest-Workflows verwendet werden können.

### 4. OpenRouter-Chat-Modell

Der KI-Agent verwendet ein OpenRouter-Chat-Modell zur Verarbeitung der Content-Idee und zur Erstellung der gewünschten Inhalte.

Dadurch wird ein KI-Sprachmodell als Bestandteil des automatisierten Content-Erstellungsprozesses eingesetzt.

### 5. Strukturierter Output

Der KI-Agent verwendet Structured Output, damit die generierten Informationen einem vorher definierten Format folgen.

Dadurch können die KI-Ergebnisse in den folgenden Workflow-Schritten leichter verarbeitet werden.

Beispiel:

```text
Titel
Beschreibung
Content
Keywords
Pinterest-bezogene Informationen
```

Die genauen Felder hängen von der im Workflow definierten Struktur ab.

### 6. Code – JavaScript

Das generierte KI-Ergebnis wird durch einen JavaScript-Code-Node verarbeitet.

Der Code-Node bereitet die Daten so auf und formatiert sie, dass sie zu den Eigenschaften der Notion-Datenbank passen.

Dadurch entsteht eine einheitliche Struktur vor der Übertragung an Notion.

### 7. Notion – Daten-Seite erstellen

Im letzten Schritt wird eine neue Daten-Seite in der vorbereiteten Notion-Datenbank erstellt.

Die generierten Inhalte werden den entsprechenden Notion-Spalten zugeordnet.

So können Content-Ideen und KI-generierte Inhalte für die spätere Verwendung gespeichert und organisiert werden.

---

## Beispiel-Workflow

```text
Content-Idee in Google Sheets
            ↓
      Zeitplan-Trigger
            ↓
   Google-Sheets-Zeile abrufen
            ↓
          KI-Agent
            ↓
   OpenRouter-Chat-Modell
            ↓
     Strukturierter Output
            ↓
       JavaScript Code
            ↓
     Notion-Daten-Seite
```

---

## Content-Pipeline

Der Workflow wandelt eine einfache Idee in organisierten Content um:

```text
Content-Idee
     ↓
Google Sheets
     ↓
KI-Verarbeitung
     ↓
Strukturierter Content
     ↓
JavaScript-Formatierung
     ↓
Notion-Datenbank
```

Damit entsteht eine wiederverwendbare Grundlage für einen zukünftigen Pinterest-Content-Automatisierungsworkflow.

---

## Verwendete Technologien

* n8n
* Google Sheets
* KI-Agent
* OpenRouter
* Structured Output
* JavaScript
* Notion
* APIs
* Workflow-Automatisierung

---

## Gezeigte Fähigkeiten

* Workflow-Automatisierung
* KI-Content-Generierung
* KI-Agent-Integration
* OpenRouter-Integration
* Strukturierter KI-Output
* Google-Sheets-Automatisierung
* JavaScript-Datenverarbeitung
* Notion-Datenbank-Automatisierung
* Content-Organisation
* Mehrstufige n8n-Workflows
* Content-Marketing-Automatisierung

---

## Projektziel

Dieses Projekt wurde als selbst entwickeltes Portfolio-Projekt erstellt, um zu zeigen, wie KI einfache Content-Ideen über einen automatisierten Workflow in strukturierte und organisierte Inhalte umwandeln kann.

Das Projekt dient außerdem als Grundlage für eine zukünftige Pinterest-Content-Automatisierung, bei der die erstellten Inhalte weiterverarbeitet und für die Veröffentlichung auf Pinterest vorbereitet werden können.

**Dies ist kein Kunden- oder Arbeitgeberprojekt.**

---

## Zukünftige Verbesserungen

* Pinterest-fertige Titel und Beschreibungen generieren
* Automatische Keyword-Generierung hinzufügen
* Pinterest-Bilder automatisch generieren
* Den Workflow mit einem Pinterest-Publishing-Workflow verbinden
* Content-Freigabe vor der Veröffentlichung hinzufügen
* Automatische Planung und Veröffentlichung hinzufügen
* Content-Performance-Tracking hinzufügen
* Weitere Marketing-Plattformen integrieren

---

## Projekt-Websites

### The Organized Habitat

🌐 https://theorganizedhabitat.runable.site/

Die Website dient als Beispielumgebung für Content-Automatisierungsprojekte.

### Persönliches Portfolio

🌐 https://floresronaldjonjon.runable.site/

Die Portfolio-Website, auf der dieses Projekt und weitere KI-Automatisierungsprojekte präsentiert werden.
