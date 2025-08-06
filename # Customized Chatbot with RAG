# Custom Chatbot with RAG Using Langchain, ChromaDB, and Gradio

## Project Overview

This project demonstrates how to build a chatbot that is customized with specific information from a source document using Retrieval-Augmented Generation (RAG). The chatbot uses **Langchain** for chaining components, **ChromaDB** for efficient vector search, and **Gradio** to provide a user-friendly interface.

---

## Tech Stack

- **Langchain** – Framework to build LLM-powered applications with RAG
- **ChromaDB** – Lightweight vector store for embedding search
- **Gradio** – UI interface for interacting with the chatbot
- **OpenAI / Hugging Face Models** – LLMs for generating responses
- **Embeddings Model** – Converts document chunks to vector representations

---

## Architecture Overview

1. **Document Ingestion**  
   A source document is loaded and pre-processed.

2. **Chunking**  
   The document is split into smaller, manageable pieces (chunks). This helps maintain context and improves retrieval accuracy.

3. **Embedding Generation**  
   Each chunk is converted into an embedding using a pre-trained embedding model (e.g., OpenAI's `text-embedding-ada-002`).

4. **Storing Embeddings**  
   Embeddings are stored in **ChromaDB**, a fast and scalable vector database.

5. **RAG (Retrieval-Augmented Generation)**  
   When a user inputs a query, the chatbot:
   - Converts the query into an embedding
   - Searches the vector store (ChromaDB) for relevant chunks
   - Feeds those chunks along with the query into an LLM to generate a response

6. **Gradio Interface**  
   A Gradio front-end wraps the pipeline, allowing users to interact with the chatbot via a web interface.

---

## Workflow Diagram

```text
User Input --> Gradio UI --> Langchain Retrieval Chain -->
  Query Embedding --> ChromaDB Search --> Relevant Chunks -->
    --> LLM Generation --> Response --> Gradio UI
