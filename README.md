# Task 4: General Health Query Chatbot (Open-Source Edition)

An interactive, open-source AI health chatbot built with Python and Meta-Llama-3-8B-Instruct via the Hugging Face Inference API. Features multi-layered safety guardrails, prompt engineering constraints, an emergency keyword filter, and conversational memory context.

## 📌 Project Objective
The core objective of this project is to build an intelligent, responsive digital medical assistant capable of answering general health-related questions. The application focuses on robust prompt engineering to maintain a supportive, clear persona while implementing strict defensive safety architecture to completely prevent diagnostic risks, off-limit medication dosage advice, or handling of emergency scenarios.

## 🛠️ Tech Stack & Tools
* **Programming Language:** Python 3.x
* **AI Model Architecture:** `meta-llama/Meta-Llama-3-8B-Instruct`
* **API Delivery Pipeline:** Hugging Face Serverless Inference API
* **Environment:** Google Colab
* **Core Dependencies:** `huggingface_hub`

## 🛡️ Multi-Layered Safety Guardrails
To handle sensitive medical topics safely, this repository implements a defense-in-depth safety paradigm:
1. **Local Input Validation Script (The Shield):** Instantly scans incoming string arrays for high-risk emergency terms (`chest pain`, `stroke`, `cannot breathe`). It overrides AI generation to prevent processing delays during real-life critical health emergencies.
2. **System Prompt Constraint Engineering (The Walls):** Hardcoded architectural directives forcing the LLM to deny specific milligram/dosage requests, avoid definitive diagnostic assertions, and force mandatory disclaimers at the suffix of every stream.
3. **Hyperparameter Determinism:** Hardcoded low text generation temperature (`temperature=0.4`) to enforce strict adherence to rules and mitigate hallucinatory deviations.

## 📁 Repository Structure
```text
task-4-health-chatbot/
│
├── General_Health_Chatbot.ipynb   # Complete interactive Google Colab notebook
└── README.md                      # Project documentation and engineering guide
