# 🚀 Backup N8N Workflow — Automation Systems & AI Solutions

![n8n](https://img.shields.io/badge/n8n-Automation-orange?style=for-the-badge&logo=n8n)
![Automation](https://img.shields.io/badge/Workflow-Automation-blue?style=for-the-badge)
![AI](https://img.shields.io/badge/AI-Integrated-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

---
A collection of practical **n8n automation workflows** covering lead generation, sales outreach, WhatsApp communication, e-commerce operations, AI content generation, news automation, and workflow management.

These workflows demonstrate how n8n can connect **AI models, APIs, Google Sheets, WhatsApp, email, telephony, RSS feeds, and external AI media-generation services** into automated business processes.

---

## 📌 Workflow Overview

| # | Workflow | Main Purpose | Key Area |
|---|---|---|---|
| 1 | Backup N8N Workflows | Workflow backup / management | n8n Operations |
| 2 | Cold Calling — No Website Prospects | Identify and process businesses without websites | Lead Generation |
| 3 | E-commerce Product Listing | Automate product-listing related operations | E-commerce |
| 4 | Lead Outreach Automation — Email + Call | AI-assisted email + phone outreach | Sales Automation |
| 5 | MASS Agency — WhatsApp Lead Engagement | Automate new-lead WhatsApp follow-ups | Lead Engagement |
| 6 | MASS Agency — WhatsApp Status Updates | Send automated project updates to clients | Client Communication |
| 7 | My Workflow | Additional/custom n8n automation | Automation |
| 8 | RSS Feed News | Collect and AI-summarize recent news | Content Automation |
| 9 | Ultimate UGC Content System with AI Agents | Generate AI-assisted UGC creative/video content | AI Content |

---

# 1. 🗂️ Backup N8N Workflows

**File:** `backup-n8n-workflows-6-FcqPBxEIyB8759D1c0Q.json`

### Overview

This workflow is part of the repository's n8n workflow backup/management collection.

It represents the practice of keeping exported n8n workflow definitions available as JSON so workflows can be versioned, restored, transferred, or maintained outside the n8n interface.

### Typical Workflow Purpose

```text
n8n Workflow
     ↓
Export Workflow
     ↓
JSON Backup
     ↓
GitHub / Repository
     ↓
Restore / Re-import when required
```

### Use Case

Useful for:

- Workflow backup
- Version control
- Disaster recovery
- Moving workflows between n8n environments
- Maintaining an automation library
- Keeping historical workflow versions

> **Note:** The exact node-level definition of this export was not available in the supplied workflow attachments, so the description above is intentionally limited to its backup/management purpose.

---

# 2. 📞 Cold Calling — No Website Prospects

**File:** `cold-calling---no-website-prospects-dehln40HliXqDFSnnbJ5o.json`

### Overview

This workflow is designed around a specific sales-prospecting use case: finding or processing businesses that **do not have a website** and preparing them for outreach.

The intended business use case is particularly relevant for a web-development agency because businesses without a website can be qualified as potential website-development prospects.

### Conceptual Flow

```text
Prospect Data
      ↓
Check Website
      ↓
No Website?
      ↓
Qualify Prospect
      ↓
Prepare Outreach
      ↓
Cold Calling / Sales Process
```

### Business Use Case

Can support:

- Website-development prospecting
- Lead qualification
- Cold-calling lists
- Local-business outreach
- Sales pipeline preparation

> **Note:** The exact node configuration of this export was not available in the supplied workflow attachments. The description is therefore based on the workflow filename/use-case rather than an invented node-by-node reconstruction.

---

# 3. 🛒 E-commerce Product Listing

**File:** `e-commerce-pdt-listing-kd8vRx_RNs2guFY2vQLCf.json`

### Overview

This workflow is focused on automating an **e-commerce product-listing process**.

The workflow is intended to reduce repetitive work involved in preparing product information for an online store or product catalog.

### Conceptual Flow

```text
Product Information
       ↓
Process / Transform Data
       ↓
Prepare Listing Content
       ↓
Product Listing
       ↓
E-commerce Catalog
```

### Potential Business Applications

- Product catalog management
- Product-data processing
- Listing preparation
- E-commerce operations
- Reducing repetitive product-entry work

> **Note:** The exact nodes and integrations were not available in the supplied workflow attachments, so this section intentionally does not claim specific AI models, APIs, or publishing destinations.

---

# 4. 📧📞 Lead Outreach Automation — Email + Call

**File:** `lead-outreach-automation---email-+-call-oz63ffoKg1RbgqSUezAA5.json`

### Overview

A sales-outreach automation that processes prospect information, qualifies leads, generates personalized outreach content using AI, sends cold emails, generates call scripts, and can make international calls through Twilio.

### Workflow Flow

```text
Google Sheets
      ↓
Read Prospects
      ↓
Process One Lead at a Time
      ↓
Clean / Normalize Lead Data
      ↓
Check Email + Phone
      ↓
Qualification
      ↓
AI Generate Email
      ↓
Send Cold Email
      ↓
Update Lead Status
      ↓
AI Generate Call Script
      ↓
Select Voice
      ↓
Twilio Phone Call
      ↓
Update Lead Status
```

### Lead Processing

The workflow extracts and normalizes information such as:

- Company name
- Location
- Phone
- Email
- Website
- Rating
- Country

It also validates email addresses and formats phone numbers for international use.

A qualification score is calculated using available contact information and rating data.

### AI Email Generation

The workflow uses an AI node to generate cold-email content and then parses the generated response into:

- Email subject
- Email body

The generated email is sent to the qualified lead and the Google Sheet is updated with the outreach status.

### AI Call Generation

If a phone number is available, the workflow:

1. Generates an AI call script.
2. Parses the script.
3. Selects a voice based on the lead's country.
4. Uses Twilio to make the call.
5. Updates the lead's status.

The workflow contains country-specific voice mapping including examples such as:

- USA
- UK
- India
- Australia
- Germany
- France
- UAE
- Singapore

### Key Integrations

- n8n
- Google Sheets
- OpenAI / AI nodes
- Email
- Twilio
- JavaScript / Code nodes

### Business Use Case

This can automate a large part of an agency's outbound-sales process:

**Lead → Qualification → Personalized Email → Phone Outreach → Status Tracking**

---

# 5. 💬 MASS Agency — WhatsApp Lead Engagement

**File:** `mass-agency---whatsapp-lead-engagement-6v7p7YZMoZIxATyO7N-Gh.json`

### Overview

A WhatsApp-based lead-engagement workflow for the MASS agency.

It is designed to automatically respond to a new lead and continue the conversation through timed follow-ups.

### Workflow Flow

```text
Lead / Webhook
      ↓
Extract Lead Information
      ↓
Welcome WhatsApp Message
      ↓
Wait
      ↓
Service / CTA Message
      ↓
Wait 24 Hours
      ↓
Follow-up Message
      ↓
Discovery Call CTA
```

### Lead Information

The workflow works with information such as:

- Name
- Phone
- Service
- Company
- Lead source

### Engagement Sequence

The workflow sends an initial welcome message, waits before sending the next message, and then follows up after a longer delay.

The objective is to keep the lead engaged without requiring a salesperson to manually send every message.

### Key Integrations

- n8n
- Webhook
- WhatsApp / Meta Graph API
- HTTP Request
- Wait nodes

### Business Use Case

Useful for:

- Website leads
- Automation-service enquiries
- Agency leads
- Follow-up automation
- Discovery-call booking flows

---

# 6. 📊 MASS Agency — WhatsApp Status Updates

**File:** `mass-agency---whatsapp-status-updates-WnY5IXIU8ujAvtiCcRVfE.json`

### Overview

An automated client-communication workflow that sends weekly project-status updates through WhatsApp.

### Workflow Flow

```text
Weekly Schedule
      ↓
Load Client List
      ↓
Process Clients One-by-One
      ↓
Generate Status Message
      ↓
Send WhatsApp Update
      ↓
Wait
      ↓
Next Client
```

### Current Schedule

The exported workflow contains a weekly schedule trigger configured for **Monday at 09:00**.

### Client Data

The workflow's sample structure includes:

- Client name
- Phone
- Project
- Status
- Progress
- Next milestone

### Example Update Structure

```text
Weekly Project Update

Project
Status
Progress
Next Milestone

Questions / follow-up
```

### WhatsApp Integration

The workflow sends messages through the WhatsApp Graph API using:

- WhatsApp phone ID
- WhatsApp access token
- HTTP Request node

### Production Improvement

The workflow itself contains a note recommending that the hardcoded client list be replaced with a **Google Sheets node** for production use.

### Business Use Case

This automation can improve:

- Client transparency
- Weekly reporting
- Project communication
- Client experience
- Agency operations

---

# 7. ⚙️ My Workflow

**File:** `my-workflow-dyEj31QGvJ5SGzQ1IdmuD.json`

### Overview

A custom workflow included in the automation backup collection.

This workflow is maintained as part of the user's personal n8n experimentation and automation library.

### Purpose

The workflow can be treated as a custom/experimental automation rather than being grouped into the repository's primary sales, WhatsApp, news, or UGC systems.

### Repository Role

```text
Custom Automation
       ↓
Experiment / Development
       ↓
Testing
       ↓
Reusable Workflow
```

> **Note:** The exact node-level export for this workflow was not available in the supplied attachments, so no specific integrations or steps are claimed here.

---

# 8. 📰 RSS Feed News — AI News Summarization

**File:** `rss-feed-news-q08YgVYcakONIND651nyG.json`

### Overview

An AI-powered news aggregation and summarization workflow.

It collects articles from RSS feeds, filters recent stories, selects a limited number of articles, formats the article information, sends the content to an AI agent for summarization, and distributes the result.

### Workflow Flow

```text
Webhook Trigger
      ↓
Read RSS Feed
      ↓
Filter Recent Articles
      ↓
Select Best 5
      ↓
Format Article Data
      ↓
AI News Summarization Agent
      ↓
   ┌───────────────┐
   ↓               ↓
HTTP API        Telegram
```

### RSS Sources

The workflow contains feeds/categories including:

- The Hans India Sports
- TechRadar AI
- OneIndia International
- OneIndia India
- BBC Business
- BBC Technology

### Processing

The workflow:

1. Receives a webhook request.
2. Reads RSS content.
3. Filters articles from the previous three days.
4. Limits the result to five articles.
5. Extracts title, content/summary, and image URL.
6. Passes the articles to an AI agent.
7. Generates structured summaries.
8. Sends the output to an HTTP API.
9. Sends output to Telegram.

### AI Models / Integrations

The exported workflow contains integrations for:

- Google Gemini
- Groq
- OpenRouter
- DeepSeek through OpenRouter

### Business Use Case

This pattern can be used for:

- Automated news portals
- News dashboards
- Telegram channels
- Editorial automation
- Content aggregation
- AI-powered news pipelines

---

# 9. 🎬 Ultimate UGC Content System with AI Agents

**File:** `ultimate-ugc-content-system-with-ai-agents-gAANDbXm4h0cuy5YHmLjB.json`

### Overview

An AI-powered UGC content-generation workflow designed to transform product information and product images into AI-generated UGC-style creative assets and video prompts.

The workflow contains separate generation paths involving **Veo 3.1, Nano Banana, and Sora 2**.

### Workflow Concept

```text
Product Information
       ↓
Google Sheets
       ↓
Product + ICP + Features + Setting
       ↓
AI Prompt Generation
       ↓
Reference / Product Image
       ↓
AI Image / Video Generation
       ↓
Check Generation Status
       ↓
Analyze / Process Output
       ↓
Update Google Sheets
```

### Product Data

The workflow works with information such as:

- Product
- Product Photo
- Ideal Customer Profile
- Product Features
- Setting
- Model
- Status
- Finished Video

### AI Video Generation

One of the workflow paths generates video prompts and sends them to the Kie.AI Veo API.

The exported workflow includes configuration for:

- Veo 3 / Veo 3.1
- 9:16 vertical video
- Product reference images
- AI-generated UGC prompts
- Generation-status checking

### UGC Prompting

The workflow is designed to generate natural, relatable, product-focused UGC-style video prompts.

The prompt system emphasizes:

- Product consistency
- Natural dialogue
- Short-form video
- Authentic presentation
- Reference-image consistency
- Vertical video format

### Other AI Generation Paths

The workflow also contains sections associated with:

- Nano Banana
- Veo 3.1
- Sora 2

### Google Sheets

Google Sheets acts as the product/content management layer, allowing the workflow to read product information and update processing status and finished-video information.

### Setup / Attribution

The workflow export contains a setup guide referencing **Nate Herk** and external templates/services.

If redistributing this workflow publicly, retain appropriate attribution and independently verify the licensing/usage terms of any referenced templates, APIs, or third-party services.

### Business Use Case

Useful for:

- E-commerce content generation
- UGC advertising
- Product marketing
- Social-media creative production
- AI video generation
- Automated creative pipelines

---

# 🔗 Overall Automation Architecture

Together, these workflows demonstrate several layers of business automation:

```text
                         ┌──────────────────────┐
                         │       n8n             │
                         │ Automation Layer      │
                         └──────────┬───────────┘
                                    │
             ┌──────────────────────┼──────────────────────┐
             │                      │                      │
             ▼                      ▼                      ▼
       Lead Generation        Client Communication     Content
             │                      │                      │
      ┌──────┴──────┐         ┌─────┴─────┐        ┌─────┴─────┐
      │             │         │           │        │           │
   Email         Calling   WhatsApp    Status    RSS News    UGC
      │             │         │           │        │           │
      └──────┬──────┘         └─────┬─────┘        └─────┬─────┘
             │                      │                    │
             └──────────────────────┼────────────────────┘
                                    ▼
                              AI + APIs + Data
```

---

# 🧰 Main Technologies & Integrations

The workflows in this repository use or reference technologies including:

### Automation

- n8n
- Webhooks
- Schedule Triggers
- Code / JavaScript nodes
- Wait nodes
- HTTP Request nodes
- Loop / batch processing

### AI

- OpenAI
- Google Gemini
- Groq
- OpenRouter
- DeepSeek
- AI Agents

### Communication

- Email
- WhatsApp / Meta Graph API
- Twilio
- Telegram

### Data

- Google Sheets
- JSON
- HTTP APIs

### AI Media

- Kie.AI
- Veo
- Nano Banana
- Sora

---

# 🔐 Security & Configuration

These workflow exports may contain references to credentials, API endpoints, spreadsheet IDs, webhook paths, phone IDs, and environment variables.

Before deploying:

1. Replace placeholder values.
2. Configure your own n8n credentials.
3. Store API keys in n8n credentials or environment variables.
4. Never commit real API keys or access tokens.
5. Replace sample Google Sheet IDs.
6. Review webhook authentication.
7. Review WhatsApp and Twilio permissions.
8. Review AI API usage and costs.
9. Add rate limiting where appropriate.
10. Remove or anonymize real customer/lead information before publishing.
11. Review third-party API terms and licensing.
12. Test workflows with dummy data before production use.

---

# 🚀 Getting Started

## 1. Install / Access n8n

Use one of:

- n8n Cloud
- Self-hosted n8n
- Local n8n installation

## 2. Import a Workflow

Open n8n and import the corresponding `.json` workflow file.

## 3. Configure Credentials

Depending on the workflow, connect the required services:

- Google Sheets
- OpenAI
- Google Gemini
- OpenRouter
- Groq
- WhatsApp
- Twilio
- Telegram
- Kie.AI

## 4. Replace Placeholders

Search the workflow for values such as:

```text
YOUR_GOOGLE_SHEET_ID
YOUR_QUALIFIED_LEADS_SHEET_ID
YOUR_PHONE_NUMBER
YOUR_API_KEY
WHATSAPP_PHONE_ID
WHATSAPP_TOKEN
```

Replace them with your own configuration.

## 5. Test Before Activation

Run each workflow with test data before enabling production execution.

---

# 🎯 Repository Purpose

This repository demonstrates practical automation patterns for:

- **Lead Generation**
- **Sales Outreach**
- **AI-assisted Sales**
- **Cold Calling**
- **WhatsApp Automation**
- **Client Communication**
- **E-commerce Operations**
- **News Aggregation**
- **AI Content Generation**
- **AI UGC Video Creation**
- **Business Process Automation**

The workflows are intended as reusable building blocks that can be adapted for agency operations, client projects, internal systems, and AI-powered business processes.

---

# 👩‍💻 Author

**Arundhati Biswas**

AI Automation • n8n • Full-Stack Development • AI Agents • Web Development • Business Automation

---

## ⚠️ Disclaimer

This repository contains workflow exports and automation experiments. Some workflows may require additional configuration, credentials, API access, external services, or changes before they can be used in production.

Always test imported workflows in a controlled environment before connecting them to live customer data or production systems.
