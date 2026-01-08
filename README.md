# n8n RAG Chatbot – Company Knowledge Base Demo

![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-blue?logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o--mini-green?logo=openai&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Vector%20Store-brightgreen?logo=supabase&logoColor=white)

**An AI-powered Retrieval-Augmented Generation (RAG) chatbot** built with **n8n** that delivers accurate, cited answers from company documents — with **zero hallucinations**.

This demo uses the iconic **Valve Employee Handbook** PDF as the knowledge source, showcasing a real-world company policy and culture knowledge base.

## Demo Highlights

- Answers pulled directly from the document with citations  
- Strict grounding: out-of-scope questions return "This information is not in the Valve Employee Handbook"  
- Multi-turn conversations thanks to built-in memory  
- Clean, annotated workflow for easy understanding  

### Sample Interaction

**User**: What is Valve's vacation policy?  
**Bot**: There is no formal vacation policy. Employees can take time off when they need it, as long as they coordinate with their team.

**User** (follow-up): How does that work with project choice?  
**Bot**: Project choice and time off are both self-managed. The key is open communication to ensure work continues smoothly.

**User**: Who is the CEO of Valve?  
**Bot**: This information is not in the Valve Employee Handbook.

## Workflow Overview

![Full Workflow with Annotations](images/workflow-overview.png)

## Features

- PDF ingestion with intelligent chunking (1000 chars + 200 overlap)  
- OpenAI embeddings stored in Supabase vector database  
- Simple Memory for natural multi-turn conversations  
- Strict system prompt to eliminate hallucinations  
- Ready for Telegram, Slack, or webhook integration  

## How to Run Locally

1. Import `rag-chatbot-valve-demo.json` into your n8n instance  
2. Set up credentials:  
   - OpenAI API key  
   - Supabase Vector Store connection  
3. Run the workflow manually once with the included `valve-handbook.pdf` to index the document  
4. Start chatting via webhook or connect to your preferred messaging platform  

## Files in This Repository

- `rag-chatbot-valve-demo.json` – Combined ingestion + chat workflow  
- `Valve_Handbook_LowRes.pdf` – Demo knowledge source (Valve Employee Handbook)  
- `/screenshots/` – Workflow overview and chat examples  

## Customization for Your Use Case

Simply swap the PDF for any company documents:
- Employee handbooks & HR policies  
- Product manuals & technical docs  
- Legal contracts & compliance guides  
- Internal knowledge bases  

Easy extensions:
- Multi-document support  
- Hybrid search  
- Voice input/output  
- CRM or Slack integrations  

**Perfect for HR onboarding, internal support bots, or knowledge management tools.**

Built as a freelance portfolio project — contact me for custom RAG solutions tailored to your business!

---
*Live demo available on request • Fully adaptable to your company's needs*
