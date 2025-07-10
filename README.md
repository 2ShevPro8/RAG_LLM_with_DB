## Overview

This project implements a **Retrieval-Augmented Generation (RAG) pipeline** combining:

* **Transformers (Llama-3.2-3B-Instruct)**
  Used as the **language model** to generate concise answers based on retrieved context.

* **Sentence Embedding Model (all-MiniLM-L6-v2)**
  Used to **embed documents and queries** for similarity search.

* **ChromaDB (Vector Store)**
  Stores **document embeddings** for fast retrieval based on semantic similarity.

* **LangChain**
  Integrates the embedding model, vector store, and LLM into a **unified RAG pipeline**.

* **SQLite (Relational Database)**
  Saves **chat history (questions and answers)** for tracking model outputs over time.

---

## Key Components

| Component                    | Usage                                                                                  |
| ---------------------------- | -------------------------------------------------------------------------------------- |
| **HuggingFace Transformers** | Loads and runs the Llama-3.2-3B-Instruct model for generation.                         |
| **HuggingFace Embeddings**   | Encodes text into embeddings for semantic search.                                      |
| **ChromaDB**                 | Stores and retrieves document embeddings efficiently.                                  |
| **LangChain**                | Provides RAG orchestration and retrieval wrapper.                                      |
| **SQLite**                   | Stores question-answer pairs in a persistent table (`chat_history`).                   |
| **Evaluate + ROUGE**         | Calculates **Exact Match, Semantic Similarity, and ROUGE-L** for automated evaluation. |

---



