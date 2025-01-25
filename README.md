# GenAI‐marble_cracks Dataset

## Overview
We propose a generative Artificial Intelligence (AI) approach, reporting the first synthetic marble crack texture image dataset using four generative adversarial networks (GANs). Each of the final four sub-datasets includes images of different cracks on marble surfaces. Moreover, to verify the effectiveness and significance of this work, two deep learning segmentation models are used to assess the quality of the synthetic marble crack image datasets.

The proposed generation and evaluation pipeline is illustrated in Fig. 1. From a finite number of original marble crack images of the MCS-2 dataset [1], four different GAN architectures are applied to generate sets of large-scale marble crack samples, forming the synthetic image dataset known as GenAI‐marble_cracks dataset. 


To evaluate the quality of the synthetic images, we tested two deep learning segmentation models: **Feature Pyramid Network (FPN)** and **U-Net**, both utilizing the efficientnetb4 backbone.

The generation and evaluation pipeline is illustrated below:
- Original marble crack images from the MCS-2 dataset were preprocessed.
- Four GAN architectures generated synthetic datasets.
- Real and synthetic images were combined and tested using different training strategies for marble crack segmentation.

## Dataset Structure
The dataset consists of real and generated marble crack images, organized as follows:

### **Folder Structure**
| Folder Name | Subfolder Name | Description |
|-------------|----------------|-------------|
| **Marble crack image generation** | **GenAI‐marble_cracks dataset** | **real images**: 440 patches from the MCS-2 dataset |
| | **gan**: 148 generated crack images with annotation masks |
| | **wgan**: 148 generated crack images with annotation masks |
| | **wgan_div**: 94 generated crack images with annotation masks |
| | **wgan_gp**: 121 generated crack images with annotation masks |
| **Marble crack segmentation** | **First experiment** | Segmentation results on real and synthetic data |
| | **Second experiment** | Results with combinations of real and synthetic images |
| | **Third experiment** | Extended segmentation evaluation |

### **Example Data Samples**
- **Real Images**: Cropped into 440 patches.
- **Generated Images**: Outputs from GAN, WGAN, WGAN-GP, and WGAN-div after 200 training epochs.

### **Video Sequences**
| File Name | Description |
|-----------|-------------|
| `Crack_Generated_Images.mp4` | Video sequence of marble crack generation results (~50 images) |
| `Crack_Segmentation_Exp_1.mp4` | Video of segmentation results from Experiment 1 |
| `Crack_Segmentation_Exp_2.mp4` | Video of segmentation results from Experiment 2 |
| `Crack_Segmentation_Exp_3.mp4` | Video of segmentation results from Experiment 3 |

## Experiments
### First Experiment
- Segmentation using **FPN** and **U-Net** on:
  - **Real images**: 281 patches + augmentation.
  - **Synthetic images**: GAN, WGAN, WGAN-div, WGAN-GP.

### Second Experiment
- Tested segmentation models on:
  - **FPN**: Real + 300 synthetic images (100 from each model).
  - **U-Net**: Real + 200 synthetic images (100 from GAN, 100 from WGAN-div).

### Third Experiment
- Extended segmentation evaluation:
  - FPN and U-Net models tested with real data + 200 GAN-generated images.

## References
1. E. Vrochidou et al., “RGB and Thermal Image Analysis for Marble Crack Detection with Deep Learning,” in *International Conference on Paradigms of Communication, Computing and Data Analytics (PCCDA 2023)*, 2023.
2. E. Vrochidou et al., “Utilizing Generative AI for Crack Detection in the Marble Industry,” *Engineering Research Express*, Jan. 2025, doi: [10.1088/2631-8695/adaca7](https://doi.org/10.1088/2631-8695/adaca7).

## Citation
If you use this dataset in your research, please cite:
