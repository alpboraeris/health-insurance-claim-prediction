# 🩺 Health Insurance Payment Prediction

This project predicts individual health insurance payments using machine learning in Python.  
It takes you from data exploration and preprocessing to model training and deployment through an interactive Streamlit app.

---

## 📘 Overview

Health insurance costs vary based on personal and medical factors such as age, BMI, blood pressure, smoking habits, and health conditions.  
This project builds a regression model to estimate those costs, demonstrating a full end-to-end data science workflow:

- Data cleaning and exploration  
- Feature encoding and scaling  
- Model training, evaluation and optimization  
- Real-time prediction through a Streamlit web interface  

---

## 🧩 Project Structure
├── insurance_claim_prediction.ipynb # Main notebook with data exploration and model training
├── app.py # Streamlit web app for prediction
├── best_model.pkl # Trained ML model
├── scaler.pkl # Feature scaler
├── label_encoder_gender.pkl # Encoded mapping for gender
├── label_encoder_diabetic.pkl # Encoded mapping for diabetic status
├── label_encoder_smoker.pkl # Encoded mapping for smoker status
├── requirements.txt # Project dependencies
└── README.md

---
# ⚙️ Key Steps

### 1. Data Cleaning & Exploration
- Handled missing and inconsistent values  
- Encoded categorical features (`gender`, `diabetic`, `smoker`) using `LabelEncoder`  
- Normalized numerical features (`age`, `bmi`, `bloodpressure`, `children`) using `StandardScaler`

### 2. Model Training & Evaluation
- Built multiple regression models (Linear Regression, Random Forest, etc.)  
- Compared models using R² and RMSE metrics  
- Saved the best-performing model as `best_model.pkl`  

### 3. Deployment with Streamlit
- Created a user-friendly interface to input personal details  
- Loaded the trained model and encoders for consistent preprocessing  
- Displayed predicted insurance payment amounts in real time  

---

## 🚀 How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/health-insurance-payment-prediction.git
cd health-insurance-payment-prediction
```
### 2. Install Dependencies
```bash
pip install -r requirements.txt
```
### 3. Run the Streamlit App
```bash
streamlit run app.py
```
