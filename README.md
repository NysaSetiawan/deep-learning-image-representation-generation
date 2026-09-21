# CGAN_Image_Gen
Optimized Conditional GAN for Helicopter and Ship image generation using TensorFlow/Keras and FID evaluation.

# Conditional GAN for Image Generation

## Overview

This project implements a **Conditional Generative Adversarial Network (CGAN)** to generate class-conditional images using the **Overhead-MNIST dataset**.

The experiment focuses on two classes:

- Helicopter
- Ship

A baseline CGAN was developed and then optimized through architectural modifications to improve image generation quality.

## Dataset

After preprocessing, the dataset contained:

- **12,342 training images**
- **1,544 test images**
- Image size: **28 × 28 grayscale**
- 2 classes: **Helicopter and Ship**

Data preprocessing included class selection, duplicate checking, validation of pixel values, image reshaping, and normalization.

## Model

Two CGAN architectures were evaluated:

### Baseline CGAN
- 100-dimensional latent space
- Label embedding
- Fully connected Generator and Discriminator
- Adam optimizer

### Modified CGAN
The architecture was improved using convolutional layers:

- Conv2DTranspose
- Batch Normalization
- Conv2D
- Gaussian Noise
- Dropout
- Label Embedding

The modified architecture was designed to better capture spatial features in the generated images.
.36**.
