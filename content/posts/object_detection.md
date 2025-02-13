+++
authors = ["Jonas Steinhauser"]
title = "YOLO-based object detection"
date = "2025-02-24"
description = "This article explores the fusion of sensor data for object detection and localization in indoor environments. Building on prior research at RWU, which benchmarked YOLOv7 and YOLOv8 on the YCB dataset, this project extends the analysis to YOLOv9."
tags = [
"Scientific Project",
]
+++

# Servus 👋

I am currently starting a new research project focused on **sensor fusion for object detection and localization in indoor environments**. In this blog, I will document the entire development process and share my progress.

## What is YOLO?

When it comes to real-time object detection, **YOLO (You Only Look Once)** is one of the most widely used deep learning-based algorithms. Unlike traditional object detection models, which analyze an image in multiple steps, YOLO takes a different approach—it processes the entire image in a single forward pass of a neural network. This makes it extremely fast and efficient, making it ideal for applications in robotics, autonomous systems, and real-time surveillance.

YOLO works by dividing an image into a grid and predicting bounding boxes along with confidence scores for potential objects within those regions. The latest versions, such as YOLOv11, have improved accuracy, speed, and adaptability for complex detection tasks, making them a great choice for applications like **sensor fusion and indoor localization**. For more details, this source provides an excellent overview: [Roboflow Guide to YOLO Models](https://blog.roboflow.com/guide-to-yolo-models/).

## Benchmarking YOLO on the YCB Dataset

A previous study conducted at RWU analyzed the performance of **YOLOv7 and YOLOv8** on the **YCB dataset**, which contains 77 household objects commonly used in robotics applications. The study aimed to compare these frameworks in terms of their efficiency and accuracy for object detection[^1].

### Key Findings:

- **Dataset & Training:** The study used the **YCB-Video and YCB-M datasets**, consisting of 21 objects, and introduced a new **Robot Domain Dataset (RDD)** with 259 images taken with an RGB-D camera in realistic environments.
- **Evaluation Metrics:** Performance was measured using the **MS COCO metric (AP@[.5:.05:.95], mAP50, mAP75)**.
- **Results:**
  - **YOLOv8** performed better or equally well as **YOLOv7** on the **YCB-M and YCB-Video** datasets.
  - **YOLOv7** significantly outperformed YOLOv8 on the **RDD dataset**, demonstrating **better generalization in novel environments** with varying backgrounds and lighting conditions.
- **Conclusion:** While **YOLOv8** is well-suited for known datasets, **YOLOv7** excels in handling **unseen environments**, making it more applicable for real-world robotics applications where adaptability is crucial.

This research provides a strong foundation for my project, as it highlights the importance of selecting the right YOLO framework depending on the use case. This work has since been extended internally to incorporate YOLOv9, which is now used for object detection. Building upon this detection system, the next steps will focus on refining sensor fusion techniques to further improve object detection and localization accuracy in robotic applications.

I look forward to sharing this journey with you. See you soon!

**Servus 👋**

*Jonas*

[^1]: Samuel Hafner, Markus Schneider, Benjamin Stähle (2024). *Performance Comparison of YOLOv7 and YOLOv8 Using the YCB Datasets YCB-M and YCB-Video*. EasyChair Preprint 13111, version 2. https://easychair.org/publications/preprint/c3GK


