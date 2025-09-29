# 🫀 Heart Failure Prediction using Logistic Regression

This project applies **Logistic Regression** to predict the likelihood of **heart failure** in patients based on selected medical features.  
It includes **data exploration, feature selection, model training, and evaluation** using metrics like accuracy and confusion matrix.  

---

## 📌 Project Overview
- **Goal**: Predict whether a patient is at risk of heart failure (`DEATH_EVENT` = 1).  
- **Dataset**: Heart failure clinical records dataset (UCI Repository / Kaggle).  
- **Type**: Binary Classification (`Heart Fail` / `Heart Not Failed`).  
- **Algorithm Used**: Logistic Regression.  

---

## 📊 Features Used
From correlation analysis, the most significant features were selected:  
- `time` – Follow-up period (days).  
- `ejection_fraction` – Percentage of blood leaving the heart at each contraction.  
- `serum_creatinine` – Level of creatinine in blood (indicator of kidney function).  

Target variable:  
- `DEATH_EVENT` – (1 = Heart Fail, 0 = Not Failed).  

---

## 🔎 Steps Performed
1. **Exploratory Data Analysis (EDA)**  
   - Checked missing values, distributions, and correlations.  
   - Visualized using `seaborn`, `matplotlib`, and heatmaps.  

2. **Feature Selection**  
   - Selected `time`, `ejection_fraction`, `serum_creatinine` based on correlation with `DEATH_EVENT`.  

3. **Model Training**  
   - Split dataset: 70% train, 30% test.  
   - Trained Logistic Regression model using `scikit-learn`.  

4. **Evaluation**  
   - Measured **accuracy, precision, recall**.  
   - Visualized performance with a **confusion matrix**.  

---

## 📈 Results
- **Accuracy**: ~86.7%  
- **Confusion Matrix**:  

|                   | Predicted: Not Failed | Predicted: Fail |
|-------------------|------------------------|-----------------|
| **Actual: Not Failed** | 60 ✅ | 6 ❌ |
| **Actual: Fail**       | 6 ❌ | 18 ✅ |

- **Precision (Fail)**: 75%  
- **Recall (Fail)**: 75%  
- **Specificity**: 91%  

✅ Model predicts heart failure fairly well, but false negatives (missed failures) are still a concern in medical context.  

---

## 🛠️ Technologies Used
- **Python** (pandas, numpy, matplotlib, seaborn)  
- **scikit-learn** (Logistic Regression, train/test split, metrics)  
- **mlxtend** (confusion matrix plotting)  
- **Plotly** (interactive visualizations)  

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/heart-failure-prediction.git
   cd heart-failure-prediction
--
