# 🚗 In-Vehicle Coupon Recommendation System

This project builds a machine learning model that predicts whether a user will **accept a coupon** while in a vehicle, using data that captures various contextual, demographic, and behavioral features. The model is particularly useful for personalized marketing strategies in smart mobility solutions.

---

## 📊 Model Performance

Using a **Tuned Random Forest Classifier**, the model achieved the following performance metrics:

- **Accuracy**: `0.744`
- **Precision**: `0.733`
- **Recall**: `0.850`
- **F1-Score**: `0.787`

These scores indicate a strong ability to identify coupon acceptances, with a high recall being especially valuable for ensuring fewer missed positives in a marketing context.

---

## 🧠 Problem Statement

Given contextual data such as time, weather, destination, and user demographics, predict whether a user will **accept** or **decline** a coupon.

---

## 📂 Dataset Overview

The dataset contains **12,684 rows** and **26 columns**, with features categorized as follows:

### 🔢 Numerical Features:
- `temperature`
- `has_children`
- `toCoupon_GEQ5min`
- `toCoupon_GEQ15min`
- `toCoupon_GEQ25min`
- `direction_same`
- `direction_opp`
- `Y` (Target Variable)

### 🔤 Categorical Features:
- `destination`
- `passanger`
- `weather`
- `time`
- `coupon`
- `expiration`
- `gender`
- `age`
- `maritalStatus`
- `education`
- `occupation`
- `income`
- `car`
- `Bar`
- `CoffeeHouse`
- `CarryAway`
- `RestaurantLessThan20`
- `Restaurant20To50`

### ❗ Missing Values:
- `car`: 99.1% missing → **dropped**
- Other features like `Bar`, `CoffeeHouse`, `CarryAway`, `RestaurantLessThan20`, `Restaurant20To50` had missing values handled via **imputation**

---

## ⚙️ Preprocessing

- Dropped the `car` column due to excessive missing data
- Handled missing values with **appropriate imputation strategies**
- Applied **one-hot encoding** to all categorical features
- Normalized numerical features (if needed)

---

## 🧪 Model Training

- Model Used: **Random Forest Classifier**
- Hyperparameter Tuning: **GridSearchCV**
- Train/Test Split Evaluation
- Evaluated using **classification report** and **performance metrics**
