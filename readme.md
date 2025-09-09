#  Denoising Autoencoder 🧹

This project implements a **convolutional autoencoder** trained to remove synthetic Gaussian noise from cigarette-smoker images.  
The model is trained on images with different noise levels (20–70 SNR) and evaluated using **PSNR, SSIM, and MAE** metrics.

---

##  Features
- **Custom Noise Generation**: Gaussian noise added to images at multiple intensities.  
- **Autoencoder Architecture**: Convolutional encoder–decoder with a latent space of 128 dimensions.  
- **Training Pipeline**: Uses TensorFlow `tf.data` for efficient batching and augmentation.  
- **Evaluation Metrics**:
  - PSNR (Peak Signal-to-Noise Ratio)  
  - SSIM (Structural Similarity Index)  
  - MAE (Mean Absolute Error)  
- **Visualization**:
  - Side-by-side plots of **Noisy → Reconstructed → Clean** images.  
  - Histograms of PSNR, SSIM, and MAE distributions.  
- **Latent Space Exploration**: Random vectors decoded to generate synthetic images.

---

##  Results
- **Average PSNR**: ~22.7 dB  
- **Average SSIM**: ~0.63  
- **Average MAE**: ~0.056  

Interpretation:
- **30+ dB PSNR** → high-quality reconstruction  
- **22–25 dB PSNR** → acceptable but noticeable distortion  
- **SSIM > 0.6** → reasonable structural similarity  

---

##  Sample Outputs
- Reconstructions from noisy images  
- Reconstructions from pure noise input (latent space exploration)  
- Histograms of metric distributions  

---
