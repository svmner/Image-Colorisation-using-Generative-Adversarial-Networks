# 🎨 Image Colorisation using Generative Adversarial Networks (GANs)

This project implements a deep learning model for automatic **image colorization** using **Generative Adversarial Networks (GANs)**. The goal is to generate realistic RGB color images from grayscale (L-channel) inputs using adversarial training and perceptual loss.

## 🧠 Core Idea

Given a black-and-white image, the model learns to hallucinate plausible colors by using:
- A **Generator** that maps grayscale to color
- A **Discriminator** that distinguishes real color images from generated ones
- **Adversarial loss** + **Per-pixel loss** + **Perceptual loss** for training stability and realism

## 🔍 Model Architecture

- **Generator:** U-Net style encoder-decoder with skip connections  
- **Discriminator:** PatchGAN to focus on local texture realism  
- **Loss Functions:**
  - L1 Loss (pixel-wise accuracy)
  - VGG-based Perceptual Loss (content similarity)
  - Binary Cross-Entropy (GAN loss)

## 📊 Dataset

- **Dataset Used:** [Places365](http://places2.csail.mit.edu/) & CIFAR-10 (for small-scale testing)
- **Input:** Grayscale L-channel
- **Target:** a, b color channels (Lab space)
- **Preprocessing:**
  - Images converted to CIELab color space
  - Normalized and resized to 256×256

## 🚀 Training

- Framework: PyTorch  
- Optimizer: Adam  
- Epochs: 100  
- Batch size: 16  
- Learning rate: 2e-4  

## 🧪 Evaluation
- PSNR (Peak Signal-to-Noise Ratio)

- SSIM (Structural Similarity Index)

- Visual inspection of color realism

