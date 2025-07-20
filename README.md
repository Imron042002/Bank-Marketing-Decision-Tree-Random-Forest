# Bank-Marketing-Decision-Tree-Random-Forest

#  Machine Learning Project - CRISP-DM Approach

##  Overview

This project applies machine learning techniques to a classification problem, following the **CRISP-DM** methodology. The goal is to train and evaluate a model that predicts a binary outcome using structured data.

---
## Data Source Bank Marketing Dataset

* From :http://archive.ics.uci.edu/ml/datasets/Bank+Marketing#  
 Kaggle: https://www.kaggle.com/datasets/henriqueyamahata/bank-marketing/data
* About:To predict customer response to subscription offers for term deposit products
* Record Count :  45211rows × 21 columns

---

##   Business Understanding

* **Objective**: To build a predictive model that classifies instances into one of two categories (`yes` or `no`), aiming to support decision-making processes in a business context.
* **Success Criteria**: High classification accuracy and meaningful model interpretation (e.g., via decision trees).

---

##   Data Understanding

* **Dataset**:

The dataset (bank.csv) contains information about bank clients, such as:

* Age, job, marital status, education

* Balance, duration of call, number of contacts

* Previous outcomes and more

* Target variable: y → Indicates if the client subscribed to the product (yes or no)

* **Key Steps**:

  * Use of `pandas` and `matplotlib` for exploration.
  * Visual inspection of distributions and possible class imbalances.

---

##   Data Preparation

* **Missing Values**: Checked and removed using `dropna()`.
* **Encoding**:

  * Categorical variables are encoded using `LabelEncoder` or dummy variables.
* **Splitting**:

  * Dataset is split into training and test sets using `train_test_split()` from scikit-learn.

---

##   Modeling

* **Model Used**: Decision Tree Classifier (`DecisionTreeClassifier` from `sklearn`).
* **Parameters**: Default or specified manually (e.g., `max_depth`, `criterion`).
* **Training**:

  * The model is trained on the preprocessed training data.

---

##   Evaluation

* **Metrics Used**:

  * Accuracy
  * Confusion Matrix
  * Classification Report (Precision, Recall, F1-score)
* **Visualization**:

  * Tree plotted using `plot_tree()` with feature and class names for interpretability.
* **Performance Summary**:

  * Model results are visualized and assessed for overfitting or underfitting.

---

##   Deployment (Optional/Future Scope)

* This project does not include deployment yet.
* For production, consider:

  * Exporting model using `joblib` or `pickle`
  * Wrapping in a Flask or FastAPI service
  * Frontend interface or API

---

##  Libraries Used

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`

---
![alt text](<Screenshot 2025-07-20 165707.png>)

# Example Results from the Project
* **From the ML.ipynb file**:

* Decision Tree:

Accuracy ≈ 0.87

Easy to understand (visualized with plot_tree)

May overfit the training data

* Random Forest:

Accuracy ≈ 0.90+

More stable predictions

Better generalization and overfitting control

Requires more time and computational resources

* **Summary**:
![alt text](<Screenshot 2025-07-20 170017.png>)

---
# Why Does the Decision Tree Only Use age and duration

* duration and age are used because they split the data most effectively at the top levels.

* Other features may be used deeper in the tree or might simply offer less predictive value.

* The default tree plot only shows the upper layers; not all features are visible.


---


---

    