# MRI-Brain-Tumor-Detection-Segmentation-using-Attention-U-Net
Developed a deep learning model for brain tumor detection and segmentation from MRI scans. Used CNN for classification and Attention U-Net for segmentation
# 🧠 Brain Tumor Segmentation using Deep Learning (BraTS 2024)

This project focuses on semantic segmentation of brain tumors using 2D MRI slices from the BraTS 2020 dataset. Leveraging a U-Net inspired convolutional neural network, the model accurately delineates tumor regions, aiding in medical imaging research and diagnosis.

---

## 📁 Dataset

- **Source**: [BraTS 2020 Challenge Dataset](https://www.med.upenn.edu/cbica/brats2020/data.html)
- Format: `.h5` files containing 3D MRI volumes and corresponding segmentation masks.
- Modalities used: FLAIR, T1, T1CE, T2 (depending on preprocessing)

---

## 🛠️ Features

- 📦 **Custom Data Pipeline**: Loads, preprocesses, and extracts 2D slices from 3D `.h5` files.
- 🎯 **Segmentation Model**: U-Net based CNN built with Keras/TensorFlow.
- 🧪 **Training & Validation**: Over 10,000 slice-mask pairs, split with shuffling for robust evaluation.
- 📊 **Evaluation**: Dice coefficient, binary accuracy; visual slice-mask overlays for inspection.
- 🖼️ **Visualization Tools**: View any slice or overlay predictions interactively.
- 💡 **Optimizations**: Dropout regularization, early stopping, and dynamic reshaping.

---

## 🧠 Model Architecture

- Input: 128x128 grayscale MRI slice  
- Layers: 
  - 2 convolutional blocks with ReLU and MaxPooling
  - Bottleneck layer with dropout
  - Up-sampling path with skip connections
  - Final layer: 1x1 convolution with sigmoid activation for binary mask output

---

## 🚀 How to Run


# Clone the repo
git clone https://github.com/your-username/brain-tumor-segmentation.git
cd brain-tumor-segmentation

# Install requirements
pip install -r requirements.txt

# Run the notebook
jupyter notebook BraTS-2024_ver-2i.ipynb

📌 # **Results**
Achieved high segmentation accuracy with smooth boundary detection.

Visual overlays showed strong alignment with ground truth masks.

🤝# Acknowledgments
BraTS 2020 Challenge

TensorFlow/Keras for deep learning tools

Community notebooks and preprocessing guides


