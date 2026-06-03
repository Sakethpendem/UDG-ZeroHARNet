# UDG-ZeroHARNet

UDG-ZeroHARNet is a domain-generalized zero-shot Human Activity Recognition framework using multi-dataset IMU sensor data.

## Overview

This project focuses on cross-dataset Human Activity Recognition, where a model is trained on multiple source datasets and evaluated on an unseen target dataset without target fine-tuning.

The goal is to improve generalization across different users, devices, sensor placements, sampling styles, and dataset domains.

## Datasets Used

- UCI HAR
- HAPT
- MotionSense
- HHAR
- KU-HAR
- Shoaib

## Activity Classes

The datasets were harmonized into four common activity classes:

- Still
- Walking
- Upstairs
- Downstairs

## Methodology

- Dataset harmonization
- Label mapping
- IMU signal preprocessing
- Fixed 6 x 128 sensor window representation
- Time-domain feature learning
- Frequency-domain feature learning using rFFT
- Gated time-frequency fusion
- Prototype-based classification
- Reconstruction learning
- Domain-adversarial training
- Source Leave-One-Dataset-Out validation

## Model Pipeline

```text
Raw IMU Datasets
        ↓
Dataset Harmonization
        ↓
Signal Preprocessing and Windowing
        ↓
Time Branch + Frequency Branch
        ↓
Gated Fusion
        ↓
Prototype Classification
        ↓
Zero-Shot Target Dataset Evaluation
