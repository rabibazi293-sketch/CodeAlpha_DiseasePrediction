# Disease Prediction Model

## Project Overview
This project predicts whether a breast tumor is malignant (cancer) or benign (not cancer) using patient medical data. It was completed as Task 2 of the CodeAlpha Machine Learning internship.

## Dataset
Breast Cancer Wisconsin dataset from scikit-learn (569 records, 30 numeric features). The target is malignant = 1 and benign = 0. There are 357 benign and 212 malignant cases, so the data is slightly imbalanced. There are no missing values.

## Approach
1. Loaded and explored the data.
2. Flipped the target so that malignant = 1.
3. Split the data into 80% training and 20% testing.
4. Scaled the features using StandardScaler.
5. Trained three models: Logistic Regression, Random Forest and SVM.
6. Evaluated them using Precision, Recall, F1-Score and ROC-AUC.

## Results
 Model | Precision | Recall | F1-Score | ROC-AUC |
 Logistic Regression | 0.975 | 0.929 | 0.951 | 0.996 |
 Random Forest | 1.000 | 0.929 | 0.963 | 0.993 |
 SVM | 1.000 | 0.929 | 0.963 | 0.995 |

All three models performed very well. SVM was selected as the final model because it had the highest F1-score (tied with Random Forest) and a slightly higher ROC-AUC.

## Limitation
All three models have the same recall: each one missed 3 of the 42 malignant cases in the test set. In medical prediction, missing a malignant case is costly. The test set is also small (114 cases), so small differences between models should not be over-interpreted.

## Tools Used
Python, pandas, scikit-learn, matplotlib, Google Colab

## How to Run
Open the notebook in Google Colab or Jupyter and run all cells from top to bottom.
