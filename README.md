# OpenCV_Shirt
This is a project using opencv

# Virtual Shirt Fitting Room

## Introduction

Welcome to the Virtual Shirt Fitting Room project! This application utilizes computer vision techniques and pose detection to create an interactive experience where users can virtually try on different shirts using their webcam. Built with Python, this project leverages libraries such as OpenCV, MediaPipe, and CVZone to track user poses and overlay shirts on the webcam feed in real-time.

## Packages to Install

Before running the project, you will need to install several Python libraries. You can install these using the following pip commands:

```python
pip install opencv-python
pip install mediapipe
pip install cvzone
pip install wheel
```


# Usage
To use the Virtual Shirt Fitting Room, ensure your webcam is connected and operational. The main script captures video from the webcam, detects the user's pose, and overlays a shirt image based on the pose. Here is a snippet to initialize the webcam:

```python
import cv2

# Using a prebuilt camera
# 0 is the index
cap = cv2.VideoCapture(0)


```


# Code Snippets
Here's a brief look at how the project handles pose detection and shirt overlay:

```python
import cvzone
from cvzone.PoseModule import PoseDetector

detector = PoseDetector()
shirtFolderPath = "Resources/Shirts"
listShirts = os.listdir(shirtFolderPath)
imageNumber = 0

while True:
    success, img = cap.read()
    img = detector.findPose(img)
    lmList, bboxInfo = detector.findPosition(img, bboxWithHands=False, draw=False)
    if lmList:
        # Code to overlay shirts goes here


```


# Images



# Conclusion
The Virtual Shirt Fitting Room showcases the potential of integrating computer vision into retail and e-commerce platforms. By allowing users to try on clothes virtually, it offers a convenient and innovative shopping experience. We hope this project inspires further exploration into the possibilities of technology in fashion retail.
