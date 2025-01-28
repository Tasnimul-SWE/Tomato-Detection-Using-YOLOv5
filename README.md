
## Tomato Detection Using YOLOv5

This repository contains code for detecting tomatoes in images using the YOLOv5 deep learning model. The project leverages PyTorch for deep learning and is optimized for use with GPU acceleration.


---

## Setup and Requirements

## Environment
Python version: 3.8 or higher

## Libraries and Versions
torch >= 1.7
PyYAML == 5.4.1
Wandb >= 0.12
split-folders >= 0.4.3

## YOLOv5 requirements:
Install YOLOv5 dependencies:
pip install -r yolov5/requirements.txt

## Hardware Requirements
GPU: NVIDIA Tesla P100 or T4 recommended for optimal performance.
CUDA and cuDNN installed for GPU acceleration.

---

## Installation
Clone the repository:
git clone https://github.com/ultralytics/yolov5

---

## Data Preparation
Download the tomato detection dataset from Kaggle:
kaggle datasets download -d andrewmvd/tomato-detection


