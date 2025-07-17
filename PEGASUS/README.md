# PEGASUS – Multi-Document Abstractive Summarization

This folder contains the implementation and evaluation of the [PEGASUS](https://arxiv.org/abs/1912.08777) model (`google/pegasus-multi_news`) for Multi-Document Summarization using the CNN/DailyMail dataset.

## ✅ Steps Implemented:
1. Dataset preparation (`CNN/Daily Mail` test split)
2. Grouping 10 documents per sample to simulate MDS
3. Inference using `google/pegasus-multi_news`
4. Evaluation with ROUGE-1, ROUGE-2, ROUGE-L

## 🚀 How to Run
1. Open `pegasus.ipynb` in Google Colab
2. Run all cells in order:
   - Install dependencies
   - Load and prepare dataset
   - Generate summaries
   - Evaluate with ROUGE
3. Summaries are printed in JSON format and metrics are logged

## 📊 ROUGE Scores (Evaluated on 5 samples)
- **ROUGE-1:** 0.1748
- **ROUGE-2:** 0.0556
- **ROUGE-L:** 0.1250

## ⏱️ Avg Inference Time
- `Avg time per sample ≈ 4.32 sec`

## ⚙️ Hyperparameters
- `num_beams = 4`
- `max_length = 256`
- `min_length = 32`
- `length_penalty = 2.0`
- `early_stopping = True`

## ⚠️ Issues Encountered
- `model.decoder.embed_positions.weight` & `model.encoder.embed_positions.weight` were newly initialized – warning expected
- High inference time due to large model size and limited GPU speed (Colab T4)
- Runtime error with NumPy ≥2.0 – fixed by downgrading: `!pip install numpy<2.0`

## 📁 Folder Contents
- `pegasus.ipynb`: Full implementation notebook
- `multidoc_test.jsonl`: Preprocessed multi-document dataset (optional export)
- `requirements.txt`: Python dependencies
- `README.md`: This documentation

---
