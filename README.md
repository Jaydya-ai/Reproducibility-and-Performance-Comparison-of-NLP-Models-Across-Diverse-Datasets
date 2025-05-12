
# 📊 Reproducible Sentiment Analysis with BERT using SNR on Amazon & IMDB Datasets

## 🔍 Project Overview

This project presents a comparative study of BERT-based sentiment classification models across two distinct datasets—Amazon Product Reviews and IMDB Movie Reviews. Our work not only focuses on classification performance (accuracy, F1-score) but also introduces **Signal-to-Noise Ratio (SNR)** as a diagnostic metric to measure **model reproducibility** and **evaluation stability**.

We propose a reproducibility-aware evaluation framework by combining **3×2 Blocked Cross-Validation (BCV)** with **SNR-based performance analysis**, validating BERT's consistency across domains.

---

## 🧪 Datasets Used

- **Amazon Reviews Dataset**: Structured consumer feedback on products, binary labeled (positive/negative).
- **IMDB Reviews Dataset**: Narrative movie reviews with rich emotional tone, binary labeled.

---

## 🧠 Model and Methodology

- **Model Architecture**: BERT-base (via Hugging Face Transformers)
- **Training Framework**: PyTorch + HuggingFace Transformers
- **Cross-Validation**: 3×2 Blocked Cross-Validation (BCV)
- **Reproducibility Metric**: Signal-to-Noise Ratio (SNR)
- **Hardware**: NVIDIA Tesla T4 GPU

### ⚙️ Hyperparameters

| Parameter         | Value       |
|------------------|-------------|
| Optimizer        | AdamW       |
| Learning Rate    | 5e-5        |
| Batch Size       | 16          |
| Epochs           | Variable (Early Stopping) |
| Callbacks        | Early Stopping, LR Scheduler |

---

## 📈 Evaluation Metrics

- **Accuracy**
- **F1 Score**
- **SNR (Signal-to-Noise Ratio)**: Quantifies model robustness and reliability
- **Mixture Estimator**: Adaptive switching between vote and average metrics (as per EMNLP SNR theory)

---

## 🔬 Results

| Dataset         | Accuracy | F1 Score | SNR (dB) |
|----------------|----------|----------|----------|
| Amazon Reviews | 92.01%   | 92.02%   | 18.33    |
| IMDB Reviews   | 91.14%   | 91.21%   | 18.23    |

---

## 📊 Visualizations

- Training & Validation Accuracy/Loss Curves
- F1-Score Progression Across Epochs
- SNR vs Reproducibility Graphs
- Confusion Matrix Plots

Plots are embedded in the provided `.ipynb` notebooks.

---

## 📁 Project Structure

```bash
├── BERT_SNR-for-IMDB_Dataset.ipynb       # IMDB-specific experiments
├── BERT_SNR-for-Amazon_Review.ipynb      # Amazon-specific experiments
├── Finalreport for NLP.docx              # Formal report with methodology, analysis, results
└── README.md                             # This file
```

---

## 📚 Key Contributions

- Fine-tuned BERT for cross-domain sentiment classification
- Proposed and validated SNR as a reproducibility metric
- Used 3×2 Blocked Cross-Validation for robust model evaluation
- Provided a theoretical grounding for SNR using EMNLP insights
- Demonstrated reproducibility concerns in modern NLP evaluation

---

## ⚠️ Limitations

- Only English datasets considered
- Evaluation limited to BERT (no RoBERTa, DeBERTa, etc.)
- Assumes linearity in performance estimation for SNR
- High GPU demand for 3×2 BCV

---

## 🔮 Future Work

- Expand evaluation to multilingual and informal text datasets
- Compare with newer transformer variants (RoBERTa, DeBERTa)
- Integrate adversarial robustness analysis
- Apply SNR metrics to real-world deployment scenarios

---

## 📑 References

- Devlin et al. (2018), BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding.
- Jin et al. (2024), Benchmarking Reproducibility in Large Language Models.
- Mohammadi et al. (2025), Explainability in Practice: A Survey of Explainable NLP.
- Longpre et al. (2024), Transparent Evaluation in NLP.
- EMNLP 2023: Reproducibility Theory for SNR and Model Comparison

---

## 👨‍💻 Authors

- **Jay Madchetti** — [madchettijp@cardiff.ac.uk](mailto:madchettijp@cardiff.ac.uk)
- **Mohammed Affan Sharjeel** — [ma@cardiff.ac.uk](mailto:ma@cardiff.ac.uk)

> Cardiff School of Computer Science and Informatics, Wales, UK

---

## 📎 License

This project is intended for educational and academic research purposes.

---
