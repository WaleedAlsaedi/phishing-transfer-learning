# Adaptive Transfer-Learning for Robust Phishing Website Detection

**KV6013 — Northumbria University**  
**Author:** Waleed Alsaedi  
**Supervisor:** Dr Sharnil Pandya

Investigating whether knowledge learned from a URL-text phishing dataset can transfer to improve detection on a structurally different webpage-feature phishing dataset.

## Key Results

| Model | Accuracy | Phishing Recall | ROC-AUC |
|-------|----------|-----------------|---------|
| DistilBERT (URLs) | 98.8% | 95.6% | 99.8% |
| MLP Transfer Learning (Primary) | 81.3% | 91.8% | 88.4% |
| Pseudo-Text + DistilBERT | 80.2% | 91.8% | 85.5% |
| Best Baseline (KNN) | 77.0% | 85.5% | 82.8% |

**Multi-seed validation (n=5) of MLP Transfer vs No-Transfer:**
- Accuracy: −0.49pp (p=0.0054, significant)
- ROC-AUC: −0.28pp (p=0.0499, borderline)
- Recall: +0.89pp (p=0.43, n.s.)

## Approaches

- **Baselines:** Logistic Regression, Random Forest, KNN
- **Approach 1:** DistilBERT Embeddings + Web Page Features
- **Approach 2:** MLP Transfer Learning (Primary Model)
- **Approach 3:** Pseudo-Text Generation + DistilBERT Fine-tuning
- **Adversarial Robustness:** 5 lexical evasion strategies tested (≥91.85% detection retained)

## Datasets

- [Phishing Site URLs](https://www.kaggle.com/datasets/taruntiwarihp/phishing-site-urls) — 507,196 samples
- [Web Page Phishing](https://www.kaggle.com/datasets/danielfernandon/web-page-phishing-dataset) — 21,891 samples

## Tech Stack

Python · scikit-learn · PyTorch · HuggingFace Transformers · Google Colab Pro (A100 GPU)
