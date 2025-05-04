# 🏃 Nike RAG Agent Workflows (n8n + Pinecone + OpenAI)

This project contains two n8n workflows that implement a **Retrieval-Augmented Generation (RAG)** system for querying Nike’s financial data from PDF reports using Pinecone and OpenAI.

---

## 📌 Workflow Overview

### 🗂️ 1. PDF Ingestion Workflow

![PDF Ingestion Workflow](assets/pdf%20ingestion%20workflow.png)

This workflow:
- Downloads a Nike earnings PDF report
- Extracts and splits the text
- Generates OpenAI embeddings
- Stores the chunks into a **Pinecone** vector database under the `Nike` namespace

📄 **Filename**: `nike-rag-ingest.json`

---

### 💬 2. Chat-Based Q&A Workflow

![Nike RAG Agent Workflow](assets/nike%20rag%20agent%20workflow.png)

This workflow:
- Uses a **LangChain Agent** with a tool connected to the Pinecone vector store
- Accepts natural language questions (e.g., “What was Nike's gross margin in Q4 2023?”)
- Retrieves relevant context from Pinecone
- Uses **GPT-4o-mini** to generate accurate, grounded answers

📄 **Filename**: `nike-rag-chat.json`

---

## 🔧 Requirements

- n8n (self-hosted or cloud)
- OpenAI API Key
- Pinecone API Key
- Uploaded or public PDF file URL

---

## 📥 Usage

1. Import both JSON files into n8n
2. Configure OpenAI and Pinecone credentials
3. Run the **PDF ingestion** workflow to populate your vector store
4. Start asking questions via the **chat workflow**

---

