# 🤖 Machine Learning Techniques

> A comprehensive collection of machine learning implementations and experiments for MLT Lab Semester 6

[![GitHub](https://img.shields.io/badge/GitHub-rika1089-blue?logo=github)](https://github.com/rika1089)
[![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)](https://www.python.org/)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Experiments](#experiments)
- [Project Structure](#project-structure)
- [Technologies](#technologies)
- [Installation](#installation)
- [How to Use](#how-to-use)

---

## 🎯 Overview

This repository contains hands-on machine learning implementations covering:

✅ **Dimensionality Reduction** (PCA, LDA)  
✅ **Classification Algorithms** (KNN, Naive Bayes, SVM)  
✅ **Regression** (Linear Regression)  
✅ **Deep Learning** (Feed Forward Neural Networks)  
✅ **Data Analysis** (EDA on real datasets)  

Each experiment includes:
- 📓 Jupyter Notebooks with complete implementations
- 📊 Real-world datasets (UCI ML Repository, Kaggle)
- 📝 Detailed documentation with objectives and results
- 🔍 Data visualization and statistical analysis

---

## 🔬 Experiments

| # | Exercise | Topic | Dataset | Key Focus |
|---|----------|-------|---------|-----------|
| 1a | Ex_1(a)_PCA | Principal Component Analysis | Iris/Custom | Dimensionality reduction, variance analysis |
| 1b | Ex_1(b)_EDA | Exploratory Data Analysis | Online Delivery | Data cleaning, visualization, insights |
| 2 | Ex_2_KNN | K-Nearest Neighbors | UCI ML Data | Classification, k-value tuning |
| 3 | Ex_3_LDA | Linear Discriminant Analysis | Dataset | Supervised dimensionality reduction |
| 4 | Ex_4_Linear_Reg | Linear Regression | Custom | Univariate & multivariate regression, R² |
| 5 | Ex_5_Naive_Bayes | Naive Bayes | Wine Dataset | Probabilistic classification |
| 6 | Ex_6_SVM | Support Vector Machines | Custom | Linear SVM, support vectors |
| 7 | Ex_7_SVM | SVM with Kernels | Custom | RBF, Polynomial, Sigmoid kernels |
| 8 | Ex_8_FFN | Feed Forward Network | Custom | Neural networks, backpropagation |

---

## 📁 Project Structure

```
Machine-Learning-Techniques/
│
├── 📂 Ex_1(a)_PCA/
│   ├── PCA.ipynb
│   └── [Supporting files & resources]
│
├── 📂 Ex_1(b)_EDA_Online_delivery/
│   ├── EDA.ipynb
│   ├── onlinedeliverydata.csv
│   ├── RESOURCES.txt
│   └── archive.zip
│
├── 📂 Ex_2_KNN/
│   ├── KNN.ipynb
│   └── [Dataset & resources]
│
├── 📂 Ex_3_LDA/
│   ├── LDA.ipynb
│   └── [Supporting files]
│
├── 📂 Ex_4_Linear_Regression/
│   ├── Linear_Regression.ipynb
│   └── [Dataset & visualization files]
│
├── 📂 Ex_5_Naive_Bayes/
│   ├── Naive_Bayes.ipynb
│   └── [Wine Dataset]
│
├── 📂 Ex_6_SVM/
│   ├── SVM.ipynb
│   └── [Supporting resources]
│
├── 📂 Ex_7_SVM(Varying_kernels)/
│   ├── SVM_Kernels.ipynb
│   └── [Kernel comparison files]
│
├── 📂 Ex_8_Feed_Forward_Network/
│   ├── FFN.ipynb
│   └── [Neural network models]
│
├── 📄 Lab_1_PCA.ipynb
├── 📄 Lab_2_KNN.ipynb
├── 📄 creditcard.csv
├── 📄 [Online delivery dataset file].txt
└── 📄 README.md
```
---

## 🛠️ Technologies Used

- **Python 3.8+** - Programming language
- **Jupyter Notebook** - Interactive coding environment
- **scikit-learn** - Machine learning algorithms
- **pandas** - Data manipulation & analysis
- **NumPy** - Numerical computing
- **Matplotlib & seaborn** - Data visualization
- **TensorFlow/Keras** - Neural networks

---

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Clone Repository
```bash
git clone https://github.com/rika1089/Machine-Learning-Techniques.git
cd Machine-Learning-Techniques
```

### Install Dependencies
```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter tensorflow keras
```

---

## 🚀 How to Use

### Open Jupyter Notebook
```bash
jupyter notebook
```

### Run Specific Exercise
```bash
cd Ex_1a_PCA
jupyter notebook PCA.ipynb
```

### Load and Explore Data
```python
import pandas as pd

# Load dataset
data = pd.read_csv('creditcard.csv')
print(data.head())
print(data.info())
print(data.describe())
```

---

## 📊 Key Learnings

✅ Feature engineering and data preprocessing  
✅ Supervised & unsupervised learning algorithms  
✅ Model evaluation (Accuracy, Precision, Recall, F1-Score)  
✅ Hyperparameter tuning & cross-validation  
✅ Neural network architectures  
✅ Real-world problem-solving with ML  

---

## 📝 Dataset Sources

- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/)
- [Kaggle Datasets](https://www.kaggle.com/datasets)
- [Online Delivery Data](https://www.kaggle.com/datasets/benroshan/online-food-delivery-)

---

## 🎓 Course Information

- **Course:** Machine Learning Techniques
- **Semester:** 6
- **Author:** Srikar (rika1089)

---

## ⭐ How to Navigate

1. **Start here:** Ex_1(a)_PCA and Ex_1(b)_EDA
2. **Learn algorithms:** Work through Ex_2 to Ex_7
3. **Advanced:** Ex_8_Feed_Forward_Network for deep learning
4. **Lab work:** Lab_1_PCA.ipynb, Lab_2_KNN.ipynb

Each folder contains complete Jupyter notebooks with explanations, code, and results.

---

## 📄 License

This project is provided for educational purposes. Feel free to use, modify, and share.

---

## 🤝 Support

If you have questions or suggestions:
- Open an issue on GitHub
- Check the RESOURCES.txt files in each folder for references
- Review the Jupyter notebooks for detailed explanations

---

**Status:** ✅ Active & Maintained  
**Last Updated:** March 2026
