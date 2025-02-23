# Brain Tumor Classification Using EfficientNet-B7

## Introduction of Dataset
The dataset for this project consists of MRI scans of brain tumors, sourced from a Google Drive zip file (brain_tumor_dataset.zip). It includes 2,870 training images and approximately 410 test images, split into four classes: glioma_tumor, meningioma_tumor, no_tumor, and pituitary_tumor. The distribution shows a mild imbalance, with 395 "no_tumor" images compared to ~820–827 images per tumor class, necessitating class weighting for balanced training.

## About This Project
This project aims to automate brain tumor detection and classification from MRI scans, addressing the challenges of manual diagnosis, especially in resource-limited settings. The system leverages deep learning to improve accuracy and efficiency, targeting high diagnostic precision for glioma, meningioma, pituitary tumors, and non-tumor cases. Implemented in Google Colab, it uses transfer learning to handle the complexity and variability of brain tumor features, with a focus on achieving robust performance on imbalanced data.

## EfficientNetB7 Model
The project employs EfficientNetB7, the largest and most advanced variant in the EfficientNet family, pre-trained on ImageNet. This model offers superior accuracy due to its compound scaling of depth, width, and resolution. The implementation includes:

Initial training with frozen base layers, followed by fine-tuning of the top 20% of layers.

Enhanced data augmentation (rotation, shifts, shear, zoom, flips) and normalization for robustness.

Class weights to address dataset imbalance, Adam optimizer with learning rates (1e-2 initially, 1e-2 for fine-tuning), and callbacks (early stopping, learning rate reduction).

Despite optimization, current test accuracy is 54.06%, indicating potential issues like insufficient fine-tuning or data preprocessing mismatches, as revealed by a confusion matrix showing poor distinction between tumor classes.

## Summary
The EfficientNetB7-based brain tumor classification system demonstrates potential for high accuracy but currently achieves only 54.06% due to challenges with imbalanced data, limited fine-tuning, or data quality. With adjustments—such as extending fine-tuning, enhancing data augmentation, and verifying dataset integrity—this model can achieve its expected performance (>90%), offering a reliable tool for automated MRI diagnosis and improving patient outcomes in clinical settings.
