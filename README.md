# Adaptive Transfer-Learning for Robust Phishing Website Detection

**KV6013 — Northumbria University**
**Supervisor:** Dr Sharnil Pandya

Investigating whether knowledge learned from one phishing dataset (URL-level or HTML/DOM-level features) can transfer to improve detection on another.

## Key Results

| Model | Accuracy | Recall | ROC-AUC |
|-------|----------|--------|---------|
| DistilBERT (URLs) | 98.8% | 96.2% | 99.8% |
| MLP Transfer Learning (Main) | 81.1% | 92.6% | 87.6% |
| Pseudo-Text + DistilBERT | 80.4% | 93.2% | 86.1% |
| Best Baseline (KNN) | 77.0% | 85.5% | 82.8% |

## Approaches
- **Baselines:** Logistic Regression, Random Forest, KNN
- **Approach 1:** DistilBERT Embeddings + Web Page Features
- **Approach 2:** MLP Transfer Learning (Primary Model)
- **Approach 3:** Pseudo-Text Generation + DistilBERT Fine-tuning

## Datasets
- [Phishing Site URLs](https://www.kaggle.com/datasets/taruntiwarihp/phishing-site-urls) — 507,196 samples
- [Web Page Phishing](https://www.kaggle.com/datasets/danielfernandon/web-page-phishing-dataset) — 21,891 samples

## Tech Stack
Python · scikit-learn · PyTorch · DistilBERT · Google Colab (A100 GPU)
