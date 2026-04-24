# Fashion MNIST Hyperparameter Tuning

## Description
This project implements an optimized MLP classifier for Fashion MNIST using hyperparameter tuning and cross-validation to find the best model configuration.

## Dataset
- **Source**: TensorFlow Keras `fashion_mnist`
- **Task**: 10-class image classification
- **Images**: 28x28 grayscale (10 clothing categories)

## Approach
1. **Data Loading**: Load Fashion MNIST dataset
2. **Preprocessing**:
   - Normalize pixel values to [0,1]
   - Flatten images to 784 features
   - Train/Validation/Test split (80/20)
   - StandardScaler normalization
3. **Baseline Models**:
   - Fixed learning rate
   - Cosine Decay learning rate schedule
4. **Hyperparameter Grid**:
   - Hidden layers: (64,), (128,), (256,128), (128,64), (256,128,64)
   - Optimizers: Adam, SGD
   - Batch sizes: 64, 128
   - Learning rates: 0.001, 0.01, 0.0005
5. **Cross-Validation**: StratifiedKFold (3 folds)
6. **Final Training**: Best configuration on full training data

## Results
- Comparative analysis: Fixed LR vs Cosine Decay
- Cross-validation results for each configuration
- Best model selection based on CV accuracy
- Final test set evaluation

## Key Metrics
- Accuracy
- Precision (macro)
- Recall (macro)
- Confusion matrix

## Technologies
- Python 3
- TensorFlow / Keras
- Scikit-learn
- Pandas, NumPy, Matplotlib

## Author
Zakaria Rebbah

## License
MIT