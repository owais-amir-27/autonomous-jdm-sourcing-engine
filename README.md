# Agentic AI Auditor (Logistics Engine)

An autonomous AI auditing agent built to verify technical specifications of global mechanical parts from unstructured data and low-resolution imagery.

## 🚀 System Architecture
This project utilizes a multi-agent state machine and Vision-Language Models (VLMs) to automate quality assurance processes in automotive logistics. It replaces manual visual inspection with an autonomous, LLMOps-secured pipeline.

## 🛠 Tech Stack
* **Language:** Python 3.11, FastAPI
* **AI Orchestration:** LangGraph, Model Context Protocol (MCP)
* **Infrastructure:** Azure AI Foundry, Docker
* **Database:** Azure Cosmos DB (Vector Search)

## ⚙️ Key Features
* **Autonomous Defect Detection:** Integrates GPT-4o/Claude via MCP to scan imagery and flag anomalies (e.g., rust, mismatched serial numbers).
* **Stateful Routing:** Uses LangGraph to route failed inspections back to a human-in-the-loop validation queue.
* **Enterprise LLMOps:** All prompts and context windows are version-controlled and tracked via Azure AI Foundry to prevent model drift and hallucination.

## 🧠 Technical Challenges Solved
* **Challenge:** LLM Hallucinations on specific car part numbers.
* **Solution:** Implemented a strict Retrieval-Augmented Generation (RAG) architecture using mathematical chunking strategies and a vector database to force the agent to ground its decisions in actual manufacturer spec sheets.

## 📦 Local Setup (Optional)
```bash
git clone [https://github.com/owaisamir/agentic-ai-auditor.git](https://github.com/owaisamir/agentic-ai-auditor.git)
cd agentic-ai-auditor
pip install -r requirements.txt
python main.py
