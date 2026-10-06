# AI Image Generation Automation — Hugging Face, Supabase & Notion

## Overview

This self-built portfolio project demonstrates how n8n can automate AI image generation and content management using Hugging Face, Supabase Storage, and Notion.

The workflow starts with a prompt stored in Google Sheets. n8n retrieves the prompt, sends it to a Hugging Face image generation endpoint, stores the generated image in Supabase Storage, retrieves the stored image, and updates an existing Notion data page with the generated image.

This project is part of a larger content automation workflow and demonstrates how AI-generated visual content can be connected to a structured content database.

---

## Workflow

```text
Schedule Trigger
        ↓
Google Sheets – Get Row
        ↓
Filter
        ↓
Edit Fields
        ↓
HTTP Request – Hugging Face
        ↓
HTTP Request – Supabase Storage
        ↓
Edit Fields
        ↓
HTTP Request – Get Image
        ↓
Notion – Update Data Page
```

---

## How It Works

### 1. Schedule Trigger

The workflow starts automatically using an n8n Schedule Trigger.

It checks the workflow on a scheduled basis so new image generation tasks can be processed automatically.

### 2. Google Sheets – Get Row

Google Sheets contains the image-generation prompt.

n8n retrieves the relevant row and gets the prompt that will be sent to the Hugging Face image generation endpoint.

### 3. Filter

The Filter node checks whether the row is ready to be processed.

This helps prevent incomplete or unapproved rows from continuing through the workflow.

### 4. Edit Fields

The Edit Fields node prepares and structures the data required for the next HTTP Request.

The image prompt and other required values are formatted for the Hugging Face request.

### 5. HTTP Request – Hugging Face

The workflow sends the prepared prompt to a Hugging Face image generation endpoint.

Hugging Face processes the prompt and returns the generated image as binary data.

```text
Prompt
   ↓
Hugging Face
   ↓
Generated Image
```

### 6. HTTP Request – Supabase Storage

The generated binary image is sent to Supabase Storage.

Supabase provides a storage location for the generated image so it can be accessed again later in the workflow.

```text
Hugging Face
      ↓
Binary Image
      ↓
Supabase Storage
```

### 7. Edit Fields

The workflow prepares the Supabase image information required for the next step.

This can include the stored image URL or other data needed to retrieve the image.

### 8. HTTP Request – Get Image

The workflow retrieves the stored image from Supabase.

This allows the image to be prepared for the final Notion update.

```text
Supabase Storage
      ↓
Retrieve Image
      ↓
Image Data
```

### 9. Notion – Update Data Page

The final step updates an existing Notion data page with the generated image.

The image becomes part of the content record stored in the Notion database.

---

## Complete Automation Flow

```text
Google Sheets
     ↓
Image Prompt
     ↓
n8n Schedule Trigger
     ↓
Filter
     ↓
Edit Fields
     ↓
Hugging Face
     ↓
AI Generated Image
     ↓
Supabase Storage
     ↓
Retrieve Image
     ↓
Notion Data Page
```

---

## Technologies

* n8n
* Hugging Face
* Supabase
* Supabase Storage
* Google Sheets
* Notion
* HTTP Request
* APIs
* Binary Data Processing
* Workflow Automation
* AI Image Generation

---

## Skills Demonstrated

* n8n workflow automation
* AI image generation integration
* Hugging Face API integration
* HTTP API integration
* Binary image handling
* Supabase Storage integration
* Google Sheets automation
* Notion database automation
* Data transformation
* Scheduled automation
* Multi-step AI workflows
* Content automation

---

## Use Case

This workflow can be used as part of a content automation system where image prompts are prepared in Google Sheets and automatically converted into AI-generated images.

The generated images can then be stored and connected to structured content records in Notion.

For example:

```text
Content Idea
     ↓
Image Prompt
     ↓
AI Image Generation
     ↓
Supabase Storage
     ↓
Notion Content Database
```

This creates a foundation for future content workflows such as Pinterest content automation and other visual marketing workflows.

---

## Project Purpose

This is a self-initiated portfolio project created to demonstrate practical experience with:

* AI automation
* n8n
* API integration
* AI image generation
* Cloud storage
* Notion automation
* Content workflow automation

This project is a personal learning and portfolio project and is not presented as paid client or production work.

---

## Project Websites

### The Organized Habitat

https://theorganizedhabitat.runable.site/

The Organized Habitat is used as an example website within the user's broader content automation projects.

### Personal Portfolio

https://floresronaldjonjon.runable.site/

The personal portfolio showcases the project, automation skills, and other AI and digital marketing projects.

---

## Future Improvements

* Add automatic image naming
* Add image metadata to Notion
* Add image validation
* Add error handling and retry logic
* Add duplicate image detection
* Add image approval before saving
* Generate multiple image variations
* Connect the workflow with Pinterest publishing
* Add automated content scheduling
* Track generated images and publishing status

---

# Deutsche Version

# KI-Bildgenerierung – Hugging Face, Supabase & Notion

## Übersicht

Dieses selbst entwickelte Portfolio-Projekt zeigt, wie n8n die KI-Bildgenerierung und Content-Verwaltung mit Hugging Face, Supabase Storage und Notion automatisieren kann.

Der Workflow startet mit einem Prompt in Google Sheets. n8n ruft den Prompt ab, sendet ihn an einen Hugging-Face-Endpunkt zur Bildgenerierung, speichert das generierte Bild in Supabase Storage, ruft das gespeicherte Bild anschließend wieder ab und aktualisiert eine bestehende Notion-Datenseite mit dem generierten Bild.

Das Projekt ist Teil eines größeren Content-Automatisierungsprozesses und zeigt, wie KI-generierte visuelle Inhalte mit einer strukturierten Content-Datenbank verbunden werden können.

