# Affiliate Content Publishing Automation — Notion to Website

## Project Overview

This is a self-built portfolio automation project that demonstrates how AI-generated affiliate content can be transferred from Notion to a website through an n8n workflow.

The previous content-generation workflow creates affiliate product content containing the product link, product image, and product review. This workflow retrieves the prepared content from Notion and sends the products to the website one by one.

The workflow uses a scheduled trigger to check for new content, processes the items individually, prepares the required website data, and sends it through an HTTP Request to the website.

**This is a self-built portfolio project — not client or employer work.**

---

## Workflow

```text
Schedule Trigger
        ↓
Notion – Get Many Pages
        ↓
Filter
        ↓
Loop Over Items
        ↓
Code Node
        ↓
HTTP Request
        ↓
Wait
        ↓
Next Item
```

---

## How It Works

### 1. Schedule Trigger

The workflow runs every minute using a Schedule Trigger.

This allows the automation to regularly check Notion for newly prepared affiliate content.

```text
Schedule Trigger
Every 1 minute
```

### 2. Notion – Get Many Pages

The workflow retrieves the prepared content from Notion.

The Notion pages contain the affiliate product information created by the previous AI content-generation workflow, including:

* Affiliate product link
* Product image
* Product review
* AI-generated product content

### 3. Filter

The Filter checks the retrieved Notion pages and allows only the items that are ready to be processed.

This prevents unfinished or unsuitable content from being sent to the website.

### 4. Loop Over Items

The Loop Over Items node processes the products individually.

For example, if 15 products are ready, the workflow does not send all 15 products at the same time.

Instead:

```text
Product 1
   ↓
Product 2
   ↓
Product 3
   ↓
...
Product 15
```

Each product passes through the remaining workflow separately.

### 5. Code Node

The Code node prepares and formats the information required by the website before sending it.

This allows the product data from Notion to be structured correctly for the website request.

### 6. HTTP Request

The HTTP Request sends the prepared product information to the website.

The request transfers the product data from the automation workflow to the website so the affiliate content can be added to the website.

### 7. Wait

The Wait node controls the workflow between items.

After one product is processed, the workflow waits before continuing to the next item.

This helps control the publishing process instead of sending all products simultaneously.

---

## Example Processing

If 15 products are available in Notion:

```text
Notion
   ↓
15 Ready Products
   ↓
Filter
   ↓
Loop Over Items
   ↓
Product 1 → Code → HTTP Request → Website
   ↓
Wait
   ↓
Product 2 → Code → HTTP Request → Website
   ↓
Wait
   ↓
Product 3 → Code → HTTP Request → Website
   ↓
...
   ↓
Product 15 → Code → HTTP Request → Website
```

The workflow continues until the available products have been processed.

---

## Connection With the Previous Workflow

This workflow works together with the previous **Affiliate Content Automation** workflow.

### Workflow 1 — Content Generation

```text
Google Sheets
      ↓
Filter
      ↓
Firecrawl
      ↓
Loop Over Items
      ↓
AI Agent
      ↓
Structured Output
      ↓
Notion
```

This workflow prepares the affiliate content and stores it in Notion.

### Workflow 2 — Website Publishing

```text
Schedule Trigger
      ↓
Notion
      ↓
Filter
      ↓
Loop Over Items
      ↓
Code
      ↓
HTTP Request
      ↓
Website
```

The second workflow takes the prepared content from Notion and sends it to the website.

Together, the two workflows create a content automation pipeline:

```text
Google Sheets
      ↓
Firecrawl
      ↓
AI Agent
      ↓
Notion
      ↓
n8n Publishing Workflow
      ↓
The Organized Habitat Website
```

---

## Technologies Used

* n8n
* Notion
* Schedule Trigger
* Loop Over Items
* Code Node
* HTTP Request
* Webhooks / APIs
* AI-generated content
* Affiliate content automation

---

## Skills Demonstrated

