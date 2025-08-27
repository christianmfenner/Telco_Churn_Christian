# Telco Customer Churn Prediction

This project applies **Machine Learning** techniques to predict customer churn using the **Telco Customer Churn Dataset**.  
It covers the full workflow: data preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and prediction on new data.

---

## 📊 Dataset
The dataset used is **Telco Customer Churn**.  
It contains information about telecom customers, their demographics, services subscribed, account details, and whether they churned or not.

- Source: `WA_Fn-UseC_-Telco-Customer-Churn.csv`
- Target variable: `Churn` (Yes/No)

---

## ⚙️ Workflow

1. **Data Preprocessing**
   - Converted `TotalCharges` to numeric.
   - Encoded categorical variables (`SeniorCitizen`, one-hot encoding).
   - Removed irrelevant columns (`customerID`, `PhoneService`, etc.).
   - Outlier treatment on `TotalCharges`.

2. **Exploratory Data Analysis**
   - Distribution plots (boxplots, histograms, pie chart for gender).
   - Correlation heatmap.
   - Chi-squared test for categorical feature significance.

3. **Modeling**
   - **Decision Tree Classifier** (with GridSearchCV for hyperparameter tuning).
   - **Logistic Regression** (final chosen model).
   - **Support Vector Machine (SVM)** (tested).
   - **Linear Regression** (tested for comparison).

4. **Evaluation**
   - Accuracy, F1-score, and classification report.
   - Confusion matrix visualization.

5. **Prediction on New Data**
   - Preprocessed new dataset (`WA_Fn-UseC_-Telco-Customer-Churn_with_dummy.xlsx`).
   - Applied the trained Logistic Regression model.
   - Added predictions (`Churn_Previsto`) and churn probability (`Probabilidade_Churn`).
   - Exported results to `df_dummy_classificado.xlsx`.

---

## 📈 Results
- The best performing model: **Logistic Regression**  
- Chosen due to consistent accuracy and F1-score performance across test data.  

---

## 🛠️ Tech Stack
- **Python**
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`

---

## 🚀 How to Run
```bash
# Clone this repository
git clone https://github.com/your-username/telco-churn-prediction.git

# Install dependencies
pip install -r requirements.txt

# Run the notebook or Python script
python churn_model.py
