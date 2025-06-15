
## 🌲 Car Evaluation using Tree-Based Classification Models

### 🧩 Overview

This project aims to build a machine learning model to **classify cars into different acceptance categories** based on their features. We used the **Car Evaluation Database**, which contains attributes like buying price, maintenance cost, number of doors, passenger capacity, luggage boot size, and safety. We have explored and evaluated several **tree-based models** including **Decision Tree, Random Forest, AdaBoost, Gradient Boosting, ** and ** XGBoost** to determine which performs best in predicting car acceptance.

---

### 💼 Business Understanding

The primary stakeholder for this project would be a business or individual involved in the car industry, such as a car manufacturer, dealership, or review platform. The business problem is to automatically evaluate the acceptability of a car based on its characteristics. When customers buy a car, they evaluate multiple factors like price, safety, maintenance, and space. This project simulates that decision-making process using machine learning models to **predict car quality ratings**, which can be valuable for:

* Recommender systems in car sales platforms
* Quality prediction systems for auto manufacturers
* Filtering mechanisms for used car platforms

---

### 📊 Data Understanding

The dataset used for this analysis is the Car Evaluation Database. It contains 1728 instances and 7 attributes. The attributes are: 'buying', 'maint', 'doors', 'persons', 'lug_boot', 'safety', and the target variable 'class'. All attributes are categorical.
The timeframe of the data is not explicitly mentioned in the dataset description, but it is derived from a model developed in 1990. This suggests the data reflects car evaluation criteria from that era, which could be a potential limitation if applying the findings to current car evaluations without considering evolving consumer preferences and safety standards.
The EDA revealed that the dataset is clean with no missing values. However, a significant class imbalance exists in the target variable 'class', with 'unacc' being the most frequent category and 'good' and 'vgood' being less represented. Visualizations of feature distributions and their relationship with the target class provided initial insights into how different car attributes relate to its acceptance.

![image](https://github.com/user-attachments/assets/bf8b19ee-07b7-484d-83d2-769137f38ab8)


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

  * **Decision Tree Classifier** :- A single decision tree with criterion='entropy' and max_depth=3 was trained. Evaluated using accuracy.
  * **Random Forest Classifier** :- An ensemble of 100 decision trees (n_estimators=100). Evaluated using accuracy.
  * **AdaBoost Classifier**: An ensemble using DecisionTreeClassifier with max_depth=10 as the base estimator and n_estimators=100. Evaluated using accuracy, classification report, and confusion matrix.
  * **Gradient Boosting Classifier** :- An ensemble with n_estimators=100, learning_rate=0.1, and max_depth=3. Evaluated using accuracy, classification report, and confusion matrix.
  * **XGBoost Classifier** :- An optimized gradient boosting implementation with objective='multi:softmax', num_class=len(set(y_train_encoded)), n_estimators=100, learning_rate=0.1, and max_depth=3. Evaluated using accuracy, classification report, and confusion matrix.


* **Hyperparameters Tuned**:

  * `n_estimators`, `max_depth`, `random_state`
* **Evaluation Metrics**:

  * Accuracy
  * Confusion Matrix
  * Classification Report (Precision, Recall, F1-score)
* **Results**:

  * AdaBoost achieved the highest accuracy (~97.4%) among the tested models

---

### 📌 Conclusion

Based on the evaluation metrics, AdaBoost achieved the highest accuracy (~97.4%) among the tested models, suggesting it is the most effective at classifying car acceptance on this dataset. Gradient Boosting and Random Forest also performed well but were slightly less accurate than AdaBoost. The single Decision Tree had significantly lower accuracy.

* Tree-based models effectively learned classification rules from structured categorical data.
* **AdaBoost outperformed the other Tree based Models**, showing better robustness to overfitting.
* This project demonstrates a practical example of **interpretable models** in decision-making systems for categorical data.

---
