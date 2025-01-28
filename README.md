
Tomato Detection Using YOLOv5

This repository contains code for detecting tomatoes in images using the YOLOv5 deep learning model. The project leverages PyTorch for deep learning and is optimized for use with GPU acceleration.

Setup and Requirements

Environment
Python version: 3.8 or higher

Libraries and Versions
torch >= 1.7
PyYAML == 5.4.1
Wandb >= 0.12
split-folders >= 0.4.3

YOLOv5 requirements:
Install YOLOv5 dependencies:
pip install -r yolov5/requirements.txt

Hardware Requirements
GPU: NVIDIA Tesla P100 or T4 recommended for optimal performance.
CUDA and cuDNN installed for GPU acceleration.

Installation
Clone the repository:
git clone https://github.com/ultralytics/yolov5

Install required libraries:
pip install torch PyYAML==5.4.1 wandb split-folders

Install YOLOv5 requirements:
pip install -r yolov5/requirements.txt

Usage

Data Preparation
Download the tomato detection dataset from Kaggle:
kaggle datasets download -d andrewmvd/tomato-detection

Unzip the downloaded dataset:
unzip *.zip && rm *.zip

Split the dataset into training, validation, and test sets using split-folders.

Training
Train the YOLOv5 model:
python train.py --img 640 --batch 4 --epochs 50 --data /path/to/data.yaml --cfg /path/to/yolov5s.yaml --weights yolov5s.pt --name yolov5s_results

Testing
Run tests on the model:
python test.py --weights /path/to/best.pt --data /path/to/data.yaml --img 640 --augment

Detection
Perform detection on images or videos:
python detect.py --img-size 640 --conf 0.4 --source /path/to/images --weights /path/to/best.pt --augment

Results and Visualization
Training and validation results can be visualized in the /runs/train directory.
Visualize confusion matrices and other metrics using Wandb or saved PNG images.
