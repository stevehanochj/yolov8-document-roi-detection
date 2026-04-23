# Document ROI Detection using YOLOv8

This repository contains a training pipeline for detecting Regions of Interest (ROI) in document images (such as receipts and invoices) using a custom YOLOv8 model. 

This is typically used as a preprocessing step for Optical Character Recognition (OCR) systems to isolate specific fields (e.g., Total Amount, Date, Vendor Name) before extracting the text.

## 🚀 Overview
- **Model:** YOLOv8s (Small)
- **Framework:** Ultralytics
- **Dataset:** Roboflow OCR-2 Dataset
- **Environment:** Google Colab (T4 GPU)

## 📁 Repository Structure
- `train_yolov8.ipynb`: The main Google Colab notebook containing the end-to-end workflow:
  - Environment setup and dependency installation.
  - Dataset retrieval via Roboflow API.
  - Model training (18 Epochs).
  - Performance validation and visualization (Confusion Matrix, Loss Curves).
  - Inference on test images.

## 🛠️ Usage
### Running the Notebook
You can view the code and run the training process directly in your browser using Google Colab. Click the badge below to open it:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ldBg7krIRNdcekuq-E1ll4eQGivcY33E)


### Dataset Configuration
The notebook is configured to download a dataset from Roboflow. You will need to insert your own Roboflow API key in the dataset download cell:
```python
from roboflow import Roboflow
rf = Roboflow(api_key="YOUR_API_KEY_HERE")
