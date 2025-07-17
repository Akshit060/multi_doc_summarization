# Hierarchical Transformer – Multi-Document Abstractive Summarization

This folder contains the implementation of a **Hierarchical Transformer model** for Multi-Document Abstractive Summarization using the CNN/DailyMail dataset. The model combines sentence-level and document-level encoding to generate summaries from grouped multi-document inputs.

## ✅ Steps Implemented:
1. CNN/DailyMail dataset preprocessing (test split)
2. Grouping 10 documents per MDS sample
3. Sentence encoding using pre-trained BERT
4. Document-level encoding via bidirectional LSTM
5. Sentence scoring and top-k extraction
6. ROUGE-based evaluation on generated summaries

## 🧠 Model Summary
- **Encoder:** BERT for sentence-level embeddings
- **Hierarchical Aggregation:** BiLSTM over sentence vectors
- **Decoder:** MLP scoring layer to rank important sentences
- **Tokenizer:** SpaCy (replaced NLTK due to persistent `punkt_tab` issue)

## 🔁 How to Run
1. Open `hierarchical_transformer.ipynb` in Google Colab
2. Run all cells sequentially:
   - Install dependencies
   - Load & preprocess dataset
   - Initialize and run the model
   - Evaluate summaries using ROUGE
3. Summaries are printed along with final average ROUGE scores

## 📊 ROUGE Scores (on 5 samples)
- **ROUGE-1:** 0.2002
- **ROUGE-2:** 0.0301
- **ROUGE-L:** 0.1153

## ⏱️ Inference Time
- Fast generation for small batch sizes (~0.02s/sample on CPU)

## 📁 Folder Contents
- `hierarchical_transformer.ipynb`: Full implementation
- `requirements.txt`: Dependency list
- `README.md`: Documentation

---
