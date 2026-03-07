# RAG Document Question Answering System
A simple GenAI project demonstrating Retrieval-Augmented Generation using FAISS and Llama 3.3.

# Retrieval-Augmented Generation (RAG) Document Question Answering System

## Overview

This project demonstrates a simple **Retrieval-Augmented Generation (RAG) pipeline** that answers user questions based on a document.

Instead of sending the entire document to the LLM, the system retrieves the **most relevant chunks using vector search** and provides them as context to the language model.

This improves:

* accuracy
* efficiency
* response relevance
* reduces hallucinations

---

## How the System Works

1. **Load Document**
   A text document is used as the knowledge source.

2. **Chunking**
   The document is divided into smaller chunks to preserve context and improve retrieval.

3. **Embedding Creation**
   Text chunks are converted into vectors using **TF-IDF embeddings**.

4. **Vector Database (FAISS)**
   All embeddings are stored in a **FAISS index** for efficient similarity search.

5. **Query Processing**
   When a user asks a question, it is converted into an embedding.

6. **Similarity Search**
   FAISS retrieves the **top relevant chunks** based on cosine similarity.

7. **LLM Response Generation**
   The retrieved context is sent to a **Large Language Model (Llama 3.3 via Groq API)** to generate the final answer.

---

## Technologies Used

* Python
* FAISS (Vector Similarity Search)
* Scikit-learn (TF-IDF Embeddings)
* Groq API
* Llama 3.3 LLM
* NumPy
* Jupyter Notebook

---

## Project Structure

```
rag-project/
│
├── RAG_pipeline.ipynb
├── requirements.txt
├── README.md
└── legal_sample_document.txt
```

---

## Installation

Clone the repository:

```
git clone https://github.com/yourusername/rag-project.git
cd rag-project
```

Install required libraries:

```
pip install -r requirements.txt
```

---

## Usage

1. Open the notebook:

```
jupyter notebook
```

2. Run all cells in **RAG_pipeline.ipynb**

3. Ask a question related to the document.

Example:

```
Query:
What is the notice period for employee termination?
```

The system retrieves the most relevant document chunks and generates an answer using the LLM.

---

## Example Output

```
The notice period for employee termination is 30 days unless a serious breach occurs such as fraud or misconduct.
```

---

## Key Concepts Demonstrated

* Retrieval-Augmented Generation (RAG)
* Document Chunking
* Vector Embeddings
* Similarity Search
* FAISS Indexing
* LLM Prompt Engineering

---

## Future Improvements

* Use **Sentence Transformers for semantic embeddings**
* Add **Hybrid Search (Keyword + Vector Search)**
* Implement **Re-ranking models**
* Build a **Streamlit interface**
* Support multiple documents

---

## Author

Namrata Dubey

Data Science & GenAI Learner
