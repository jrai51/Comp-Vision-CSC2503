# CSC2503 - Assignment 1: Computer Vision and Deep Learning

This repository contains all code, models, and results for **CSC2503 Assignment 1**, which covers convolutional neural networks, transfer learning, cross-dataset generalization, and object tracking using OpenCV.

The implementation work and reports are implemented in **Jupyter Notebook (`hw1.ipynb`)**, with supporting datasets, models, and scripts organized as shown below.

---

## Repository Structure

```
COMP-VISION-CSC2503/
│
├── dog-breed-images/ # Dog Breed Images (DBI) dataset
│ ├── bernese_mountain_dog/
│ ├── border_collie/
│ ├── chihuahua/
│ ├── golden_retriever/
│ ├── labrador/
│ ├── pug/
│ └── siberian_husky/
│
├── stanford-dogs-dataset/ # Stanford Dogs Dataset (SDD)
│ ├── annotations/ # Annotation files (not used directly)
│ └── images/
│ ├── bernese_mountain_dog/
│ ├── border_collie/
│ ├── chihuahua/
│ ├── golden_retriever/
│ ├── labrador/
│ ├── pug/
│ └── siberian_husky/
│
├── models/ # Pretrained model definitions
│ ├── deploy.prototxt.txt # Face detector model definition
│ └── res10_300x300_ssd_iter_140000.caffemodel # Face detector weights
│
├── goturn.caffemodel # GOTURN tracker weights (large file)
├── goturn.prototxt # GOTURN model definition
│
├── hw1.ipynb # Main notebook (all code + report)
├── environment.yml # Conda environment file
│
├── TheOffice.mp4 # Short video clip used for face tracking
├── iou_comparison.png # Comparison plot for tracker IoUs
├── simpleCNN_loss.png # CNN training loss visualization
├── tracks.json # Saved tracking results
└── README.md # You are here!
```

## Create the Conda Environment

This project uses an environment.yml file to ensure consistent dependencies across systems. 
```
conda env create -f environment.yml
conda activate compvision
```
Make sure you’re running the notebook kernel using the compvision environment. In Jupyter, you can confirm this by selecting Kernel → Change Kernel → compvision.

## Large Model Files

Some pretrained models are too large to include in GitHub directly.
If you are missing these files, download them manually:

| File                                                  | Description                      | Download Link                                                                                                                               |
| ----------------------------------------------------- | -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **`models/res10_300x300_ssd_iter_140000.caffemodel`** | OpenCV DNN Face Detector weights | [Download Here](https://github.com/opencv/opencv_3rdparty/blob/dnn_samples_face_detector_20170830/res10_300x300_ssd_iter_140000.caffemodel) |
| **`models/deploy.prototxt.txt`**                      | Face detector architecture       | [Download Here](https://github.com/opencv/opencv/blob/master/samples/dnn/face_detector/deploy.prototxt)                                     |
| **`goturn.caffemodel`**                               | GOTURN tracker weights           | [Download Here](https://github.com/Mogball/goturn-files)                                                           |
| **`goturn.prototxt`**                                 | GOTURN model architecture        | [Download Here](https://github.com/Mogball/goturn-files)

Once downloaded, place them in the project root (same directory as hw1.ipynb).



