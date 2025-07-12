Objective: To identify fraudulent credit card transactions using machine learning models, with a focus on handling extreme class imbalance.

Dataset:Public dataset containing 284,807 transactions with anonymized features (V1–V28 via PCA), transaction amount, and a binary fraud label.

Highly imbalanced: only ~0.17% fraud cases.

Techniques Used:
->Data Preprocessing:
->Feature scaling (StandardScaler)
->Dropped irrelevant features like Time
->Addressed class imbalance using SMOTE oversampling

Models Trained:
-> Logistic Regression – baseline linear model
-> Random Forest – ensemble-based decision tree model
-> XGBoost – optimized gradient boosting model

Evaluation Metrics:
Accuracy alone isn't enough — so I focused on precision, recall, F1-score, and confusion matrix to ensure fraud cases were properly identified.

Results:
->Achieved up to 94% accuracy, with significantly improved recall for fraud detection after applying undersampling on both valid and fraud transaction and concatenation to create new dataset.
->Compared performance across models to find the best balance between performance and interpretability.
