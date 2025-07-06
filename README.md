# Super-Resolution
Super Resolution Using Different Deep Learning Architectures

This project explores and compares multiple deep learning architectures for Single Image Super-Resolution (SISR) on the DIV2K dataset. The implemented models include SRCNN, ESRGAN, and Restormer-Tiny with variations and hyperparameter tuning.

📂 Dataset: DIV2K

The DIV2K dataset (DIVerse 2K resolution dataset) is widely used for image super-resolution tasks.

Image Resolution: ~2040x1080 pixels (PNG format)

Subsets:

DIV2K_train_HR: 800 high-resolution training images

DIV2K_valid_HR: 100 high-resolution validation images

DIV2K_test_HR: 100 high-resolution test images

For consistency, bicubic downscaling (scale=4) was used to generate low-resolution (LR) images from high-resolution (HR) ones.

🧠 Models and Results

1️⃣ SRCNN (Super-Resolution Convolutional Neural Network)

A simple 3-layer convolutional network:

Layer 1: Feature extraction

Layer 2: Non-linear mapping

Layer 3: Image reconstruction

📌 Variations:

🔹 SRCNNx2

Epochs: 100

LR: 1e-4

Optimizer: Adam

Filters: 64

Scale: 2

Activation: ReLU

Training Time: 93.35 min

Results: PSNR: 37.64 dB, SSIM: 0.9649

🔹 SRCNNx2 (Hyperparameter Tuning)

Optimizer: AdamW (Weight Decay: 1e-4)

Filters: 128

Training Time: 551.47 min

Results: PSNR: 37.79 dB, SSIM: 0.9650

🔹 SRCNNx4

Scale: 4

Filters: 64

Training Time: 106.41 min

Results: PSNR: 33.75 dB, SSIM: 0.9212

2️⃣ ESRGAN (Enhanced Super-Resolution GAN)

An improvement on SRGAN with:

Generator: Residual-in-Residual Dense Blocks (RRDB)

Discriminator: Relativistic loss

Perceptual Loss: Uses VGG19 (35th layer)

📌 Hyperparameters:

in_channels: 3, out_channels: 3

channels: 64, growth_channels: 32

num_blocks: 23, res_scale: 0.2

scale_factor: 4, LeakyReLU slope: 0.2

⚠️ Training:

Unstable with PSNR: 19–26, SSIM: 0.4–0.65

Qualitative Results: Visually acceptable but quantitatively poor.

3️⃣ Restormer-Tiny

A lightweight Transformer-based model for SISR.

📌 Variations:

🔹 Global Multi-Head Attention

Dim: 32, Num_blocks: 4, Num_heads: 2

Scale: 2

Training Time: 218.37 min

Results: PSNR: 38.88 dB, SSIM: 0.9688

🔹 Local Window-Based Attention

window_size: 8, num_heads: 4

Training Time: Efficient

Results: PSNR: 38.55 dB, SSIM: 0.9643

📊 Summary of Results

Model Variation

Scale

PSNR (dB)

SSIM

Training Time

SRCNNx2

2

37.64

0.9649

93.35 min

SRCNNx2 (Tuned)

2

37.79

0.9650

551.47 min

SRCNNx4

4

33.75

0.9212

106.41 min

ESRGAN

4

19–26

0.4–0.65

Unstable

Restormer-Tiny (Global)

2

38.88

0.9688

218.37 min

Restormer-Tiny (Local)

2

38.55

0.9643

Efficient

🚀 Highlights

✅ Best Quantitative Results: Restormer-Tiny (Global Attention)
✅ Best Qualitative Results: ESRGAN (despite low PSNR/SSIM)
✅ Fastest Training: SRCNNx2
-----------------------------------------------------------------------------------

## 1️⃣ ESRGAN
- **Model:** ESRGAN (Enhanced Super-Resolution Generative Adversarial Networks)  
- **Notebook:** `ESRGAN.ipynb`   
- **Inference Examples (for comparison):** `for_comaprison_ESRGAN`

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

-----------------------------------------------------------------------------------

## 5️⃣ SRCNNx2 Hyperparameter Tuning
- **Model:** SRCNN with scale=2 + hyperparameter tuning  
- **Notebook:** `SRCNNx2HT.ipynb`  
- **Model Weights:** `srcnnx2ht.pth`  
- **Inference Examples (for comparison):** `for comparison`
- **Inference Examples (results):** `Results`

-----------------------------------------------------------------------------------

## 6️⃣ SRCNNx4
- **Model:** SRCNN with scale=4  
- **Notebook:** `SRCNNx4.ipynb`  
- **Model Weights:** `srcnnx4.pth`  
- **Inference Examples (for comparison):** `SRCNNx4_to compare`
- **Inference Examples (results):** `SRCNNx4_Results`

-----------------------------------------------------------------------------------






