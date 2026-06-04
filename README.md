# MNIST Autoencoder Denoising

This project uses a convolutional autoencoder to remove Gaussian noise from MNIST handwritten digit images.

The model receives a noisy input image and reconstructs a cleaner output image.  
The performance is evaluated both visually and quantitatively using MSE, PSNR, and SSIM.

## Overview

The goal of this project was to train an autoencoder that can denoise 28x28 grayscale MNIST images.

The model was tested with different Gaussian noise levels:

- Sigma = 0.1
- Sigma = 0.3
- Sigma = 0.5

For each noise level, the model takes noisy images as input and outputs denoised images.

## Model Architecture

The autoencoder has three main parts:

- Encoder
- Latent representation
- Decoder

The encoder compresses the input image into a smaller representation.  
The decoder reconstructs the original clean image from that compressed representation.

The model uses convolutional layers, transposed convolutional layers, Batch Normalization, ReLU activation, and a final sigmoid activation.

## Technologies Used

- Python
- PyTorch
- torchvision
- NumPy
- Matplotlib
- scikit-image
- Google Colab / T4 GPU
- MNIST dataset

## Training Details

- Dataset: MNIST
- Loss function: Mean Squared Error (MSE)
- Optimizer: Adam
- Learning rate: 0.001
- Batch size: 128
- Epochs: 20
- Training noise level: Sigma = 0.3

## Evaluation Metrics

The model was evaluated using:

- MSE: Measures pixel-level reconstruction error
- PSNR: Measures image reconstruction quality
- SSIM: Measures structural similarity between the original and reconstructed images

## Results

The model performed well at lower and moderate noise levels.

At Sigma = 0.1, the model reconstructed images almost perfectly.  
At Sigma = 0.3, the model still produced clear denoised images.  
At Sigma = 0.5, the model was still able to reconstruct images, but some noise remained.

## What I Learned

Through this project, I learned how autoencoders can be used for image denoising.  
I also gained experience with PyTorch, convolutional neural networks, image reconstruction, and model evaluation using MSE, PSNR, and SSIM.
