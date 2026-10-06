# Pinterest Account Upload Automation — n8n, Make.com & Notion

## Overview

This self-built portfolio project demonstrates how n8n can automate the transfer of prepared content from Notion to a Pinterest account using a Make.com webhook.

The workflow starts by retrieving prepared content from a Notion database. n8n filters the records that are ready for publishing, sends the required content and image information to a Make.com webhook through an HTTP Request, and Make.com handles the Pinterest publishing process.

After the publishing workflow is completed, the process returns to n8n, where the Notion data page is updated with the latest content and image information.

This project is part of a larger content automation pipeline for AI-generated and affiliate content.

---

## Workflow

```text
Schedule Trigger
        ↓
Notion – Get Many Pages
        ↓
Filter
        ↓
HTTP Request
        ↓
Make.com Webhook
        ↓
Pinterest Account
        ↓
Publishing Result
        ↓
n8n
        ↓
Notion – Update Data Page
```

---

## How It Works

### 1. Schedule Trigger

The workflow starts automatically using an n8n Schedule Trigger.

This allows n8n to periodically check the Notion database for content that is ready to be sent for Pinterest publishing.

### 2. Notion – Get Many Pages

n8n retrieves multiple pages from the Notion database.

The database contains prepared content, including information such as:

* Content title
* Description
* Image
* Link
* Pinterest-related content
* Publishing status

The exact properties depend on the Notion database configuration.

### 3. Filter

The Filter node checks which records are ready to continue through the workflow.

This prevents content that is not ready from being sent to the publishing workflow.

For example:

```text
Status = Ready
```

Only matching records continue.

### 4. HTTP Request

n8n sends the prepared content to a Make.com webhook using an HTTP Request.

The request can contain the information required by the Make.com scenario, such as:

```text
Title
Description
Image
URL
Content ID
```

The Make.com webhook acts as the connection between the n8n workflow and the Pinterest publishing process.

```text
n8n
 ↓
HTTP Request
 ↓
Make.com Webhook
```

### 5. Make.com Webhook → Pinterest

Make.com receives the data from n8n and continues the automation.

The Make.com scenario handles the Pinterest publishing process and sends the prepared content to the connected Pinterest account.

```text
Make.com Webhook
        ↓
Pinterest
        ↓
Publish Content
```

### 6. Return to n8n

After the Make.com publishing process, the result is returned to the n8n workflow.

This allows n8n to continue processing the content record.

### 7. Notion – Update Data Page

The final step updates the corresponding Notion data page.

The Notion record can be updated with the latest content and image information, as well as publishing-related information depending on the configured workflow.

This helps keep the Notion database synchronized with the publishing workflow.

---

## Complete Automation Flow

```text
Notion Content
      ↓
Schedule Trigger
      ↓
Get Many Pages
      ↓
Filter Ready Content
      ↓
HTTP Request
      ↓
Make.com Webhook
      ↓
Pinterest Account
      ↓
Publishing Result
      ↓
n8n
      ↓
Update Notion
```

---

## Connection With Previous Content Workflows

This project can be connected to the previous content automation workflows.

### Content Generation

```text
Google Sheets
      ↓
Firecrawl / AI
      ↓
AI Agent
      ↓
Notion
```

### Content Publishing

```text
Notion
      ↓
n8n
      ↓
Make.com Webhook
      ↓
Pinterest
```

### Combined Content Pipeline

```text
Content Idea
      ↓
AI Content Generation
      ↓
Notion
      ↓
AI Image Generation
      ↓
Notion
      ↓
n8n Publishing Workflow
      ↓
Make.com
      ↓
Pinterest
      ↓
Notion Update
```

This creates a foundation for a larger AI-powered content and Pinterest automation system.

---

## Technologies

* n8n
* Make.com
* Pinterest
* Notion
* HTTP Request
* Webhooks
* APIs
* Workflow Automation
* Content Automation
* Pinterest Automation

---

## Skills Demonstrated

* n8n workflow automation
* Make.com integration
* Webhook integration
* HTTP API integration
* Notion database automation
* Pinterest workflow automation
* Scheduled automation
* Content filtering
* Data transfer between automation platforms
* Content synchronization
* Multi-platform workflow design
* Marketing automation

