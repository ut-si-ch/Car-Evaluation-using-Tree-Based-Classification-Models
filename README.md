
## 🌲 Car Evaluation using Tree-Based Classification Models

### 🧩 Overview

This project applies **tree-based supervised learning algorithms** to classify car acceptability based on categorical features. The models help identify which vehicle configurations are acceptable, good, or unacceptable for potential buyers. Techniques used include **Decision Trees** and **Random Forests**.

---

### 💼 Business Understanding

When customers buy a car, they evaluate multiple factors like price, safety, maintenance, and space. This project simulates that decision-making process using machine learning models to **predict car quality ratings**, which can be valuable for:

* Recommender systems in car sales platforms
* Quality prediction systems for auto manufacturers
* Filtering mechanisms for used car platforms

---

### 📊 Data Understanding

* **Dataset**: UCI Car Evaluation Dataset
* **Size**: 1,728 rows × 7 features
* **Features**:

  * Buying, Maintenance, Doors, Persons, Luggage Boot, Safety
  * Target: Car Evaluation (`class`) – {unacc, acc, good, vgood}
* **Key Characteristics**:

  * All features are categorical
  * Balanced distribution across classes
  * No missing or null values

---

### 🤖 Modeling and Evaluation

* **Preprocessing**:

  * Label Encoding for all categorical columns
* **Models Used**:

  * **Decision Tree Classifier**
  * **Random Forest Classifier**
* **Hyperparameters Tuned**:

  * `n_estimators`, `max_depth`, `random_state`
* **Evaluation Metrics**:

  * Accuracy
  * Confusion Matrix
  * Classification Report (Precision, Recall, F1-score)
* **Results**:

  * Random Forest achieved higher accuracy and generalization compared to single tree

---

### 📌 Conclusion

* Tree-based models effectively learned classification rules from structured categorical data.
* **Random Forest outperformed the Decision Tree**, showing better robustness to overfitting.
* This project demonstrates a practical example of **interpretable models** in decision-making systems for categorical data.

---
