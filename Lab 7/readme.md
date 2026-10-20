# Deep Learning Lab 7: Autoencoders

## Overview

This experiment explores different types of autoencoders for image reconstruction, denoising, latent representation learning, and image generation using deep learning. The MNIST handwritten digit dataset is used to train and evaluate the models.

The experiment covers four architectures: Fully Connected Autoencoder, Convolutional Autoencoder, Denoising Convolutional Autoencoder, and Variational Autoencoder (VAE).

## Objectives

- Understand the encoder, latent representation, and decoder architecture.
- Implement autoencoders for image reconstruction.
- Compare fully connected and convolutional autoencoders.
- Remove noise from corrupted images using denoising autoencoders.
- Explore latent space representations and generate new images using VAEs.
- Evaluate reconstruction quality using MSE, MAE, and SSIM.

## Dataset

The experiment uses the **MNIST Handwritten Digit Dataset**, which contains grayscale images of handwritten digits from 0 to 9.

- Image dimensions: 28 × 28 pixels
- Input normalization: Pixel values scaled to [0, 1]
- Training samples: 10,000
- Testing samples: 2,000

## Models Implemented

### 1. Fully Connected Autoencoder
Uses dense layers to compress images into a 16-dimensional latent representation and reconstruct them. It learns the overall shape of digits but may lose fine details.

### 2. Convolutional Autoencoder (CAE)
Uses convolutional and upsampling layers to preserve spatial information, producing sharper and more accurate image reconstructions.

### 3. Denoising Autoencoder
Trains on noisy images with clean images as targets. Gaussian noise is added at different levels to study the model's ability to recover the original digit structure.

### 4. Variational Autoencoder (VAE)
Learns a probabilistic latent representation using the mean and variance of the latent distribution. The reparameterization trick and KL-divergence loss enable latent-space sampling, image generation, and interpolation.

## Evaluation Metrics

- **Mean Squared Error (MSE):** Measures the average squared difference between original and reconstructed pixels.
- **Mean Absolute Error (MAE):** Measures the average absolute pixel difference.
- **Structural Similarity Index (SSIM):** Measures similarity in image structure.
- **Reconstruction Loss:** Tracks model performance during training and validation.

## Key Results

| Model | Test MSE | Test MAE | SSIM |
|---|---:|---:|---:|
| Fully Connected AE | 0.0234 | 0.0611 | 0.7217 |
| Convolutional AE | 0.0024 | 0.0144 | 0.9760 |
| Denoising CAE (σ = 0.2) | 0.0044 | 0.0206 | 0.9462 |

The Convolutional Autoencoder achieved the best reconstruction quality among the deterministic reconstruction models. The denoising model successfully recovered the major digit structures from noisy inputs. The VAE demonstrated latent-space visualization, image generation, and smooth interpolation between latent points.

## Visualizations

The experiment includes:

- Original and reconstructed image comparisons
- Training and validation loss curves
- Fully connected versus convolutional reconstruction
- Clean, noisy, and denoised images
- Reconstruction quality at different noise levels
- VAE latent-space visualization
- Randomly generated digit images
- Latent-space interpolation
- Reconstruction-error distribution and high-error samples

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- scikit-image
- MNIST Dataset

## Conclusion

This experiment demonstrates how different autoencoder architectures learn compressed image representations and reconstruct images. Convolutional layers preserve spatial information more effectively than fully connected layers, while denoising autoencoders recover image structure from corrupted inputs. VAEs extend the reconstruction process by learning a continuous probabilistic latent space that supports image generation and interpolation.

## References

- [TensorFlow Documentation](https://www.tensorflow.org/)
- [Keras Documentation](https://keras.io/)
- [MNIST Dataset](https://www.tensorflow.org/api_docs/python/tf/keras/datasets/mnist)
- Kingma and Welling, *Auto-Encoding Variational Bayes*, ICLR 2014.
