# 🏥 Patient Experience Analytics Engine (RAG-based)

A cutting-edge Retrieval-Augmented Generation (RAG) system designed to transform unstructured patient feedback into actionable operational insights. This project uses a modern AI stack to bridge the gap between raw data and hospital management decision-making.

---

## 🚀 The Dual Perspective (Why this exists?)
As someone with a background in both **Engineering Logic** and **Product Strategy**, I recognized that great data (patient reviews) is useless if it doesn't solve a user's problem (hospital management efficiency). This tool doesn't just "chat"; it analyzes, cites evidence, and provides a professional UI for non-technical stakeholders.

## 🛠️ Tech Stack
* **Core Framework:** LangChain (LCEL)
* **LLM:** Google Gemini 1.5 Flash / 2.0 Flash
* **Vector Database:** ChromaDB
* **Embeddings:** Google `text-embedding-004`
* **UI/Frontend:** Gradio
* **Language:** Python 3.10+

---

## 🏗️ System Architecture



1.  **Ingestion:** Patient reviews are loaded from a CSV and chunked.
2.  **Vectorization:** Text is converted into 768-dimensional embeddings via Google’s embedding model.
3.  **Storage:** Vectors are stored in a persistent ChromaDB instance for fast semantic retrieval.
4.  **Retrieval:** When a user asks a question, the top `k` most similar reviews are retrieved.
5.  **Generation:** The Gemini LLM synthesizes the retrieved reviews into a professional, evidence-based response.

---

## ✨ Key Features
* **Evidence-Based Responses:** The system is engineered to cite specific reviews, reducing AI hallucinations.
* **Persistent Storage:** Built with a persistent vector store, so the knowledge base doesn't need to be rebuilt every time.
* **Modular Pipeline:** Uses LangChain Expression Language (LCEL) for easy swapping of models or databases.
* **Rate-Limit Resilience:** Includes error handling and automatic retry logic for API quotas.

---

## 📁 Repository Structure
```text
📂 ML Projects
 ┗ 📂 Patient-Experience-Analytics-RAG
   ┣ 📜 Chat_with_Your_Knowledge_Base.ipynb  # Main Notebook
   ┣ 📜 reviews.csv                             # Dataset
   ┗ 📜 README.md                               # Documentation
