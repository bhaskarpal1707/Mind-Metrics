# 🧠 Mind Metrics

### Detecting Depression, Anxiety, and Stress in Students using Machine Learning

![image](https://github.com/user-attachments/assets/6fc501d9-8914-48b2-9313-2ee279fb7ebc)


> Final Year MCA Capstone Project  
> Department of Computer Science  
> **Sister Nivedita University**, Kolkata – 2025

---

## 📑 Overview

**Mind Metrics** is a machine learning-based system developed to detect and predict mental health conditions such as **depression**, **anxiety**, and **stress** among university students. Using self-reported survey data, we built and benchmarked multiple ML models to enable **scalable**, **objective**, and **early intervention** strategies in academic environments.

The project addresses limitations in traditional assessment methods by integrating data-driven intelligence into a streamlined prediction framework using Python and open-source ML libraries.

---

## 📋 Contents

- [Objective](#objective)
- [Dataset Description](#dataset-description)
- [System Architecture](#system-architecture)
- [Machine Learning Models](#machine-learning-models)
- [Performance Metrics](#performance-metrics)
- [Installation & Usage](#installation--usage)
- [Project Directory Structure](#project-directory-structure)
- [Challenges & Solutions](#challenges--solutions)
- [Future Scope](#future-scope)
- [Authors](#authors)
- [License](#license)

---

## 🎯 Objective

### Primary Goal:
Develop a **multi-output machine learning system** to predict:
- Depression levels
- Anxiety levels
- Stress levels

### Sub-goals:
- Clean and preprocess psychological survey data.
- Compare simple vs ensemble ML methods.
- Implement cross-validation for generalization.
- Optimize hyperparameters and select best model.
- Visualize evaluation metrics and model outputs.

---

## 📊 Dataset Description

- **Source**: Kaggle (Student Mental Health Assessment)
- **Records**: 7,022
- **Target Labels**:
  - `Depression_Score` (0 to 5)
  - `Anxiety_Score` (0 to 5)
  - `Stress_Score` (0 to 5)

### Key Features:
- **Demographics**: Age, Gender, Residence Type
- **Academic**: CGPA, Course, Credit Load
- **Lifestyle**: Diet, Physical Activity, Sleep Quality
- **Behavioral**: Substance Use, Financial Stress, Social Support

### Preprocessing Steps:
- Null handling
- Label encoding
- Normalization
- Feature selection (ANOVA / SelectKBest)

---

## 🏗️ System Architecture

1. **User Data Collection** (via survey form)
2. **Data Preprocessing**
3. **Feature Engineering**
4. **Model Training (multi-output classifiers)**
5. **Evaluation (Accuracy, F1, ROC-AUC)**
6. **Prediction Outputs**
7. **Result Feedback & Logging**

### Diagrams Included:
- Flowchart
- DFD Level 0 & Level 1

---

## 🤖 Machine Learning Models

### 1. Classical Models
- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree Regressor

### 2. Bagging (Ensemble)
- Random Forest
- Bagging-SVM
- Bagging-RandomForest

### 3. Boosting
- AdaBoost ✅ (Top performer)
- XGBoost
- Gradient Boosting
- CatBoost
- LightGBM

---

## 📈 Performance Metrics

| Model                    | Accuracy (%) | F1 Score | ROC-AUC | K-Fold Accuracy |
|-------------------------|--------------|----------|---------|-----------------|
| **AdaBoostRegressor**   | **73.86**    | **44.31**| 63.30   | **77.74**       |
| GradientBoosting        | 73.43        | 41.47    | 61.82   | 74.63           |
| XGBRegressor            | 73.36        | 41.21    | 61.71   | 74.83           |
| CatBoost                | 73.12        | 32.58    | 60.90   | 74.75           |
| RandomForest            | 73.31        | 38.94    | 62.40   | 58.55           |
| Logistic Regression     | 71.39        | 8.01     | 58.17   | -458.31         |

> 🏆 **AdaBoost** shows best accuracy and generalization ability.

### Visualizations:
- Bar chart: Accuracy, F1, AUC comparison
- Line graph: Accuracy vs K-Fold Accuracy

---

## ⚙️ Installation & Usage

### Prerequisites:
- Python 3.8 or later
- pip / conda

### Clone & Setup
```bash
git clone https://github.com/yourusername/mind-metrics.git
cd mind-metrics
pip install -r requirements.txt
```

### Run Training
```bash
python src/train.py --model adaboost
```

### Run Prediction
```bash
python src/predict.py --input data/sample_input.csv
```

### Output
- Predictions will be saved in `results/` directory.

---

## 📁 Project Directory Structure

```bash
mind-metrics/
├── data/                  # Raw and cleaned datasets
├── notebooks/             # Jupyter notebooks for EDA, models
├── src/                   # Scripts for preprocessing, training, prediction
│   ├── preprocess.py
│   ├── features.py
│   ├── models.py
│   ├── train.py
│   └── predict.py
├── results/               # Output predictions, graphs
├── requirements.txt       # Dependencies
└── README.md
```

---

## 🛠 Challenges & Solutions

| Challenge                             | Solution                                      |
|--------------------------------------|-----------------------------------------------|
| Imbalanced dataset                   | Used SMOTE, stratified K-Fold, AdaBoost       |
| Stigma in self-reporting             | Anonymized data, neutral framing              |
| Model generalization                 | Cross-validation, ensemble methods             |
| Interpretability                     | Feature importance, SHAP (future)             |
| Low recall in classical models       | Adopted ensemble boosting models              |

---

## 🔮 Future Scope

- Real-time mobile/web integration
- Integration of NLP, facial emotion, and voice data
- Deep Learning (CNN, RNN, Transformers)
- Explainable AI for counselor-facing tools
- Dataset expansion across demographics
- Personalized academic recommendations

---

## 👨‍💻 Authors

| Name                   | Email                                |
|------------------------|----------------------------------------|
| Bhaskar Pal            | bhaskar2k02@gmail.com                 |
| Shreyash Mulate        | shreyashmulate@gmail.com              |
| Debprasad Manna        | debprasadmanna2002@gmail.com          |
| Sudip Kumar Patra      | sudippatra3711@gmail.com              |
| Debanjan Bhattacharya  | debanjanbhattacharya69@gmail.com      |

> MCA, Department of Computer Science, 2025  
> **Sister Nivedita University**, Kolkata

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---


> ⚠️ **Disclaimer**: This project is academic research only. It is not a diagnostic tool.
