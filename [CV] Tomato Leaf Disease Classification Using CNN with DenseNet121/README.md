# Tomato Leaf Disease Classification Using CNN with DenseNet121

## Introduction

This project was developed as part of the *Digital Image Processing* course assignment at Universitas Indonesia. The goal is to build a Convolutional Neural Network (CNN)-based model using DenseNet121 architecture to classify various types of tomato leaf diseases. I completed this project individually.

## Motivation

Tomato crops are highly valuable in Indonesia, but their productivity is often threatened by leaf diseases that are difficult to identify visually. Misdiagnosis leads to excessive pesticide use, reduced yields, and financial loss for farmers. This project aims to provide an accurate and automated solution for disease detection using deep learning and image-based classification.

## Data

We used the **Tomato Leaf Disease Dataset** from PlantVillage (available on Kaggle), which includes 14,529 labeled images across 10 classes, including both healthy leaves and leaves infected with diseases like Early Blight, Late Blight, Yellow Leaf Curl Virus, etc.

- Total classes: 10  
- Image size standardized to: 224×224 pixels  
- Dataset split: 80% training, 20% validation  

## Methodology

### Model
- **Base architecture**: DenseNet121 (pre-trained on ImageNet)
- **Modifications**:
  - GlobalAveragePooling
  - Dropout (0.3)
  - Dense softmax layer for 10-class output
- **Training strategy**:
  - Stage 1: Transfer Learning (base model frozen)
  - Stage 2: Fine-tuning (unfreezing top layers)

### Preprocessing
- Image resizing and normalization
- Applied `preprocess_input` specific to DenseNet
- Data augmentation handled via `ImageDataGenerator`

### Training Details
- Optimizer: Adam  
- Learning rate: 1e-4 (initial), 1e-5 (fine-tuning)  
- Loss function: Categorical Crossentropy  
- Epochs: 10 (initial) + 5 (fine-tuning)

## Results

- **Final validation accuracy**: **96.18%**
- **Validation loss**: 0.1172
- Test images (e.g., Early Blight, Late Blight) were predicted with over 96% confidence
- Confusion matrix and learning curves showed high stability and low overfitting

## Conclusion

The CNN model based on DenseNet121 achieved high performance in classifying tomato leaf diseases. The use of transfer learning significantly improved training efficiency. This model could potentially be deployed as part of a mobile or web-based disease detection tool to support farmers in early diagnosis and targeted treatment.

## Future Work

- Evaluate model performance on images from different lighting or environmental conditions
- Extend to real-time detection in field scenarios using mobile devices
- Consider lightweight models for edge deployment

