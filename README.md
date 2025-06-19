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
├── denoiser_unet_model.h5 # Trained U-Net model
├── images_test/
│ ├── noisy/ # Noisy test images
│ └── clean/ # Clean test images
│
├── denoising_and_outlier_detection.ipynb # Main notebook
├── utils.py # PSNR/SSIM/Outlier functions (optional)
└── README.md
