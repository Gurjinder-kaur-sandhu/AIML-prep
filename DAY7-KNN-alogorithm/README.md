# K-Nearest Neighbors (KNN) – Machine Learning

## 📌 Overview

This repository contains a **simple and beginner-friendly implementation of the K-Nearest Neighbors (KNN)** algorithm using **scikit-learn**.

The goal of this project is to understand **how KNN works in practice**, not just theory.

---

## 🧠 What does this algorithm do? (Simple Explanation)

KNN works like this:

> **“Show me your nearest neighbors, and I’ll decide based on them.”**

When a new data point comes:

1. The algorithm finds the **K closest data points** from the training data.
2. It checks their classes.
3. The class with the **majority vote** becomes the prediction.

📌 **Key line:**
**KNN predicts the class based on the majority of its nearest neighbors.**

---

## 🔢 Role of K

* **K** = number of neighbors to consider
* Small K → sensitive to noise
* Large K → smoother predictions

Common values: **3, 5, 7**

---

## 📏 Distance Used

* **Euclidean Distance**
* Since distance is used, **feature scaling is mandatory**

---

## ⚠️ Why StandardScaler is Important

KNN is a **distance-based algorithm**.
If features are on different scales, distance calculation becomes incorrect.

📌 Rule:

> Distance-based algorithms **must be scaled**
> (KNN, K-Means, SVM)

---

## 🗂 Dataset

* **Breast Cancer Dataset** (from `sklearn.datasets`)
* Binary classification problem

---

## 🔁 Machine Learning Workflow

1. Load dataset
2. Split into features (X) and target (y)
3. Train-test split
4. Feature scaling using `StandardScaler`
5. Train KNN model
6. Make predictions
7. Evaluate accuracy

---

## 🧪 Implementation

### Requirements

```bash
pip install scikit-learn
```

### Code

```python
from sklearn.datasets import load_breast_cancer
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.neighbors import KNeighborsClassifier
from sklearn.metrics import accuracy_score

# Load dataset
data = load_breast_cancer()
X = data.data
y = data.target

# Train-test split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Feature scaling
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

# KNN model
knn = KNeighborsClassifier(n_neighbors=5)
knn.fit(X_train, y_train)

# Prediction
y_pred = knn.predict(X_test)

# Accuracy
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)
```

---

## 📊 Output

* The model predicts whether the tumor is **malignant or benign**
* Accuracy is printed at the end

---

## ✅ Key Takeaways

* KNN is a **lazy learner**
* No training phase, only comparison
* Simple but powerful
* Works best on small to medium datasets

---

## 🚀 Future Improvements

* Try different values of **K**
* Apply KNN on **Iris dataset**
* Visualize decision boundaries
* Compare with Logistic Regression

---

## 👤 Author

**Gurjinder kaur sandhu**
Machine Learning  Learner

---

⭐ If you found this helpful, give the repo a star!
