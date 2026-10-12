# MNIST Data Extraction and Preprocessing

A Python-based data preparation project demonstrating how to download, inspect, and preprocess the MNIST handwritten digit dataset using TensorFlow and NumPy in Google Colab.

## Overview

The MNIST dataset contains grayscale images of handwritten digits from 0 to 9. This project covers the initial data preparation workflow required before building an image classification model.

The focus is on understanding the dataset, validating its structure, normalizing pixel values, and preparing a flattened representation of the images.

## Objectives

- Download the dataset directly from the provided source URL.
- Extract the training images, training labels, testing images, and testing labels.
- Explore the dataset dimensions, data types, pixel values, and digit labels.
- Visualize sample handwritten digit images.
- Validate the structure and basic quality of the data.
- Normalize pixel values to the range 0–1.
- Flatten 28 × 28 images into 784 features for fully connected neural network workflows.

## Dataset

**Source:** [MNIST dataset — TensorFlow Keras](https://storage.googleapis.com/tensorflow/tf-keras-datasets/mnist.npz)

The dataset is distributed as a compressed NumPy archive (`.npz`).

| Component | Number of samples | Shape per sample |
|---|---:|---|
| Training images | 60,000 | 28 × 28 |
| Training labels | 60,000 | One digit label |
| Testing images | 10,000 | 28 × 28 |
| Testing labels | 10,000 | One digit label |

Each image represents a handwritten digit from 0 to 9.

## Tools and Technologies

- Python
- Google Colab
- TensorFlow
- NumPy
- Matplotlib

## Workflow

1. Import the required libraries.
2. Download the dataset from the source URL.
3. Verify the downloaded file and inspect the archive.
4. Extract the training and testing arrays.
5. Explore image dimensions, labels, data types, and pixel ranges.
6. Visualize representative images.
7. Validate the data structure and label integrity.
8. Normalize pixel values from 0–255 to 0–1.
9. Flatten images into 784 features where required.
10. Perform final validation of the processed data.

## Preprocessing Details

**Normalization:** Image values are converted to `float32` and divided by 255 so that pixel intensities fall between 0 and 1.

**Flattening:** Each 28 × 28 image is reshaped into a vector of 784 features. The flattened representation is intended for fully connected neural networks; convolutional neural networks generally use image-shaped inputs instead.

**Validation:** Assertions check expected dimensions, data types, finite values, pixel ranges, and consistency between images and labels.

The original training/testing split is preserved, and the notebook does not train a model.

## Expected Results

- 60,000 training images and 10,000 testing images.
- Image dimensions of 28 × 28 before flattening.
- 784 features per image after flattening.
- Normalized pixel values in the range 0–1.
- Successful completion of the final data validation checks.

These are expected dataset characteristics; the actual results should be confirmed by running the notebook.

## How to Run

1. Open the notebook in Google Colab.
2. Run the cells sequentially from top to bottom.
3. Allow the notebook to download the dataset from the source URL.
4. Review the exploration, visualization, preprocessing, and validation outputs.

No separate dataset download or local dataset upload is required.

## Project Scope

This project covers dataset extraction, exploration, preprocessing, and validation. Model training, prediction, and evaluation metrics are outside the current scope.

## Author

Developed as a practical exercise in Python-based dataset preparation and machine learning fundamentals.
