# ai-academic-support-chatbot
A syllabus-constrained neural intent classifier with calibrated hybrid guardrails (Uysal, 2026) for engineering academic support.

# Effectiveness of AI-Powered Chatbots in Academic Support

**Author:** Eduan Cloete (Student ID: 202106179)  
**Supervisor:** Mrs. Nthabiseng Modiba  
**Institution:** Sol Plaatje University — Department of Computer Science & Information Technology  
**Client:** Academic Directorate & Faculty Board, Sol Plaatje University  

---

## 📌 Project Overview
This repository contains the implementation of a curriculum-aligned academic support assistant designed for first-year engineering mathematics (`EM115AB`). 

Unlike unconstrained commercial LLMs that hallucinate departmental rules and mathematical derivations, this system pairs a **Sentence Transformer (`all-MiniLM-L6-v2`)** and **Keras Deep MLP** with a **Calibrated Hybrid Guardrail (Uysal, 2026)** to enforce strict syllabus fidelity.

## 🚀 Key Features
- **Dense Semantic Classification:** Maps natural language queries to 9 curriculum and administrative intents.
- **Mathematical Hallucination Elimination:** Multiplies softmax probability by maximum corpus cosine similarity ($\tau = P_{\text{max}} \times S_{\text{cos}}$). At threshold $\tau^* = 0.50$, it delivers **100% in-domain coverage** and **100% out-of-domain rejection**.
- **Edge-Optimized Footprint (Tarisayi, 2024):** ~18 ms CPU inference latency and <2 KB payload per request, making it accessible under low-bandwidth mobile conditions.
- **Multi-Turn Gradio UI:** Interactive web chat interface with real-time audit logging to CSV.

## 🛠️ Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/<your-username>/ai-academic-support-chatbot.git
   cd ai-academic-support-chatbot
