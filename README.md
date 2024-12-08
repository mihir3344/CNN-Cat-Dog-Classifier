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
- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy

The model achieves:
- **Training Accuracy**:0.95%
- **Validation Accuracy**:0.90%

---

## Prediction

Use the following script to predict images:

```python
import numpy as np
from tensorflow.keras.preprocessing import image

def predict_image(img_path, model):
    img = image.load_img(img_path, target_size=(150, 150))
    img_array = image.img_to_array(img)
    img_array = np.expand_dims(img_array, axis=0)
   
