# 📊 Customer Churn Prediction

This project uses a machine learning model to predict whether a customer is likely to churn (i.e., stop using a service). The model takes customer demographic and service usage information as input and returns a binary prediction (Churn / No Churn).

---

## 🚀 Features

- Pretrained model loaded via `pickle`
- Input preprocessing using `LabelEncoder`
- Robust handling of missing and unseen categorical values
- Supports inference on new customer data

---

## 🧠 Model Details

- Model Type: *(e.g., Random Forest / XGBoost / Logistic Regression — replace as applicable)*
- Trained on: Telco Customer Churn Dataset
- Input Features: 19 total features including:
  - Gender, SeniorCitizen, Partner, Dependents
  - Tenure, PhoneService, InternetService, etc.
  - MonthlyCharges, TotalCharges

---

## 📂 Files

- `Customer_Churn_Prediction.ipynb`: Main Jupyter notebook for model inference
- `model.pkl`: Trained model file
- `encoders.pkl`: Dictionary of `LabelEncoder` objects used for categorical features

---

## 🛠️ How It Works

1. Input customer data as a Python dictionary
2. Preprocess the input using saved encoders:
   - Ensure all features are present
   - Encode categorical variables using `LabelEncoder`
   - Convert numeric fields safely
3. Predict churn using the trained model
4. Output a human-readable result

---

## 🧪 Example Input

```python
input_data = {
    'gender': 'Male',
    'SeniorCitizen': 1,
    'Partner': 'No',
    'Dependents': 'No',
    'tenure': 2,
    'PhoneService': 'Yes',
    'MultipleLines': 'No',
    'InternetService': 'Fiber optic',
    'OnlineSecurity': 'No',
    'OnlineBackup': 'No',
    'DeviceProtection': 'No',
    'TechSupport': 'No',
    'StreamingTV': 'Yes',
    'StreamingMovies': 'No',
    'Contract': 'Month-to-month',
    'PaperlessBilling': 'Yes',
    'PaymentMethod': 'Electronic check',
    'MonthlyCharges': 75.5,
    'TotalCharges': '151.2'
}
