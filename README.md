# Brain-Tumor-Detect-Sys-using-MobileNet-UNet-computer-vision-
A comprehensive deep learning system for automated brain tumor detection and segmentation in MRI scans, combining MobileNet for classification and U-Net with MobileNetV2 encoder for precise tumor segmentation.

## Overview
This project implements an intelligent medical imaging system that assists radiologists in diagnosing brain tumors through two main tasks:
•	Binary Classification: Detecting the presence or absence of brain tumors using a lightweight MobileNet architecture
•	Tumor Segmentation: Accurately localizing and segmenting tumor regions using a U-Net model with MobileNetV2 encoder
## Key Features
•	High Accuracy: Achieves 92.18% validation accuracy in classification and 99.37% in segmentation
•	Lightweight Architecture: Optimized for real-world deployment with minimal computational overhead
•	User-Friendly Interface: Interactive Gradio-based web interface for easy MRI image upload and real-time predictions
•	Complete Pipeline: End-to-end solution from preprocessing to visualization with tumor region highlighting
•	Transfer Learning: Leverages ImageNet pre-trained weights for faster convergence and better performance
## Technologies Used
•	Deep Learning Frameworks: TensorFlow/Keras
•	Neural Network Architectures: MobileNet, MobileNetV2, U-Net
•	Image Processing: OpenCV, PIL
•	Web Interface: Gradio
•	Development Environment: Python, Google Colab with GPU support
## Dataset
•	Source: Kaggle Brain MRI Images for Brain Tumor Detection
•	Total Images: 3,929 T1-weighted contrast-enhanced MRI scans
•	Classes: Binary (tumor present/absent)
•	Format: JPEG with varying resolutions
•	Split: 75% training, 15% validation, 10% testing

## Architecture
### Classification Model (MobileNet)
•	Pre-trained MobileNet backbone with custom classification head
•	Input: 224×224×3 RGB images
•	Output: Binary classification (tumor/no tumor)
•	Optimizer: Adam with binary cross-entropy loss
### Segmentation Model (U-Net + MobileNetV2)
•	MobileNetV2 encoder with frozen pre-trained weights
•	U-Net decoder with skip connections for precise localization
•	Output: Binary segmentation mask highlighting tumor regions
•	Loss: Binary cross-entropy with Dice coefficient
## Performance Metrics
### Classification Results
•	Training Accuracy: 91.32%
•	Validation Accuracy: 92.18%
•	Training Loss: 0.2158
•	Validation Loss: 0.2132
### Segmentation Results
•	Training Accuracy: 99.25%
•	Validation Accuracy: 99.37%
•	Dice Coefficient: High overlap between predictions and ground truth
•	IoU Score: Excellent intersection over union metrics
## Getting Started
### Prerequisites
bash
pip install tensorflow keras opencv-python gradio numpy matplotlib
## Usage
1.	Clone the repository
2.	Load the pre-trained models
3.	Run the Gradio interface
4.	Upload MRI images for instant classification and segmentation results
## Web Interface
### The Gradio-based interface provides:
•	Easy MRI image upload
•	Automatic preprocessing and normalization
•	Real-time tumor detection
•	Visual segmentation with tumor regions highlighted in red
•	Clear text-based classification results
•	Error handling for invalid inputs
### Research Applications
This system demonstrates the practical application of AI in medical imaging, offering:
•	Automated diagnostic assistance for radiologists
•	Fast and accurate tumor detection
•	Reduced diagnosis time
•	Support for treatment planning
•	Educational tool for medical students

 ## References
Based on research in deep learning for medical image analysis, utilizing state-of-the-art CNN architectures optimized for medical imaging tasks.
 ## License
This project is intended for educational and research purposes in medical AI applications.
________________________________________
⚠️Medical Disclaimer: This system is designed as a diagnostic aid and should not replace professional medical judgment. All results should be verified by qualified healthcare professionals.
