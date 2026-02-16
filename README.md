# 🧠 Mini RAG Chatbot (Free GenAI Project)

A fully functional Retrieval-Augmented Generation (RAG) system built using HuggingFace embeddings, ChromaDB vector database, and Groq LLM (Llama 3.1).

This project demonstrates how modern GenAI systems retrieve context from documents before generating responses — reducing hallucinations and improving factual accuracy.

---

## 🚀 Project Overview

This system allows users to:

- Upload a PDF document
- Split it into semantic chunks
- Convert chunks into embeddings
- Store embeddings in a vector database (Chroma)
- Retrieve relevant context using similarity search
- Generate grounded answers using Groq LLM

The AI answers questions strictly based on the uploaded document.

---

## 🏗️ Architecture
PDF Upload
↓
Text Extraction
↓
Chunking (Recursive Splitter)
↓
HuggingFace Embeddings
↓
Chroma Vector Database
↓
Query Embedding
↓
Similarity Search (Top-k Retrieval)
↓
Groq LLM (Llama 3.1)
↓
Final Answer

---

## 🛠️ Tech Stack

- Python
- LangChain (0.2.x)
- HuggingFace Sentence Transformers
- ChromaDB (Vector Database)
- Groq API (Llama 3.1 model)
- Google Colab

---

## 🔍 Key Concepts Implemented

- Retrieval-Augmented Generation (RAG)
- Semantic Search using Embeddings
- Cosine Similarity
- Vector Storage & Indexing
- LLM Context Grounding
- Hallucination Reduction via Retrieval

---

## 📚 How It Works

1. The PDF is uploaded and converted into text.
2. The text is split into smaller overlapping chunks.
3. Each chunk is converted into a 384-dimensional embedding vector.
4. Vectors are stored in ChromaDB.
5. When a user asks a question:
   - The question is embedded
   - Similar chunks are retrieved
   - Retrieved context is sent to Groq LLM
6. The LLM generates an answer grounded in the document.

---

## 💡 Why RAG?

Traditional LLMs:
- Answer from training data
- May hallucinate

RAG systems:
- Retrieve real document context
- Improve factual accuracy
- Are used in enterprise AI systems

---

## 🔐 API Setup (Groq)

To run this project:

1. Create a free Groq account:
   https://console.groq.com

2. Generate an API key

3. Set it in the notebook:

```python
import os
os.environ["GROQ_API_KEY"] = "your_api_key_here"
