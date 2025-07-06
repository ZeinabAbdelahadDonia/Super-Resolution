# Super-Resolution
Super Resolution Using Different Deep Learning Architectures

This project explores and compares multiple deep learning architectures for Single Image Super-Resolution (SISR) on the DIV2K dataset. The implemented models include SRCNN, ESRGAN, and Restormer-Tiny with variations and hyperparameter tuning.

## 📂 Dataset: DIV2K

- The DIV2K dataset (DIVerse 2K resolution dataset) is widely used for image super-resolution tasks.

- Image Resolution: ~2040x1080 pixels (PNG format)

  **Subsets:**

    - DIV2K_train_HR: 800 high-resolution training images

    - DIV2K_valid_HR: 100 high-resolution validation images

    - DIV2K_test_HR: 100 high-resolution test images

  For consistency, bicubic downscaling (scale=4) was used to generate low-resolution (LR) images from high-resolution (HR) ones.

-----------------------------------------------------------------------------------

## 1️⃣ ESRGAN
- **Model:** ESRGAN (Enhanced Super-Resolution Generative Adversarial Networks)  
- **Notebook:** `ESRGAN.ipynb`   
- **Inference Examples (for comparison):** `for_comaprison_ESRGAN`
- **Details:**

    Generator: Residual-in-Residual Dense Blocks (RRDB)

    Discriminator: Relativistic loss

    Perceptual Loss: VGG19 (35th layer)

    PSNR: 19–26 dB, SSIM: 0.4–0.65

    **Notes:** Training was unstable; qualitative results were acceptable despite lower quantitative metrics.
-----------------------------------------------------------------------------------

## 2️⃣ Restormer-Tiny (Local Window-Based Attention)
- **Model:** Restormer-Tiny with Local Window-Based Attention  
- **Notebook:** `Restormer-Tiny.ipynb`  
- **Model Weights:** `restormer_tiny.pth`  
- **Inference Examples (for comparison):** `Restormer-Tiny_to Compare`

-----------------------------------------------------------------------------------

## 3️⃣ Restormer-Tiny-Attention (Global Multi-Head Attention)
- **Model:** Restormer-Tiny with Global Multi-Head Attention  
- **Notebook:** `Restormer-TinyAttention.ipynb`  
- **Model Weights:** `restormerTinyAttention.pth`  
- **Inference Examples (for comparison):** `for_comparison`
  
-----------------------------------------------------------------------------------

## 4️⃣ SRCNNx2
- **Model:** SRCNN with scale=2  
- **Notebook:** `SRCNNx2.ipynb`  
- **Model Weights:** `srcnnx2.pth`  
- **Inference Examples (for comparison):** `SRCNNx2_to compare`
- **Inference Examples (results):** `SRCNNx2_Results`
- **Details:**
    A simple 3-layer convolutional network:

   - Layer 1: Feature extraction
   - Layer 2: Non-linear mapping
   - Layer 3: Image reconstruction
     
 - Training Time: 93.35 min
 - Results: PSNR: 37.64 dB, SSIM: 0.9649
  
- **Hyperparameters:**
    -Epochs: 100
    -LR: 1e-4
    -Optimizer: Adam
    -Filters: 64
    -Scale: 2
    -Activation: ReLU

   
-----------------------------------------------------------------------------------

## 5️⃣ SRCNNx2 Hyperparameter Tuning
- **Model:** SRCNN with scale=2 + hyperparameter tuning  
- **Notebook:** `SRCNNx2HT.ipynb`  
- **Model Weights:** `srcnnx2ht.pth`  
- **Inference Examples (for comparison):** `for comparison`
- **Inference Examples (results):** `Results`
- **Details:**
-  Training Time: 551.47 min
-  Results: PSNR: 37.79 dB, SSIM: 0.9650
- **Hyperparameters:**
-  Optimizer: AdamW (Weight Decay: 1e-4)
-  Filters: 128

-----------------------------------------------------------------------------------

## 6️⃣ SRCNNx4
- **Model:** SRCNN with scale=4  
- **Notebook:** `SRCNNx4.ipynb`  
- **Model Weights:** `srcnnx4.pth`  
- **Inference Examples (for comparison):** `SRCNNx4_to compare`
- **Inference Examples (results):** `SRCNNx4_Results`

-----------------------------------------------------------------------------------






