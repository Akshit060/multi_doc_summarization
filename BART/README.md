# BART – Multi-Document Abstractive Summarization

This folder contains the implementation and evaluation of the [BART](https://arxiv.org/abs/1910.13461) model for Multi-Document Summarization on the CNN/DailyMail dataset.

## ✅ Steps Implemented:
1. Dataset preparation (`CNN/Daily Mail dataset`)
2. Inference using `facebook/bart-large-cnn`
3. Evaluation with ROUGE-1, ROUGE-2, ROUGE-L

## 🚀 How to Run
1. Open `bart.ipynb` in Google Colab
2. Upload the `multidoc_test.jsonl` dataset file when prompted
3. Run all cells in order to generate summaries and ROUGE scores

## 📊 ROUGE Scores (Evaluated on 10 samples)
- **ROUGE-1:** 0.2428
- **ROUGE-2:** 0.1030
- **ROUGE-L:** 0.1826

## ⏱️ Training Time
- `Avg time per sample = 0.01 sec`

## 🔧 Hyperparameters
- `num_beams = 4`
- `max_length = 256`
- `min_length = 32`
- `length_penalty = 2.0`
- `early_stopping = True`

## 🐛 Issues Encountered
- `rouge_score` module missing – resolved by installing with pip
- Inference output was fast, but ROUGE values slightly lower than PRIMERA
- Padding warnings during input – normal behavior, ignored

## 📁 Folder Contents
- `bart.ipynb`: Full implementation notebook
- `multidoc_test.jsonl`: Preprocessed multi-document dataset
- `requirements.txt`: All Python package dependencies
- `README.md`: This documentation

---
