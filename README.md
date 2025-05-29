# BraTS2020 Brain Tumor Segmentation

## Project Overview

Brain tumor segmentation involves identifying and outlining tumor regions within MRI scans. This process plays a critical role in diagnosis, treatment planning, and tracking the progression of brain tumors. However, the task is complicated by the variability in tumor shape, size, location, and the presence of surrounding tissues with similar intensities, making manual segmentation both difficult and time consuming.

To address these challenges, deep learning techniques, particularly convolutional neural networks (CNNs) and U Net architectures, have emerged as powerful tools. These models can capture both spatial and contextual information from MRI scans, enabling automated segmentation of tumor subregions such as the enhancing tumor, edema, and necrotic core, which are vital for clinical decisions.

## Dataset: BraTS 2020

This project uses the BraTS 2020 dataset from the Brain Tumor Segmentation Challenge. The dataset comprises 3D MRI scans from 369 patients, each including four different modalities:

- T1 weighted (T1)
- T1 weighted post contrast (T1CE)
- T2 weighted (T2)
- Fluid Attenuated Inversion Recovery (FLAIR)

Each scan is accompanied by ground truth masks that segment tumor regions into:

- Necrotic and non enhancing tumor core
- Peritumoral edema
- Enhancing tumor

[Dataset on Kaggle](https://www.kaggle.com/datasets/awsaf49/brats20-dataset-training-validation/data)

## Model Architecture: U Net

This project employs the U Net architecture, widely recognized for its effectiveness in medical image segmentation. U Net features a symmetric encoder decoder structure:

- The encoder captures contextual information through successive downsampling
- The decoder reconstructs detailed segmentation maps via upsampling

A key strength of U Net is the use of skip connections between corresponding encoder and decoder layers, which preserve fine spatial details that are crucial for accurate segmentation.

U Net is particularly suitable for scenarios with limited training data, a common issue in medical imaging. With techniques like data augmentation, U Net maintains high segmentation accuracy while remaining computationally efficient.

## References and Further Reading

1. [BraTS 2020 Dataset on Kaggle](https://www.kaggle.com/datasets/awsaf49/brats20-dataset-training-validation)  
2. [BraTS U Net Segmentation BNS Reenu GitHub](https://github.com/bnsreenu/python_for_microscopists/tree/master/231_234_BraTa2020_Unet_segmentation)  
3. [U Net Convolutional Networks for Biomedical Image Segmentation arXiv](https://arxiv.org/abs/1505.04597)  
4. [Understanding Evaluation Metrics in Medical Image Segmentation Medium](https://medium.com/@nghihuynh_37300/understanding-evaluation-metrics-in-medical-image-segmentation-d289a373a3f)
