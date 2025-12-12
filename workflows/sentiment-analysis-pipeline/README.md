# 😊 Sentiment Analysis Pipeline

![Workflow overview](workflow.png)

This workflow implements an **end-to-end sentiment and aspect-based analysis pipeline** using **n8n** and an **LLM-based sentiment model**.

It is designed to process user comments, extract relevant aspects, analyze sentiment, and persist structured results for further analysis.

---

## 🧩 Workflow overview

The pipeline follows these main steps:

1. 📥 **Data ingestion**  
   Comments are retrieved via an HTTP request (e.g. API endpoint).

2. ✂️ **Comment separation**  
   Incoming payloads are split so that each comment is processed independently.

3. 🏷️ **Aspect definition**  
   Relevant aspects are defined per comment to enable aspect-based sentiment analysis.

4. 🤖 **Sentiment analysis with AI**  
   Each comment and its aspects are sent to an LLM to obtain sentiment information.

5. 🧹 **Field extraction & formatting**  
   The AI response is parsed and formatted to keep only relevant fields.

6. 🔀 **Merge results**  
   Original comment data and sentiment analysis results are merged into a single structure.

7. 💾 **Persistence**  
   Final structured data (comments, aspects and sentiments) is stored in Google Sheets.

---

## 📥 Inputs

- Text comments
- Optional metadata (source, date, product, etc.)
- Predefined aspects per comment

---

## 📤 Outputs

- Sentiment label (e.g. positive / neutral / negative)
- Aspect-level sentiment information
- Structured records ready for analysis or reporting

---

## 🔧 Nodes used

- 🌐 HTTP Request
- ✂️ Split / Item processing
- ✏️ Set / Manual nodes
- 🤖 LLM (sentiment analysis)
- 🔀 Merge
- 📊 Google Sheets (append rows)

---

## 🧠 Notes

- The workflow is designed to be **modular** and easy to extend.
- Aspect definition can be adapted depending on the domain.
- The persistence layer can be replaced with a database or data warehouse.
- Credentials and API keys are managed via n8n credentials (not included in this repo).

---

## ⚠️ Disclaimer

This workflow is provided for **demonstration and educational purposes**.  
No sensitive data or credentials are included.
