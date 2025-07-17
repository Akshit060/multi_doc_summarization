# LED (Longformer Encoder-Decoder) – Multi-Document Abstractive Summarization

This directory contains the implementation of the **Longformer Encoder-Decoder (LED)** model from AllenAI for Multi-Document Summarization (MDS). It is designed to handle **long input sequences up to 16,384 tokens**, making it ideal for summarizing concatenated clusters of multiple documents.

## ✅ Steps Implemented:
1. Dataset Preparation using `CNN/Daily Mail` test subset
2. Grouping of 10 articles into 5 multi-document clusters
3. LED tokenizer + input formatting with global attention mask
4. Summary generation using `allenai/led-base-16384`
5. ROUGE evaluation (1, 2, L)

## 🧠 Long Document Support Logic
- All 10 documents joined into a single long string
- Tokenized with truncation up to 16,384 tokens
- Global attention applied to the first token (`<s>`)
- Summary generated via beam search decoding

## 🚀 How to Run
1. Open `led_summarization.ipynb` in Google Colab
2. Run cells in order:
   - Install dependencies
   - Load and group dataset
   - Run LED model and generate summaries
   - Evaluate with ROUGE

## 📊 ROUGE Scores (Evaluated on 5 samples)
- **ROUGE-1:** 0.0721
- **ROUGE-2:** 0.0029
- **ROUGE-L:** 0.0503

## 📁 Folder Contents
- `led_summarization.ipynb`: Full notebook
- `requirements.txt`: Python dependencies
- `README.md`: This documentation file

---
