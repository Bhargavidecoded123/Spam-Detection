# Spam Detection using Cost-Sensitive Machine Learning

This project implements a cost-sensitive spam detection system using the UCI Spambase dataset. The focus is on minimizing misclassification costs, especially false negatives, which are considered 10 times more costly than false positives. Multiple supervised learning models were built and evaluated using nested cross-validation and robust classification metrics.

## Dataset

- **Source:** [UCI Machine Learning Repository - Spambase Dataset](https://archive.ics.uci.edu/ml/datasets/spambase)
- **Records:** 4,601 email samples
- **Attributes:** 57 continuous features extracted from email content, plus 1 binary target label (1 = spam, 0 = not spam)

## Models Implemented

- Logistic Regression
- k-Nearest Neighbors (kNN)
- Decision Tree
- Linear Regression (for classification via thresholding)
- Ensemble Methods (Bagging, Boosting)
- Neural Network
- Support Vector Regression (SVR with classification logic)

## Methodology

- Preprocessing:
  - Feature scaling (MinMaxScaler)
  - Train-validation-test split (60-20-20)
- Cost-sensitive modeling:
  - Misclassification cost ratio set at **10:1 (FN:FP)**
- Model selection:
  - Nested cross-validation (5-fold inner loop + outer loop)
  - Hyperparameter tuning using `GridSearchCV`
- Performance metrics:
  - Accuracy, Precision, Recall, F1-score, ROC-AUC
  - Average Misclassification Cost
  - ROC and Lift Charts

## Key Results

- Cost-sensitive modeling significantly reduced the average misclassification cost compared to baseline models.
- Models like Decision Trees and Ensemble methods performed best in terms of balancing sensitivity and cost.
- ROC-AUC values showed strong separability across multiple models.

## Project Structure
Spam-Detection.ipynb #Main notebook with all the code and results
README.md #Project Documantation

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Bhargavidecoded123/Spam-Detection.git
   cd Spam-Detection

2. Open the notebook
3. Ensure you have the required python packages:
   ```bash
   pip install -r requirements.txt  
