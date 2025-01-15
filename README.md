# README

## Repository Overview

This repository consists of two folders:

1. **Folder 1: Subtask 1 - CNN Model for AI vs Real Image Classification**
   - Description: This folder contains a Convolutional Neural Network (CNN) model trained on a provided dataset to classify images as either AI-generated or real. The model is implemented using a sequential architecture.
   - Model Architecture:
     ```
     ┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━┓
     ┃ Layer (type)                         ┃ Output Shape                ┃         Param # ┃
     ┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━┩
     │ conv2d (Conv2D)                      │ (None, 358, 358, 32)        │             896 │
     ├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
     │ max_pooling2d (MaxPooling2D)         │ (None, 179, 179, 32)        │               0 │
     ├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
     │ conv2d_1 (Conv2D)                    │ (None, 177, 177, 64)        │          18,496 │
     ├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
     │ max_pooling2d_1 (MaxPooling2D)       │ (None, 88, 88, 64)          │               0 │
     ├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
     │ conv2d_2 (Conv2D)                    │ (None, 86, 86, 128)         │          73,856 │
     ├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
     │ max_pooling2d_2 (MaxPooling2D)       │ (None, 43, 43, 128)         │               0 │
     ├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
     │ flatten (Flatten)                    │ (None, 236672)              │               0 │
     ├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
     │ dense (Dense)                        │ (None, 128)                 │      30,294,144 │
     ├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
     │ dense_1 (Dense)                      │ (None, 1)                   │             129 │
     └──────────────────────────────────────┴─────────────────────────────┴─────────────────┘
      Total params: 30,387,521 (115.92 MB)
      Trainable params: 30,387,521 (115.92 MB)
      Non-trainable params: 0 (0.00 B)
     ```
   - Input Format: Images reshaped into 360x360x3 arrays containing RGB values for all pixels.
   - Output: The model outputs the probability of the image being AI-generated. A threshold of 0.5 is applied to classify images as AI (if above threshold) or Real (if below threshold).

2. **Folder 2: Subtask 2 - GAN for Anime Character Face Generation**
   - Description: This folder contains a Generative Adversarial Network (GAN) trained to generate AI images of anime character faces using a public dataset.
   - Model Components:
     - **Generator:** Generates images that attempt to fool the discriminator into predicting them as real.
     - **Discriminator:** Classifies images as real or fake.
   - Training Details:
     - Custom Loss Function: Derived from binary cross-entropy loss.
     - Training Loop: A custom loop where the model that fails (generator or discriminator) is trained to improve performance.
     - Epochs: The model was trained for 10 epochs, balancing training time and image quality.
   - Additional Information: More details about the model implementation can be found in the `.py` file attached in this folder.


## Usage
- For Subtask 1:
  - Load the CNN model from the provided folder.
  - Input images as specified and obtain classification results.
- For Subtask 2:
  - Run the GAN training script or load pre-trained models to generate anime character faces.


