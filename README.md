# StackOverflow Q&A Chatbot using Gemini + Text Embeddings

This notebook implements a simple chatbot that takes a user query, finds the **most semantically similar StackOverflow question**, and returns the **corresponding answer**. The project is part of the [DeepLearning.AI](https://www.deeplearning.ai) short course:  
**_Understanding and Applying Text Embeddings_**.

---

## 🔍 Project Overview

Given a user query (e.g., "How to store dataframe pandas"), the chatbot:

1. Generates an embedding using the `text-embedding-005` model.
2. Calculates cosine similarity with a database of StackOverflow Q&A embeddings.
3. Retrieves the most relevant question-answer pair.
4. Uses `gemini-2.0-flash-lite-001` on Vertex AI to generate a response using the retrieved context.

---

## 📘 What You'll Learn

- ✅ **Project setup in Google Cloud**
- ✅ Migrating from **PaLM API (text-bison)** to **Gemini API (Vertex AI)** including syntactic and semantic changes.
- ✅ Working with **stable versions** of models (`text-embedding-005`, `gemini-2.0-flash-lite-001`).
- ✅ Understanding **how Vertex AI** handles generative models.
- ✅ Common debugging tips (e.g., `utils.py` must be in the same working directory to avoid clashing with system modules).

---

## 🚀 Tech Stack

- Google Cloud Vertex AI
- Gemini Flash Lite Model (`gemini-2.0-flash-lite-001`)
- Text Embedding Model (`text-embedding-005`)
- Python (Jupyter Notebook)
- scikit-learn (for cosine similarity)

---

## ⚠️ Notes

- Be sure to keep your `utils.py` file in the **same directory** as the notebook to avoid import errors due to conflicts with preinstalled modules named `utils`.
- Gemini may return fallback responses if your prompt is too strict or your retrieved context isn't relevant. Consider using **top-k retrieval** to improve accuracy.

---

## 📁 Files

- `ChatbotAI.ipynb`: Main notebook with code.
- `so_database_app`: Q&A data with embeddings.
- `README.md`: This file.

---

## 📌 Credits

Part of the **"Understanding and Applying Text Embeddings"** course by [DeepLearning.AI](https://www.deeplearning.ai).
