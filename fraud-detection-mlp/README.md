# Fraud Detection with MLP

## Description
This project implements a multi-layer perceptron (MLP) for fraud detection using a credit card transaction dataset. The model performs binary classification to identify fraudulent transactions.

## Dataset
- **Source**: `dataset_fraude.csv`
- **Task**: Binary classification (fraud vs normal)
- **Features**: Transaction attributes
- **Target**: `label_fraud` column

## Approach
1. **Data Loading & Exploration**: Load the dataset and analyze the target variable distribution
2. **Preprocessing**: Feature separation, train/test split
3. **Model Architecture**: MLP with Keras/TensorFlow
4. **Training & Evaluation**: Train the model and evaluate with confusion matrix, precision, recall, F1-score

## Results
- Binary classification performance metrics
- Confusion matrix visualization
- Classification report with precision/recall per class

## Technologies
- Python 3
- TensorFlow / Keras
- Scikit-learn
- Pandas, NumPy, Matplotlib

## Author
Zakaria Rebbah

## License
MIT