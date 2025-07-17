# T5 – Multi-Document Abstractive Summarization

This folder contains the implementation and evaluation of the [T5 (Text-to-Text Transfer Transformer)](https://arxiv.org/abs/1910.10683) model for Multi-Document Summarization using the CNN/DailyMail dataset. Both `t5-base` and `t5-large` variants are used.

## ✅ Steps Implemented:
1. Dataset preparation (`CNN/Daily Mail` test split)
2. Grouping 10 documents per sample to simulate MDS
3. Inference using `t5-base` and `t5-large`
4. Evaluation with ROUGE-1, ROUGE-2, ROUGE-L

## 🚀 How to Run
1. Open `t5.ipynb` in Google Colab
2. Run all cells in order:
   - Install dependencies
   - Load and prepare dataset
   - Generate summaries using both base and large models
   - Evaluate with ROUGE
3. Summaries and metrics for both models are printed

## 📊 ROUGE Scores (Evaluated on 10 MDS samples)
### 🔹 t5-base
- **ROUGE-1:** 0.36808773776260567
- **ROUGE-2:** 0.1682702932217026
- **ROUGE-L:** 0.2922502866508864

### 🔹 t5-large
- **ROUGE-1:** 0.3666637238987361
- **ROUGE-2:** 0.15719075955622336
- **ROUGE-L:** 0.26758998668050543

## ⏱️ Avg Inference Time
- `t5-base ≈ 1.5225 sec/sample`
- `t5-large ≈ 3.1691 sec/sample`

## ⚙️ Hyperparameters
- `num_beams = 4`
- `max_length = 256`
- `min_length = 32`
- `length_penalty = 2.0`
- `early_stopping = True`

## ⚠️ Issues Encountered
- Tokenizer warning about `max_length=512` in Transformers v5 – safe to ignore for now
- Model loading and inference slower for `t5-large` due to size
- NumPy >=2.0 caused runtime errors – fixed by downgrading: `!pip install numpy<2.0`

## 📁 Folder Contents
- `t5.ipynb`: Full implementation notebook (both base and large)
- `multidoc_test.jsonl`: Preprocessed multi-document dataset (optional export)
- `requirements.txt`: Python dependencies
- `README.md`: This documentation

---
