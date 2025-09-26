# 🤖 Jervis – AI Orchestration Workflow

This n8n workflow implements an **AI supervisor agent called “Jervis”** that receives messages from Telegram and intelligently delegates tasks to specialized tools or sub-agents.  
It is designed to **assist Srinu with his specific needs**, acting as a coordinator between various services.

---

## 📋 Features
- **Telegram Chatbot**: Receives user messages and replies directly in Telegram.
- **AI Supervisor Agent**: Uses a large language model to decide which tools or agents to call in sequence.
- **Connected Tools/Agents**:
  - **Calendar Agent** – Manage or retrieve calendar information.
  - **Contacts Agent** – Look up or interact with contact details.
  - **Gmail Agent** – For email-related actions.
  - **Google Search** – Perform live web searches.
  - **Calculator** – Perform mathematical calculations.
  - **Perplexity** – Retrieve concise answers from the Perplexity API.
  - **LinkedIn Comment Agent** – Handle LinkedIn comment–related actions.

The supervisor itself **does not create content or perform tasks directly**.  
It simply orchestrates these tools and then formulates a friendly, final response.

---

## 🏗 Workflow Overview

```text
Telegram Trigger → AI Agent (Jervis)
   ├─ Calendar Agent
   ├─ Contacts Agent
   ├─ Gmail Agent
   ├─ Google Search
   ├─ Calculator
   ├─ Perplexity
   └─ LinkedIn Comment Agent
           ↓
       Telegram Response
