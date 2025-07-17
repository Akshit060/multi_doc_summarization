# Deep Communicating Agents (DCA-style) – Multi-Document Abstractive Summarization

This folder contains a simplified implementation of **Deep Communicating Agents (DCA)**-style summarization using document-level compression and aggregation with the BART model, evaluated on the CNN/DailyMail dataset.

## ✅ Steps Implemented:
1. Dataset preparation (`CNN/Daily Mail` test split)
2. Grouping 10 documents per sample to simulate MDS
3. Each document acts as an "agent" → local summarization
4. Agent outputs are aggregated into one sequence
5. Final summary is generated using `facebook/bart-base`
6. ROUGE evaluation (1, 2, L)

## 🚀 How to Run
1. Open `DCA.ipynb` in Google Colab
2. Run all cells in sequence:
   - Install dependencies
   - Load dataset
   - Run DCA-style inference using BART
   - Evaluate results with ROUGE
3. Summaries and reference pairs are printed for each sample

## 📊 ROUGE Scores (on 5 multi-document samples)
- **ROUGE-1:** 0.257919
- **ROUGE-2:** 0.085205
- **ROUGE-L:** 0.127675

## ⏱️ Avg Inference Time
- `Avg time per sample ≈ 3.5 sec (on Colab T4 GPU)`
- `Model: facebook/bart-base`

## ⚙️ Method Summary
- Compress each document to 512 tokens (agent encoding)
- Simulate communication via string merging
- Use BART decoder to generate a final unified summary

## 📁 Folder Contents
- `DCA.ipynb`: Full implementation notebook
- `requirements.txt`: Python dependencies
- `README.md`: This documentation

---
