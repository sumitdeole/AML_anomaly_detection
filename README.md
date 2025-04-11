# Credit Card Fraud Detection

## What & Why

Credit card fraud is a costly issue for banks and customers. The goal of this project is to detect fraudulent transactions using anomaly detection and ML techniques on real anonymized transactional data. This helps improve financial security and reduce losses due to fraud.

## How

We use the [Credit Card Fraud Detection dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud), which contains 284,807 transactions with only 492 frauds (~0.17%). Due to this imbalance, we evaluate anomaly detection, classical supervised models, and deep learning with and without oversampling.

Steps include:

- Preprocessing and feature scaling  
- Exploratory data analysis  
- Model training (Isolation Forest, Neural Networks, DNNs)  
- Evaluation and visual inspection  

All code and outputs are in this [`jupyter notebook`](https://github.com/sumitdeole/AML_anomaly_detection/blob/main/AML_Anomaly_Detection.ipynb).

## 📊 Model Performance

| Model               | Type                  | Precision | Recall |   F1   | ROC AUC |
|---------------------|-----------------------|-----------|--------|--------|---------|
| Isolation Forest     | Anomaly Detection     | 22.76%    | 37.84% | 28.43% | 68.81%  |
| NN (Imbalanced)      | Supervised Learning   | 84.85%    | 75.68% | 80.00% | 87.83%  |
| NN (SMOTE)           | Supervised Learning   | 76.92%    | 74.32% | 75.60% | 87.14%  |
| DNN (Imbalanced)     | Deep Learning         | 42.61%    | 83.78% | 56.49% | 91.79%  |
| DNN (SMOTE)          | Deep Learning         | 84.43%    | 69.59% | 76.30% | 84.79%  |

**Findings:**  
Deep neural networks on imbalanced data performed best in terms of AUC. SMOTE helps traditional NNs generalize better, but in some cases, simple models on raw data outperform oversampled variants. Isolation Forest performed poorly due to limited fraud signal in high-dimensional feature space.

## Key Figures

- [Fig. 1: Fraud network analysis](https://github.com/sumitdeole/AML_anomaly_detection/blob/main/1.Fraud_network_analysis.pdf)  
- [Fig. 2: Class balancing using SMOTE](https://github.com/sumitdeole/AML_anomaly_detection/blob/main/2.SMOTE_balancing_before_vs_after.pdf)  
- [Fig. 3: Model performance comparison](https://github.com/sumitdeole/AML_anomaly_detection/blob/main/3.Model_performance.pdf)

All figures are saved as PDFs during notebook execution.

## 🛠 Setup

1. **Clone this repository**

```bash
git clone https://github.com/yourusername/creditcard-fraud-detection.git
cd creditcard-fraud-detection

2. **Install requirements**
pip install -r requirements.txt

3. **Execute notebook cells**
