# 🧠 Brain Tumor Detection from MRI Scans

CNN-based classifier for brain tumor detection from MRI scans achieving **93.18% test accuracy** on 4 tumor types.

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.18-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-3.8-red?logo=keras)
![Accuracy](https://img.shields.io/badge/Accuracy-93.18%25-brightgreen)

> **M.Tech Project** · VNIT Nagpur · Author: Sumit Raj (MT24AAI011)

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Architecture](#️-architecture)
- [Tech Stack](#️-tech-stack)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Requirements](#-requirements)
- [Configuration](#️-configuration)
- [Usage](#-usage)
- [Results](#-results)
- [Dataset](#-dataset)
- [Author](#-author)
- [License](#-license)

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
- **Class balancing** with weighted augmentation

---

## 🏗️ Architecture

```
Input (128x128x3)
        ↓
Conv2D(32, 3x3, ReLU) → MaxPool(2x2)
        ↓
Conv2D(64, 3x3, ReLU) → MaxPool(2x2)
        ↓
Conv2D(128, 3x3, ReLU) → MaxPool(2x2)
        ↓
Flatten → Dense(128, ReLU) → Dropout(0.5)
        ↓
Dense(4, Softmax)
```

**Total params:** 3,305,156 (12.61 MB)

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| Language | Python 3.10 |
| Deep Learning | TensorFlow 2.18, Keras 3.8 |
| Image Processing | OpenCV, PIL, imutils |
| Data Handling | NumPy, Pandas |
| Utils | split-folders, scikit-learn |
| Visualization | Matplotlib, Seaborn |

---

## 📁 Project Structure

```
brain-tumor-detection/
├── Brain_Tumor_Detection.ipynb   # Main notebook (training + eval)
├── best_model.h5                 # Trained model (generated after training)
├── requirements.txt              # Dependencies
├── README.md                     # This file
└── content/
    └── archive.zip               # Dataset (download separately)
```

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/sumit966/brain-tumor-detection.git
cd brain-tumor-detection
```

### 2. Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate        # Windows
source venv/bin/activate     # Mac/Linux
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

**Or install manually:**

```bash
pip install tensorflow opencv-python split-folders scikit-learn matplotlib seaborn imutils pandas numpy
```

---

## 📋 Requirements

Create `requirements.txt`:

```
tensorflow>=2.18.0
keras>=3.8.0
opencv-python>=4.8.0
split-folders>=0.5.1
scikit-learn>=1.3.0
matplotlib>=3.7.0
seaborn>=0.12.0
imutils>=0.5.4
pandas>=2.0.0
numpy>=1.24.0
jupyter>=1.0.0
```

---

## ⚙️ Configuration

### Dataset Path (`Brain_Tumor_Detection.ipynb`)

Update the dataset path in the notebook:

```python
# Cell 2 - Extract dataset
import zipfile
with zipfile.ZipFile('content/archive.zip', 'r') as zip_ref:
    zip_ref.extractall('content/')
```

### Training Hyperparameters

```python
IMG_SIZE = 128              # Input image size
BATCH_SIZE = 32             # Batch size
EPOCHS = 20                 # Training epochs
LEARNING_RATE = 0.001       # Adam optimizer LR
AUGMENTATION_FACTOR = 5     # 5x data expansion
```

### Early Stopping Settings

```python
EarlyStopping(
    monitor='val_accuracy',
    patience=5,
    restore_best_weights=True
)
```

---

## 🎮 Usage

### Option 1: Run Notebook (Jupyter)

```bash
jupyter notebook Brain_Tumor_Detection.ipynb
```

Run all cells top-to-bottom. The notebook will:
1. Extract dataset
2. Augment images (5x)
3. Split into train/val/test
4. Train CNN
5. Evaluate on test set
6. Save `best_model.h5`

### Option 2: Run on Google Colab

1. Upload `Brain_Tumor_Detection.ipynb` to Colab
2. Upload `archive.zip` to Colab
3. Run all cells
4. Download `best_model.h5`

### Single Image Prediction

```python
import tensorflow as tf
from tensorflow.keras.preprocessing import image
import numpy as np

# Load trained model
model = tf.keras.models.load_model('best_model.h5')
class_names = ['glioma', 'meningioma', 'no_tumor', 'pituitary']

def predict(img_path):
    img = image.load_img(img_path, target_size=(128, 128))
    arr = np.expand_dims(image.img_to_array(img) / 255.0, axis=0)
    pred = model.predict(arr)
    confidence = np.max(pred) * 100
    return class_names[np.argmax(pred)], confidence

# Example
label, conf = predict('scan.jpg')
print(f"Prediction: {label} ({conf:.2f}%)")
# → Prediction: pituitary (97.45%)
```

---

## 📊 Results

### Training Metrics

| Metric | Value |
|--------|-------|
| Training Accuracy | 89.97% |
| Validation Accuracy | 95.89% |
| **Test Accuracy** | **93.18%** |
| Test Loss | 0.1365 |

### Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Glioma | 0.94 | 0.92 | 0.93 |
| Meningioma | 0.91 | 0.90 | 0.905 |
| No Tumor | 0.98 | 0.99 | 0.985 |
| Pituitary | 0.95 | 0.96 | 0.955 |

### Confusion Matrix

```
              Predicted
           GL   ME   NT   PI
Actual GL  92%   4%   1%   3%
       ME   5%  90%   2%   3%
       NT   0%   1%  99%   0%
       PI   2%   2%   1%  95%
```

---

## 📊 Dataset

### Source
- **Name:** Brain Tumor MRI Dataset
- **Source:** [Kaggle](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
- **Original size:** ~7,000 images

### After Augmentation
- **Total:** ~14,345 images
- **Augmentation:** 5x per image (rotation, shift, flip, brightness)

### Class Distribution

| Class | Original | Augmented |
|-------|----------|-----------|
| Glioma | 826 | 4,129 |
| Meningioma | 822 | 4,109 |
| No Tumor | 395 | 1,975 |
| Pituitary | 827 | 4,132 |

### Data Split

| Split | Images |
|-------|--------|
| Train | 11,480 |
| Validation | 1,434 |
| Test | 1,436 |

---

## 🧪 Testing

```bash
# In Jupyter notebook:
# Run Cell: "Evaluate on Test Set"
```

Expected output:
```
Test Loss: 0.1365
Test Accuracy: 93.18%
```

---

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| CUDA out of memory | Reduce BATCH_SIZE to 16 |
| Dataset not found | Ensure `content/archive.zip` exists |
| Low accuracy | Increase AUGMENTATION_FACTOR to 8 |
| Slow training | Use GPU (Colab/Kaggle) |
| Module not found | Run `pip install -r requirements.txt` |

---

## 👤 Author

**Sumit Raj** (MT24AAI011)
M.Tech Applied AI & ML · VNIT Nagpur

- 🌐 Portfolio: [sumit966-github-io.vercel.app](https://sumit966-github-io.vercel.app)
- 💼 LinkedIn: [linkedin.com/in/er-sumit-raj](https://linkedin.com/in/er-sumit-raj)
- 🐙 GitHub: [github.com/sumit966](https://github.com/sumit966)
- 📧 Email: info.sr0909@gmail.com

---

## 🙏 Acknowledgements

- [Kaggle Brain Tumor Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
- [TensorFlow](https://tensorflow.org/)
- [VNIT Nagpur](https://vnit.ac.in/)

---

## 📄 License

This project is for **academic evaluation purposes only**.

© 2024 Sumit Raj · VNIT Nagpur
