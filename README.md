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

----------------------------------------------------------------------------------
## 🧠 Models and Results

## 1️⃣ ESRGAN
- **Model:** ESRGAN (Enhanced Super-Resolution Generative Adversarial Networks)  
- **Notebook:** `ESRGAN.ipynb`   
- **Inference Examples (for comparison):** `for_comaprison_ESRGAN`
- **Details:**
    - Generator: Residual-in-Residual Dense Blocks (RRDB)
    - Discriminator: Relativistic loss
    - Perceptual Loss: VGG19 (35th layer)
    - Unstable with PSNR: 19–26, SSIM: 0.4–0.65
    - **Notes:** Training was unstable; qualitative results were acceptable despite lower quantitative metrics.
- **Hyperparameters:**
    - in_channels: 3
    - out_channels: 3
    - channels: 64
    - growth_channels: 32
    - num_blocks: 23
    - res_scale: 0.2
    - scale_factor: 4
    - LeakyReLU slope: 0.2
 
----------------------------------------------------------------------------------

## 2️⃣ Restormer-Tiny (Local Window-Based Attention)
- **Model:** Restormer-Tiny with Local Window-Based Attention  
- **Notebook:** `Restormer-Tiny.ipynb`  
- **Model Weights:** `restormer_tiny.pth`  
- **Inference Examples (for comparison):** `Restormer-Tiny_to Compare`
- **Details:**
   - A lightweight Transformer-based model for SISR
   - Local Window-Based Attention
   - Training Time: Efficient
   - Results: PSNR: 38.55 dB, SSIM: 0.9643
-**Hyperparameters:**
   - window_size: 8
   - num_heads: 4
----------------------------------------------------------------------------------

## 3️⃣ Restormer-Tiny-Attention (Global Multi-Head Attention)
- **Model:** Restormer-Tiny with Global Multi-Head Attention  
- **Notebook:** `Restormer-TinyAttention.ipynb`  
- **Model Weights:** `restormerTinyAttention.pth`  
- **Inference Examples (for comparison):** `for_comparison`
- **Details:**
   - A lightweight Transformer-based model for SISR
   - Global Multi-Head Attention
   - Training Time: 218.37 min
   - Results: PSNR: 38.88 dB, SSIM: 0.9688
- **Hyperparameter:**
   - Dim: 32
   - Num_blocks: 4
   - Num_heads: 2
   - Scale: 2

----------------------------------------------------------------------------------

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
    - Epochs: 100
    - LR: 1e-4
    - Optimizer: Adam
    - Filters: 64
    - Scale: 2
    - Activation: ReLU

   
----------------------------------------------------------------------------------

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

----------------------------------------------------------------------------------

## 6️⃣ SRCNNx4
- **Model:** SRCNN with scale=4  
- **Notebook:** `SRCNNx4.ipynb`  
- **Model Weights:** `srcnnx4.pth`  
- **Inference Examples (for comparison):** `SRCNNx4_to compare`
- **Inference Examples (results):** `SRCNNx4_Results`
- **Details:**
   -  Training Time: 106.41 min
   -  Results: PSNR: PSNR: 33.75 dB, SSIM: 0.9212
- **Hyperparameters:**
   -  Scale: 4
   -  Filters: 64
----------------------------------------------------------------------------------

🚀 Highlights

✅ Best Quantitative Results: Restormer-Tiny (Global Attention)
✅ Best Qualitative Results: All models are proficient (despite low PSNR/SSIM in ESRGAN)
✅ Fastest Training: SRCNNx2





