# COMP8460 Final Project — Drug AI Assistant (Streamlit + RAG + Tools)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=LangChain)
![Ollama](https://img.shields.io/badge/Ollama-Local%20LLM-black?style=for-the-badge)

An interactive **Streamlit web app** and **CLI assistant** that answers questions about **drug reviews**.

## 🎥 Project Demo

<div align="center">
  <video src="./video/demo_video.mp4" controls="controls" muted="muted" style="max-width: 100%;">
  </video>
  <p><i>Watch the Drug AI Assistant in action</i></p>
</div>

---

## 📖 Overview

This project implements a local AI agent capable of answering questions based on medical data using:

- A **RAG (Retrieval-Augmented Generation) pipeline** over a local ChromaDB vector store built from `drugsComTest_raw.csv`.
- A set of **tool-calling agents** for:
  - 📷 **OCR** on uploaded medicine images (EasyOCR)
  - 🔍 **Searching reviews** and side effects (RAG over ChromaDB)
  - 📊 **Basic analytics** like average rating, review counts, and Top-5 lists (Pandas)
- A local **Ollama** LLM (e.g., `gemma3:4b`) and **HuggingFace** sentence embeddings.

You can interact with the project via:
- `app.py` → **Streamlit UI** (Recommended for demos)
- `main.py` → **Backend / CLI assistant** (For debugging/experimentation)

---

## 📂 Project Structure

```text
.
├─ app.py                 # Streamlit web application (UI and glue)
├─ main.py                # Backend logic, tools, RAG, OCR, and CLI
├─ drugsComTest_raw.csv   # Dataset of drug reviews
├─ video/                 # Demo assets
│  └─ demo_video.mp4
├─ chroma_db/             # ChromaDB collection (auto-created on first run)
├─ requirements.txt       # Python dependencies
└─ README.md              # This file