---

## Use Case

This workflow can be used to automate the transfer of prepared marketing content from a Notion database to a Pinterest publishing workflow.

Instead of manually copying content from Notion into Pinterest, the automation can prepare and transfer the required information through a Make.com webhook.

Example:

```text
Notion
  ↓
Prepared Pinterest Content
  ↓
n8n
  ↓
Make.com Webhook
  ↓
Pinterest
```

---

## Project Purpose

This is a self-initiated portfolio project created to demonstrate practical experience with:

* Workflow automation
* n8n
* Make.com
* Webhooks
* HTTP requests
* Notion
* Pinterest automation
* Content management

This project is a personal learning and portfolio project and is not presented as paid client or production work.

---

## Future Improvements

* Add publishing status tracking
* Add Pinterest board selection
* Add duplicate detection
* Add automatic retry handling
* Add error notifications
* Add publishing logs
* Add content approval before publishing
* Add automated scheduling
* Add support for multiple Pinterest accounts
* Add performance tracking
* Connect Pinterest results back to the content database

---

# Deutsche Version

# Pinterest-Account-Upload-Automatisierung – n8n, Make.com & Notion

## Übersicht

Dieses selbst entwickelte Portfolio-Projekt zeigt, wie n8n die Übertragung vorbereiteter Inhalte aus Notion zu einem Pinterest-Account über einen Make.com-Webhook automatisieren kann.

Der Workflow ruft vorbereitete Inhalte aus einer Notion-Datenbank ab. n8n filtert die Datensätze, die zur Veröffentlichung bereit sind, und sendet die benötigten Content- und Bildinformationen über einen HTTP Request an einen Make.com-Webhook.

Make.com übernimmt anschließend den Pinterest-Veröffentlichungsprozess.

Nach Abschluss des Publishing-Prozesses wird das Ergebnis wieder an n8n übergeben. Anschließend wird die entsprechende Notion-Datenseite mit den aktuellen Content- und Bildinformationen aktualisiert.

---

## Workflow

```text
Schedule Trigger
        ↓
Notion – Mehrere Seiten abrufen
        ↓
Filter
        ↓
HTTP Request
        ↓
Make.com Webhook
        ↓
Pinterest-Account
        ↓
Veröffentlichungsergebnis
        ↓
n8n
        ↓
Notion – Datenseite aktualisieren
```

---

## Funktionsweise

### 1. Schedule Trigger

Der Workflow startet automatisch über einen n8n Schedule Trigger.

Dadurch kann n8n die Notion-Datenbank regelmäßig auf Inhalte überprüfen, die für die Pinterest-Veröffentlichung bereit sind.

### 2. Notion – Mehrere Seiten abrufen

n8n ruft mehrere Seiten aus der Notion-Datenbank ab.

Die Datenbank enthält vorbereitete Inhalte, zum Beispiel:

* Titel
* Beschreibung
* Bild
* Link
* Pinterest-bezogene Inhalte
* Veröffentlichungsstatus

Die genauen Eigenschaften hängen von der verwendeten Notion-Datenbank ab.

### 3. Filter

Der Filter prüft, welche Datensätze zur weiteren Verarbeitung bereit sind.

Beispiel:

```text
Status = Ready
```

Nur passende Datensätze werden weitergeleitet.

### 4. HTTP Request

n8n sendet die vorbereiteten Daten über einen HTTP Request an einen Make.com-Webhook.

Dabei können beispielsweise folgende Informationen übertragen werden:

```text
Titel
Beschreibung
Bild
URL
Content ID
```

Der Make.com-Webhook dient als Verbindung zwischen n8n und dem Pinterest-Publishing-Prozess.

### 5. Make.com Webhook → Pinterest

Make.com empfängt die Daten von n8n und führt anschließend das konfigurierte Publishing-Szenario aus.

Die vorbereiteten Inhalte werden an den verbundenen Pinterest-Account weitergeleitet.

```text
Make.com Webhook
        ↓
Pinterest
        ↓
Inhalt veröffentlichen
```

### 6. Rückgabe an n8n

