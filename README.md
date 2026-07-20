# AI Customer Support Agent (n8n)

An automated, AI-powered customer support workflow built with **n8n**. The workflow monitors a Gmail inbox, classifies incoming emails, and—for genuine customer support requests—generates and sends grounded responses using a **Retrieval-Augmented Generation (RAG)** knowledge base.

This project was developed for the fictional company **Steel Alborz Solutions** as a portfolio demonstration of AI agent orchestration using n8n.

## Workflow

The following diagram illustrates the overall workflow of the AI Customer Support Agent.

![Customer Service Workflow](images/customer-service-flow.png)

## What It Does

1. **Gmail Trigger** – Polls the Gmail inbox every minute for new messages.
2. **Text Classifier (LLM)** – Classifies each email as either **Customer Support** or **Other**. Emails classified as **Other** are ignored.
3. **AI Agent ("Mr. Helpful")** – Answers customer support questions using a Retrieval-Augmented Generation (RAG) workflow.
4. **Supabase Vector Store + OpenAI Embeddings** – Performs semantic search over the knowledge base stored in the `documents` table.
5. **Gmail Reply** – Sends the generated response back to the customer in the original email thread.

## Tech Stack

- **n8n**
- **OpenRouter (LLM)**
- **LangChain AI Agent**
- **LangChain Text Classifier**
- **Supabase Vector Store**
- **OpenAI Embeddings**
- **Gmail**
