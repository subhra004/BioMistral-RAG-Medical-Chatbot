# 🧠 BioMistral RAG Medical Chatbot

A domain-specific medical chatbot that integrates **BioMistral** (a biomedical LLM) with **LangChain’s Retrieval-Augmented Generation (RAG)** pipeline. This project allows users to interact with medical documents (PDF/Text) conversationally and receive contextually accurate answers using powerful embeddings and vector-based retrieval.

> ⚠️ For research and educational use only. Not a substitute for professional medical consultation.

---

## 📌 Table of Contents

- [Features](#features)
- [Architecture](#architecture)



## 🚀 Features

- ✅ **BioMistral Model**: Tailored biomedical reasoning and natural language generation
- 🔍 **LangChain RAG Pipeline**: Retrieval-Augmented Generation for grounded responses
- 📁 **Document Ingestion**: Load and parse PDFs or plain text files
- 🧠 **Semantic Search with FAISS**: Fast, accurate vector similarity retrieval
- 💬 **Conversational Memory**: Maintains chat context for better continuity
- 🔗 **HuggingFace Embeddings**: Converts text into vector form for semantic understanding
- 🛠️ Easy to extend with other LLMs, APIs, or frontends

---

## 🧠 Architecture

```text
           ┌────────────┐
           │  Medical   │
           │ Documents  │
           └────┬───────┘
                │
                ▼
        ┌──────────────┐
        │ Text Splitter│
        └────┬─────────┘
             ▼
    ┌─────────────────────┐
    │ Embedding Generator │ ← HuggingFace
    └────────┬────────────┘
             ▼
        ┌────────┐
        │ FAISS  │ ← Vector Store
        └────┬───┘
             ▼
     ┌─────────────────────┐
     │ LangChain Retriever │
     └────────┬────────────┘
              ▼
        ┌─────────────┐
        │ BioMistral  │ ← LLM Model
        └────┬────────┘
             ▼
       ┌─────────────┐
       │   Chatbot   │
       └─────────────┘