---

## Workflow

```text
Schedule Trigger
        ↓
Google Sheets – Zeile abrufen
        ↓
Filter
        ↓
Edit Fields
        ↓
HTTP Request – Hugging Face
        ↓
HTTP Request – Supabase Storage
        ↓
Edit Fields
        ↓
HTTP Request – Bild abrufen
        ↓
Notion – Datenseite aktualisieren
```

---

## Funktionsweise

### 1. Schedule Trigger

Der Workflow startet automatisch über einen n8n Schedule Trigger.

Er überprüft den Workflow nach einem festgelegten Zeitplan, damit neue Aufgaben zur Bildgenerierung automatisch verarbeitet werden können.

### 2. Google Sheets – Zeile abrufen

Google Sheets enthält den Prompt für die Bildgenerierung.

n8n ruft die entsprechende Zeile ab und übernimmt den Prompt für die Anfrage an den Hugging-Face-Endpunkt.

### 3. Filter

Der Filter prüft, ob der Datensatz für die Verarbeitung bereit ist.

Dadurch können unvollständige oder noch nicht freigegebene Datensätze zurückgehalten werden.

### 4. Edit Fields

Der Edit-Fields-Schritt bereitet die benötigten Daten für die nächste HTTP-Anfrage vor und strukturiert sie.

### 5. HTTP Request – Hugging Face

Der vorbereitete Prompt wird an einen Hugging-Face-Endpunkt zur Bildgenerierung gesendet.

Hugging Face verarbeitet den Prompt und gibt das generierte Bild als Binärdaten zurück.

```text
Prompt
   ↓
Hugging Face
   ↓
Generiertes Bild
```

### 6. HTTP Request – Supabase Storage

Das generierte Binärbild wird anschließend in Supabase Storage gespeichert.

```text
Hugging Face
      ↓
Binärbild
      ↓
Supabase Storage
```

### 7. Edit Fields

Die Informationen zum gespeicherten Bild werden für den nächsten Schritt vorbereitet.

### 8. HTTP Request – Bild abrufen

Das gespeicherte Bild wird erneut aus Supabase abgerufen.

Damit kann das Bild für die abschließende Aktualisierung in Notion vorbereitet werden.

### 9. Notion – Datenseite aktualisieren

Zum Abschluss wird eine bestehende Notion-Datenseite mit dem generierten Bild aktualisiert.

Das Bild wird dadurch Teil des entsprechenden Content-Eintrags in der Notion-Datenbank.

---

## Vollständiger Automatisierungsprozess

```text
Google Sheets
     ↓
Bild-Prompt
     ↓
n8n Schedule Trigger
     ↓
Filter
     ↓
Edit Fields
     ↓
Hugging Face
     ↓
KI-generiertes Bild
     ↓
Supabase Storage
     ↓
Bild abrufen
     ↓
Notion-Datenseite
```

---

## Technologien

* n8n
* Hugging Face
* Supabase
* Supabase Storage
* Google Sheets
* Notion
* HTTP Request
* APIs
* Binärdatenverarbeitung
* Workflow-Automatisierung
* KI-Bildgenerierung

---

## Gezeigte Fähigkeiten

* n8n Workflow-Automatisierung
* Integration von KI-Bildgenerierung
* Hugging-Face-API-Integration
* HTTP-API-Integration
* Verarbeitung von Binärbildern
* Supabase-Storage-Integration
* Google-Sheets-Automatisierung
* Notion-Datenbank-Automatisierung
* Datenverarbeitung und Transformation
* Zeitgesteuerte Automatisierung
* Mehrstufige KI-Workflows
* Content-Automatisierung

---

## Anwendungsfall

Dieser Workflow kann Teil eines Content-Automatisierungssystems sein, bei dem Bild-Prompts in Google Sheets vorbereitet und automatisch in KI-generierte Bilder umgewandelt werden.

Die generierten Bilder können anschließend gespeichert und mit strukturierten Content-Datensätzen in Notion verbunden werden.

```text
Content-Idee
     ↓
Bild-Prompt
     ↓
KI-Bildgenerierung
     ↓
Supabase Storage
     ↓
Notion Content-Datenbank
```

Der Workflow bildet damit eine Grundlage für zukünftige Content-Prozesse, beispielsweise für Pinterest-Content-Automatisierung und andere visuelle Marketing-Workflows.

---

## Projektzweck

Dieses Projekt wurde selbstständig als Portfolio- und Lernprojekt entwickelt, um praktische Erfahrungen mit:

* KI-Automatisierung
* n8n
* API-Integration
* KI-Bildgenerierung
* Cloud-Speicher
* Notion-Automatisierung
* Content-Workflow-Automatisierung

zu demonstrieren.

Es handelt sich um ein persönliches Lern- und Portfolio-Projekt und nicht um eine bezahlte Kunden- oder Produktionslösung.

---

## Projekt-Websites

### The Organized Habitat

https://theorganizedhabitat.runable.site/

The Organized Habitat wird als Beispiel-Website innerhalb der umfassenderen Content-Automatisierungsprojekte verwendet.

### Persönliches Portfolio

https://floresronaldjonjon.runable.site/

Das persönliche Portfolio zeigt dieses Projekt sowie weitere Projekte und praktische Erfahrungen im Bereich KI-Automatisierung und digitales Marketing.

---

## Zukünftige Verbesserungen

* Automatische Bildbenennung
* Bild-Metadaten in Notion speichern
* Bildvalidierung
* Fehlerbehandlung und Retry-Logik
* Erkennung von doppelten Bildern
* Bildfreigabe vor dem Speichern
* Mehrere Bildvarianten generieren
* Verbindung mit Pinterest Publishing
* Automatische Content-Planung
* Tracking von generierten Bildern und Veröffentlichungsstatus
