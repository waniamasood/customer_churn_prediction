
# Customer Churn Prediction (Bank Customers)

## 📌 Objective
The goal of this project is to predict which bank customers are likely to leave (churn) using the **Churn Modelling Dataset**.  
By analyzing customer demographics, account details, and banking activity, we can identify high-risk customers and take proactive retention measures.

---

## 📂 Dataset
**Name:** Churn Modelling Dataset  
**Target Variable:** `Exited`  
- `1` → Customer has left the bank  
- `0` → Customer has stayed with the bank  

**Key Features:**
- `Geography` → Customer’s country (France, Spain, Germany)
- `Gender` → Male or Female
- `Age`, `Balance`, `CreditScore`, `EstimatedSalary`
- Banking activity details (`Tenure`, `NumOfProducts`, `HasCrCard`, `IsActiveMember`)

---

## 🛠️ Skills Demonstrated
- Data Cleaning & Preprocessing
- Categorical Encoding (Label Encoding & One-Hot Encoding)
- Train-Test Split
- Supervised Classification (Random Forest)
- Model Evaluation (Accuracy, Precision, Recall, F1-score)
- Feature Importance Analysis

---

## 🚀 Steps Performed

### 1️⃣ Load & Explore Data
- Read CSV into Pandas DataFrame
- Removed unnecessary columns: `RowNumber`, `CustomerId`, `Surname`
- Checked for missing values

### 2️⃣ Encode Categorical Variables
- **Label Encoding** for `Gender` (Male=1, Female=0)
- **One-Hot Encoding** for `Geography` (drop first to avoid dummy trap)

### 3️⃣ Split Data
- Features: All columns except `Exited`
- Target: `Exited`
- Train-Test Split (80% training, 20% testing)

### 4️⃣ Model Training
- Used **RandomForestClassifier** (scikit-learn)
- Random seed set to ensure reproducibility

### 5️⃣ Model Evaluation
- Accuracy Score
- Confusion Matrix
- Classification Report (Precision, Recall, F1-score)

### 6️⃣ Feature Importance
- Plotted top features affecting churn
- Helps understand what influences customer decisions

---

## 📊 Results
- **Accuracy:** ~ (Depends on training run)
- **Top Influencing Features:** Balance, Age, Number of Products, Is Active Member, Geography

---

## 🖥️ Example Usage
```python
# Train and predict
model.fit(X_train, y_train)
y_pred = model.predict(X_test)

# Evaluate
print(accuracy_score(y_test, y_pred))
````

---

## 📌 Insights

* Customers with **low activity** and **high balance** were more likely to churn.
* **Geography** and **Age** played a significant role in predicting churn.
* Retention campaigns can be targeted at high-risk groups.

---

## 📚 Requirements

* Python 3.x
* Pandas
* scikit-learn
* Matplotlib / Seaborn

Install dependencies:

```bash
pip install pandas scikit-learn matplotlib seaborn
```

---

