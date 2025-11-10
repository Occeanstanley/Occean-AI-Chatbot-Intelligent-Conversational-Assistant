title | subtitle | author | course | institution | date
--- | --- | --- | --- | --- | ---
Occean AI Chatbot — Intelligent Conversational Assistant | Project 2 – Deliverables 1, 2 & 3 | Stanley Occean | CS676 – Algorithms for Data Science (Fall 2025) | Pace University – Seidenberg School of CSIS | November 2025

# 🤖 Occean AI Chatbot — Intelligent Conversational Assistant

### 🌐 Live App  
👉 [**Launch on Hugging Face Spaces**](https://occeanstanley9-chatbot.hf.space/)

---

## 📘 Project Overview

The **Occean AI Chatbot** is an intelligent assistant powered by **OpenAI GPT models**, **Gradio**, and **Python**.  
It allows users to interact naturally with an AI that can understand uploaded documents, generate creative images, and export results in multiple formats.  

This chatbot integrates **Retrieval-Augmented Generation (RAG)** and **generative AI** to demonstrate an AI system capable of learning from context and reasoning interactively.  

This project fulfills **Deliverables 1, 2, and 3** for **CS676 – Algorithms for Data Science**, aligning with the “TinyTroupe Simulation” concept by showcasing an agentic AI workflow.

---

# 🧩 Deliverable 1 – Draft App

### 🎯 Objective
To design and build the **first working prototype** of the chatbot, demonstrating:
- API connectivity with OpenAI models.
- Real-time text conversation.
- Basic image generation using DALL·E.
- Simple Gradio interface.

### 🧠 Implementation Summary
At this early stage, the chatbot could:
- Accept user text prompts.
- Stream GPT model responses in real time.
- Generate AI-created images from text prompts.
- Operate in a local environment using `.env` for API key management.

### 🧰 Tools and Libraries
| Tool | Purpose |
|------|----------|
| Python 3.12 | Core language |
| Gradio | Interactive web interface |
| OpenAI API | GPT & DALL·E integration |
| dotenv | Secure API key handling |

### 🧪 Output Example
A user types:  
> “Generate a greeting message and an image of a calm beach.”

The chatbot:
- Streams back a GPT-generated text response.
- Displays an image produced by DALL·E.

---

# 🧩 Deliverable 2 – Beta Version & Technical Report

### 🎯 Objective
To extend the chatbot into a **RAG (Retrieval-Augmented Generation)** system capable of:
- Reading and indexing uploaded files (PDF, DOCX, TXT).
- Retrieving relevant text based on user queries.
- Generating context-grounded answers.

---

## 🧠 System Design

### Architecture

### Core Components
| Component | Description |
|------------|--------------|
| **Frontend (Gradio)** | Manages chat, uploads, and exports. |
| **Embedding Engine** | Converts text into dense vectors using `text-embedding-3-small`. |
| **Retriever** | Finds the most relevant document chunks using cosine similarity. |
| **Generator** | GPT-4o-mini synthesizes contextually accurate answers. |
| **Image Creator** | DALL·E generates visual output for creative prompts. |

---

## 🧮 Algorithms and Methods

### 1. Text Chunking
Documents are split into overlapping chunks to preserve context.
```python
chunks = split_text(document, chunk_size=800, overlap=120)
