# Affiliate Content Update Automation — Google Sheets, Firecrawl, AI & Notion

## English

### Project Overview

This is a self-built portfolio project demonstrating how AI and workflow automation can be used to prepare and update affiliate product content.

The workflow starts with product information entered into Google Sheets, including a product URL, image, and review information. Firecrawl extracts product information from the provided website, while an AI Agent processes the content and creates structured product content that is stored in Notion.

The workflow is designed to process up to 15 product items in one run.

### Workflow

```text
Google Sheets Trigger
        ↓
Filter – Status = Ready
        ↓
Firecrawl – Extract Product Information
        ↓
Loop Over Items
        ↓
AI Agent – Chat Model + Structured Output
        ↓
Notion – Create Data Page
        ↓
Wait
        ↓
Next Item
        ↓
Loop continues until all items are processed
```

### How It Works

1. Product information is entered into Google Sheets.
2. The Google Sheets row contains the product URL, image, review information, and processing status.
3. The workflow checks the sheet every minute for items with the status **Ready**.
4. The Filter node allows only ready items to continue.
5. Firecrawl reads the provided product URL and extracts product information, including product descriptions.
6. The workflow processes the extracted product items one at a time using a Loop.
7. An AI Agent using a chat model processes each product and generates structured content.
8. The generated content is combined with the product link and image from Google Sheets.
9. A Notion Create Data Page node stores the processed product content.
10. The Wait node controls the workflow before continuing with the next product item.
11. The loop continues until all available product items have been processed.
12. The workflow can process up to 15 product items in one run.

### Content Workflow

The automation is designed to help prepare affiliate product content in a consistent format.

For each product, the workflow can combine:

* Product information extracted with Firecrawl
* Product URL from Google Sheets
* Product image from Google Sheets
* Product review information
* AI-generated product content
* Structured output for Notion

### Technologies Used

* n8n
* Google Sheets
* Firecrawl
* AI Agent
* Chat Model
* Structured Output
* Notion
* Webhooks / APIs

### Key Features

#### Google Sheets Input

Google Sheets is used as the starting point for product URLs, images, review information, and workflow status.

#### Automated Filtering

The workflow checks for rows marked **Ready** and processes only those items.

#### Website Content Extraction

Firecrawl extracts product information from the provided URLs.

#### Loop Processing

Products are processed individually instead of being processed all at once.

#### AI Content Generation

An AI Agent processes the extracted information and creates structured product content.

#### Notion Content Storage

The generated content is saved as individual data pages in Notion for further use in the affiliate content workflow.

#### Batch Processing

The workflow is designed to process up to 15 product items in one run.

### Skills Demonstrated

* Workflow automation
* AI content generation
* Firecrawl website extraction
* Structured AI output
* Loop-based automation
* Google Sheets automation
* Notion automation
* Affiliate content workflows
* API integration
* Data processing
* Content organization

### Project Purpose

This project was created as a self-initiated portfolio project to demonstrate practical skills in AI automation, content automation, website data extraction, and affiliate marketing workflows.

It is not client or employer work.

### Future Improvements

* Connect the Notion content directly to the affiliate website
* Add automated content publishing
* Add product data validation
* Improve AI content quality and formatting
* Add additional product sources
* Add automated error handling and retry logic

---

# Affiliate Content-Automatisierung — Google Sheets, Firecrawl, KI & Notion

## Deutsch

### Projektübersicht

Dieses selbst entwickelte Portfolio-Projekt zeigt, wie KI und Workflow-Automatisierung zur Vorbereitung und Aktualisierung von Affiliate-Produktinhalten eingesetzt werden können.

Der Workflow beginnt mit Produktinformationen, die in Google Sheets eingetragen werden, darunter eine Produkt-URL, ein Bild und Bewertungsinformationen. Firecrawl extrahiert Produktinformationen von der angegebenen Website. Anschließend verarbeitet ein KI-Agent die Inhalte und erstellt strukturierte Produktdaten, die in Notion gespeichert werden.

Der Workflow ist dafür ausgelegt, bis zu 15 Produkte pro Durchlauf zu verarbeiten.

### Workflow

```text
Google Sheets Trigger
        ↓
Filter – Status = Ready
        ↓
Firecrawl – Produktinformationen extrahieren
        ↓
Loop über die Produkte
        ↓
KI-Agent – Chat-Modell + strukturierte Ausgabe
        ↓
Notion – Daten-Seite erstellen
        ↓
Wait
        ↓
Nächstes Produkt
        ↓
Loop läuft weiter, bis alle Produkte verarbeitet wurden
```

