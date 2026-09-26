# Hybrid RAG Document QA

A **Retrieval-Augmented Generation (RAG)** system for answering questions from PDF documents using a combination of semantic and keyword-based retrieval.

The project demonstrates how an LLM can be grounded in retrieved document context instead of relying only on its pretrained knowledge.

## 🚀 Project Overview

The system follows this pipeline:

```text
PDF Document
     ↓
Document Loading
     ↓
Text Chunking
     ↓
Hugging Face Embeddings
     ↓
Vector Database
     ↓
Hybrid Retrieval
     ├── BM25
     └── Vector Similarity
     ↓
Relevant Context
     ↓
LLM
     ↓
Answer
```

## 🧠 Key Features

* 📄 PDF document processing with `PyPDFLoader`
* ✂️ Text chunking with LangChain text splitters
* 🔢 Semantic embeddings using `all-MiniLM-L6-v2`
* 🔎 Keyword retrieval using **BM25**
* 🗄️ Vector storage and similarity search
* 🔀 Hybrid retrieval combining keyword and semantic search
* 🤖 LLM-based answer generation using `gpt-4o-mini`
* 📚 Context-grounded responses

## 🛠️ Technologies

* Python
* LangChain
* Hugging Face
* Sentence Transformers
* BM25
* Vector Database
* OpenAI API
* Jupyter Notebook / Google Colab

## ⚙️ Installation

Install the required packages:

```bash
pip install langchain
pip install langchain-community
pip install langchain-huggingface
pip install langchain-openai
pip install sentence-transformers
pip install rank-bm25
```

## 🔑 API Key

Set your OpenAI API key as an environment variable:

```python
import os

os.environ["OPENAI_API_KEY"] = "your-api-key"
```

**Never commit your real API key to GitHub.**

## ▶️ How to Run

1. Clone the repository.
2. Open the notebook in **Jupyter Notebook or Google Colab**.
3. Add your PDF document.
4. Configure your OpenAI API key.
5. Run the notebook cells sequentially.
6. Enter questions about the document.
7. The RAG pipeline retrieves relevant context and generates an answer.

## 📌 Example

**Question:**

```text
What is covered under warranty?
```

The system retrieves relevant document sections and passes the context to the LLM to generate the response.

## 🎯 Learning Objectives

This project was built to understand the core concepts behind modern **LLM and RAG systems**, including:

* Document ingestion
* Text chunking
* Embeddings
* Vector search
* Keyword search
* Hybrid retrieval
* Context augmentation
* LLM-based generation

## 🔮 Future Improvements

* Add a web-based interface using Streamlit
* Add source citations to generated answers
* Support multiple PDF documents
* Add conversation memory
* Evaluate retrieval accuracy
* Add advanced reranking

## 👨‍💻 Author

**Ahrar Amin**

Exploring **Machine Learning, Deep Learning, NLP, LLMs, and Generative AI**.
