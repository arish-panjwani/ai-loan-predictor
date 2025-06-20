# 🚀 AI-Loan-Predictor
> *Note: This repository was created as part of our semester project in the AI and Data Science program (Post Graduate Certificate) at Loyalist College, Toronto.*

---

## 📝 Problem Statement
In the modern financial landscape, the influx of loan applications poses significant challenges for institutions. Manual evaluation of these applications is time-consuming and prone to error. Our task was to build a **machine learning–powered loan eligibility prediction system** to automate the decision of approving or rejecting loan requests, thus streamlining the approval process.

---

## ⚙ Technologies Used
- Google Colab
- Python  
- **Libraries:** Pandas, Numpy, Matplotlib, Seaborn, Scikit-learn, Joblib

---

## 📊 Dataset
**Source:** [Kaggle Loan Approval Prediction Dataset](https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset)  
**Rows:** 4269  
**Features:** 13  

| Feature Name               | Description |
|----------------------------|-------------|
| loan_id                    | Unique loan identifier |
| no_of_dependents            | Number of dependents |
| education                   | Graduate / Not Graduate |
| self_employed               | Employment status |
| income_annum                | Annual income |
| loan_amount                 | Requested loan amount |
| loan_term                   | Loan term (years) |
| cibil_score                 | Credit score |
| residential_assets_value     | Value of residential assets |
| commercial_assets_value      | Value of commercial assets |
| luxury_assets_value          | Value of luxury assets |
| bank_asset_value             | Bank balance |
| loan_status                  | Loan approval status (Approved / Rejected) |

---

## 📈 Project Flow
1️⃣ **Problem definition + dataset selection**  
2️⃣ **Data preprocessing:** handled nulls, cleaned categories, converted categorical features to numerical  
3️⃣ **EDA:** histograms, box plots, KDE plots, correlation matrix, pair plots  
4️⃣ **Feature scaling:** MinMaxScaler and StandardScaler  
5️⃣ **Model selection:** Logistic Regression + Random Forest  
6️⃣ **Model evaluation:** accuracy, recall, confusion matrix, classification report  
7️⃣ **Model export:** best model + scaler saved for deployment  

---

## ✅ Final Model
After rigorous evaluation, the **best model** is:
- **Random Forest Classifier with MinMaxScaler**
- **Accuracy:** 0.98  
- **Recall:** 0.99  
- **Confusion Matrix:**

|                | Predicted Rejected (0) | Predicted Approved (1) |
|----------------|-----------------------|-----------------------|
| **Actual Rejected (0)** | 305                   | 13                    |
| **Actual Approved (1)** | 7                     | 529                   |

- **Reason for selection:** High accuracy and recall with balanced performance across both loan approval and rejection classes.

---

## 💾 Deployment
We exported:
- `rf_minmax.pkl` — trained Random Forest model  
- `minmax_scaler.pkl` — corresponding MinMaxScaler  

✅ The model is ready for deployment via **Flask API**, **Streamlit app**, or on **Fly.io / Render / Heroku**.

---

## 🔍 Key Insights
- **CIBIL score** is the most significant factor influencing loan approval.
- **Income and loan amount** are positively correlated — higher income generally means larger loans.
- **Asset values** (luxury, residential) correlate with financial stability and loan amount.

---

## 🚀 Next Steps
- Enhance model with additional features (e.g. employment duration, location data).  
- Deploy as a scalable web service for real-time loan eligibility prediction.

