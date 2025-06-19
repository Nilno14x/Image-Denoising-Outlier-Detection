# Image Denoising with CNN + U-Net and Outlier Detection

This project applies deep learning techniques to denoise color images using a hybrid CNN + U-Net architecture. It includes performance evaluation using PSNR/SSIM and outlier detection based on reconstruction error (MSE).

---

## 🧠 Project Highlights

- 📸 **Input:** Noisy color images of cats and dogs
- 🧼 **Output:** Denoised images using a trained U-Net model
- 📊 **Evaluation:** SSIM, PSNR metrics
- ⚠️ **Outlier Detection:** Identifies low-quality denoised outputs using MSE thresholding
- 🧪 **Visualization:** Line plots for SSIM, PSNR, and MSE across test samples

---

## 📂 Project Structure

Image-Denoising-Outlier-Detection/
│
├── denoiser_unet_model.h5 
├── images/
│ ├── noisy/ 
| |   ├── train/ 
| |   ├── test/ 
| |   └── val/ 
│ └── clean/ 
|     ├── train/ 
|     ├── test/ 
|     └── val/ 
├── images_test/
│ ├── noisy/ # Noisy test images
│ └── clean/ # Clean test images
│
├── denoising_and_outlier_detection.ipynb # Main notebook
├── Model_uses.py 
├── Model.ipynb 
└── README.md


📈 Evaluation Metrics
> PSNR (Peak Signal-to-Noise Ratio): Indicates how much the denoised image resembles the ground truth. Higher is better.
> SSIM (Structural Similarity Index): Measures visual similarity. Ranges from 0 to 1. Higher is better.
> MSE (Reconstruction Error): Used to detect outlier images after denoising.

⚙️ Outlier Detection Logic
  1.Compute MSE between clean and denoised images.
  2.Calculate threshold = mean + 2 * std_dev. 
  3.Flag images with reconstruction error > threshold as outliers.
