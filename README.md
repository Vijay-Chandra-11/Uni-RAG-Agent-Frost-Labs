# Uni-RAG – Offline-First Secure AI Knowledge Assistant

## Domain
Open Innovation

---

## Overview

Uni-RAG is an **offline-first, secure AI knowledge assistant** that enables users to ask natural-language questions over local documents such as PDFs, presentations, notes, and images.

Unlike traditional AI tools that rely on internet connectivity and cloud data upload, Uni-RAG performs all processing **locally on the user’s device**, ensuring data privacy, security, and reliable access even in low-connectivity or restricted environments.

---

## Problem Statement

Most AI-powered knowledge tools require constant internet access and cloud-based data processing.  
This creates challenges in environments where:

- Data privacy and security are critical  
- Zero-trust policies are enforced  
- Internet connectivity is unreliable or unavailable  

As a result, users are unable to safely apply AI intelligence to their own data.

---

## Solution

Uni-RAG addresses this problem by providing a **local Retrieval-Augmented Generation (RAG) pipeline** that:

- Ingests documents locally  
- Extracts and processes text offline  
- Stores embeddings in a local vector database  
- Uses a local language model to generate context-aware answers  

All data remains on the device at all times.

---

## Key Features

- Offline document ingestion (PDFs, PPTs, DOCX, images)
- Local OCR and vision-based text extraction
- Retrieval-Augmented Generation (RAG)
- Context-aware, grounded question answering
- Zero-trust, on-device processing
- Simple and intuitive user interface
- Optional text-to-speech output

---

## Tech Stack

### AI & Machine Learning
- **LLaMA 3** (via Ollama) – Local reasoning and answer generation  
- **MiniCPM-V** – Vision-based OCR and image understanding  
- **all-MiniLM-L6-v2** – Embedding generation  

### Retrieval & Storage
- **ChromaDB** – Local vector database  
- **LangChain** – Document handling and RAG orchestration  

### Backend & Processing
- **FastAPI** – Backend API  
- **Uvicorn** – ASGI server  
- **OpenCV** – Image preprocessing and enhancement  
- **PyPDF / pdf2image / python-docx / python-pptx** – Document parsing  

### Optional Add-ons
- **Coqui TTS** – Text-to-speech output (optional)

---

## Architecture Overview

Uni-RAG follows a **three-layer architecture**:

1. **User Interface (Offline)**  
   - Document upload  
   - Query input  
   - Answer display  

2. **Offline Core (Zero-Trust Zone)**  
   - Local OCR and text extraction  
   - Embedding generation  
   - Local vector storage (ChromaDB)  
   - Local AI reasoning (LLaMA 3)  

3. **Hybrid-Ready Cloud (Future Scope)**  
   - Google Cloud – scalable deployment  
   - Google Drive API – secure document ingestion  

> Core MVP runs fully offline. Cloud services are optional and policy-gated.

---

## Google Technologies (Future / Hybrid Scope)

- **Google Cloud**
  - Scalable deployment for institutional use
  - Managed infrastructure for performance and reliability

- **Google Drive API**
  - Secure ingestion of documents from institutional Drive
  - Controlled access to shared repositories

> These are **future enhancements** and are not required for core functionality.

---

## Demo

- The MVP runs locally in offline mode.
- A demo video showcasing document ingestion and question answering is provided as part of the hackathon submission.
📽️ [Click here to watch the demo video](https://drive.google.com/file/d/1Qlr_BELhkUFR_ptauaLIR7fqGog0Df4F/view?usp=drive_link)

---

## How to Run (Local)

1. Clone the repository
2. Create and activate a Python virtual environment
3. Install required dependencies
4. Ensure Ollama is running with the required models
5. Start the FastAPI server using Uvicorn

---

## Hackathon Submission Notes

- Built as part of the **Frost Labs Hackathon**
- Domain: **Open Innovation**
- Core MVP developed during the hackathon
- Focused on feasibility, security, and real-world constraints

---

## License

This project is developed for hackathon and academic purposes.
