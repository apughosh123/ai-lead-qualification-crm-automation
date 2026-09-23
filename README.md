# 🤖 AI Lead Qualification & CRM Automation

AI-powered lead qualification and CRM automation built with **n8n, OpenRouter, Google Sheets, and Gmail**.

This workflow automatically collects lead information, uses AI to qualify and score each lead, routes leads based on their score, stores them in Google Sheets, and sends automated follow-up emails.

## 🚀 Workflow Overview

```text
Lead Qualification Form
        ↓
Data Validation & Preparation
        ↓
AI Lead Qualification
        ↓
Parse AI Qualification
        ↓
Lead Score Routing
       / \
      /   \
   Hot     Warm
  80–100   50–79
    ↓        ↓
Google     Google
Sheets     Sheets
    ↓        ↓
Hot Email  Warm Email

          < 50
            ↓
        Cold Lead
            ↓
       Google Sheets
```

## ✨ Features

* 📝 Lead submission through an n8n Form
* 🤖 AI-powered lead qualification
* 📊 Automatic lead scoring from 0–100
* 🔥 Hot / 🟡 Warm / 🔵 Cold lead routing
* 📋 Automatic CRM storage in Google Sheets
* 📧 Automated email for Hot leads
* 📧 Automated email for Warm leads
* 🔗 OpenRouter API integration
* ⚙️ End-to-end workflow automation with n8n

## 🧠 AI Qualification

The AI analyzes lead information such as:

* Job title
* Company size
* Business requirements
* Automation needs
* Urgency
* Potential business value

The AI returns structured qualification data:

```json
{
  "qualification": "Hot",
  "lead_score": 92,
  "reason": "Strong and urgent automation requirement",
  "recommended_action": "Schedule a discovery call"
}
```

## 🔀 Lead Routing Logic

| Lead Score | Qualification | Action                     |
| ---------- | ------------- | -------------------------- |
| 80–100     | 🔥 Hot        | Google Sheets + Hot Email  |
| 50–79      | 🟡 Warm       | Google Sheets + Warm Email |
| 0–49       | 🔵 Cold       | Google Sheets              |

## 🛠️ Tech Stack

* **n8n** — Workflow automation
* **OpenRouter API** — AI integration
* **OpenAI GPT-5.2** — AI model
* **Google Sheets** — CRM/data storage
* **Gmail** — Automated email communication
* **REST API** — API integration
* **n8n Forms** — Lead collection

## 📸 Workflow

### 1. Lead Qualification Form

The workflow starts by collecting lead information through an n8n form.

### 2. AI Lead Qualification

The submitted lead is analyzed by AI and receives a qualification and score.

### 3. Lead Score Routing

The workflow automatically routes leads into Hot, Warm, or Cold branches based on the lead score.

### 4. Google Sheets CRM

Lead information and AI qualification results are automatically stored in Google Sheets.

### 5. Automated Email

Hot and Warm leads automatically receive follow-up emails.

## 🧪 Test Results

The workflow was tested with different lead scenarios.

### 🔥 Hot Lead

**Lead Score:** 92
**Qualification:** Hot

```text
AI Qualification
      ↓
Score: 92
      ↓
Hot Route
      ↓
Google Sheets
      ↓
Hot Email
```

### 🟡 Warm Lead

**Lead Score:** 72
**Qualification:** Warm

```text
AI Qualification
      ↓
Score: 72
      ↓
Warm Route
      ↓
Google Sheets
      ↓
Warm Email
```

### 🔵 Cold Lead

Low-intent leads are routed to the Cold branch and stored in Google Sheets without triggering a sales email.

## 🎯 Business Use Case

This automation helps businesses reduce manual lead qualification and respond to potential customers faster.

Instead of manually reviewing every form submission, the workflow automatically:

1. Collects the lead
2. Analyzes the lead with AI
3. Assigns a score
4. Routes the lead
5. Stores the information
6. Sends the appropriate follow-up email

## 🔐 Security

API keys and credentials should **never be stored directly inside the workflow JSON or committed to GitHub**.

Use n8n Credentials or environment variables for sensitive information.

> **Important:** Remove all API keys, OAuth credentials, passwords, and private information before publishing workflow files.

## 📂 Project Structure

```text
ai-lead-qualification-crm-automation/
│
├── workflow/
│   └── lead-qualification-workflow.json
│
├── screenshots/
│   ├── lead-form.png
│   ├── ai-qualification.png
│   ├── lead-routing.png
│   ├── google-sheets.png
│   ├── hot-email.png
│   └── warm-email.png
│
└── README.md
```

## 📈 Future Improvements

* 📅 Automatic discovery-call scheduling
* 🔔 Slack/Telegram notifications for Hot leads
* 📧 Cold-lead nurture campaigns
* 🗄️ CRM integration
* 📊 Lead analytics dashboard
* 🔁 Automated follow-up sequences
* 🧠 Advanced AI lead scoring

## 👨‍💻 Author

**Apu Ghosh**

AI Automation Specialist focused on:

* n8n Workflow Automation
* AI Agents
* API Integrations
* Business Process Automation
* RAG & AI Automation Systems

---

⭐ Built with **n8n + AI + API Integrations**
