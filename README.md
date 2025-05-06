# RAG Chatbot for Car Manual Queries
RAG chatbot powered by GPT-4o-mini for answering car manual queries using OpenAI, LangChain, and Chroma vectorstore.

This project demonstrates how to build a **Retrieval-Augmented Generation (RAG)** chatbot that can answer user questions based on technical documentation — using the HTML-based car manual of the MG ZS vehicle.

## Use Case

The assistant answers user questions like:

> "The Gasoline Particulate Filter Full warning has appeared. What does this mean and what should I do about it?"

By leveraging relevant chunks from the manual, the LLM generates precise and helpful responses, simulating a **smart assistant for technical support**.

---

## Technologies Used

- **LangChain** (core, OpenAI, Chroma, text-splitters)
- **OpenAI GPT-4o-mini** (via OpenAI API)
- **ChromaDB** for vector-based document retrieval
- **Unstructured HTML parsing** for document loading

---


---

## How It Works

1. **Load & Parse HTML Manual**: Extracts content using `UnstructuredHTMLLoader`.
2. **Text Splitting**: Divides content into overlapping chunks for better retrieval.
3. **Vectorstore Setup**: Embeds and indexes chunks using OpenAIEmbeddings + Chroma.
4. **RAG Pipeline**:
   - Fetches relevant context using a retriever
   - Passes context + question to GPT-4o-mini for final answer generation

---

## Sample Query & Answer

**Query:**
> *"The Gasoline Particulate Filter Full warning has appeared. What does this mean and what should I do about it?"*

**Answer:**
> *This warning means the gasoline particulate filter is clogged. You should drive the vehicle at a higher speed for a period of time to clean it. If the warning persists, contact a service center.*

---

## Getting Started

1. Add your **OpenAI API Key** as an environment variable:
```bash
export OPENAI_API_KEY="your-api-key"


