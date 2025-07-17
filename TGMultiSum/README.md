# TG-MultiSum – Graph-based Multi-Document Abstractive Summarization

This folder contains the implementation and evaluation of the **TG-MultiSum** model for Multi-Document Summarization using the CNN/DailyMail dataset.
TG-MultiSum uses an **unsupervised graph-based architecture** where sentence nodes are connected based on cosine similarity (TF-IDF), encoded using GCN layers, and scored using a neural scorer to select salient sentences for the final summary.

## ✅ Steps Implemented:
1. Dataset preparation (`CNN/Daily Mail` test split)
2. Sentence graph construction using TF-IDF + cosine similarity
3. GCN encoding of sentence nodes
4. Sentence scoring using an MLP
5. Sentence ranking and selection for summary
6. ROUGE evaluation (1, 2, L)

## 🚀 How to Run
1. Open `TGMultisum.ipynb` in Google Colab
2. Run all cells in order:
   - Install dependencies
   - Load and prepare dataset
   - Build sentence graphs
   - Run GCN forward pass
   - Score and select summary sentences
   - Evaluate with ROUGE

## 📊 ROUGE Scores (Evaluated on 5 samples)
- **ROUGE-1:** 0.177608
- **ROUGE-2:** 0.022534
- **ROUGE-L:** 0.091695

## ⚙️ Method Summary
- Sentence Tokenization (NLTK)
- TF-IDF Vectorization
- Cosine similarity thresholded graph
- GCNEncoder with 2-layer message passing
- MLP-based relevance scoring

## 📁 Folder Contents
- `TGMultisum.ipynb`: Full implementation notebook
- `requirements.txt`: Python dependencies
- `README.md`: This documentation

---
