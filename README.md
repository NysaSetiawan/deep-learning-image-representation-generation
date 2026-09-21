# Deep Learning: Image Representation & Generation

Exploring image representation and generation using a Convolutional Autoencoder and Conditional Generative Adversarial Network (CGAN) on the Overhead-MNIST dataset.

## Overview

This project covers two deep learning approaches for image understanding and generation:

- **Convolutional Autoencoder** — reduces image dimensionality from 784 (28×28) to a 128-dimensional latent representation while reconstructing the original images.
- **Conditional GAN (CGAN)** — generates synthetic images conditioned on their class labels.

The models were evaluated using **SSIM** for image reconstruction and **FID** for image generation quality.

---

## 1. Image Representation — Convolutional Autoencoder

The Autoencoder performs dimensionality reduction from:

**784 dimensions → 128-dimensional latent representation**

The model was trained on two classes from the Overhead-MNIST dataset:

- Helicopter
- Ship

### Result

| Model | SSIM |
|---|---:|
| Baseline Autoencoder | 0.6493 |
| Modified Autoencoder | **0.8064** |

The modified architecture improved reconstruction quality by approximately **24.2%** in SSIM.

### Architecture Improvements

The modified Autoencoder introduced:

- Increased convolutional filters
- Batch Normalization
- Deeper encoder and decoder
- Larger intermediate dense representation
- Conv2DTranspose for image reconstruction

---

## 2. Image Generation — Conditional GAN

A Conditional GAN was developed to generate images based on class labels.

The model focuses on:

- **Class 2 — Helicopter**
- **Class 7 — Ship**

The CGAN consists of:

- Conditional Generator
- Conditional Discriminator
- Class embeddings
- Convolutional layers
- Batch Normalization
- Dropout
- Gaussian Noise

### Result

| Model | FID |
|---|---:|
| Baseline CGAN | 262.47 |
| Modified CGAN | **148.36** |

The modified CGAN reduced FID by approximately **43.5%**, indicating improved generated-image quality compared with the baseline.

---

