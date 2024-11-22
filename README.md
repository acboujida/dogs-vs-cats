# Dog vs Cat: Deep Learning Image Classification Project

## Overview

The project uses a CNN to process images, extract features, and classify them as either **Dog** or **Cat**. Images are resized to a standard size of `100x100` pixels, and the model uses multiple convolutional, pooling, and dense layers for feature extraction and classification.

---

## Dataset

The dataset consists of images stored in the directory `PetImages/`, organized into two categories:

```
PetImages
├── Dog/
├── Cat/
```

- **CATEGORIES**: `["Dog", "Cat"]`
- **Image Size**: All images are resized to `100x100` pixels for uniformity.

---

## Model Architecture

The CNN model has the following structure:

1. **Convolutional Layers**:
   - Three convolutional layers with filter sizes 32, 64, and 128.
   - Kernel size: `(3, 3)`.
   - Activation: ReLU (except for the first convolutional layer, which has no activation specified).

2. **Pooling Layers**:
   - MaxPooling layers with pool size `(2, 2)` are applied after each convolutional layer.

3. **Dropout Layers**:
   - Dropout rates of 0.25 and 0.5 are applied to reduce overfitting.

4. **Flattening**:
   - Flattens the feature maps from the convolutional layers for input into dense layers.

5. **Dense Layers**:
   - A dense layer with 128 units and ReLU activation for feature learning.
   - A final dense layer with 1 unit and sigmoid activation for binary classification.

6. **Compilation**:
   - Optimizer: Adam.
   - Loss Function: Binary Crossentropy.
   - Metric: Accuracy.
