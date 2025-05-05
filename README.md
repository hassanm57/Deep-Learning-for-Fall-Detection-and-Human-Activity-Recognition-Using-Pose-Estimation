# Deep Learning for Fall Detection and Human Activity Recognition Using Pose Estimation

This repository demonstrates the use of **Deep Learning** techniques for **Fall Detection** and **Human Activity Recognition (HAR)** using **pose estimation** across three different datasets: **UR Fall Dataset**, **Le2i Dataset**, and **Montreal Fall Dataset**. Despite the variety of datasets, the same processing pipeline and feature extraction methods are applied to all of them, creating a unified approach for detecting falls and recognizing human activities.

## Overview

The project utilizes **MediaPipe Pose Estimation** to extract keypoints from human poses in video frames. These keypoints are processed into meaningful features such as joint angles, velocity, acceleration, and the center of gravity. These features are then fed into a deep learning model to classify between **falls** and **activities of daily life (ADLs)**.

## Steps

### 1. **Pose Estimation with MediaPipe**
- MediaPipe's pose estimation model is employed to detect 33 keypoints for each frame. Each keypoint includes (x, y) coordinates and visibility score.
- These keypoints are used as features to represent human poses in the video frames.
![outp11ut](https://github.com/user-attachments/assets/878cbdb7-9abf-4aeb-ac61-ac8e13726d99)
![image](https://github.com/user-attachments/assets/07167f31-387d-4999-9e07-c88712a8fade)
![image](https://github.com/user-attachments/assets/d4784574-f6a3-496c-af55-99aa434f8a53)



### 2. **Pre-processing of Image Sequences**
- The datasets consist of video sequences that are processed frame-by-frame to extract keypoints.
- Each sequence is labeled: **1 for fall** and **0 for ADL**.

### 3. **Feature Extraction**
- Key features like joint angles, velocity, and acceleration are computed from the detected keypoints.
- The center of gravity and other pose-based attributes are also included as features for better model accuracy.

### 4. **Model Training**
- A deep learning model (e.g., CNN or RNN) is trained on these features to classify each sequence as either a **fall** or **ADL**.
- The model is evaluated on the respective datasets, providing a general framework for fall detection and activity recognition.

## Datasets

This project uses the following datasets:

- **UR Fall Dataset**: Contains video sequences of falls and normal activities.
  ![image](https://github.com/user-attachments/assets/c44d793b-8d19-4cd9-855c-5574ce363de4)

- **Le2i Dataset**: Includes video data with activities like walking, sitting, and falling.
![image](https://github.com/user-attachments/assets/486bacaa-99d0-4f3d-9670-b9a1f4f10b36)

- **Montreal Fall Dataset**: A collection of videos with labeled falls and other activities.
  ![image](https://github.com/user-attachments/assets/c295feb9-0f8e-4d23-99a5-94cf0d7f0f4a)


## Requirements

- Python 3.x
- TensorFlow/Keras
- MediaPipe
- OpenCV
- NumPy
- pandas

