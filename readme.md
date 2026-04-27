# 🤖 Model Validation, Overfitting Control & Hyperparameter Tuning (House Price Prediction System)

## 📌 Project Overview

This project focuses on improving machine learning model performance using advanced techniques such as **model validation, overfitting detection, and hyperparameter tuning**.
It builds upon previous tasks and demonstrates a complete optimization workflow.

---

## 📊 Dataset Information

* **Dataset:** California Housing Dataset
* **Total Records:** 20,640
* **Features:** 8 numerical features

### 🔑 Features:

* MedInc (Median Income)
* HouseAge
* AveRooms
* AveBedrms
* Population
* AveOccup
* Latitude
* Longitude

### 🎯 Target Variable:

* **MedHouseVal** (Median House Value)

---

## ⚙️ Workflow

### 1️⃣ Data Preprocessing

* Train-Test Split (80/20)
* Feature Scaling using **StandardScaler**
* Avoided **data leakage** by scaling after split

---

### 2️⃣ Overfitting Detection

* Decision Tree used as baseline model
* Compared **Train RMSE vs Test RMSE**

📌 Observation:

* Train RMSE ≈ 0
* Test RMSE significantly higher
  ➡️ Indicates **overfitting**

---

### 3️⃣ Cross Validation

* Applied **K-Fold Cross Validation**
* Used `cross_val_score`

📌 Purpose:

* Evaluate model stability
* Avoid reliance on a single train-test split

---

### 4️⃣ Hyperparameter Tuning

* Used **GridSearchCV**

#### 🔧 Parameters Tuned:

* `max_depth`
* `min_samples_split`

📌 Best Parameters:

* max_depth = 10
* min_samples_split = 10

---

## 📈 Model Performance

### 🔥 Tuned Decision Tree:

* **RMSE:** 0.645
* **R² Score:** 0.682

---

## 📊 Model Comparison

| Model                   | RMSE      | R² Score  |
| ----------------------- | --------- | --------- |
| Linear Regression       | 0.745     | 0.576     |
| Ridge Regression        | 0.745     | 0.576     |
| **Tuned Decision Tree** | **0.645** | **0.682** |

---

## 📊 Visualizations

* Actual vs Predicted Plot
* Residual Plot
* Before vs After Tuning Comparison

---

## 🧠 Key Concepts Learned

* Overfitting vs Underfitting
* Bias-Variance Tradeoff
* Cross Validation
* Hyperparameter Tuning
* Model Generalization

---

## ✅ Conclusion

* Initial Decision Tree model suffered from **overfitting**
* Cross-validation revealed instability
* Hyperparameter tuning significantly improved performance
* **Tuned Decision Tree** selected as final model

---

## 🚀 Future Improvements

* Random Forest Regressor
* Gradient Boosting (XGBoost)
* Feature Engineering
* Outlier Handling

---

## 🛠️ Tech Stack

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

---

## 📌 How to Run

```bash
git clone https://github.com/Prashant517/Model-Validation-Overfitting-Control-Hyperparameter-Tuning-House-Price-Prediction-System.git
cd Model-Validation-Overfitting-Control-Hyperparameter-Tuning-House-Price-Prediction-System
pip install -r requirements.txt
jupyter notebook cross_validation_based_evaluation.ipynb
```


