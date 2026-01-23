# Multi-Object Tracking & Re-Identification (Computer Vision)

This project explores **object detection, tracking, and re-identification** in video sequences using state-of-the-art computer vision models.

---

## Problem

Detect and track multiple objects (cups) across video frames while maintaining consistent object identities despite:

- Occlusion
- Object removal and reappearance
- Camera motion
- Scale and viewpoint changes

The task reflects real-world challenges commonly encountered in multi-object tracking (MOT) systems.

---

## Approach

The pipeline is composed of three main stages:

### Object Detection
- **YOLOv8** (pretrained on the COCO dataset)
- Robust detection across varying scales and partial occlusions

### Object Tracking & Re-Identification
- **BoT-SORT** as the primary tracker
- Comparative evaluation with:
  - ByteTrack
  - StrongSORT
  - OC-SORT
  - DeepOC-SORT
- Motion and appearance-based association

### Evaluation
- Qualitative analysis through visual inspection
- Tracking performance analyzed using MOT metrics:
  - HOTA
  - Detection Accuracy (DetA)
  - Association Accuracy (AssA)
  - Localization Accuracy (LocA)

---

## Key Findings

- YOLOv8 achieved strong detection performance across scales
- BoT-SORT outperformed other trackers in re-identification scenarios
- Re-identification accuracy degraded under large viewpoint changes
- Detection accuracy remained high; association accuracy was the main limitation

---

## Limitations

- Re-identification struggled under extreme viewpoint changes
- Hyperparameters were tuned on MOT datasets rather than task-specific data
- Full quantitative evaluation was limited by hardware constraints (Apple M1 compatibility issues)

---

## Possible Improvements

- Fine-tuning YOLOv8 on task-specific data
- Dataset-specific hyperparameter tuning
- Using larger detection backbones to improve scale robustness
- Incorporating additional appearance features for stronger re-identification

---

