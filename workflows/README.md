# 🔄 Automation Workflows

This directory contains a collection of **AI-driven automation workflows built with n8n**.

Each workflow is designed as a **self-contained unit**, combining data ingestion, processing logic, AI-based analysis and persistence or reporting steps.

The focus is on **real-world use cases**, emphasizing clarity, modularity and extensibility.

---

## 📂 Structure

Each workflow is organized in its own directory and includes:

- 📄 `workflow.json`  
  Exported n8n workflow ready to be imported.

- 🖼 `workflow.png`  
  Visual overview of the workflow for quick understanding.

- 📝 `README.md`  
  Detailed documentation explaining:
  - the use case
  - inputs and outputs
  - main processing steps
  - relevant nodes and notes

---

## 🧠 Design principles

- 🔹 **Modularity**: workflows are easy to adapt and extend.
- 🔹 **Readability**: clear structure and descriptive node naming.
- 🔹 **Practical focus**: oriented to applied automation scenarios.
- 🔹 **AI-first**: integration of NLP and LLM-based processing where relevant.

---

## ⚠️ Notes

- Credentials and API keys are managed via n8n credentials and are **not included**.
- Workflows can be executed locally using the Docker setup provided in the repository.
- Persistence layers (e.g. Google Sheets, databases) can be replaced depending on the use case.

---

Each workflow directory provides all the information needed to understand and run the automation independently.
