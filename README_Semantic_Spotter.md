
# 🧠 Semantic Spotter: An LLM-Powered RAG System for Insurance

> A cutting-edge Retrieval Augmented Generation (RAG) project designed to accurately answer queries from complex insurance policy documents using advanced Large Language Model techniques. Build a smart system that can search through documents and give clear, helpful answers to questions. It uses LlamaIndex to power the search. It combines two powerful tools:
• LlamaIndex (to search and find relevant information in documents)
• GPT-3.5-turbo/GPT 4 (to improve the answers and make them more user-friendly).

---

## 📌 Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Setup Instructions](#setup-instructions)
- [How It Works](#how-it-works)
- [Conclusion]

---

## 🧾 Overview
**Semantic Spotter** is an intelligent document question-answering system built using **LlamaIndex** and **OpenAI's LLMs**. The system leverages document chunking, vector-based similarity search, and a conversational interface to respond to natural language questions using content extracted from insurance policy documents (e.g., HDFC policy PDFs).

---

## 🛠️ Tech Stack

| Component              | Technology |
|------------------------|------------|
| RAG Framework          | LlamaIndex |
| Vector Embeddings      | SentenceTransformers (MiniLM-L-2-v2) |
| LLM API                | OpenAI GPT |
| Caching                | DiskCache |
| Programming Language   | Python |
| UI & Development       | Jupyter Notebook |
| Document Source        | HDFC Life Insurance PDFs |

---

## 🔍 Features

- ✅ Document ingestion and chunking
- ✅ Query understanding and vector similarity matching
- ✅ Response generation using OpenAI’s LLM
- ✅ Citation support with page numbers and document titles
- ✅ Custom LLM nodes and evaluation pipeline
- ✅ Caching to reduce API calls and improve speed
- ✅ Feedback capture for performance monitoring

---

## 🚀 Setup Instructions

1. **Install Required Libraries**
   ```bash
   pip install llama-index openai sentence-transformers diskcache
   ```

2. **Mount Google Drive** (if using Colab)
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

3. **Set OpenAI Key**
   ```python
   import os
   os.environ["OPENAI_API_KEY"] = "your-openai-key"
   ```

4. **Run the Cells Sequentially**
   - Load documents
   - Initialize the index
   - Run `initialize_conv()` to start chat interface

5. **Batch Test Using `testing_pipeline()`**
   - Add questions to a list
   - Run pipeline for automated testing and evaluation

---

## 🧠 How It Works

1. **Document Parsing**  
   PDF documents are read and split into manageable text chunks using recursive text splitting.

2. **Vectorization**  
   Each chunk is converted into a dense vector using Sentence Transformers.

3. **Caching**  
   Queries and responses are stored using DiskCache for fast retrieval.

4. **Query Processing**  
   Input queries are vectorized, and top-k similar chunks are retrieved.

5. **LLM Response Generation**  
   Retrieved context is passed to OpenAI's GPT to generate answers along with source references.

6. **Evaluation & Feedback**  
   Users can provide feedback on responses, helping to improve future accuracy.

---

## 📊 Conclusion
This project built an efficient query engine that quickly finds relevant information from
documents and combines it with the conversational power of GPT-3.5-turbo/GPT 4 with
Llamaindex framework. It not only retrieves useful information but also improves the
responses and adapts based on user feedback. The system can be further developed and
applied to other areas like law, education, or finance, making it versatile beyond just
insurance.


