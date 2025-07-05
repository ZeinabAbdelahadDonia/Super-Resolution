# Super-Resolution
Super Resolution Using Different Deep Learning Architectures

-----------------------------------------------------------------------------------

## 1️⃣ ESRGAN
- **Model:** ESRGAN (Enhanced Super-Resolution Generative Adversarial Networks)  
- **Notebook:** `ESRGAN.ipynb`  
- **Discriminator Weights:** `esrgan_discriminator.pth`  
- **Generator Weights:** `esrgan_generator.pth`  
- **Inference Examples (for comparison):** `for_comaprison_ESRGAN`

-----------------------------------------------------------------------------------

## 2️⃣ Restormer-Tiny (Local Window-Based Attention)
- **Model:** Restormer-Tiny with Local Window-Based Attention  
- **Notebook:** `Restormer-Tiny.ipynb`  
- **Model Weights:** `restormer_tiny.pth`  
- **TensorBoard Logs:** `restormerTensorboard`  
- **Inference Examples (for comparison):** `Restormer-Tiny_to Compare`

### ▶ How to Run TensorBoard
```bash
cd ./RestormerTiny
tensorboard --logdir=restormerTensorboard

-----------------------------------------------------------------------------------

## 3️⃣ Restormer-Tiny-Attention (Global Multi-Head Attention)
- **Model:** Restormer-Tiny with Global Multi-Head Attention 
- **Notebook:** `Restormer-TinyAttention.ipynb`  
- **Model Weights:** `restormerTinyAttention.pth`  
- **TensorBoard Logs:** `Tensorboard`  
- **Inference Examples (for comparison):** `for_comparison`

### ▶ How to Run TensorBoard
```bash
cd ./Restormer-Tiny-attention
tensorboard --logdir=Tensorboard

-----------------------------------------------------------------------------------

## 4️⃣ SRCNNx2
- **Model:** SRCNN with scale=2  
- **Notebook:** `SRCNNx2.ipynb`  
- **Model Weights:** `srcnnx2.pth`  
- **TensorBoard Logs:** `srcnnx2Tensorboard`  
- **Inference Examples (for comparison):** `SRCNNx2_to compare`
- **Inference Examples (results): ** `SRCNNx2_Results`

### ▶ How to Run TensorBoard
```bash
cd ./SRCNNx2
tensorboard --logdir=srcnnx2Tensorboard

-----------------------------------------------------------------------------------

## 5️⃣ SRCNNx2 Hyperparameter Tuning
- **Model:** SRCNN with scale=2 + hyperparameter tuning  
- **Notebook:** `SRCNNx2HT.ipynb`  
- **Model Weights:** `srcnnx2ht.pth`  
- **TensorBoard Logs:** `Tensorboard`  
- **Inference Examples (for comparison):** `for comparison`
- **Inference Examples (results): ** `Results`

### ▶ How to Run TensorBoard
```bash
cd ./SRCNNx2Hyyperparameter\ Tuning
tensorboard --logdir=Tensorboard

-----------------------------------------------------------------------------------

## 6️⃣ SRCNNx4
- **Model:** SRCNN with scale=4  
- **Notebook:** `SRCNNx4.ipynb`  
- **Model Weights:** `srcnnx4.pth`  
- **TensorBoard Logs:** `srcnnx4Tensorboard`  
- **Inference Examples (for comparison):** `SRCNNx4_to compare`
- **Inference Examples (results): ** `SRCNNx4_Results`

### ▶ How to Run TensorBoard
```bash
cd ./SRCNNx4
tensorboard --logdir=srcnnx4Tensorboard