* Workflow automation
* Scheduled automation
* Notion automation
* Loop-based processing
* Data transformation
* HTTP API integration
* Website content automation
* Affiliate content workflows
* AI content pipeline integration
* Multi-step n8n workflows
* API-based website integration

---

## Project Purpose

This project was created as a self-initiated portfolio project to demonstrate how AI-generated content can move through an automation pipeline and be transferred from a content management system to a website.

The project demonstrates practical experience with n8n, Notion, APIs, data processing, and website automation.

**This is not client or employer work.**

---

## Project Websites

### The Organized Habitat

🌐 https://theorganizedhabitat.runable.site/

The website used as the destination for the automated affiliate content workflow.

### Personal Portfolio

🌐 https://floresronaldjonjon.runable.site/

The portfolio website where this automation project and other AI automation projects are presented.

---

# Deutsche Version

# Affiliate Content Publishing Automation — Notion zur Website

## Projektübersicht

Dies ist ein selbst entwickeltes Portfolio-Automatisierungsprojekt, das zeigt, wie KI-generierte Affiliate-Inhalte über einen n8n-Workflow von Notion auf eine Website übertragen werden können.

Der vorherige Content-Generierungs-Workflow erstellt Affiliate-Produktinhalte mit Produktlink, Produktbild und Produktbewertung. Dieser Workflow ruft die vorbereiteten Inhalte aus Notion ab und überträgt die Produkte einzeln an die Website.

Der Workflow verwendet einen zeitgesteuerten Trigger, um neue Inhalte zu prüfen, verarbeitet die Produkte einzeln, bereitet die erforderlichen Website-Daten auf und sendet sie über einen HTTP Request an die Website.

**Dies ist ein selbst entwickeltes Portfolio-Projekt – kein Kunden- oder Arbeitgeberprojekt.**

---

## Workflow

```text
Zeitplan-Trigger
        ↓
Notion – Mehrere Seiten abrufen
        ↓
Filter
        ↓
Loop Over Items
        ↓
Code Node
        ↓
HTTP Request
        ↓
Warten
        ↓
Nächstes Produkt
```

---

## Funktionsweise

### 1. Zeitplan-Trigger

Der Workflow wird jede Minute über einen Schedule Trigger gestartet.

Dadurch kann die Automatisierung regelmäßig prüfen, ob neue vorbereitete Affiliate-Inhalte in Notion vorhanden sind.

```text
Schedule Trigger
Alle 1 Minute
```

### 2. Notion – Mehrere Seiten abrufen

Der Workflow ruft die vorbereiteten Inhalte aus Notion ab.

Die Notion-Seiten enthalten die Produktinformationen aus dem vorherigen KI-Content-Workflow, einschließlich:

* Affiliate-Produktlink
* Produktbild
* Produktbewertung
* KI-generierte Produktinhalte

### 3. Filter

Der Filter prüft die abgerufenen Notion-Seiten und lässt nur die Inhalte weiterlaufen, die zur Verarbeitung bereit sind.

Dadurch werden unfertige oder nicht geeignete Inhalte nicht an die Website gesendet.

### 4. Loop Over Items

Der Loop-Over-Items-Node verarbeitet die Produkte einzeln.

Wenn beispielsweise 15 Produkte bereit sind, werden nicht alle 15 Produkte gleichzeitig an die Website gesendet.

Stattdessen:

```text
Produkt 1
   ↓
Produkt 2
   ↓
Produkt 3
   ↓
...
Produkt 15
```

Jedes Produkt durchläuft den restlichen Workflow einzeln.

### 5. Code Node

Der Code Node bereitet die von der Website benötigten Informationen auf und formatiert sie vor dem Versand.

Dadurch können die Produktdaten aus Notion in der für die Website erforderlichen Struktur verarbeitet werden.

### 6. HTTP Request

Der HTTP Request sendet die vorbereiteten Produktinformationen an die Website.

