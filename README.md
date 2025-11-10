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

---

## 🌟 Deliverable 3 – Final Container-Ready App  

### 🎯 Objective  
Deliver a **fully functional, production-ready chatbot** deployed on **Hugging Face Spaces**, complete with end-to-end integration, reliability testing, and documentation.  
This deliverable demonstrates that the system is scalable, maintainable, and accessible to both technical and non-technical users.

---

### 🚀 Deployment Summary  

| Item | Description |
|------|--------------|
| **Platform** | Hugging Face Spaces |
| **App URL** | [https://occeanstanley9-chatbot.hf.space/](https://occeanstanley9-chatbot.hf.space/) |
| **Runtime Environment** | Python 3.12   •  Gradio 4.17.0 |
| **Secrets Management** | `OPENAI_API_KEY` (Hugging Face variable) |
| **Repository** | [GitHub – Occeanstanley/chatbot](https://github.com/Occeanstanley/chatbot) |

---

### 🧰 Final Tech Stack  

| Tool | Purpose |
|------|----------|
| **Python** | Core backend and logic |
| **Gradio** | Web-based interactive UI |
| **OpenAI API** | GPT-4o-mini for chat, text-embedding-3-small for RAG, DALL·E for images |
| **pandas / fpdf2 / python-docx** | File export (TXT, PDF, DOCX, CSV, JSON) |
| **scikit-learn** | Similarity search using cosine distance |
| **dotenv** | Secure key storage and environment management |

---

### 🧪 Testing and Validation  

| Test Case | Result | Notes |
|------------|---------|-------|
| **Chat Interaction** | ✅ Passed | Smooth streaming responses, low latency (≈ 1–3 s) |
| **Document Retrieval (RAG)** | ✅ Passed | Context-aware answers verified on sample files |
| **Image Generation** | ✅ Passed | DALL·E returns relevant, high-quality visuals |
| **File Exports** | ✅ Passed | All formats download successfully |
| **Concurrent Users** | ✅ Passed | Stable across multiple sessions on Hugging Face |

---

### 💡 Key Achievements  

- Integrated **text, document, and image** generation into one unified Gradio application.  
- Deployed a stable cloud version accessible to the public.  
- Implemented Retrieval-Augmented Generation for context-driven answers.  
- Designed a clean and responsive UI with dark mode.  
- Enabled multi-format export capabilities for data analysis and record keeping.  

---

### 🧩 Challenges and Solutions  

| Challenge | Solution |
|------------|-----------|
| **Handling large documents** | Implemented chunking and batch embedding for RAG. |
| **API rate limits** | Added retry logic and batched requests. |
| **Formatting inconsistencies** | Used `fpdf2` and `python-docx` for robust exports. |
| **Maintaining context** | Leveraged cosine similarity to anchor relevant sections. |
| **Cloud deployment setup** | Configured Gradio `app.py` to auto-launch in Spaces runtime. |

---

### 🧭 Future Enhancements  

- 🔹 Integrate **TinyTroupe personas** for AI role-based simulations.  
- 🔹 Enable **multi-file cross-reference** retrieval.  
- 🔹 Add **memory persistence** to maintain chat history across sessions.  
- 🔹 Develop a **feedback dashboard** to analyze user queries and model accuracy.  
- 🔹 Integrate **speech input/output** for voice-enabled conversation.  

---

### 📈 Summary and Outcome  

The **Occean AI Chatbot** is now a fully deployed, AI-driven conversational assistant that combines language understanding, document context, and visual generation.  
It stands as a proof of concept for agentic AI systems and paves the way for multi-persona TinyTroupe integration in future research projects.

---

### 👨‍💻 Author  

**Stanley Occean**  
M.S. Data Science Candidate – Pace University  
📎 [LinkedIn](https://linkedin.com/in/stanleyoccean)  |  [GitHub](https://github.com/Occeanstanley)

---

### 📚 References  

- OpenAI API Documentation  
- Gradio 4.17 User Guide  
- Pace University CS676 Course Repository  
- Microsoft TinyTroupe Framework (2025)  
- Hugging Face Spaces Deployment Docs  

---

