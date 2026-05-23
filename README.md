# Emotion Classification from Facial Expressions

A Deep Learning based Emotion Detection project that classifies human facial expressions into different emotion categories using CNN and Transfer Learning models.

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

- The project uses the FER-2013 (Facial Expression Recognition) dataset.
- The dataset used for this task consists of 48x48 pixel grayscale images of faces. The faces have been automatically centered and scaled so that each face occupies a similar amount of space within the image. Note that the dataset is imbalanced, which poses a challenge for training accurate models.


# Models Used

The project includes training and evaluation of 4 different models.

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
- Macro F1-Score: 0.14 
- Weighted F1-Score: 0.17 

---

### Observations

The "Disgust" class showed very poor performance due to class imbalance.

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

---
### Observations

- Data augmentation helped reduce overfitting compared to the basic CNN model.
- The model achieved slightly better generalization performance.

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