Nach dem Make.com-Prozess wird das Ergebnis wieder an den n8n-Workflow übergeben.

Dadurch kann n8n den entsprechenden Datensatz weiterverarbeiten.

### 7. Notion – Datenseite aktualisieren

Zum Abschluss wird die entsprechende Notion-Datenseite aktualisiert.

Je nach Workflow-Konfiguration können dabei Content-, Bild- und Veröffentlichungsinformationen aktualisiert werden.

Dadurch bleibt die Notion-Datenbank mit dem Publishing-Prozess synchronisiert.

---

## Vollständiger Automatisierungsprozess

```text
Notion Content
      ↓
Schedule Trigger
      ↓
Mehrere Seiten abrufen
      ↓
Bereite Inhalte filtern
      ↓
HTTP Request
      ↓
Make.com Webhook
      ↓
Pinterest-Account
      ↓
Veröffentlichungsergebnis
      ↓
n8n
      ↓
Notion aktualisieren
```

---

## Verbindung mit den vorherigen Content-Workflows

Dieser Workflow kann mit den bereits erstellten Content-Automatisierungen verbunden werden.

### Content-Generierung

```text
Google Sheets
      ↓
Firecrawl / KI
      ↓
KI-Agent
      ↓
Notion
```

### Content-Veröffentlichung

```text
Notion
      ↓
n8n
      ↓
Make.com Webhook
      ↓
Pinterest
```

### Gesamter Content-Prozess

```text
Content-Idee
      ↓
KI-Content-Generierung
      ↓
Notion
      ↓
KI-Bildgenerierung
      ↓
Notion
      ↓
n8n Publishing Workflow
      ↓
Make.com
      ↓
Pinterest
      ↓
Notion Aktualisierung
```

Damit entsteht eine Grundlage für ein umfangreicheres KI-gestütztes Content- und Pinterest-Automatisierungssystem.

---

## Technologien

* n8n
* Make.com
* Pinterest
* Notion
* HTTP Request
* Webhooks
* APIs
* Workflow-Automatisierung
* Content-Automatisierung
* Pinterest-Automatisierung

---

## Gezeigte Fähigkeiten

* n8n Workflow-Automatisierung
* Make.com-Integration
* Webhook-Integration
* HTTP-API-Integration
* Notion-Datenbank-Automatisierung
* Pinterest-Workflow-Automatisierung
* Zeitgesteuerte Automatisierung
* Content-Filterung
* Datentransfer zwischen Automatisierungsplattformen
* Content-Synchronisierung
* Entwicklung plattformübergreifender Workflows
* Marketing-Automatisierung

---

## Anwendungsfall

Dieser Workflow kann verwendet werden, um vorbereitete Marketing-Inhalte aus einer Notion-Datenbank automatisch an einen Pinterest-Publishing-Prozess zu übertragen.

Anstatt Inhalte manuell von Notion nach Pinterest zu kopieren, kann die Automatisierung die benötigten Informationen über einen Make.com-Webhook übertragen.

```text
Notion
  ↓
Vorbereiteter Pinterest-Content
  ↓
n8n
  ↓
Make.com Webhook
  ↓
Pinterest
```

---

## Projektzweck

Dieses selbst entwickelte Portfolio-Projekt wurde erstellt, um praktische Erfahrungen mit folgenden Bereichen zu demonstrieren:

* Workflow-Automatisierung
* n8n
* Make.com
* Webhooks
* HTTP Requests
* Notion
* Pinterest-Automatisierung
* Content-Management

Es handelt sich um ein persönliches Lern- und Portfolio-Projekt und nicht um eine bezahlte Kunden- oder Produktionslösung.

---

## Zukünftige Verbesserungen

* Veröffentlichungsstatus verfolgen
* Pinterest-Board-Auswahl hinzufügen
* Erkennung doppelter Inhalte
* Automatische Retry-Logik
* Fehlermeldungen und Benachrichtigungen
* Publishing-Logs
* Content-Freigabe vor der Veröffentlichung
* Automatische Veröffentlichungsplanung
* Unterstützung mehrerer Pinterest-Accounts
* Performance-Tracking
* Pinterest-Ergebnisse zurück in die Content-Datenbank übertragen
