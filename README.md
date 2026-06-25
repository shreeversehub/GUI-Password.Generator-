# House Price Forecasting

A machine learning project that predicts house prices using regression models on the California Housing dataset.

## 📋 Project Overview

This project implements and compares multiple regression models to forecast house prices. It uses the California housing dataset and evaluates model performance using cross-validation and standard metrics.

## 📊 Dataset

- **Source**: Scikit-learn California Housing Dataset
- **File**: `house_price_forecasting.csv`
- **Records**: 20,640 samples
- **Features**: 
  - MedInc (Median Income)
  - HouseAge
  - AveRooms
  - AveBedrms
  - Population
  - AveOccup
  - Latitude
  - Longitude

## 🎯 Models Implemented

### 1. **Linear Regression**
- Simple linear model with cross-validation
- CV Score: Computed across 5 folds
- Metrics: RMSE, R² Score

### 2. **Ridge Regression**
- Regularized linear regression (alpha=1.0)
- Reduces overfitting with L2 penalty
- CV Score: Computed across 5 folds
- Metrics: RMSE, R² Score

## 🛠️ Technologies Used
Python 3.x
Pandas (data manipulation)
NumPy (numerical operations)
Scikit-learn:
fetch_california_housing (dataset)
train_test_split (data splitting)
StandardScaler (feature scaling)
LinearRegression & Ridge (models)
cross_val_score (validation)
mean_squared_error, r2_score (metrics)
## 📁 Project Structure
batch-7/
├── README.md
├── Source code/
│   └── [your code file]
├── house_price_forecasting.csv
└── requirements.txt
## ⚙️ Installation

1. Clone the repository:
```bash
git clone https://github.com/lalithashreem/batch-7.git
cd batch-7
Install dependencies:
pip install pandas numpy scikit-learn
Or use requirements.txt:
pip install -r requirements.txt
🚀 How to Run
python Source\ code/your_script.py
The script will:
Load the California housing dataset
Prepare features and target variable
Scale the features using StandardScaler
Split data into train (80%) and test (20%)
Train Linear Regression with 5-fold cross-validation
Train Ridge Regression with 5-fold cross-validation
Print RMSE and R² scores for both models
📊 Expected Output
Linear Regression CV Score: X.XX
Linear Regression RMSE: $XXXXX
Linear Regression R2 Score: X.XX

Ridge Regression CV Score: X.XX
Ridge Regression RMSE: $XXXXX
Ridge Regression R2 Score: X.XX
🔍 Key Features
✅ Data Preprocessing
Automatic feature scaling using StandardScaler
Proper train-test split
✅ Model Evaluation
Cross-validation (5-fold)
Multiple metrics (RMSE, R² Score, CV Score)
✅ Model Comparison
Linear Regression vs Ridge Regression
Performance analysis
📈 Model Comparison
Model
Strength
When to use
Linear Regression
Simple, interpretable
Baseline model
Ridge Regression
Prevents overfitting
Better generalization
💡 Code Highlights
# Feature scaling
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Train-test split
X_train, X_test, y_train, y_test = train_test_split(
    X_scaled, y, test_size=0.2, random_state=42
)

# Cross-validation
cv_scores_lr = cross_val_score(lr, X_train, y_train, cv=5)

# Predictions and evaluation
y_pred = lr.predict(X_test)
print("RMSE:", np.sqrt(mean_squared_error(y_test, y_pred)))
print("R2 Score:", r2_score(y_test, y_pred))
👤 Author
Lalit (lalithashreem)
Paavai College of Engineering
AI & Data Science Department
Batch-7
📧 Contact
GitHub: @lalithashreem
Repository: batch-7
📄 License
MIT License - Free to use and modify
🚀 Future Improvements
[ ] Add more advanced models (Gradient Boosting, XGBoost)
[ ] Hyperparameter tuning
[ ] Feature engineering
[ ] Model persistence (save/load)
[ ] Web API deployment
[ ] Visualization dashboards
