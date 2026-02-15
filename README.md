# **Heart Disease Prediction App**

## **a. Problem Statement**
Heart disease is one of the leading causes of death worldwide. Early detection and accurate prediction of heart disease risk can save lives by enabling timely medical intervention. The goal of this project is to build a **Streamlit web application** that allows users to test multiple machine learning models on heart disease data, evaluate their performance, and visualize results. The app provides an interactive interface for uploading test datasets, selecting models, and viewing evaluation metrics, confusion matrices, and classification reports.

---

## **b. Dataset Description** 
The dataset used is the **UCI Heart Disease dataset (heart.csv)**, which contains patient health records with attributes such as:

- **Age**: Patient’s age in years  
- **Sex**: Male (1) or Female (0)  
- **Chest Pain Type (cp)**: 0–3 categorical values  
- **Resting Blood Pressure (trestbps)**: mm Hg  
- **Cholesterol (chol)**: mg/dl  
- **Fasting Blood Sugar (fbs)**: >120 mg/dl (1 = true, 0 = false)  
- **Resting ECG (restecg)**: 0–2 categorical values  
- **Max Heart Rate Achieved (thalach)**  
- **Exercise Induced Angina (exang)**: 1 = yes, 0 = no  
- **ST Depression (oldpeak)**  
- **Slope of ST Segment (slope)**: 0–2 categorical values  
- **Number of Major Vessels (ca)**: 0–3  
- **Thalassemia (thal)**: 1 = normal, 2 = fixed defect, 3 = reversible defect  
- **Target**: 1 = heart disease present, 0 = no heart disease  

This dataset is widely used for benchmarking classification models in healthcare.

---

## **c. Models Used** 

Six machine learning models were trained and evaluated:

- **Logistic Regression**  
- **Decision Tree**  
- **k-Nearest Neighbors (kNN)**  
- **Naive Bayes**  
- **Random Forest (Ensemble)**  
- **XGBoost (Ensemble)**  

### **Comparison Table of Evaluation Metrics**

| **ML Model Name**          | **Accuracy** | **AUC**   | **Precision** | **Recall** | **F1**     | **MCC**    |
|-----------------------------|--------------|-----------|---------------|------------|------------|------------|
| Logistic Regression         | 0.809756     | 0.929810  | 0.761905      | 0.914286   | 0.831169   | 0.630908   |
| Decision Tree               | 0.985366     | 0.985714  | 1.000000      | 0.971429   | 0.985507   | 0.971151   |
| kNN                         | 0.863415     | 0.962905  | 0.873786      | 0.857143   | 0.865385   | 0.726935   |
| Naive Bayes                 | 0.829268     | 0.904286  | 0.807018      | 0.876190   | 0.840183   | 0.660163   |
| Random Forest (Ensemble)    | 1.000000     | 1.000000  | 1.000000      | 1.000000   | 1.000000   | 1.000000   |
| XGBoost (Ensemble)          | 1.000000     | 1.000000  | 1.000000      | 1.000000   | 1.000000   | 1.000000   |

---

## **d. Observations on Model Performance** 

| **ML Model Name**           | **Observation about model performance** |
|------------------------------|-----------------------------------------|
| Logistic Regression          | Performs well with balanced accuracy and recall. It is interpretable and useful for understanding feature importance, but slightly weaker than tree-based models. |
| Decision Tree                | Very strong performance with high accuracy and precision. However, it may overfit if not pruned properly. |
| kNN                          | Performs reasonably well but is sensitive to the choice of k and scaling of features. Slightly lower recall compared to Logistic Regression. |
| Naive Bayes                  | Performs decently with good recall, but assumes feature independence, which may not hold true in medical datasets. |
| Random Forest (Ensemble)     | Achieves perfect scores due to ensemble averaging, reducing overfitting and improving generalization. Highly reliable for this dataset. |
| XGBoost (Ensemble)           | Also achieves perfect scores, leveraging gradient boosting for superior performance. It is highly effective but computationally more intensive. |

---

