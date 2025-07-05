# Super-Resolution
Super Resolution Using Different Deep Learning Architectures

-----------------------------------------------------------------------------------

1. ESRGAN 

Model: ESRGAN 
Notebook: ESRGAN.ipynb
Discriminator Weights: esrgan_discriminator.pth
Generator Weights: esrgan_generator.pth
Inference Examples to Compare between other models: for_comaprison_ESRGAN

-----------------------------------------------------------------------------------

2. Restormer-Tiny

Model: Restormer-Tiny with Local Window-based Attention
Notebook: Restormer-Tiny.ipynb
Model Weights: restormer_tiny.pth
Tensorboard: restormerTensorboard
Inference Examples to Compare between other models: Restormer-Tiny_to Compare

TO RUN TENSORBOARD
*Navigate to the folder ./RestormerTiny in the cmd
*run this command ( tensorboard --logdir=restormerTensorboard)
*click on localhost link

-----------------------------------------------------------------------------------

3. Restormer-Tiny-attention

Model: Restormer-Tiny with Global Multi-Head Attention
Notebook: Restormer-TinyAttention.ipynb
Model Weights: restormerTinyAttention.pth
Tensorboard: Tensorboard
Inference Examples to Compare between other models: for_comparison

TO RUN TENSORBOARD
*Navigate to the folder ./Restormer-Tiny-attention in the cmd
*run this command ( tensorboard --logdir=Tensorboard)
*click on localhost link

-----------------------------------------------------------------------------------

4. SRCNNx2

Model: SRCNN with scale=2
Notebook: SRCNNx2.ipynb
Model Weights: srcnnx2.pth
Tensorboard: srcnnx2Tensorboard
Inference Examples to Compare between other models: SRCNNx2_to compare
Inference Examples: SRCNNx2_Results

TO RUN TENSORBOARD
*Navigate to the folder ./SRCNNx2 in the cmd
*run this command ( tensorboard --logdir=srcnnx2Tensorboard)
*click on localhost link

-----------------------------------------------------------------------------------

5.  SRCNNx2Hyyperparameter Tuning

Model: SRCNN with scale=2 + hyperparameter tuning
Notebook: SRCNNx2HT.ipynb
Model Weights: srcnnx2ht.pth
Tensorboard: Tensorboard
Inference Examples to Compare between other models: for comparison
Inference Examples: Results

TO RUN TENSORBOARD
*Navigate to the folder ./SRCNNx2Hyyperparameter Tuning in the cmd
*run this command ( tensorboard --logdir=Tensorboard)
*click on localhost link

-----------------------------------------------------------------------------------

6. SRCNNx4

Model: SRCNN with scale=4
Notebook: SRCNNx4.ipynb
Model Weights: srcnnx4.pth
Tensorboard: srcnnx4Tensorboard
Inference Examples to Compare between other models: SRCNNx4_to compare
Inference Examples: SRCNNx4_Results

TO RUN TENSORBOARD
*Navigate to the folder ./SRCNNx4 in the cmd
*run this command ( tensorboard --logdir=srcnnx4Tensorboard)
*click on localhost link



