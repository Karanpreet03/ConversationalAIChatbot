<div align="center">

# 🤖 First Conversational AI Agent

<img src="https://img.shields.io/badge/Built%20With-Flowise-blue?style=for-the-badge&logo=node.js&logoColor=white" />
<img src="https://img.shields.io/badge/Powered%20By-Groq-orange?style=for-the-badge&logo=lightning&logoColor=white" />
<img src="https://img.shields.io/badge/Status-Live-brightgreen?style=for-the-badge" />
<img src="https://img.shields.io/badge/License-MIT-purple?style=for-the-badge" />
<img src="https://img.shields.io/badge/Cost-Free-gold?style=for-the-badge" />

<br/>

> **A fully functional conversational AI agent built on a 100% free stack — designed for data Q&A, analytics insights, and real-world deployability.**

<br/>

---

</div>

## 📖 Table of Contents

- [🌟 Overview](#-overview)
- [🏗️ Architecture](#️-architecture)
- [✨ Features](#-features)
- [🖥️ Screenshots](#️-screenshots)
- [⚙️ Tech Stack](#️-tech-stack)
- [🚀 Getting Started](#-getting-started)
- [🔐 Security](#-security)
- [📊 Analytics & Monitoring](#-analytics--monitoring)
- [🌐 Public Deployment](#-public-deployment)
- [🗺️ Roadmap](#️-roadmap)
- [📝 Learnings](#-learnings)

---

## 🌟 Overview

This project is my **first hands-on AI agent**, built as a learning exercise to understand the core concepts behind conversational AI — before working with enterprise platforms like Microsoft Copilot Studio.

The agent is a **General Q&A data chatbot** that can:
- Answer questions about data it has been trained on
- Maintain conversation context using buffer memory
- Enforce security rules (e.g. reject confidential inputs)
- Be deployed publicly via a shareable link
- Capture user leads and feedback

> 💡 **Why this stack?** Everything used here is **completely free** — Groq for AI models, Flowise for the agent builder. Perfect for learning without any cost.

---

## 🏗️ Architecture

The agent is made up of **3 core modules** connected in Flowise:

```
┌─────────────────────────────────────────────────────────┐
│                   FLOWISE CHATFLOW                       │
│                                                          │
│   ┌──────────────┐     ┌────────────────┐               │
│   │  Groq LLM    │────▶│  Buffer Window │               │
│   │  (AI Brain)  │     │    Memory      │               │
│   └──────────────┘     └───────┬────────┘               │
│          │                     │                         │
│          └──────────┬──────────┘                         │
│                     ▼                                     │
│           ┌──────────────────┐                           │
│           │  Conversation    │                           │
│           │     Chain        │◀── System Prompt / Role   │
│           └──────────────────┘                           │
│                     │                                     │
│                     ▼                                     │
│              🌐 Public Chat UI                           │
└─────────────────────────────────────────────────────────┘
```

### Module Breakdown

| Module | Purpose | Why It Matters |
|--------|----------|----------------|
| 🧠 **Groq LLM** | The AI model (e.g. Llama, DeepSeek) | Free access to powerful open-source models |
| 💾 **Buffer Window Memory** | Remembers last N messages | Keeps responses contextually relevant without burning free credits |
| 💬 **Conversation Chain** | Orchestrates the chat flow | Applies system prompt, role, and output formatting |

---

## ✨ Features

### Core
- [x] 💬 Natural language Q&A on custom data
- [x] 🧠 Contextual memory across conversation turns
- [x] 🎭 Customizable AI persona via system prompt
- [x] 📊 Data analytics capability with role-based instructions

### User Experience
- [x] 🚀 Starter prompts for guided conversations
- [x] 🔄 Follow-up prompt suggestions after each response
- [x] ⭐ End-of-conversation feedback collection
- [x] 📋 Lead capture form for marketing use

### Security
- [x] 🔒 Blocks sharing of passwords and confidential information
- [x] 🚫 Ignores and flags sensitive data inputs
- [x] 👁️ Full interaction monitoring dashboard
- [x] 🛡️ No storage of confidential user inputs

---

## 🖥️ Screenshots

### 1. Backend Flow — The Agent Architecture
> The three-node Flowise flow: Groq LLM + Buffer Memory + Conversation Chain

<img width="667" height="449" alt="image" src="https://github.com/user-attachments/assets/dc24b635-5e91-4fad-bb7c-514cd58f8fac" />


---

### 2. Default Agent Response
> Asking the agent what it can do — out of the box response

<img width="469" height="281" alt="image" src="https://github.com/user-attachments/assets/d527b1df-0ee9-41c4-b985-7cc13c6715c8" />


---

### 3. Custom System Prompt in Action
> After adding a custom role and output format via the Conversation Chain parameters

<img width="470" height="196" alt="image" src="https://github.com/user-attachments/assets/9e851e2f-becf-4785-9380-beaedddc2e30" />


---

### 4. Data Analytics Mode
> Agent responding to data-specific questions after system prompt update

<img width="959" height="503" alt="image" src="https://github.com/user-attachments/assets/ddf93b70-49fe-47bc-af7a-b66a6532b910" />


---

### 5. Public Shareable Chat UI
> The embeddable chat widget Flowise generates for public deployment



---

### 6. Live Q&A — Toronto Stock Exchange Query
> Real question asked about TSX top-performing stocks

<img width="470" height="211" alt="image" src="https://github.com/user-attachments/assets/6598e975-b7d8-48af-85ea-d031fd293ad8" />


---

### 7. Interaction Monitoring Dashboard
> Flowise's built-in analytics showing user sessions and message logs



---

### 8. Starter Prompts Configuration
> Pre-configured prompts shown to users at the start of a chat



---

### 9. Follow-Up Prompts
> Auto-generated follow-up suggestions after each AI response



---

### 10. Lead Capture
> Form that collects user info — useful for marketing and outreach

<img width="471" height="247" alt="image" src="https://github.com/user-attachments/assets/a97e6c09-8427-4f86-a1fc-3ce68a0fa6f5" />


---

### 11 & 12. Detailed Analytics Response
> Agent providing in-depth analysis on auto insurance quote price increases



---

### 13. Security — Confidential Data Rejection
> Agent detecting a password shared in chat and refusing to process or store it

<img width="956" height="503" alt="image" src="https://github.com/user-attachments/assets/6e079919-138a-4143-a225-a76111dc62fa" />


---

## ⚙️ Tech Stack

| Tool | Role | Cost |
|------|------|------|
| [Flowise](https://flowiseai.com/) | Visual agent builder & deployment | ✅ Free (self-hosted) |
| [Groq](https://groq.com/) | LLM API (Llama 3, DeepSeek, etc.) | ✅ Free tier |
| Node.js | Runtime for Flowise | ✅ Free |
| npm | Package manager | ✅ Free |

> **Total cost to run this project: $0**

---

## 🚀 Getting Started

### Prerequisites

- Node.js v18+ installed → [Download](https://nodejs.org/)
- A free Groq API key → [Get one here](https://console.groq.com/)

### 1. Install Flowise

```bash
npm install -g flowise
```

### 2. Start Flowise

```bash
npx flowise start
```

Open your browser at: `http://localhost:3000`

### 3. Import This Chatflow

1. Download `chatflow.json` from this repo
2. In Flowise, click **Add New** → **Load Chatflow**
3. Select `chatflow.json`

### 4. Add Your Groq API Key

1. In the imported flow, click the **Groq Chat Model** node
2. Click **Connect Credential** → **Add New**
3. Paste your Groq API key
4. Click **Save**

### 5. Configure Environment Variables

Copy `.env.example` to `.env` and fill in your values:

```bash
cp .env.example .env
```

```env
# .env
GROQ_API_KEY=your_groq_api_key_here
FLOWISE_USERNAME=admin        # optional, for Flowise login
FLOWISE_PASSWORD=yourpassword # optional
```

### 6. Run and Chat!

Hit **Save Chatflow** in Flowise, then click the **Chat** button to start talking to your agent.

---

## 🔐 Security

This agent has built-in guardrails:

- **Password Detection** — If a user shares a password or secret in chat, the agent will:
  - ❌ Refuse to acknowledge or use the information
  - ⚠️ Display a warning message to the user
  - 🚫 Not store the sensitive data

- **Interaction Logging** — All conversations are logged in the Flowise dashboard so you can monitor for misuse

- **No Confidential Storage** — The agent is configured to never retain or repeat back sensitive inputs

> ⚠️ **Never commit your `.env` file or API keys to GitHub.** The `.gitignore` in this repo already excludes it.

---

## 📊 Analytics & Monitoring

Flowise provides a built-in monitoring dashboard where you can:

- 👁️ View all user sessions and message history
- 📈 Track usage volume over time
- ⭐ Collect user feedback ratings
- 📋 Export captured leads for marketing follow-up
- 🔍 Review what questions users are asking most

---

## 🌐 Public Deployment

To share your agent with others:

1. In Flowise, open your chatflow
2. Click the **Share** icon (top right)
3. Toggle **Make Public**
4. Copy the shareable link or embed code

The public UI is a clean chat widget that can be:
- Shared as a standalone link
- Embedded in a company website
- Used as an internal team tool

---

## 🗺️ Roadmap

- [ ] 📄 Add PDF document loader for knowledge base
- [ ] 📊 Connect to live data sources (Google Sheets, CSV upload)
- [ ] 🔁 Add n8n automation for scheduled monthly reports
- [ ] 🏢 Migrate concepts to Microsoft Copilot Studio
- [ ] 🌍 Multi-language support
- [ ] 📧 Email summary integration via n8n

---

## 📝 Learnings

This project was built as a personal learning exercise. Key takeaways:

1. **Agent = LLM + Memory + Tools** — the three nodes in Flowise map directly to this mental model
2. **System prompts matter enormously** — a few sentences of role definition dramatically changes output quality
3. **Memory has a cost** — on free tiers, keep the buffer window small to preserve credits
4. **Flowise concepts transfer to Copilot Studio** — nodes → actions, conversation chain → topics, credentials → connectors
5. **Security should be designed in from day one**, not added later

---

<div align="center">

**Built with curiosity 🧠 | Powered by free tools 🆓 | Shared for learning 📚**

⭐ If this helped you, consider starring the repo!

</div>
