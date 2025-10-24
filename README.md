# 🤖 N8N WhatsApp Automation Project
> JSON-based workflow automation for managing WhatsApp campaigns, messages, and logs using Google Sheets as source data.

![n8n](https://img.shields.io/badge/n8n-Workflow-orange?logo=n8n)  
![JSON](https://img.shields.io/badge/JSON-Export-blue?logo=json)  
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Data%20Source-green?logo=google-sheets)  
![GitHub](https://img.shields.io/badge/GitHub-CI%2FCD-black?logo=github)  

---

## 🌟 Project Overview
This project demonstrates a **WhatsApp messaging automation system** built in n8n, fully driven by Google Sheets data.  
The automation handles:  
- Drafting messages 📝  
- Managing receivers & senders 👥  
- Sending WhatsApp messages 📲  
- Logging message status and history 📊  

The goal is to create **reusable, scalable, and JSON-exportable workflows** that integrate Google Sheets as a backend for campaign management.

---

## 🛠 Tech Stack
- 🤖 **n8n** – Workflow orchestration and automation  
- 📄 **JSON** – Exported workflows for versioning and import  
- 🟢 **Google Sheets** – Campaign, senders, receivers, and message logs as data source  
- 💻 **GitHub** – Repository, documentation, and collaboration  

---

## 📄 Google Sheets Structure

### 1️⃣ Campaign Sheet
- Contains draft messages to be sent  
- Fields: `Campaign ID`, `Message Text`, `Scheduled Time` 📝  

### 2️⃣ Receivers Sheet
- Contains recipient information  
- Fields: `Receiver Name`, `Phone Number`, `Campaign ID` 👥  

### 3️⃣ Senders Sheet
- Contains WhatsApp sender accounts or numbers  
- Fields: `Sender Name`, `Phone Number`, `Status` 🟢  

### 4️⃣ Message Logs Sheet
- Tracks the status of sent messages  
- Fields: `Message ID`, `Receiver`, `Sender`, `Status`, `Timestamp` 📊  

---

## 📄 Workflows

### 1️⃣ WhatsApp Campaign Workflow
- **Purpose:** Sends scheduled messages to all recipients in a campaign 📲  
- **Google Sheets Integration:** Reads from Campaign, Receivers, and Senders sheets  
- **Key Nodes:** Google Sheets → HTTP Request → Function → Set  
- **Screenshot:** ![whatsapp_campaign](screenshots/whatsapp_campaign.png)  

### 2️⃣ Message Logging Workflow
- **Purpose:** Updates the Message Logs sheet with the delivery status of messages ✅  
- **Key Nodes:** HTTP Request → Google Sheets → Function  
- **Screenshot:** ![message_logs](screenshots/message_logs.png)  

### 3️⃣ Follow-up Workflow
- **Purpose:** Sends reminders or follow-ups for unsent or failed messages ⏰  
- **Key Nodes:** Google Sheets → IF → HTTP Request → Google Sheets  
- **Screenshot:** ![followup_workflow](screenshots/followup_workflow.png)  

---

## ⚡ Features
- Google Sheets as dynamic backend for campaigns 🟢  
- Multi-step workflow automation for WhatsApp messages 🔄  
- Automatic logging and status tracking 📊  
- JSON-exportable workflows for reuse in any n8n instance 📥  

---

## 📂 Repository Structure
📁 n8n_whatsapp_project/
│
├── 📂 workflows/ – JSON exports of all n8n workflows
├── 📂 screenshots/ – Workflow screenshots
├── 📂 sheets/ – Sample Google Sheets (Campaign, Receivers, Senders, Logs)
├── 📄 README.md – Project overview
└── 📘 .gitignore

yaml
Copy code

---

## 🚀 Deliverables
- 🔗 JSON workflow files for n8n  
- 📸 Screenshots showing workflow setup and execution  
- 📄 Sample Google Sheets for campaigns, receivers, senders, and logs  
- 📘 Detailed README documentation  

---

## 👤 Author
**Yashi Gupta**  
Automation & Workflow Enthusiast
