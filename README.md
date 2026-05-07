# 🤖 Ai-Automations

> A centralized collection of AI automation projects and custom JavaScript nodes built for **n8n** — enabling smarter, AI-powered workflow automation pipelines.

---

## 📌 Overview

This repository serves as a personal library of production-ready **n8n workflow automation files** — all exported as `.json` and ready to import directly into any n8n instance. The workflows span a wide range of use cases including email automation, CRM syncing, calendar management, AI-powered content generation, data processing, and more.

Each workflow is built to be modular, reusable, and easily adaptable to fit different environments and requirements. Whether you're a developer, freelancer, or business owner looking to automate repetitive tasks using AI, this repo gives you a solid starting point.

---

## 🗂️ What's Inside

The repo contains **100+ n8n workflow JSON files**, organized by the tools and services they integrate. Here's a breakdown of the major categories:

### 📧 Email Automation
Workflows that handle intelligent email processing, sorting, responding, and forwarding using Gmail, Outlook, and IMAP.

- AI-powered email autoresponder with human approval (Yes/No gate)
- Auto-label and categorize incoming Gmail messages using OpenAI
- Analyze and sort suspicious emails using ChatGPT Vision
- Human-in-the-loop email response system via IMAP
- Gmail → Google Sheets / Google Drive sync on trigger

### 📅 Calendar & Scheduling
Workflows that bridge scheduling tools with project management and communication platforms.

- Calendly → Notion (triggered on new bookings)
- Calendly → Mautic (CRM contact creation)
- Google Calendar → Google Sheets (auto-logging events)
- Google Calendar → Slack (webhook-triggered alerts)
- Google Forms → Google Calendar (event creation from form submissions)
- Sub-workflow execution on calendar triggers

### 📊 Google Sheets Automation
Workflows for reading, writing, transforming, and exporting spreadsheet data.

- Scheduled Cron jobs for sheet automation
- Webhook-triggered sheet creation and updates
- Sheet → Telegram, Slack, Discord, and email notifications
- Sheet → Webflow CMS sync
- IMAP email data → Google Sheets logging
- Google Drive file monitoring → Sheets

### 📁 Google Drive & Docs
Workflows that automate file handling, document creation, and content extraction.

- Google Drive → Google Sheets (file-triggered automation)
- Extract content from Drive files and process with AI
- Google Docs creation via webhook
- Document monitoring with Drive tool integration

### 🤖 AI-Powered Content & Assistants
Workflows that use LLMs (DeepSeek, MistralAI, OpenAI, Anthropic) for intelligent content automation.

- Auto-categorize and tag WordPress blog posts using AI
- AI blog creation in a custom brand voice
- Automated content generator for WordPress using DeepSeek R1
- Author and publish blog posts directly from Google Sheets
- Ask questions about a PDF using AI
- Break down documents into study notes using MistralAI + Qdrant
- Build an OpenAI Assistant with Google Drive integration
- Automated fine-tuning of OpenAI models with Drive integration

### 📲 Messaging & Chatbots
- WhatsApp chatbot (first setup flow)
- Angie — Personal AI assistant with Telegram voice & text support
- Google Tasks → Telegram automation via webhook

### 📈 CRM & Lead Management
- Zoho CRM → Trello (card creation on CRM trigger)
- Facebook Lead Ads → Sticky Note (lead capture automation)
- Typeform → Google Sheets (form submission sync)
- Automate sales meeting prep with AI + APIFY, delivered to WhatsApp

### 📉 Analytics Automation
- Google Analytics → Code Node (scheduled reporting)
- Analytics automation via webhook (multiple variants)

### 🖼️ Utilities & Media
- Automatic background removal for images stored in Google Drive
- Binary file handling: read, move, and process in workflows
- Gmail → Google Drive (attachment storage automation)

---

## 🧰 Tech Stack & Tools Used

| Category | Tools / Platforms |
|---|---|
| Automation Platform | [n8n](https://n8n.io/) |
| AI / LLMs | OpenAI (GPT-4, GPT-4 Vision), DeepSeek R1, MistralAI |
| Google Workspace | Gmail, Google Sheets, Google Drive, Google Docs, Google Calendar, Google Analytics, Google Tasks |
| CRM & Marketing | Zoho CRM, Mautic, Facebook Lead Ads |
| Productivity | Notion, Trello, Calendly |
| Messaging | Slack, Discord, Telegram, WhatsApp |
| Web & Publishing | Webflow, WordPress |
| Vector DB | Qdrant |
| Scraping | APIFY |
| Triggers | Webhook, Cron/Schedule, Event-based |

---

## 🚀 How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/blackwolfraheel/Ai-Automations.git
```

### 2. Open Your n8n Instance

Make sure you have n8n running locally or on a cloud server. You can spin one up quickly with:

```bash
npx n8n
```

Or via Docker:

```bash
docker run -it --rm --name n8n -p 5678:5678 n8nio/n8n
```

### 3. Import a Workflow

1. Open your n8n dashboard at `http://localhost:5678`
2. Click **"+"** to create a new workflow
3. Click the **menu icon (⋮)** → **Import from File**
4. Select any `.json` file from this repo
5. Configure credentials for the services used in that workflow
6. Activate and test

---

## 📁 File Naming Convention

Most workflow files follow this naming pattern:

```
[ID]_[Service1]_[Service2]_[Action]_[TriggerType].json
```

**Example:** `0814_GoogleSheets_Gmail_Send_Triggered.json`

- `0814` → Workflow ID
- `GoogleSheets` → Primary service
- `Gmail` → Secondary service
- `Send` → Action performed
- `Triggered` → How the workflow is activated (Triggered / Webhook / Scheduled)

Some workflows use descriptive names for clarity, especially the more complex AI-driven ones:

- `AI-powered email processing autoresponder and response approval (Yes_No).json`
- `Angie, Personal AI Assistant with Telegram Voice and Text.json`

---

## ⚙️ Prerequisites

Before importing and running workflows, ensure you have the following ready:

- **n8n** (self-hosted or cloud) — [Get started](https://docs.n8n.io/getting-started/)
- **API credentials** for the services used in each workflow (Google OAuth, OpenAI API key, Slack token, etc.)
- Basic familiarity with n8n's node-based interface

---

## 🙏 Contributing

This is primarily a personal automation library, but contributions, suggestions, and improvements are welcome. Feel free to:

- Fork the repo and submit a pull request
- Open an issue for bugs or workflow ideas
- Share workflows you've built on top of these

---

## 📄 License

This project is open for personal and educational use. Please review individual tool and API terms of service when deploying workflows in production environments.

---

## 🔗 Connect

Built and maintained by [@blackwolfraheel](https://github.com/blackwolfraheel)

> *Automating the boring stuff — one workflow at a time.*

