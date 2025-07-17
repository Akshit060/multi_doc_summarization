# Topic-Guided Summarization using BART – Multi-Document Abstractive Summarization

This directory contains the implementation of a **topic-guided BART-based model** for Multi-Document Summarization (MDS). It leverages extracted keywords from the document collection to guide the summarization model toward more **focused and relevant summaries**, simulating external knowledge incorporation.

## ✅ Steps Implemented:
1. Dataset Preparation using `CNN/Daily Mail` test subset
2. Grouping of 10 articles into 5 multi-document clusters
3. Keyword extraction from source documents (unsupervised)
4. Prompt-guided summarization using BART (`facebook/bart-large-cnn`)
5. ROUGE evaluation (1, 2, L)

## 🧠 External Knowledge Logic
- Extracted top-`k` keywords using TF-IDF
- Injected into prompt: `"summarize with focus on: <keywords> <docs>"`
- Summary generated using guided prompt with BART

## 🚀 How to Run
1. Open `topic_guided_summarization.ipynb` in Google Colab
2. Run cells in order:
   - Install dependencies
   - Load and preprocess dataset
   - Extract keywords and generate summaries
   - Evaluate with ROUGE

## 📊 ROUGE Scores (Evaluated on 5 samples)
- **ROUGE-1:** 0.1236
- **ROUGE-2:** 0.0445
- **ROUGE-L:** 0.0844

## 📁 Folder Contents
- `topic_guided_summarization.ipynb`: Full notebook
- `requirements.txt`: Python dependencies
- `README.md`: This documentation file

---
