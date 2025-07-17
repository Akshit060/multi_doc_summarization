# Absformer – Multi-Document Abstractive Summarization (Unsupervised)

This folder contains the implementation and evaluation of the **Absformer** model for Multi-Document Summarization using the CNN/DailyMail dataset.
Absformer is an **unsupervised extractive** MDS system that selects salient sentences from multiple documents using a scoring and ranking method based on sentence similarity and importance.

## ✅ Steps Implemented:
1. Dataset preparation (`CNN/Daily Mail` test split)
2. Grouping 10 documents per sample to simulate MDS
3. Sentence ranking and extraction using Absformer logic
4. ROUGE evaluation (1, 2, L)

## 🚀 How to Run
1. Open `absformer.ipynb` in Google Colab
2. Run all cells in order:
   - Install dependencies
   - Load and prepare dataset
   - Generate summaries with Absformer
   - Evaluate with ROUGE
3. Summaries are printed in JSON format and metrics are logged

## 📊 ROUGE Scores (Evaluated on 5 samples)
- **ROUGE-1:** 0.3403
- **ROUGE-2:** 0.1422
- **ROUGE-L:** 0.2720

## ⏱️ Avg Inference Time
- `Avg time per sample ≈ 0.01 sec` (CPU-only)
- `Avg time per training (sentence scoring + ranking): ≈ 0.012 sec/sample`

## ⚙️ Method Summary
- Sentence Tokenization (NLTK)
- TF-IDF Vectorization (sklearn)
- Cosine similarity scoring
- Top-N sentence selection

## 📁 Folder Contents
- `absformer.ipynb`: Full implementation notebook
- `multidoc_test.jsonl`: Preprocessed multi-document dataset (optional export)
- `requirements.txt`: Python dependencies
- `README.md`: This documentation

---
