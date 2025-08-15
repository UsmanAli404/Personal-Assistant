# 🤖 Multi-Agent AI Personal Assistant System with Supervisor

This repository contains **n8n workflows** for building a multi-agent AI system featuring:
- A **Supervisor Agent** to coordinate tasks
- **Worker Agents** for email, calendar, contacts, and content creation
- A **Custom Knowledge Base** for document-based Q&A

---
## n8n Workflow
![img](supervisor-workers-model.png)

---
## 📝 Project Overview

### **Core Components**
1. **Supervisor Agent**  
   - Orchestrates communication between worker agents  
   - Uses tools like **Serp API** for web search  
   - Delegates tasks dynamically based on user input

2. **Worker Agents**  
   - **Email Agent** – Send, read, and reply to Gmail messages  
   - **Calendar Agent** – Create and retrieve Google Calendar events  
   - **Contacts Agent** – Access, create, and update Google Contacts  
   - **Content Creator Agent** – Generate written content (research papers, blogs, social updates)

3. **Custom Knowledge Base**  
   - Integrated with **Pinecone** for document-based queries  
   - Supports PDFs, CSVs, Word docs, and more

4. **Memory Management**  
   - Implements window buffer memory for conversation context retention

---

## 🚀 Getting Started

You’ll need **n8n** installed locally or via its cloud service.

### **Prerequisites**
- **n8n Instance** – Local install or cloud account  
- **API Keys & Credentials**:
  - **OpenAI API Key** – For GPT-4o (mini) agents *(can use open-source LLMs like Qwen/Grok for free alternatives)*  
  - **Serp API Key** – For Google search integration ([get one here](https://serpapi.com))  
  - **Google Credentials** – For Gmail & Contacts APIs (requires Google Cloud project + OAuth 2.0)  
  - **Pinecone API Key** – For the knowledge base ([create a free account](https://pinecone.io))

---

## ⚙️ Installation & Setup

1. **Install n8n** – [Docs here](https://docs.n8n.io/getting-started/installation/)  
2. **Download Workflows** – From this repository  
3. **Import Workflows** – In n8n:  
   - Go to the **Workflows** page  
   - Click **⋮ Menu** → **Import**  
   - Select the JSON workflow file(s)  
4. **Configure Credentials** – Add API keys for OpenAI, Serp API, Google, and Pinecone  
5. **(Optional) Upload Knowledge Base Docs** – Use the **Update Knowledge Base** workflow to push files into Pinecone

---

## 🖥 Using the Workflows

- **Supervisor Agent**  
  - Activate the “Supervisor Agent” workflow  
  - Open the chat interface to send tasks  
  - Watch as it delegates to the relevant worker agents

- **Worker Agents**  
  - Triggered by the Supervisor Agent  
  - Can also be tested individually with mock data via the “When executed by another workflow” trigger

- **Knowledge Base Update**  
  - Use the dedicated workflow to upload documents to Pinecone  
  - Ensure Pinecone credentials and index are correctly set

---

## 🤝 Contributing
Found a bug or have an improvement?  
Fork this repo, make changes, and submit a **pull request**.

---
