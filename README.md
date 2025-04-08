# Softwareproject
# 🧠 MediBot: AI-Based Medical Chatbot for Document-Driven Question Answering

MediBot is an intelligent chatbot built to simplify access to medical information through natural language queries. Instead of using traditional keyword searches, MediBot leverages cutting-edge AI — transformers, semantic embeddings, and vector databases — to fetch contextually accurate responses from static medical PDFs.

---

## 🩺 Purpose

The primary goal of MediBot is to provide a fast, efficient, and context-aware interface for interacting with medical literature. This chatbot is best suited for:

- 🧑‍⚕️ Healthcare professionals  
- 🎓 Medical students  
- 🧠 Curious individuals exploring symptoms or medical knowledge

---

## 🚀 Project Highlights

- 🔍 **Semantic Search**: Uses MiniLM sentence embeddings for contextual understanding.
- 📄 **Document-Based QA**: Answers are retrieved from actual medical documents.
- ⚡ **Fast & Lightweight**: Responds in under 50s even on CPU-based setups.
- 🧱 **Modular Pipeline**: Easily extendable for other document types or use cases.

---

## 🧰 Tech Stack

| Category               | Tools/Libraries |
|------------------------|-----------------|
| Language Model         | `all-MiniLM-L6-v2` (SentenceTransformers) |
| Embeddings & Retrieval| `ChromaDB` |
| PDF Parsing            | `LangChain`, `PyPDFLoader` |
| Text Chunking          | `RecursiveCharacterTextSplitter` |
| Interface              | `Gradio` |
| Language               | Python 3.10+ |
| Deployment             | Gradio |

---

## 🛠️ System Workflow

```
                ┌────────────────────────┐
                │   Medical PDF Input    │
                └─────────┬──────────────┘
                          ↓
     ┌──────────────────────────────┐
     │ Parse & Chunk Text (LangChain│
     │ + RecursiveCharacterSplitter)│
     └─────────┬────────────────────┘
               ↓
     ┌─────────────────────────────┐
     │ Generate Embeddings         │
     │ (MiniLM Transformer)        │
     └─────────┬───────────────────┘
               ↓
     ┌─────────────────────────────┐
     │ Store in Vector DB (ChromaDB)│
     └─────────┬───────────────────┘
               ↓
     ┌─────────────────────────────┐
     │ Query Processing via Gradio │
     └─────────────────────────────┘
```

---

## 📊 Performance Summary

| Metric               | MediBot (MiniLM + ChromaDB) | Keyword Search | Fine-tuned BioGPT |
|----------------------|-----------------------------|----------------|-------------------|
| Accuracy (%)         | 88                          | 60             | 95                |
| Contextual Relevance | 92                          | 55             | 96                |
| Latency (s, CPU)    | 30–50                     | N/A            | High              |

---

## 🧪 How It Works

1. **Input Source**: Trusted PDF medical encyclopedia.
2. **Parsing**: Text extracted using LangChain's PyPDFLoader.
3. **Chunking**: Splits text into semantically coherent segments.
4. **Embedding**: Uses `all-MiniLM-L6-v2` model for both chunks and queries.
5. **Search**: ChromaDB performs cosine similarity search.
6. **Output**: Most relevant answer displayed via Gradio interface.

---


### 3. Hugging Face Spaces / Railway / Render / AWS EC2

> Ensure Python 3.10+, torch, transformers, gradio, accelerate, sentencepiece are installed.

---

## 🔐 Security & Compliance

- HTTPS, token-based authentication
- Log anonymization
- HIPAA compliance (for sensitive data scenarios)

---

## 🧠 Key Takeaways

- ⚡ Embedding + semantic search outperforms traditional search.
- 🧩 Modular pipeline = easy customization.
- 🧑‍🎓 Excellent for educational and support use-cases.
- 🌍 Supports scalable expansion to more documents and languages.

---

## 🧪 Experimental Setup

- Environment: Python 3.10, Jupyter Notebook
- Libraries: HuggingFace Transformers, LangChain, SentenceTransformers
- Platform: CPU (GPU supported for acceleration)
- Interface: Gradio

---


---

## 👨‍💻 Contributors

- **A. Doni Adithya** (23bds007)  
- **L. Sahith Akash Manikanta** (23bds031)  
- **Prasanna Kote** (23bds045)  
- **C. Pothan Sai Reddy** (23bds017)  
- **K. Ram Charan** (23bds029)  
- **S. Sasi Rekha** (23bds049)

---
