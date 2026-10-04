# 🧠 Brain Tumor Detection from MRI Scans

CNN-based classifier for brain tumor detection from MRI scans achieving **93.18% test accuracy** on 4 tumor types.

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.18-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-3.8-red?logo=keras)
![Accuracy](https://img.shields.io/badge/Accuracy-93.18%25-brightgreen)

> **M.Tech Project** · VNIT Nagpur · Author: Sumit Raj (MT24AAI011)

---

## 🎯 Overview

Deep learning model to classify brain MRI scans into 4 categories:

| Class | Description |
|-------|-------------|
| Glioma Tumor | Tumor in the brain or spine |
| Meningioma Tumor | Tumor from meninges (brain/spinal cord membranes) |
| No Tumor | Healthy brain scan |
| Pituitary Tumor | Tumor in the pituitary gland |

---

## ✨ Features

- **Custom CNN architecture** (3 conv blocks: 32 → 64 → 128 filters)
- **Data augmentation** (rotation, shift, flip, brightness) — 5x expansion per image
- **Smart cropping** to remove black borders from MRI scans
- **Early stopping** + model checkpointing for best model selection
- **93.18% test accuracy** on 1,436 test images
- **Prediction pipeline** for single-image inference

---

## 🏗️ Architecture
