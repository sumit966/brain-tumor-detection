<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- 🧠 Brain Tumor Detection — Animated README 2026 -->
<!-- ═══════════════════════════════════════════════════════════════ -->

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24,30&height=220&section=header&text=🧠%20Brain%20Tumor%20Detection&fontSize=44&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=CNN-Based%20MRI%20Classification%20%7C%2093.18%25%20Accuracy&descAlignY=58&descSize=18" />
</div>

<div align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=600&size=22&duration=3000&pause=800&color=8B5CF6&center=true&vCenter=true&multiline=true&width=750&height=100&lines=🧬+4-Class+Brain+Tumor+Classifier;🎯+93.18%25+Test+Accuracy;🧠+Custom+CNN+Architecture;⚡+TensorFlow+%2B+Keras+3.8" alt="Typing SVG" />
  </a>
</div>

<br/>

<div align="center">
  <a href="https://github.com/sumit966/brain-tumor-detection/stargazers">
    <img src="https://img.shields.io/github/stars/sumit966/brain-tumor-detection?style=for-the-badge&color=8b5cf6&labelColor=0d1117&logo=github&logoColor=white" />
  </a>
  <a href="https://github.com/sumit966/brain-tumor-detection/network/members">
    <img src="https://img.shields.io/github/forks/sumit966/brain-tumor-detection?style=for-the-badge&color=3b82f6&labelColor=0d1117&logo=git&logoColor=white" />
  </a>
  <a href="https://github.com/sumit966/brain-tumor-detection/issues">
    <img src="https://img.shields.io/github/issues/sumit966/brain-tumor-detection?style=for-the-badge&color=ec4899&labelColor=0d1117&logo=github&logoColor=white" />
  </a>
  <a href="https://github.com/sumit966/brain-tumor-detection/commits/main">
    <img src="https://img.shields.io/github/last-commit/sumit966/brain-tumor-detection?style=for-the-badge&color=10b981&labelColor=0d1117&logo=git&logoColor=white" />
  </a>
</div>

<br/>

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/TensorFlow-2.18-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" />
  <img src="https://img.shields.io/badge/Keras-3.8-D00000?style=for-the-badge&logo=keras&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenCV-4.8-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" />
</div>

<br/>

<div align="center">
  <img src="https://img.shields.io/badge/Test_Accuracy-93.18%25-10b981?style=for-the-badge&logo=target&logoColor=white" />
  <img src="https://img.shields.io/badge/Classes-4_Types-8b5cf6?style=for-the-badge&logo=brain&logoColor=white" />
  <img src="https://img.shields.io/badge/Parameters-3.3M-3b82f6?style=for-the-badge&logo=tensorflow&logoColor=white" />
  <img src="https://img.shields.io/badge/Model_Size-12.61_MB-f59e0b?style=for-the-badge&logo=keras&logoColor=white" />
</div>

<br/>

<div align="center">
  <i>🎓 M.Tech Project · VNIT Nagpur · <b>Sumit Raj</b> (MT24AAI011)</i>
</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" />

---

## 📑 Table of Contents

<div align="center">

