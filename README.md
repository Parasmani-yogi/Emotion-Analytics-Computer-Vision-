# Emotion Classification from Facial Expressions

A Deep Learning-based Emotion Detection project that classifies human facial expressions into different emotion categories using CNN and Transfer Learning models.

---

## Project Overview

The objective of this project is to detect and classify emotions from facial expressions using Deep Learning techniques.

The model predicts the following emotions:

- Angry
- Disgust
- Fear
- Happy
- Sad
- Surprise
- Neutral

This project compares multiple Deep Learning architectures and analyzes their performance on the FER-2013 dataset.

---

# Dataset 

The project uses the FER-2013 (Facial Expression Recognition) dataset.

The dataset consists of 48x48 grayscale facial images. The faces are automatically centered and scaled to occupy a similar amount of space in each image. The dataset is imbalanced, which creates challenges during model training and affects minority emotion classes.

---

# Models Used

The project includes training 4 different models.

---

## Model 1 — Basic CNN

### Architecture

- Convolutional Neural Network (CNN)
- MaxPooling Layers
- Dropout Layers
- Fully Connected Dense Layers

### Performance

- Training Accuracy: 63.92%
- Validation Accuracy: 55.48%

### Observations

- The model learned basic facial features successfully.
- The "Disgust" class showed very poor performance due to class imbalance.
- Overfitting was observed during training.

---

## Model 2 — CNN with Data Augmentation

### Techniques Used

- Rotation
- Zoom
- Horizontal Flip
- Width/Height Shift

### Features

- Improved generalization
- Reduced overfitting
- Better robustness

### Performance

- Training Accuracy: 54.31%
- Validation Accuracy: 53.04%

### Observations

- Data augmentation helped reduce overfitting compared to the basic CNN model.
- The model achieved slightly better generalization performance.
- Performance improvement was limited because of dataset imbalance.

---

## Model 3 — Transfer Learning with VGG16

### Architecture

- Pre-trained VGG16 model
- Transfer Learning approach
- Custom Dense classification layers
- Softmax Output Layer
- Fine-tuning on FER-2013 dataset

### Features

- Pre-trained ImageNet weights
- Better feature extraction capability
- Faster convergence during training
- Improved facial pattern learning

### Performance

- Training Accuracy: 74.30%
- Validation Accuracy: 63.07%

### Observations

- Transfer Learning significantly improved training and validation accuracy compared to previous CNN models.
- The VGG16 model extracted facial features more effectively than custom CNN architectures.
- The model still struggled with minority classes like "Disgust" due to dataset imbalance.
- Overfitting was reduced, and the model showed better generalization capability on unseen data.

---

## Model 4 — Transfer Learning with ResNet50

### Architecture

- Pre-trained ResNet50 model
- Transfer Learning approach
- Residual Learning Architecture
- Custom Dense classification layers
- Softmax Output Layer

### Features

- Deep residual connections
- Better gradient flow during training
- Improved feature extraction
- Reduced vanishing gradient problem

### Performance

- Training Accuracy: 58.55%
- Validation Accuracy: 58.76%

### Observations

- ResNet50 achieved balanced training and validation accuracy with reduced overfitting.
- Residual connections helped the model learn deeper facial representations effectively.
- The "Disgust" class remained difficult to classify because of severe class imbalance and limited samples.
- Compared to earlier CNN models, ResNet50 provided more stable validation performance and better generalization.

---

# Final Selected Model

After comparing all models, the VGG16 Transfer Learning model was selected as the final model because it achieved the best overall performance.

### Final Model Performance

| Metric | Value |
|--------|--------|
| Training Accuracy | 74.30% |
| Validation Accuracy | 63.07% |

### Reason for Selection

- Highest validation accuracy among all models
- Better feature extraction capability
- Reduced overfitting
- Better generalization on unseen facial images

---

# Project Workflow

1. Data Collection
2. Data Preprocessing
3. Data Augmentation
4. Model Building
5. Model Training
6. Performance Evaluation
7. Emotion Prediction

---

# Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- OpenCV
- Scikit-learn

---
