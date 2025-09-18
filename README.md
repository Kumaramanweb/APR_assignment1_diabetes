# Diabetes Classification using SVM

This project implements a **Support Vector Machine (SVM)** to classify diabetes cases based on patient health data. It includes preprocessing, model training, evaluation, and visualization.

---

## Introduction to SVM
**Support Vector Machine (SVM)** is a supervised machine learning algorithm used for classification and regression tasks.  
- It works by finding the **optimal hyperplane** that separates data points of different classes.  
- SVM can handle **linear and non-linear** data using kernel functions such as RBF, polynomial, and linear kernels.  
- Effective for datasets with **high-dimensional features** and works well for small to medium datasets.

---

## Dataset Structure
The dataset contains patient health information and a target column (`CLASS`) indicating diabetes status.  

| Column Name    | Description                             |
|----------------|-----------------------------------------|
| `Gender`       | Male/Female (categorical)               |
| Health Features| Numeric indicators (e.g., glucose, BMI)|
| `CLASS`        | Target variable for classification      |
| `ID`           | Dropped (not used)                      |
| `No_Pation`    | Dropped (not used)                      |

**Preprocessing Steps:**  
- Strip whitespace from string columns  
- Encode categorical columns (`Gender`, `CLASS`)  
- Standardize features using `StandardScaler`  

---

## Algorithm Overview
1. **Data Preprocessing**: Clean dataset, encode categorical variables, drop irrelevant columns.  
2. **Train-Test Split**: Split dataset into 80% training and 20% testing sets using stratification.  
3. **Feature Scaling**: Standardize features for better SVM performance.  
4. **SVM Training**: Train `SVC` model with RBF kernel.  
5. **Prediction & Evaluation**: Predict test set, compute **confusion matrix** and **classification report**.  
6. **Visualization**: Reduce features to 2D using PCA and plot predicted classes.

---

## 🚀 How to Run

1. Clone this repository:

   bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   

2. Install dependencies:

   bash
   pip install -r requirements.txt
   

3. Open and run the notebook:

   bash
   jupyter notebook Apr_Assignment.ipynb
   

---

## ✅ Conclusion

- SVM was successfully applied to classify wine quality.
- The model performs reasonably well but shows class imbalance issues (most samples are medium quality).
- Future improvements could include *class balancing techniques, **parameter tuning*, or testing other algorithms (Random Forest, XGBoost).
