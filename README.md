# ☀️ Solar AI Lead Generation Agent

An AI-powered solar sales assistant built using **n8n**, **LLM tool calling**, **Google Solar APIs**, and **Airtable CRM**.

This project helps website visitors learn about solar, receive a personalized rooftop estimate, and become qualified leads — all through a single conversational AI agent.

---

## 🚀 Features

✅ Answers customer questions from a knowledge base
✅ Generates solar estimates based on address + electricity bill
✅ Uses Google APIs for rooftop and location analysis
✅ Calculates approximate savings and energy output
✅ Captures customer contact information
✅ Stores leads automatically in Airtable CRM
✅ Built using a **single AI agent + tools architecture**

---

## 🏗 Architecture

```text
Website Chat Widget (n8nChatUI)
            ↓
      n8n Webhook
            ↓
      Single AI Agent
            ↓
 ┌────────────────────┐
 │ Agent Tools        │
 │                    │
 │ • Knowledge Base   │
 │ • Solar Estimate   │
 │ • Lead Capture     │
 └────────────────────┘
            ↓
      Airtable CRM
```

---

## ⚙️ Workflow

### Step 1 — User starts conversation

Example:

> "I'd like a solar estimate for my home."

---

### Step 2 — AI collects required information

The agent asks for:

* Property address
* Monthly electricity bill (INR)

Example:

```json
{
  "address":"Greater Kailash, Delhi",
  "monthlyBillINR":4500
}
```

---

### Step 3 — Solar estimate tool runs

Internal workflow:

**Address**
↓
Google Geocoding API

**Coordinates**
↓
Google Solar API

**Solar Data**
↓
n8n Code Node

**Simplified Estimate**
↓
AI Response

---

### Step 4 — AI returns estimate

Example:

> Your property appears suitable for approximately 18 solar panels and may offset around 87% of your electricity usage with estimated monthly savings of ₹9,000.

---

### Step 5 — Lead capture

AI asks:

> Would you like a solar specialist to contact you?

If yes:

* Name
* Phone number

Lead automatically gets saved to Airtable.

---

## 🛠 Tech Stack

### AI & Workflow

* n8n
* n8nChatUI
* Gemini 2.5 Flash / OpenAI

### APIs

* Google Geocoding API
* Google Solar API

### Storage

* Airtable CRM

### Knowledge Base

* Vector retrieval inside n8n

---

## 📊 CRM Fields

Lead information stored:

* Name
* Phone
* Address
* Monthly Bill (INR)
* Estimated Panels
* Estimated Annual kWh
* Estimated Monthly Savings
* Estimated Offset %
* Lead Status
* Timestamp

---

## 📷 Screenshots 

### Chat Widget

(Add screenshot here)

### n8n Workflow

(Add screenshot here)

### Airtable CRM

(Add screenshot here)

---

## 🔮 Future Improvements

* WhatsApp integration
* PDF proposal generation
* Automated follow-up workflows
* Lead scoring
* Calendar scheduling
* Multi-language support

---

## 👨‍💻 Author

**Aarav Lavania**
18 | India 🇮🇳

Building AI agents, workflows, and practical automations using APIs and LLMs.
