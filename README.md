# Cat vs. Dog Classification with VGG16

This project classifies images as cats or dogs using a Convolutional Neural Network (CNN) built on top of a pre-trained VGG16 model. The project uses transfer learning and achieves excellent accuracy.

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training and Validation](#training-and-validation)
- [Prediction](#prediction)
- [Installation](#installation)
- [Usage](#usage)

---

## Overview

This project leverages the pre-trained VGG16 model for feature extraction, freezing its convolutional layers, and adding custom dense layers for classification. The model performs well in distinguishing between cats and dogs.

---

## Dataset

- **Source**: [Kaggle's Cat and Dog Dataset](https://www.kaggle.com/tongpython/cat-and-dog)
- **Structure**:
  - `training_set`: Contains labeled images of cats and dogs.
  - `test_set`: Used for validation.

---

## Model Architecture

The model includes:
1. **VGG16 as Base**: Pre-trained weights on ImageNet.
2. **Custom Dense Layers**: Added for classification.
3. **Dropout**: Prevents overfitting.
4. **Sigmoid Output**: For binary classification.

---

## Training and Validation

- **Batch Size**: 32
- **Image Size**: 150x150 pixels
- **Epochs**: 10
- **Optimizer**: Rmsprop
- **Loss Function**: Binary Crossentropy

The model achieves:
- **Training Accuracy**: 99.89%
- **Validation Accuracy**: 94.07%

---

## Prediction

To make predictions on new images:
1. **Download the images**: Make sure the images you want to predict are in either `cat` or `dog` format.
2. **Resize the images**: The images must be resized to 150x150 pixels to be compatible with the VGG16 model input size.

---

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/cat-vs-dog-vgg16.git
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

---

## Usage

1. Place the image(s) you want to classify in the `predict_images/` folder.
2. Run the prediction script:
    ```bash
    python predict.py
    ```

3. View the predictions output on the console.