Die Produktdaten werden vom Automatisierungs-Workflow an die Website übertragen, damit die Affiliate-Inhalte dort verarbeitet bzw. hinzugefügt werden können.

### 7. Wait

Der Wait Node steuert die Verarbeitung zwischen den einzelnen Produkten.

Nach der Verarbeitung eines Produkts wartet der Workflow, bevor er mit dem nächsten Produkt fortfährt.

Dadurch werden nicht alle Produkte gleichzeitig an die Website gesendet.

---

## Beispielverarbeitung

Wenn 15 Produkte in Notion bereitstehen:

```text
Notion
   ↓
15 fertige Produkte
   ↓
Filter
   ↓
Loop Over Items
   ↓
Produkt 1 → Code → HTTP Request → Website
   ↓
Warten
   ↓
Produkt 2 → Code → HTTP Request → Website
   ↓
Warten
   ↓
Produkt 3 → Code → HTTP Request → Website
   ↓
...
   ↓
Produkt 15 → Code → HTTP Request → Website
```

Der Workflow läuft weiter, bis die verfügbaren Produkte verarbeitet wurden.

---

## Verbindung mit dem vorherigen Workflow

Dieser Workflow arbeitet zusammen mit dem vorherigen **Affiliate Content Automation**-Workflow.

### Workflow 1 – Content-Generierung

```text
Google Sheets
      ↓
Filter
      ↓
Firecrawl
      ↓
Loop Over Items
      ↓
KI-Agent
      ↓
Strukturierter Output
      ↓
Notion
```

Dieser Workflow erstellt die Affiliate-Inhalte und speichert sie in Notion.

### Workflow 2 – Website-Veröffentlichung

```text
Schedule Trigger
      ↓
Notion
      ↓
Filter
      ↓
Loop Over Items
      ↓
Code
      ↓
HTTP Request
      ↓
Website
```

Der zweite Workflow übernimmt die vorbereiteten Inhalte aus Notion und überträgt sie an die Website.

Zusammen bilden die beiden Workflows eine Content-Automatisierungspipeline:

```text
Google Sheets
      ↓
Firecrawl
      ↓
KI-Agent
      ↓
Notion
      ↓
n8n Publishing Workflow
      ↓
The Organized Habitat Website
```

---

## Verwendete Technologien

* n8n
* Notion
* Schedule Trigger
* Loop Over Items
* Code Node
* HTTP Request
* Webhooks / APIs
* KI-generierte Inhalte
* Affiliate-Content-Automatisierung

---

## Gezeigte Fähigkeiten

* Workflow-Automatisierung
* Zeitgesteuerte Automatisierung
* Notion-Automatisierung
* Verarbeitung mit Loops
* Datenverarbeitung und -transformation
* HTTP-API-Integration
* Website-Content-Automatisierung
* Affiliate-Content-Workflows
* KI-Content-Pipeline-Integration
* Mehrstufige n8n-Workflows
* API-basierte Website-Integration

---

## Projektziel

Dieses Projekt wurde als selbst entwickeltes Portfolio-Projekt erstellt, um zu zeigen, wie KI-generierte Inhalte durch eine Automatisierungspipeline verarbeitet und von einem Content-Management-System an eine Website übertragen werden können.

Das Projekt demonstriert praktische Kenntnisse in n8n, Notion, APIs, Datenverarbeitung und Website-Automatisierung.

**Dies ist kein Kunden- oder Arbeitgeberprojekt.**

---

## Projekt-Websites

### The Organized Habitat

🌐 https://theorganizedhabitat.runable.site/

Die Website dient als Ziel für den automatisierten Affiliate-Content-Workflow.

### Persönliches Portfolio

🌐 https://floresronaldjonjon.runable.site/

Die Portfolio-Website, auf der dieses Automatisierungsprojekt und weitere KI-Automatisierungsprojekte präsentiert werden.
