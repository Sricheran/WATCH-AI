# WATCHAI


# Multi-Camera Object Tracking with DeepSort and YOLO

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Requirements](#2-requirements)
3. [Project Structure](#3-project-structure)
4. [Installation](#4-installation)
5. [Documentation of Code](#5-documentation-of-code)
6. [Contributors](#6-contributors)

## 1. Project Overview

This project demonstrates multi-camera object tracking using the DeepSort algorithm for tracking and the YOLO (You Only Look Once) object detection model. The project tracks objects across two video streams and displays the tracked objects with bounding boxes and unique IDs in real-time.

## 2. Requirements

Before running this project, ensure you have the following dependencies installed:

- Python 3.x
- OpenCV (cv2)
- PyTorch
- NumPy
- Ultralytics
- DeepSort
- YOLOv8
- easydict

You can install these dependencies using `pip`:

```bash
pip install opencv-python-headless torch numpy ultralytics deep_sort easydict
```

## 3. Project Structure

The project's directory structure is as follows:

```
project-root/
    ├── deep_sort/
    │   ├── deep/
    │   │   └── checkpoint/
    │   │       └── ckpt.t7
    │   └── ...
    ├── yolov8n.pt
    ├── your_script.py
```

- **`deep_sort/`**: Contains the DeepSort algorithm code and model checkpoint.
- **`yolov8n.pt`**: YOLOv8 model checkpoint for object detection.
- **`your_script.py`**: The Python script for object detection and tracking.

## 4. Installation

1. Clone or download the project repository to your local machine.
2. Install the required dependencies as mentioned in the [Requirements](#2-requirements) section.
3. Place your YOLOv8 model checkpoint file (`yolov8n.pt`) in the project directory.

## 5. Documentation of Code

Below are the key components and functions in the code:

- Import necessary libraries and modules:
    - `cv2`: OpenCV for video capturing and image processing.
    - `torch`: PyTorch for deep learning.
    - `numpy`: NumPy for numerical operations.
    - `YOLO`: Ultralytics' YOLO for object detection.
    - `DeepSort`: DeepSort for object tracking.
- Define video paths (`video_path1` and `video_path2`) for your camera feeds.
- Initialize DeepSort trackers (`tracker1` and `tracker2`) with the provided model checkpoint.
- Create video capture objects for both camera streams (`cap1` and `cap2`).
- Define frame buffers (`frames1` and `frames2`) for storing frames (not used in this code).
- Start a loop to process frames from both cameras.
- Read frames from both cameras (`frame1` and `frame2`).
- Perform object detection using YOLO on both frames and obtain detection results (`results1` and `results2`).
- Iterate through the detection results and extract information such as bounding boxes, class names, and confidence scores.
- Update the DeepSort trackers with the detected objects' information.
- Draw bounding boxes and track IDs on the frames based on the tracked objects.
- Display the frames with tracking information using OpenCV.
- The loop continues until 'q' is pressed, and then it releases video capture objects and closes all windows.

## 6. Contributors

- CH SRICHERAN - [sricharan320@gmail.com](mailto:sricharan320@gmail.com)
- PN SANJAY - [sanjayperam2604@gmail.com](mailto:sanjayperam2604@gmail.com)
- PVS SUKRITH - [sukrithpvs2005@gmail.com](mailto:sukrithpvs2005@gmail.com)
- ADITHYA VARDAN - [adithyavardan.melam@gmail.com](mailto:adithyavardan.melam@gmail.com)

 
