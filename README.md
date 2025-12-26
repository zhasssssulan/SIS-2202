# Automated Essay Scoring Using Machine Learning

## 📌 Project Overview
This project focuses on building an Automated Essay Scoring (AES) system using
Natural Language Processing (NLP) and Machine Learning techniques. The goal is to
predict human-assigned essay scores automatically and consistently.

The project was developed as a semester project for the **Machine Learning** course.

---

## 🎯 Objectives
- Apply NLP techniques to preprocess essay text
- Extract meaningful textual features
- Train baseline and optimized machine learning models
- Evaluate models using regression metrics and Quadratic Weighted Kappa (QWK)
- Analyze limitations and propose future improvements

---

## 📂 Dataset
- **ASAP Automated Essay Scoring Dataset**
- Source: Kaggle
- Essays with human-assigned scores
- Target variable: `domain1_score`

> Due to licensing restrictions, the dataset is not included in this repository.
> Please download it from Kaggle and place it in the `data/raw/` directory.

---

## 🛠️ Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- NLTK
- Matplotlib / Seaborn
- Jupyter Notebook

---

## 🔄 Project Workflow
1. Data Cleaning & Preprocessing
2. Exploratory Data Analysis (EDA)
3. Feature Engineering (TF-IDF, word count)
4. Model Training
   - Baseline: Linear Regression
   - Improved: Random Forest Regressor
5. Model Evaluation
   - RMSE, MAE, R²
   - Quadratic Weighted Kappa (QWK)
6. Analysis & Reporting

---

## 🚀 How to Run the Project

### 1️⃣ Clone the repository
```bash
git clone https://github.com/yourusername/automated-essay-scoring-ml.git
cd automated-essay-scoring-ml
