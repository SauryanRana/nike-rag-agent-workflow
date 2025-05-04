# Nike RAG Agent Workflow for n8n

This workflow uses LangChain, Pinecone, and OpenAI to answer Nike earnings questions using a RAG (Retrieval-Augmented Generation) approach.

## Features
- PDF ingestion
- Pinecone vector search
- OpenAI GPT-4o mini model
- LangChain Tools Agent

## Setup
1. Import into n8n
2. Set Pinecone and OpenAI credentials
3. Trigger via chat to ask questions like:
   - "What was Nike's revenue in Q4 2023?"

## File
- `nike-rag-workflow.json`
