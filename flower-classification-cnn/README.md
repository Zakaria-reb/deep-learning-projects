# Flower Classification with CNN and Transfer Learning

## Description
This project implements image classification for the TF Flowers dataset using two approaches:
1. **CNN from scratch**: Custom convolutional neural network
2. **Transfer Learning**: Fine-tuned MobileNetV2 pre-trained on ImageNet

## Dataset
- **Source**: TensorFlow Datasets `tf_flowers`
- **Classes**: 5 (daisy, dandelion, roses, sunflowers, tulips)
- **Images**: Variable size, RGB color

## Part I: CNN from Scratch

### Approach
1. **Data Loading**: Load tf_flowers dataset
2. **Preprocessing**:
   - Resize all images to 128x128
   - Normalize to [0,1]
   - Train/Val/Test split (70/15/15)
3. **Data Augmentation**:
   - RandomFlip
   - RandomRotation(0.1)
   - RandomZoom(0.1)
4. **Model Architecture**:
   - Conv2D(32) → MaxPool → Conv2D(64) → MaxPool → Conv2D(128) → MaxPool
   - GlobalAveragePooling2D
   - Dense(128) + Dropout(0.4)
   - Dense(5, softmax)
5. **Training**: EarlyStopping, ReduceLROnPlateau
6. **Evaluation**: Accuracy, Confusion Matrix, Classification Report

## Part II: Transfer Learning

### Approach
1. **Base Model**: MobileNetV2 (ImageNet weights)
2. **Feature Extraction**: Freeze base model layers
3. **Custom Head**:
   - GlobalAveragePooling2D
   - Dense(128) + Dropout(0.5)
   - Dense(5, softmax)
4. **Fine-tuning**: Train only custom layers
5. **Comparison**: Scratch vs Transfer Learning

## Results
- CNN from scratch: ~70% accuracy
- Transfer Learning: ~85% accuracy
- Transfer learning significantly outperforms training from scratch

## Key Insights
- Transfer learning leverages general image features
- Pre-trained models need less data to generalize
- MobileNetV2 is efficient for mobile deployment

## Technologies
- Python 3
- TensorFlow / Keras
- TensorFlow Datasets
- Scikit-learn
- Seaborn, Matplotlib

## Author
Zakaria Rebbah

## License
MIT