### Funktionsweise

1. Produktinformationen werden in Google Sheets eingetragen.
2. Die Google-Sheets-Zeile enthält die Produkt-URL, das Bild, Bewertungsinformationen und den Bearbeitungsstatus.
3. Der Workflow überprüft jede Minute, ob Produkte den Status **Ready** haben.
4. Der Filter lässt nur bereitstehende Produkte weiterlaufen.
5. Firecrawl liest die angegebene Produkt-URL und extrahiert Produktinformationen, einschließlich Produktbeschreibungen.
6. Die Produkte werden über einen Loop einzeln verarbeitet.
7. Ein KI-Agent mit einem Chat-Modell verarbeitet jedes Produkt und erstellt strukturierte Inhalte.
8. Die erstellten Inhalte werden mit dem Produkt-Link und dem Bild aus Google Sheets kombiniert.
9. Mit „Notion Create Data Page“ werden die Produktinhalte in Notion gespeichert.
10. Der Wait-Schritt steuert den Workflow, bevor das nächste Produkt verarbeitet wird.
11. Der Loop läuft weiter, bis alle verfügbaren Produkte verarbeitet wurden.
12. Der Workflow kann bis zu 15 Produkte pro Durchlauf verarbeiten.

### Content-Workflow

Die Automatisierung hilft dabei, Affiliate-Produktinhalte strukturiert und einheitlich vorzubereiten.

Für jedes Produkt können folgende Informationen kombiniert werden:

* Mit Firecrawl extrahierte Produktinformationen
* Produkt-URL aus Google Sheets
* Produktbild aus Google Sheets
* Bewertungsinformationen
* KI-generierte Produktinhalte
* Strukturierte Ausgabe für Notion

### Verwendete Technologien

* n8n
* Google Sheets
* Firecrawl
* KI-Agent
* Chat-Modell
* Strukturierte Ausgabe
* Notion
* Webhooks / APIs

### Hauptfunktionen

#### Google-Sheets-Eingabe

Google Sheets dient als Ausgangspunkt für Produkt-URLs, Bilder, Bewertungsinformationen und den Workflow-Status.

#### Automatische Filterung

Der Workflow überprüft die Einträge mit dem Status **Ready** und verarbeitet nur diese Produkte.

#### Website-Inhaltsextraktion

Firecrawl extrahiert Produktinformationen aus den angegebenen URLs.

#### Loop-Verarbeitung

Die Produkte werden einzeln verarbeitet, anstatt alle gleichzeitig zu bearbeiten.

#### KI-Content-Generierung

Ein KI-Agent verarbeitet die extrahierten Informationen und erstellt strukturierte Produktinhalte.

#### Notion-Inhaltsspeicherung

Die generierten Inhalte werden als einzelne Daten-Seiten in Notion gespeichert und können anschließend für den Affiliate-Content-Workflow verwendet werden.

#### Verarbeitung mehrerer Produkte

Der Workflow ist dafür ausgelegt, bis zu 15 Produkte pro Durchlauf zu verarbeiten.

### Gezeigte Fähigkeiten

* Workflow-Automatisierung
* KI-Content-Generierung
* Firecrawl-Website-Extraktion
* Strukturierte KI-Ausgabe
* Loop-basierte Automatisierung
* Google-Sheets-Automatisierung
* Notion-Automatisierung
* Affiliate-Content-Workflows
* API-Integration
* Datenverarbeitung
* Content-Organisation

### Projektziel

Dieses Projekt wurde als selbstinitiiertes Portfolio-Projekt erstellt, um praktische Kenntnisse in KI-Automatisierung, Content-Automatisierung, Website-Datenextraktion und Affiliate-Marketing-Workflows zu demonstrieren.

Es handelt sich nicht um ein Kunden- oder Arbeitgeberprojekt.

### Zukünftige Verbesserungen

* Notion-Inhalte direkt mit der Affiliate-Website verbinden
* Automatische Veröffentlichung von Inhalten hinzufügen
* Produktdaten validieren
* Qualität und Formatierung der KI-Inhalte verbessern
* Weitere Produktquellen hinzufügen
* Automatische Fehlerbehandlung und Wiederholungslogik hinzufügen

## Project Website
## Websites

🌐 [Visit The Organized Habitat](https://theorganizedhabitat.runable.site/)

👤 [Visit My Personal Portfolio](https://floresronaldjonjon.runable.site/)
