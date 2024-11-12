# Real_Time_Object_detection

This Python program is for real-time object detection using the YOLOv9 model and OpenCV. It detects objects in video frames captured from the system's default camera, draws bounding boxes around detected objects, and labels them with the object class and detection confidence.

# Code Overview
The program performs the following steps:

**Model Initialization:**

The YOLOv9 model (yolov9c.pt) is loaded and moved to the appropriate device (GPU if available, otherwise CPU).
Video Capture:

The program initializes the default webcam (device 0) using OpenCV's cv2.VideoCapture() function.
It checks if the webcam is opened successfully and starts reading video frames.
Object Detection:

For each frame, the YOLOv9 model processes the frame and detects objects in it.
The model returns bounding box coordinates, class IDs, and confidence scores for each detected object.
Drawing Bounding Boxes:

For each detected object, the program draws a bounding box and places a label showing the object class and confidence score on the frame.
Displaying Results:

The processed frame (with bounding boxes and labels) is displayed in a window.
The program continuously captures frames and updates the display until the user presses q to quit.
Release Resources:

After quitting, the program releases the video capture device and closes the display window.

# Requirements
Python 3.8+
OpenCV
PyTorch
Ultralytics YOLOv9 model

**To install dependencies:**

pip install opencv-python-headless torch ultralytics