| 🎯 | 🎯 | 🎯 |
|:---:|:---:|:---:|
| [Overview](#-overview) | [Features](#-features) | [Architecture](#️-architecture) |
| [Tech Stack](#️-tech-stack) | [Project Structure](#-project-structure) | [Installation](#-installation) |
| [Requirements](#-requirements) | [Configuration](#️-configuration) | [Usage](#-usage) |
| [Results](#-results) | [Dataset](#-dataset) | [Author](#-author) |
| [License](#-license) | | |

</div>

---

## 🎯 Overview

<div align="center">
  <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" width="400" alt="Brain scan animation"/>
</div>

<br/>

Deep learning model to classify brain MRI scans into **4 categories**:

<table align="center">
<tr>
<td width="25%" valign="top" align="center">

### 🔴 Glioma

Tumor in the **brain or spine**

</td>
<td width="25%" valign="top" align="center">

### 🟡 Meningioma

Tumor from **meninges** (brain/spinal cord membranes)

</td>
<td width="25%" valign="top" align="center">

### 🟢 No Tumor

**Healthy** brain scan

</td>
<td width="25%" valign="top" align="center">

### 🟣 Pituitary

Tumor in the **pituitary gland**

</td>
</tr>
</table>

---

## ✨ Features

<table align="center">
<tr>
<td width="50%" valign="top">

### 🧠 Model Architecture

- 🏗️ **Custom CNN** (3 conv blocks: 32 → 64 → 128)
- 🎯 **93.18% test accuracy** on 1,436 test images
- 📊 **3.3M parameters** (12.61 MB model)
- 🎨 **Softmax** 4-class output

</td>
<td width="50%" valign="top">

### 🛠️ Training Pipeline

- 🔄 **Data augmentation** (rotation, shift, flip, brightness) — **5x expansion**
- ✂️ **Smart cropping** to remove black borders
- ⏹️ **Early stopping** + model checkpointing
- ⚖️ **Class balancing** with weighted augmentation

</td>
</tr>
</table>

<br/>

<div align="center">
  <img src="https://img.shields.io/badge/🔮_Prediction_Pipeline-Single_Image_Inference-8b5cf6?style=for-the-badge" />
</div>

---

## 🏗️ Architecture

### 🧬 CNN Model Pipeline

```mermaid
flowchart TD
    A[📸 Input 128x128x3] --> B[🔷 Conv2D 32 filters 3x3 ReLU]
    B --> C[⬇️ MaxPool 2x2]
    C --> D[🔷 Conv2D 64 filters 3x3 ReLU]
    D --> E[⬇️ MaxPool 2x2]
    E --> F[🔷 Conv2D 128 filters 3x3 ReLU]
    F --> G[⬇️ MaxPool 2x2]
    G --> H[📊 Flatten]
    H --> I[🧠 Dense 128 ReLU]
    I --> J[💧 Dropout 0.5]
    J --> K[🎯 Dense 4 Softmax]
    
    style A fill:#8b5cf6,stroke:#fff,color:#fff
    style K fill:#10b981,stroke:#fff,color:#fff
    style I fill:#3b82f6,stroke:#fff,color:#fff
```

### 📐 ASCII Fallback

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

<div align="center">

**📊 Total params:** `3,305,156` &nbsp;·&nbsp; **💾 Model size:** `12.61 MB`

</div>

---

## 🛠️ Tech Stack

<table align="center">
<tr>
<td><b>Category</b></td>
<td><b>Technology</b></td>
</tr>
<tr>
<td>🐍 Language</td>
<td><img src="https://img.shields.io/badge/Python_3.10-3776AB?style=flat-square&logo=python&logoColor=white" /></td>
</tr>
<tr>
<td>🧠 Deep Learning</td>
<td><img src="https://img.shields.io/badge/TensorFlow_2.18-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" /> <img src="https://img.shields.io/badge/Keras_3.8-D00000?style=flat-square&logo=keras&logoColor=white" /></td>
</tr>
<tr>
<td>👁️ Image Processing</td>
<td><img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" /> <img src="https://img.shields.io/badge/PIL-3776AB?style=flat-square" /> <img src="https://img.shields.io/badge/imutils-FF6B6B?style=flat-square" /></td>
</tr>
<tr>
<td>📊 Data Handling</td>
<td><img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" /> <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" /></td>
</tr>
<tr>
<td>🔧 Utils</td>
<td><img src="https://img.shields.io/badge/split--folders-8b5cf6?style=flat-square" /> <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" /></td>
</tr>
<tr>
<td>📈 Visualization</td>
<td><img src="https://img.shields.io/badge/Matplotlib-11557C?style=flat-square" /> <img src="https://img.shields.io/badge/Seaborn-3776AB?style=flat-square" /></td>
</tr>
</table>

---

## 📁 Project Structure

```
brain-tumor-detection/
├── 🧠 Brain_Tumor_Detection.ipynb   # Main notebook (training + eval)
├── 💾 best_model.h5                 # Trained model (generated after training)
├── 📋 requirements.txt              # Dependencies
├── 📖 README.md                     # This file
└── 📁 content/
    └── 📦 archive.zip               # Dataset (download separately)
```

---

## 🚀 Installation

<div align="center">
  <img src="https://img.shields.io/badge/⏱️_10_min_setup-3776AB?style=for-the-badge" />
  <img src="https://img.shields.io/badge/🎯_GPU_recommended-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
</div>

<br/>

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/sumit966/brain-tumor-detection.git
cd brain-tumor-detection
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate        # Windows
source venv/bin/activate     # Mac/Linux
```

### 3️⃣ Install Dependencies

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

```txt
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

### 📂 Dataset Path (`Brain_Tumor_Detection.ipynb`)

Update the dataset path in the notebook:

```python
# Cell 2 - Extract dataset
import zipfile
with zipfile.ZipFile('content/archive.zip', 'r') as zip_ref:
    zip_ref.extractall('content/')
```

### 🎛️ Training Hyperparameters

```python
IMG_SIZE = 128              # Input image size
BATCH_SIZE = 32             # Batch size
EPOCHS = 20                 # Training epochs
LEARNING_RATE = 0.001       # Adam optimizer LR
AUGMENTATION_FACTOR = 5     # 5x data expansion
```

### ⏹️ Early Stopping Settings

```python
EarlyStopping(
    monitor='val_accuracy',
    patience=5,
    restore_best_weights=True
)
```

---

## 🎮 Usage

### 🅰️ Option 1: Run Notebook (Jupyter)

```bash
jupyter notebook Brain_Tumor_Detection.ipynb
```

Run all cells top-to-bottom. The notebook will:

1. 📦 Extract dataset
2. 🔄 Augment images (5x)
3. ✂️ Split into train/val/test
4. 🧠 Train CNN
5. 📊 Evaluate on test set
6. 💾 Save `best_model.h5`

### 🅱️ Option 2: Run on Google Colab

1. Upload `Brain_Tumor_Detection.ipynb` to Colab
2. Upload `archive.zip` to Colab
3. Run all cells
4. Download `best_model.h5`

### 🔮 Single Image Prediction

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

<div align="center">
  <img src="https://img.shields.io/badge/Train_Accuracy-89.97%25-3b82f6?style=for-the-badge&logo=target&logoColor=white" />
  <img src="https://img.shields.io/badge/Val_Accuracy-95.89%25-8b5cf6?style=for-the-badge&logo=target&logoColor=white" />
  <img src="https://img.shields.io/badge/Test_Accuracy-93.18%25-10b981?style=for-the-badge&logo=target&logoColor=white" />
  <img src="https://img.shields.io/badge/Test_Loss-0.1365-f59e0b?style=for-the-badge" />
</div>

<br/>

### 📈 Training Metrics

| Metric | Value |
|--------|-------|
| 🎯 Training Accuracy | 89.97% |
| 📊 Validation Accuracy | 95.89% |
| ⭐ **Test Accuracy** | **93.18%** |
| 📉 Test Loss | 0.1365 |

### 🎯 Per-Class Performance

| Class | Precision | Recall | F1-Score |
|-------|:---------:|:------:|:--------:|
| 🔴 Glioma | 0.94 | 0.92 | 0.93 |
| 🟡 Meningioma | 0.91 | 0.90 | 0.905 |
| 🟢 No Tumor | 0.98 | 0.99 | 0.985 |
| 🟣 Pituitary | 0.95 | 0.96 | 0.955 |

### 🔢 Confusion Matrix

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

### 📚 Source

<table align="center">
<tr>
<td><b>Name</b></td>
<td>Brain Tumor MRI Dataset</td>
</tr>
<tr>
<td><b>Source</b></td>
<td><a href="https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset">Kaggle</a></td>
</tr>
<tr>
<td><b>Original Size</b></td>
<td>~7,000 images</td>
</tr>
</table>

### 🔄 After Augmentation

- 📦 **Total:** ~14,345 images
- 🎨 **Augmentation:** 5x per image (rotation, shift, flip, brightness)

### 📊 Class Distribution

| Class | Original | Augmented |
|-------|:--------:|:---------:|
| 🔴 Glioma | 826 | 4,129 |
| 🟡 Meningioma | 822 | 4,109 |
| 🟢 No Tumor | 395 | 1,975 |
| 🟣 Pituitary | 827 | 4,132 |

### ✂️ Data Split

| Split | Images |
|-------|:------:|
| 🚂 Train | 11,480 |
| ✅ Validation | 1,434 |
| 🧪 Test | 1,436 |

---

## 🧪 Testing

```bash
# In Jupyter notebook:
# Run Cell: "Evaluate on Test Set"
```

**Expected output:**

```bash
Test Loss: 0.1365
Test Accuracy: 93.18%
```

---

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| 🔴 CUDA out of memory | Reduce `BATCH_SIZE` to 16 |
| 📂 Dataset not found | Ensure `content/archive.zip` exists |
| 📉 Low accuracy | Increase `AUGMENTATION_FACTOR` to 8 |
| 🐌 Slow training | Use GPU (Colab/Kaggle) |
| 📦 Module not found | Run `pip install -r requirements.txt` |

---

## 👤 Author

<div align="center">

<img src="https://img.shields.io/badge/Sumit_Raj-MT24AAI011-8b5cf6?style=for-the-badge&labelColor=0d1117" />

<br/><br/>

<b>M.Tech Applied AI & ML · VNIT Nagpur</b>

<br/><br/>

<a href="https://sumit966-github-io.vercel.app">
  <img src="https://img.shields.io/badge/Portfolio-Visit-3b82f6?style=for-the-badge&logo=googlechrome&logoColor=white" />
</a>
<a href="https://www.linkedin.com/in/er-sumit-raj-/">
  <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>
<a href="https://github.com/sumit966">
  <img src="https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>
<a href="mailto:info.sr0909@gmail.com">
  <img src="https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
</a>

</div>

---

## 🙏 Acknowledgements

<div align="center">

<a href="https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset">
  <img src="https://img.shields.io/badge/Kaggle_Dataset-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" />
</a>
<a href="https://tensorflow.org/">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" />
</a>
<a href="https://vnit.ac.in/">
  <img src="https://img.shields.io/badge/VNIT_Nagpur-8b5cf6?style=for-the-badge" />
</a>

</div>

---

## 📄 License

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12,20,24,30&height=2&width=60%" />

<br/>

<img src="https://img.shields.io/badge/⚖️_ACADEMIC_USE_ONLY-f59e0b?style=for-the-badge&labelColor=0d1117" />

<br/><br/>

<samp>
This project is for <b>academic evaluation purposes only</b>.
</samp>

<br/><br/>

<sub><samp>© 2024 &nbsp;·&nbsp; SUMIT RAJ &nbsp;·&nbsp; VNIT NAGPUR</samp></sub>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12,20,24,30&height=2&width=60%" />

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24,30&height=120&section=footer&text=🧠%20AI%20for%20Better%20Healthcare&fontSize=20&fontColor=ffffff&animation=twinkling" width="100%" />
