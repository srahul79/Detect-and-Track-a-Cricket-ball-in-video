# 🏏 Cricket Ball Detect & Track in Video

This project focuses on **detecting a cricket ball in a video**, **tracking its movement frame by frame**, and **visualizing its trajectory** using a fine-tuned **YOLOv11 object detection model**.

The system detects the ball, extracts its coordinates, stores them in a structured file, and generates an annotated video with a **trajectory overlay**.

---

##  Project Objectives

- Detect the cricket ball in a video using a deep learning model
- Fine-tune a YOLOv8 model on a custom cricket ball dataset
- Extract the ball’s center coordinates `(x, y)` for each frame
- Maintain a **visibility flag** for missed detections
- Save detection results in a CSV file
- Generate an output video with:
  - Bounding box
  - Label (`ball`)
  - Trajectory path overlay

---

##  Approach Overview

1. **Dataset Preparation**
   - Extract frames from cricket videos
   - Annotate cricket ball bounding boxes in YOLO format
   - Organize dataset using YOLO directory structure

2. **Model Training**
   - Use pretrained YOLOv8 weights
   - Fine-tune the model on a single class: `cricket_ball`

3. **Inference & Tracking**
   - Run detection on video frames
   - Compute ball center from bounding box
   - Track ball positions across frames

4. **Visualization & Storage**
   - Draw bounding box and label on video
   - Overlay trajectory path using historical coordinates
   - Save coordinates to CSV for analysis

---
