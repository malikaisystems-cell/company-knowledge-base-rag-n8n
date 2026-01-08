# n8n RAG Chatbot – Company Knowledge Base Demo
![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-blue?logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o--mini-green?logo=openai&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Vector%20Store-brightgreen?logo=supabase&logoColor=white)
An AI-powered Retrieval-Augmented Generation (RAG) chatbot built with n8n that answers questions from company documents with accurate, cited responses and zero hallucinations.
This demo uses the famous Valve Employee Handbook PDF as the knowledge source – a perfect example of a company policy/manual knowledge base.
Demo Highlights

* Precise answers pulled directly from the document
* Strict grounding: Out-of-scope questions → "This information is not in the Valve Employee Handbook"
* Multi-turn conversation support (memory included)
* Clean, production-style workflow with annotations

## Sample Interaction
User: What is Valve's vacation policy?
Bot: There is no formal vacation policy – employees can take time off when needed, as long as they coordinate with their team.
User (follow-up): How does that work with project choice?
Bot: Since there are no managers, project choice and time off are self-managed. The key is communication and ensuring work continues smoothly.
User: Who is the CEO of Valve?
Bot: This information is not in the Valve Employee Handbook.
Workflow Overview
Full Workflow with Sticky Notes
Features

## PDF ingestion & intelligent chunking (1000 chars + overlap)
OpenAI embeddings + Supabase vector store
Simple Memory for natural multi-turn conversations
Strict system prompt to prevent hallucinations
Ready for Telegram, Slack, or webhook integration

## How to Run Locally

Import rag-chatbot-valve-demo.json into your n8n instance
Set up credentials:
OpenAI API key
Supabase Vector Store

Run the workflow manually once with the included valve-handbook.pdf to index
Start chatting via webhook or connect to Telegram/Slack

## Files in This Repo

rag-chatbot-valve-demo.json – Main workflow (ingestion + chat)
valve-handbook.pdf – Demo knowledge source
/screenshots/ – Workflow and chat examples

## Customization for Clients
Swap the PDF for any company documents:

* Employee handbooks
* Product manuals
* Legal contracts
* Internal policies

Add features like:

* Hybrid search
* Voice input/output
* Multi-document support

Perfect for HR onboarding, internal support bots, or knowledge management tools.
Built as a freelance portfolio project – contact me for custom RAG solutions!
