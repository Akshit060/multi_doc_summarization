# PRIMERA – Multi-Document Abstractive Summarization

This folder contains the implementation and evaluation of the [PRIMERA](https://arxiv.org/abs/2106.03819) model for Multi-Document Summarization on the CNN/DailyMail dataset.

## ✅ Steps Implemented:
1. Dataset preparation (`CNN/Daily Mail dataset`)
2. Inference using `allenai/PRIMERA`
3. Evaluation with ROUGE-1, ROUGE-2, ROUGE-L

## 🚀 How to Run
1. Open `primera.ipynb` in Google Colab
2. Upload the `multidoc_test.jsonl` dataset file when prompted
3. Run all cells in order to generate summaries and ROUGE scores

## 📊 ROUGE Scores (Evaluated on 10 samples)
- **ROUGE-1:** 0.3062
- **ROUGE-2:** 0.0898
- **ROUGE-L:** 0.1744

##Training Time
- `Avg time per sample = 0.02 sec`

##Hyperparameters
- `num_beams = 4`
- `max_length = 256`
- `min_length = 32`
- `length_penalty = 2.0`
- `early_stopping = True`

##Issues Encountered
- `fsspec` compatibility error with dataset loading – resolved by forcing downgrade to `fsspec==2023.6.0`
- `IndexError` during sample selection – handled by using `.select(range(...))` safely
- Slow inference on CPU/T4 GPU – testing restricted to 10 documents for speed

##Folder Contents
- `primera.ipynb`: Full implementation notebook
- `multidoc_test.jsonl`: Preprocessed multi-document dataset
- `requirements.txt`: All Python package dependencies
- `README.md`: This documentation

---
