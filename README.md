***AI Customer Support Agent (n8n)***

An automated, AI-powered customer support workflow built in n8n. It watches a Gmail inbox, classifies incoming email
and for genuine support questions — drafts and sends a grounded reply using a Retrieval-Augmented Generation (RAG) knowledge base.
Built for a fictional company, Steel Alborz Solutions, as a portfolio demonstration of AI agent orchestration in n8n.

***What it does***

1. Gmail Trigger – polls the inbox every minute.
2. Text Classifier (LLM) – sorts email into Customer Support or Other (Other → ignored).
3. AI Agent ("Mr. Helpful") – answers support questions using a knowledge-base tool.
4. Supabase Vector Store + OpenAI Embeddings – semantic search over a documents table (RAG).
5. Gmail Reply – sends the answer back in the original thread.
# Tech stack: n8n · OpenRouter (LLM) · LangChain Text Classifier & AI Agent · Supabase Vector Store · OpenAI Embeddings · Gmail.

The full file also includes an architecture diagram, a setup guide (import + credentials + Supabase documents/match_documents setup), and an improvements section.
