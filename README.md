# Customer Churn Prediction with Artificial Neural Networks (ANN)

## 📝 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Dataset Description](#-dataset-description)
- [Model Architecture](#-model-architecture)
- [Training Parameters](#-training-parameters)
- [Performance Metrics](#-performance-metrics)
- [Installation Guide](#-installation-guide)
- [Usage Instructions](#-usage-instructions)
- [Results Visualization](#-results-visualization)
- [License](#-license)
- [Contact Information](#-contact-information)

## 🌟 Project Overview
This project implements an Artificial Neural Network (ANN) to predict customer churn for a banking institution. The model achieves **85.95% accuracy** on test data, demonstrating strong predictive capability to identify customers at risk of leaving the bank.

## 🚀 Key Features
- Complete data preprocessing pipeline
- Categorical feature encoding (Label & One-Hot Encoding)
- ANN implementation with TensorFlow/Keras
- Comprehensive model evaluation
- Visual performance analysis

## 📊 Dataset Description
**Source:** Churn_Modelling.csv (10,000 records, 14 features)  
**Target Variable:** Exited (Binary: 1 = Customer left, 0 = Stayed)

### Key Features:
- CreditScore
- Geography (France/Germany/Spain)
- Gender
- Age
- Tenure
- Balance
- NumOfProducts
- HasCrCard
- IsActiveMember
- EstimatedSalary


## 🧠 Model Architecture
```python
ann = tf.keras.models.Sequential()
ann.add(tf.keras.layers.Dense(units=6, activation='relu'))
ann.add(tf.keras.layers.Dense(units=6, activation='relu'))
ann.add(tf.keras.layers.Dense(units=1, activation='sigmoid'))
```
## ⚙️ Training Parameters

**Neural Network Configuration:**
| Parameter | Value | Description |
|-----------|-------|-------------|
| Optimizer | ![Adam](https://img.shields.io/badge/Adam-optimizer-ff69b4) | Adaptive Moment Estimation |
| Loss Function | ![BCE](https://img.shields.io/badge/Loss-Binary_Crossentropy-red) | Binary classification loss |
| Batch Size | ![32](https://img.shields.io/badge/Batch-32-blue) | Samples per weight update |
| Epochs | ![100](https://img.shields.io/badge/Epochs-100-success) | Full training cycles |
| Validation Split | ![20%](https://img.shields.io/badge/Validation-20%25-orange) | Holdout for tuning |

## 📈 Performance Metrics

### Model Evaluation Matrix
| Metric | Training | Test Set |
|--------|----------|----------|
| **Accuracy** | 86.59% | 86.20% |
| **Loss** | 0.3309 | 0.3521 |


**Confusion Matrix:**
```python
[[1531   76]  # True Negative | False Positive
 [ 200  193]] # False Negative | True Positive
```

## 📥 Installation Guide
1. Clone repository:
```bash
git clone https://github.com/barisgudul/ANN_Customer_Churn-_Prediction.git
cd ANN_Customer_Churn-_Prediction
```

2. Create virtual environment:
```bash
# Unix/macOS
python -m venv churn_env
source churn_env/bin/activate

# Windows
python -m venv churn_env
churn_env\Scripts\activate
```

## 🖥️ Usage Instructions
1. Place dataset in Datasets/Artificial Neural Networks (ANN)/ directory
Run Jupyter notebook:
```bash
jupyter notebook ANN.ipynb
```
2. Execute cells sequentially
3. Check Results/ directory for generated outputs

## 📊 Results Visualization

### Confusion Matrix Heatmap
![Confusion Matrix Heatmap](Artificial%20Neural%20Networks/heatmap.png) 

**Prediction Distribution:**
- **True Negatives (TN):** 1531  
  *Customers correctly identified as staying*
- **False Positives (FP):** 76 
  *Loyal customers mistakenly flagged as churn risks*
- **False Negatives (FN):** 200  
  *Churning customers missed by the model*
- **True Positives (TP):** 193 
  *Churn risks accurately predicted*

---

## 📄 License

**MIT License**  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Permissions:**  
✅ Free academic/research use  
✅ Modification and redistribution  
❌ Commercial use requires written consent  

Full license terms available in [LICENSE](LICENSE) file.

---

## 📧 Contact Information

**Project Maintainer**  
[![Author Badge](https://img.shields.io/badge/Author-barisgudul-blue.svg)]()  
[![Email](https://img.shields.io/badge/Contact_Me-Email%3A%20mehmetbarisgudul%40gmail.com-e74c3c?style=flat-square&logo=gmail)](mailto:mehmetbarisgudul@gmail.com)    
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-informational.svg)](https://linkedin.com/in/mehmet-baris-gudul-1101bg)

**Contribution Guidelines:**  
We welcome collaborations! Please reach out via email before submitting PRs.

**Technical Support:**  
For implementation assistance, include "[Churn Model]" in your email subject line.
