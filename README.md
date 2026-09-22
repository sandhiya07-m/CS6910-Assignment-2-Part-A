# CS6910 Assignment 2 - Part A

## Overview

This repository contains the implementation for CS6910 Assignment 2 Part A.

The project focuses on image classification using Convolutional Neural Networks (CNNs) with PyTorch on the iNaturalist 12K dataset.

## Dataset

The iNaturalist 12K dataset contains 10 classes:

- Amphibia
- Animalia
- Arachnida
- Aves
- Fungi
- Insecta
- Mammalia
- Mollusca
- Plantae
- Reptilia

The original training data was divided into 80% training and 20% validation data using a class-wise split.

The separate held-out test data was not used during hyperparameter tuning.

## Part A - Question 1

A CNN was built from scratch using PyTorch.

The network consists of five convolutional blocks followed by fully connected layers.

## Part A - Question 2

W&B Sweep was used for hyperparameter tuning.

The following hyperparameters were explored:

- Number of filters
- Filter organisation
- Activation function
- Data augmentation
- Batch normalization
- Dropout
- Learning rate
- Batch size

Random search was used for the sweep.

## Best Configuration

The best configuration obtained from the evaluated sweep runs was:

- Initial filters: 64
- Filter organisation: Double
- Activation: SiLU
- Data augmentation: No
- Batch normalization: No
- Dropout: 0.2
- Learning rate: 0.0001
- Batch size: 16

The best validation accuracy obtained during the sweep was 31.67%.

## Question 4 - Test Evaluation

The selected model was retrained and evaluated on the held-out test set.

Test accuracy: 34.50%

Correct predictions: 690 / 2000

A 10 x 3 grid of 30 test images with their true and predicted labels was generated as part of the evaluation.

## Tools Used

- Python
- PyTorch
- Torchvision
- Google Colab
- Weights & Biases

## How to Run

### Requirements

- Python 3.x
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Pillow
- Weights & Biases
- Google Colab with GPU recommended

### Running the Notebook

1. Open the `Copy_of_Untitled0.ipynb` notebook in Google Colab.
2. Select a GPU runtime.
3. Mount or provide the iNaturalist 12K dataset.
4. Run the notebook cells in order.
5. The original training data is divided into 80% training and 20% validation data.
6. The separate held-out test data is used only for final evaluation.

### Evaluation

The best CNN configuration from the W&B sweep is retrained and evaluated on the held-out test set.

Final test accuracy: **34.50%**

Correct predictions: **690 / 2000**
