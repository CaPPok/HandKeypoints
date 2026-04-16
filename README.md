# Hand Keypoints Detection

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)

## Project Overview
This repository contains a Deep Learning project focused on detecting **21 hand keypoints**. The model processes RGB images and predicts both the bounding box and the spatial coordinates `(x, y)` for the 21 points of a human hand.

## Model Architecture & Methodology
- **Framework:** PyTorch
- **Model:** Convolutional Neural Network (CNN) - ResNet18
- **Loss Function:** Mean Squared Error (`nn.MSELoss`) applied for both Bounding Box and Keypoints prediction.
- **Optimizer:** Adam (`lr=1e-4`)
- **Epochs:** 30

## Dataset
The model is trained on the **Ultralytics Hand Keypoints Dataset**.
- **Train set:** 18,776 images
- **Validation set:** 7,992 images
- **Format:** YOLO Pose format. Each `.txt` label contains the class, bounding box coordinates, and 21 keypoints `(x, y, visible)`.

> **Note:** The raw images (`images/train` and `images/val`) and labels (`labels/train` and `labels/val`) are not included in this repository. You can download the dataset using the instructions in `data.yaml` or [download it here](https://github.com/ultralytics/assets/releases/download/v0.0.0/hand-keypoints.zip).

## Repository Structure
```text
.
├── images/             # (Ignored in Git) Download and place images here
├── labels/             # (Ignored in Git) Download and place labels here
├── data.yaml           # Dataset configuration
├── DATH_TTNT.ipynb     # Main pipeline
├── Report.pdf          # Project report
└── README.md           # README file
```