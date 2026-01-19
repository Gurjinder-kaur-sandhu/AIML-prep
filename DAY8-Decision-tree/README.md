# Decision Tree Classification – Breast Cancer Dataset

## 📌 Project Overview

This project demonstrates how to build, train, and evaluate a **Decision Tree Classifier** using the **Breast Cancer dataset** from `scikit-learn`.
The goal is to understand the **working of Decision Trees**, handle **overfitting**, and evaluate model performance using standard metrics.

---

## 🎯 Objectives

* Understand the intuition behind Decision Trees
* Implement a Decision Tree Classifier step by step
* Analyze **overfitting** using different tree depths
* Evaluate the model using **accuracy** and **confusion matrix**

---

## 📂 Dataset

* **Name:** Breast Cancer Wisconsin Dataset
* **Source:** `sklearn.datasets.load_breast_cancer`
* **Classes:**

  * `0` → Malignant (cancer)
  * `1` → Benign (non-cancer)

---

## 🛠️ Technologies Used

* Python
* scikit-learn
* NumPy

---

## 🔁 Machine Learning Workflow

### 1️⃣ Load the Dataset

The Breast Cancer dataset is loaded using `load_breast_cancer()` from sklearn.

### 2️⃣ Feature and Target Selection

* **X** → Input features (tumor measurements)
* **y** → Target labels (malignant or benign)

### 3️⃣ Train-Test Split

The dataset is split into:

* 80% training data
* 20% testing data

This helps evaluate model performance on unseen data.

### 4️⃣ Model Building

A **DecisionTreeClassifier** is used with:

* `criterion = "gini"`
* Different values of `max_depth` to control overfitting

### 5️⃣ Model Training

The model is trained using the `.fit()` method on training data.

### 6️⃣ Prediction

Predictions are made on test data using `.predict()`.

### 7️⃣ Evaluation

Model performance is evaluated using:

* **Accuracy Score**
* **Confusion Matrix**

---

## 🌳 Overfitting Analysis

Decision Trees can easily overfit if they grow too deep.

### Experiments Performed:

* `max_depth = 2`

  * Model is very simple
  * May underfit
* `max_depth = 5`

  * Balanced complexity
  * Better generalization

### Key Observation:

> **Limiting tree depth helps reduce overfitting.**

The best depth is chosen based on **test accuracy**, not training accuracy.

---

## 📊 Evaluation Metrics

* **Accuracy Score:** Measures overall correctness
* **Confusion Matrix:** Shows detailed classification results

  * True Positives
  * True Negatives
  * False Positives
  * False Negatives

This is especially important for medical datasets.

---

## 🧠 Key Learnings

* Decision Trees split data based on feature conditions
* Gini Index measures impurity
* Deep trees can overfit
* Controlling `max_depth` improves generalization
* Confusion matrix provides better insight than accuracy alone

---

## ✍️ Conclusion

This project provides a clear understanding of how Decision Trees work, how overfitting occurs, and how to control it using tree depth. The Breast Cancer dataset makes this a practical and meaningful classification problem.

---

## 🚀 Future Improvements

* Tree visualization
* Hyperparameter tuning (`min_samples_split`, `min_samples_leaf`)
* Precision, Recall, and F1-score analysis
* Cross-validation

---

**Author:** Guri
**Purpose:** Machine Learning Fundamentals & Interview Preparation
