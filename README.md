# FraudRadar-AU
## An AI-Powered E-Commerce Scam Detection System for Australian Online Marketplaces

---

## Project Overview
FraudRadar-AU is a multi-paradigm AI system designed to detect fraudulent product listings on Australian e-commerce platforms such as Gumtree, Facebook Marketplace, and eBay AU. The system combines deep learning, probabilistic reasoning, anomaly detection, and LLM-generated explainability into a unified risk-scoring pipeline.

---

## System Architecture

Layer 1: Text-Based Fraud Detection
SMS Text → DistilBERT + Naïve Bayes → NLP Risk Score
Layer 2: Numerical Anomaly Detection
Product Features → Isolation Forest → Anomaly Score
Final Integration
Rank-Based Alignment → Combined Risk Score → LLM Explanation → Risk Report

---

## Team Members
| Member | Responsibility |
|--------|---------------|
| Member 1 (Nian-Ya Weng) | Project Management, Data Preparation & Baseline Models |
| Member 2 (Fang Yee Tan) | DistilBERT Neural Network |
| Member 3 (Rohan Yadav)| Isolation Forest Anomaly Detection |
| Member 4 (Taiki Komori) | Naïve Bayes Probabilistic Classifier |
| Member 5 (Yin Kao) | LLM Explainability & Final Integration |

## Individual Contributions

**Member 1 (Nian-Ya Weng) — Project Management & Data Preparation**
- Defined project scope, topic selection, and overall system architecture
- Coordinated team communication and managed task allocation
- Set up and managed the GitHub repository
- Prepared and cleaned all datasets (SMS Spam + Counterfeit Products)
- Built baseline models (Rule-Based + Logistic Regression)
- Resolved integration issues across all model components

**Member 2 (Fang Yee Tan) — DistilBERT Neural Network**
- Fine-tuned DistilBERT model for fraudulent text classification
- Evaluated model using Accuracy, Precision, Recall, F1-Score
- Generated full dataset predictions for ensemble integration

**Member 3 (Rohan Yadav)— Isolation Forest Anomaly Detection**
- Built Isolation Forest model using Counterfeit Products dataset
- Performed feature engineering on numerical product features
- Evaluated model performance and visualised anomaly detection results

**Member 4 (Taiki Komori) — Naïve Bayes Classifier**
- Built Naïve Bayes probabilistic classifier for text-based fraud detection
- Evaluated model and generated predictions for ensemble integration

**Member 5 (Yin Kao) — LLM Explainability & Final Integration**
- Integrated all three model outputs using Rank-Based Alignment
- Calculated Combined Final Risk Score (CFRS)
- Implemented Claude/GPT API for human-readable risk explanations
- Produced final risk report for Trust and Safety reviewers

---

## AI Techniques Used
- **DistilBERT** — Deep learning text classification (Multi-layer Network)
- **Naïve Bayes** — Probabilistic reasoning for urgency keyword screening
- **Isolation Forest** — Unsupervised anomaly detection on product features
- **Rank-Based Alignment** — Cross-dataset ensemble integration
- **LLM (Claude/GPT API)** — Generative AI for human-readable explanations

---

## Dataset
| Dataset | Source | Purpose |
|---------|--------|---------|
| SMS Spam Collection | UCI / Kaggle | Text-based model training (DistilBERT, Naïve Bayes) |
| Counterfeit Products | Kaggle | Numerical anomaly detection (Isolation Forest) |

---

## Repository Structure

FraudRadar-AU/
├── data/
│   ├── processed/
│   │   ├── sms_balanced.csv
│   │   └── counterfeit_balanced.csv
│   └── synthetic/
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   ├── 02_bert_model.ipynb
│   ├── 03_Isolation_forest.ipynb
│   ├── 04_naive_bayes_ensemble.ipynb
│   └── 05_llm_explainer.ipynb
├── results/
│   ├── figures/
│   ├── baseline_results.csv
│   └── DistilBERT_all_predictions.csv
├── README.md
└── requirements.txt
---

## Setup Instructions
```bash
# Clone repository
git clone https://github.com/Amanda1005/FraudRadar-AU.git
cd FraudRadar-AU

# Install dependencies
pip install -r requirements.txt

# Run notebooks in order
# 01 → 02 → 03 → 04 → 05
```

---

## Baseline Results
| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Rule-Based Keyword Filtering | 0.8779 | 0.9459 | 0.8015 | 0.8678 |
| Logistic Regression + TF-IDF | 0.9580 | 0.9688 | 0.9466 | 0.9575 |

---

## Data Sources
- Scamwatch 2024 Annual Report: https://www.scamwatch.gov.au
- SMS Spam Collection: https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset
- Counterfeit Products: https://www.kaggle.com/datasets/aimlveera/counterfeit-product-detection-dataset