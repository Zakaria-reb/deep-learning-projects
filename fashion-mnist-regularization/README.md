# Fashion MNIST Classification with Regularization

## Description
This project implements an MLP classifier for Fashion MNIST dataset with various regularization techniques (L1, L2, L1_L2).

## Dataset
- **Source**: TensorFlow Keras `fashion_mnist`
- **Task**: 10-class image classification
- **Images**: 28x28 grayscale (10 clothing categories)

## Approach
1. **Data Loading**: Load Fashion MNIST dataset
2. **Preprocessing**: Normalize pixel values to [0,1], flatten images
3. **Regularization Experiments**:
   - L1 regularization (Lasso)
   - L2 regularization (Ridge)
   - L1_L2 regularization (Elastic Net)
4. **Model Training**: MLP with different regularizers
5. **Comparison**: Compare regularization techniques impact

## Results
- Classification accuracy comparison
- Effect of regularization on overfitting prevention
- Confusion matrix and classification reports

## Technologies
- Python 3
- TensorFlow / Keras
- Scikit-learn
- Pandas, NumPy, Matplotlib

## Author
Zakaria Rebbah

## License
MIT