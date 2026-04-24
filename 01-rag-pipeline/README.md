# 01 — RAG Pipeline: Document Q&A for a Scottish Food & Drink SME

## Business Problem
Staff at a Scottish craft brewery need to query internal documents — compliance policies, supplier agreements, and HR procedures — without manually searching through multiple PDFs. This project demonstrates how a RAG pipeline can enable plain English querying across a document library.

## Approach
This project implements a full RAG pipeline:

1. **Load** — reads plain text documents from the data folder
2. **Split** — chunks documents into overlapping segments to preserve context
3. **Embed** — converts chunks into vector representations using Sentence Transformers
4. **Store** — saves vectors in a local ChromaDB vector store
5. **Retrieve** — finds the most relevant chunks for a given query
6. **Generate** — passes retrieved context to Llama 3.3 via Groq to produce an answer

## Use Case
Fictional company: Highland Brew Co., Inverness. Documents covered:
- Product compliance and quality standards
- Supplier and procurement policy
- Health, safety and staff policy

## Tech Stack
- Python
- LangChain
- ChromaDB
- Groq API (Llama 3.3 70b)
- Sentence Transformers
- Google Colab

## Files
- `rag_pipeline.ipynb` — main notebook, open in Google Colab
- `data/` — source documents used by the pipeline