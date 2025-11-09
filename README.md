# 🩺💶 Health Insurance Claim Prediction

A machine learning project that predicts individual health insurance claim amounts using Python.
It walks through a complete data science workflow, covering exploratory data analysis, feature engineering, model selection and deployment with Streamlit.

## 📘 Overview

Health insurance claims depend on a range of personal and medical factors such as age, BMI, blood pressure, smoking habits and chronic conditions.
This project builds and deploys a regression model that estimates those costs accurately, showing the full pipeline from raw data to an interactive web app.

- Data cleaning and exploration  
- Feature encoding and scaling  
- Model training, tuning, and evaluation 
- Real-time prediction through a Streamlit web interface  

## 🗂️ Project Structure
```
├── insurance_claim_prediction.ipynb   # EDA, model training and evaluation
├── app.py                             # Streamlit web app
├── best_model.pkl                     # Trained XGBoost model
├── scaler.pkl                         # StandardScaler for numeric features
├── label_encoder_*.pkl                # LabelEncoders for categorical variables
├── requirements.txt                   # Project dependencies
└── README.md
```
<img width="829" height="741" alt="image" src="https://github.com/user-attachments/assets/674e62b4-53d7-47ea-947f-0242d964824c" />


## 🔍 Exploratory Data Analysis (EDA)

Before modeling, the dataset was analyzed to identify key patterns and correlations:

- **Distribution Analysis:** Checked the spread of numerical variables (`age`, `bmi`, `bloodpressure`, `children`, `claim`)  
- **Categorical Insights:** Visualized the impact of `gender`, `smoker`, and `diabetic` on claim amounts  
- **Correlation Heatmap:** Revealed strong relationships between **bloodpressure**, **BMI** and insurance claim  
- **Behavioral Patterns:** Found that smokers consistently have higher average claims across all demographics  

These insights guided feature selection and model choice later in the workflow.  

## ⚙️ Model Development  

### 1. Data Preprocessing  
- Handled missing and inconsistent values  
- Encoded categorical columns (`gender`, `diabetic`, `smoker`) with `LabelEncoder`  
- Normalized numerical features with `StandardScaler`  

### 2. Model Training & Evaluation  
Trained and compared multiple regression models:  
- Linear Regression  
- Polynomial Regression  
- Random Forest Regressor  
- Support Vector Regressor (SVR)  
- XGBoost Regressor  

**Evaluation metrics:** R², RMSE, MAE  

**XGBoost** achieved the highest R² and lowest RMSE, and was saved as `best_model.pkl` for deployment.  

### 3. Streamlit Deployment  
- Developed a web app (`app.py`) for real-time predictions  
- Accepts user inputs for personal and health-related attributes  
- Applies the same preprocessing pipeline and displays predicted insurance claim amount in real time    



## 🛠 How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/health-insurance-claim-prediction.git
cd health-insurance-claim-prediction
```
### 2. Install Dependencies
```bash
pip install -r requirements.txt
```
### 3. Run the Streamlit App
```bash
streamlit run app.py
```
