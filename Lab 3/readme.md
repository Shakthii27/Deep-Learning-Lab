# Deep Learning Lab 3

## CNN for CIFAR-10 Image Classification

This experiment implements a Convolutional Neural Network (CNN) for image
classification using the CIFAR-10 dataset and PyTorch.

## Objectives

- Load and preprocess the CIFAR-10 dataset.
- Understand convolution using different kernel sizes.
- Compare stride and padding.
- Visualize CNN feature maps.
- Compare Max Pooling and Average Pooling.
- Build and train a CNN for image classification.
- Evaluate the model using accuracy, precision, recall, F1-score and confusion matrix.

## Tasks

1. Load and visualize the CIFAR-10 dataset.
2. Compare 3x3, 5x5 and 7x7 convolution kernels.
3. Compare different stride and padding settings.
4. Visualize feature maps from the CNN.
5. Compare Max Pooling and Average Pooling.
6. Build and train a CNN using Adam optimizer for 20 epochs with batch size 32.
7. Evaluate the trained model using classification metrics and a confusion matrix.

## Dataset

CIFAR-10 contains 50,000 training images and 10,000 testing images
belonging to 10 classes.

Each image is a 32 × 32 RGB image.

Classes:
- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

## Technologies Used

- Python
- PyTorch
- Torchvision
- Hugging Face Datasets
- NumPy
- Matplotlib
- Scikit-learn

## Model Training

The CNN is trained using:

- Optimizer: Adam
- Epochs: 20
- Batch Size: 32
- Loss Function: Cross Entropy Loss

## Evaluation

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Classification Report

## Files

- `DL_Lab_3.ipynb` - Complete implementation of the experiment.
