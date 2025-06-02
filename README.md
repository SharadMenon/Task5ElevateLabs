# 🫀 Heart Disease Prediction using Decision Tree and Random Forest

This project focuses on predicting the presence of heart disease based on clinical attributes using two machine learning models: **Decision Tree Classifier** and **Random Forest Classifier**. The analysis includes model training, overfitting control, accuracy comparison, feature interpretation, and cross-validation.

---

## 📌 Objective

To evaluate and compare the performance of Decision Tree and Random Forest algorithms for classifying whether a patient has heart disease based on medical parameters.

---

## 🗂️ Dataset

- **File Used**: `heart.csv`
- **Records**: 1025 patients
- **Features**: 13 clinical parameters (e.g., age, cholesterol, chest pain type, maximum heart rate)
- **Target Variable**: `target` (0 = no disease, 1 = disease)

---

## ✅ Tasks Performed

### 1. **Model Training:**
- Trained a **Decision Tree Classifier** on the dataset.
- Visualized the structure of the decision tree to understand its splits and depth.

### 2. **Overfitting Analysis:**
- Observed that the default Decision Tree achieved very high accuracy, suggesting potential overfitting.
- Controlled tree complexity by setting a maximum depth to generalize better and reduce overfitting.

### 3. **Random Forest Training:**
- Trained a **Random Forest Classifier** with multiple decision trees.
- Compared its performance to the single Decision Tree model for better generalization and robustness.

### 4. **Feature Importance:**
- Identified which clinical features contributed most to the prediction.
- Visualized feature importances from the Random Forest to gain medical insight.

### 5. **Cross-Validation:**
- Used 5-fold cross-validation to assess the stability and generalization of both models.
- Compared average validation scores to ensure consistency and mitigate data-split bias.

---

## 📊 Results & Insights

| Metric                     | Decision Tree | Random Forest |
|----------------------------|----------------|----------------|
| Accuracy on Test Set       | ~100%          | ~100%          |
| Cross-Validation Score     | ~1.00          | ~0.90+         |
| Overfitting Observed?      | Yes (Tree)     | Less (RF)      |
| Top Features Identified    | Chest Pain, Max Heart Rate, ST Depression, etc.

- The Decision Tree showed signs of **overfitting**, achieving perfect scores even with limited depth.
- Random Forest performed slightly better in terms of **generalization**, with slightly lower but more realistic cross-validation scores.
- **Feature importance** revealed that certain attributes, such as chest pain type and maximum heart rate, were strong predictors of heart disease.

---

## 📌 Conclusion

Both models performed well on this dataset, but due to the potential for overfitting in Decision Trees, the **Random Forest Classifier** is more reliable and generalizes better. This project demonstrates the importance of validating model performance using cross-validation and interpreting feature contributions for practical insights in medical data analysis.

---

## 🧠 Future Improvements

- Perform hyperparameter tuning with GridSearchCV
- Add ROC-AUC, precision-recall curves for deeper evaluation
- Apply data preprocessing like scaling or PCA
- Test with external validation datasets

---
