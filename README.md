# 🧠 Developer's Assistant (CrewAI + Ollama) 🚀

This project builds a dynamic, intelligent developer assistant powered by **CrewAI**, **FAISS**, and **Ollama** that understands user queries, retrieves the most appropriate API endpoint from Sikka’s documentation, and auto-generates full-stack code (Flask + React.js) tailored to the use case.

---

## 📌 Table of Contents

- [Overview](#overview)
- [How It Works](#how-it-works)
- [Tech Stack](#tech-stack)

---

## ✅ Overview

The assistant:
- Parses user queries (e.g., "Create a new patient record"),
- Retrieves the most relevant Sikka API from a **FAISS** vector store,
- Passes this API info to a **code-generation agent**,
- Dynamically generates backend and frontend code using **Ollama's Mistral model**,
- Returns production-ready Python (Flask) + React.js code without templates.

---

## ⚙️ How It Works

The workflow involves 2 intelligent agents using **CrewAI**:
1. **Retriever Agent**: Retrieves the most relevant API from a FAISS vector DB using similarity search.
2. **Code Generator Agent**: Uses `ollama/mistral` to generate executable backend and frontend code with explanations, based on the retrieved API and user query.

These agents are orchestrated via **CrewAI** and communicate using tasks and tools.

---

## 🛠 Tech Stack

| Tool          | Purpose                         |
|---------------|---------------------------------|
| Python        | Core programming                |
| CrewAI        | Agent Orchestration Framework   |
| Ollama (Mistral) | Local LLM for code generation |
| FAISS         | Vector similarity search        |
| Flask         | Backend (auto-generated)        |
| React.js      | Frontend (auto-generated)       |
| LangChain     | Document embedding + chunking   |
| pandas        | API CSV processing              |

---
