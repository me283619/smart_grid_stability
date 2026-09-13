# ⚡ Smart Grid Stability Prediction

## 📌 Overview
This project predicts **electrical grid stability** using **Machine Learning** and **Deep Learning** models.  
We use the *Smart Grid Stability Augmented Dataset* and apply multiple classifiers, then combine them with a **Stacking Classifier** to achieve high accuracy.

---

## 🛠️ Steps

1. **Data Loading & Exploration**
   - Load CSV dataset with `pandas`.
   - Explore shape, columns, and info.
   - Encode target column `stabf` using `LabelBinarizer`.

2. **Preprocessing**
   - Split data into features (X) and target (y).
   - Train/Test split with stratification.
   - Standardize features using `StandardScaler`.

3. **Models**
   - Logistic Regression (balanced).
   - Random Forest Classifier.
   - Decision Tree Classifier.
   - XGBoost Classifier (with `scale_pos_weight`).
   - Neural Network (Keras Sequential).

4. **Stacking**
   - Combine all models using `StackingClassifier`.
   - Final estimator: Logistic Regression.
   - Train with cross-validation and predict test set.

5. **Evaluation**
   - Accuracy on train/test sets.
   - Confusion Matrix.
   - Classification Report (Precision, Recall, F1-score).
   - Heatmap visualization with `seaborn`.
     
 6. **📊 Results**

    The stacked model achieved **very high accuracy**:
    - Training Accuracy:** 99.96%  
    - Testing Accuracy:** 98.59%  


8. **Model Saving**
   - Save final stacked model using `dill` into `final project.pkl`.

---

## 📊 Results
- Achieved high accuracy on test data.
- Confusion matrix and classification report show strong performance.
- Neural Network + Ensemble improved prediction reliability.

---

## 💻 Requirements
- Python 3.8+
- Libraries:
  - pandas  
  - numpy  
  - scikit-learn  
  - xgboost  
  - scikeras  
  - tensorflow / keras  
  - seaborn  
  - dill  

Install all dependencies:
```bash
pip install -r requirements.txt
