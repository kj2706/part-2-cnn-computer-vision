# Part 2: CNN Computer Vision Project

## Project Overview

This project implements a Convolutional Neural Network (CNN) for manufacturing defect detection using image classification techniques. The model classifies product surface images into different defect categories such as normal, scratch, dent, and stain.

The project demonstrates the complete deep learning workflow including:
- Dataset exploration
- Image preprocessing
- CNN model creation
- Model training and evaluation
- Prediction visualization
- Business use case mapping

---

# Dataset Description

The dataset contains manufacturing product surface images divided into four classes:

- normal
- scratch
- dent
- stain

Each image belongs to one category representing the defect type present on the product surface.

---

# Task 1: Problem Identification

## Selected Problem Type:
Image Classification

### Explanation:
This dataset represents an image classification problem because each image is assigned a single class label representing the type of defect present on the product surface.

The CNN model predicts one class for the entire image among:
- normal
- scratch
- dent
- stain

### Why Other Problem Types Are Not Suitable

#### Object Detection
Object detection is not suitable because the dataset does not contain bounding box annotations for locating defects.

#### Semantic Segmentation
Semantic segmentation is not suitable because the dataset does not contain pixel-wise masks.

#### Instance Segmentation
Instance segmentation is not suitable because the dataset does not contain separate instance masks for defects.

### Conclusion
Therefore, the dataset is best categorized as an Image Classification problem.

---

# Task 2: Dataset Exploration

## Number of Classes
The dataset contains 4 classes:
- normal
- scratch
- dent
- stain

## Number of Images per Class
The number of images in each class was analyzed using Python during dataset exploration.

## Sample Images
Sample images from each class were displayed to understand visual differences between defect categories.

## Image Dimensions
Image dimensions were checked using the PIL library to ensure proper preprocessing before CNN training.

## Dataset Imbalance
The dataset was analyzed to determine whether all classes contain similar numbers of images. Balanced datasets improve model performance and reduce prediction bias.

---

# Task 3: Image Preprocessing

## Objective
Image preprocessing is performed before training the CNN model.

### Preprocessing Steps:
- Resizing images to a fixed size
- Normalizing pixel values
- Splitting data into training and testing sets
- Applying image augmentation techniques

### Resizing
All images are resized to:
128 × 128 pixels

This ensures consistent input dimensions for the CNN.

### Normalization
Pixel values are normalized from:
0–255 → 0–1

Normalization improves model convergence and training stability.

### Train-Test Split
The dataset is divided into:
- 80% Training Data
- 20% Validation/Test Data

### Data Augmentation
Image augmentation techniques such as:
- rotation
- zoom
- horizontal flipping

are applied to improve model generalization and reduce overfitting.

---

# Task 4: CNN Model Creation

## Objective
A Convolutional Neural Network (CNN) model is developed for manufacturing defect classification.

## CNN Architecture

The CNN model includes:

### Convolution Layers
Used to extract image features such as edges, textures, and patterns.

### Activation Function
ReLU activation function is used to introduce non-linearity.

### Pooling Layers
MaxPooling layers reduce feature dimensions and computational complexity.

### Flatten Layer
Converts feature maps into a one-dimensional vector.

### Dense Layers
Used for classification learning.

### Output Layer
Softmax activation is used for multi-class classification with 4 output classes.

---

# Task 5: Model Training and Evaluation

## Model Training
The CNN model was trained using the preprocessed image dataset.

## Evaluation Metrics

### Training Accuracy and Loss
Training accuracy and loss were monitored during model training.

### Validation Accuracy and Loss
Validation metrics were used to evaluate model generalization.

### Testing Performance
Model performance was evaluated on validation/testing data.

### Confusion Matrix
A confusion matrix was generated to analyze prediction performance across all classes.

### Sample Predictions
The trained model was tested on sample images to visualize predicted defect classes.

---

# Results

The project generated the following outputs:

## Accuracy and Loss Curves
Stored in:
results/accuracy_loss_curves.png

## Confusion Matrix
Stored in:
results/confusion_matrix.png

## Sample Prediction Outputs
Stored in:
sample_predictions/prediction_outputs.png

---

# Task 6: CNN Concept Explanation

## What is Convolution?

Convolution is a mathematical operation used in CNNs to extract important image features such as edges, textures, and shapes. Small filters called kernels move across the image and detect meaningful visual patterns.

## Why is Pooling Used?

Pooling reduces the size of feature maps generated by convolution layers.

Benefits of pooling:
- reduces computation
- reduces memory usage
- prevents overfitting
- improves feature robustness

Max Pooling is commonly used because it preserves the most important features.

## Why is ReLU Commonly Used in CNNs?

ReLU (Rectified Linear Unit) is an activation function defined as:

f(x) = max(0, x)

It converts negative values into zero while keeping positive values unchanged.

Benefits of ReLU:
- faster training
- reduces vanishing gradient problem
- improves model performance
- introduces non-linearity

## Why are CNNs Better than Regular Feed-Forward Networks for Image Data?

CNNs are specifically designed for image processing tasks.

Advantages of CNNs:
- automatic feature extraction
- fewer parameters
- better image understanding
- preserves spatial relationships
- higher accuracy for image classification

Regular feed-forward networks cannot efficiently process spatial image information.

---

# Task 7: Business Use Case Mapping

## Manufacturing Industry Use Case

CNN-based computer vision systems are widely used in manufacturing industries for automated quality inspection.

The trained CNN model can automatically detect product defects such as:
- scratches
- dents
- stains
- damaged surfaces

using images captured from production lines.

### Benefits:
- improves product quality
- reduces manual inspection effort
- minimizes human error
- increases production efficiency
- reduces manufacturing costs
- enables real-time defect detection

### Industries Using CNN-Based Inspection:
- automobile manufacturing
- electronics production
- textile industries
- packaging industries
- metal surface inspection

CNN-based computer vision systems are important components of smart manufacturing and industrial automation.

---

# Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- PIL

# Conclusion

This project successfully demonstrates the implementation of a CNN-based image classification system for manufacturing defect detection. The CNN model can classify product surface images into different defect categories and can be applied in real-world industrial quality inspection systems.