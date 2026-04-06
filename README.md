# 🧬 Age & Gender Detector from Face

<div align="center">

![Age Detector Banner](https://img.shields.io/badge/AI-Computer_Vision-00D4FF?style=for-the-badge&logo=openai&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

<p align="center">
  <b>A professional-grade real-time facial analysis system powered by Deep Neural Networks.</b>
  <br />
  Detect, analyze, and classify age and gender with high accuracy using OpenCV's DNN module.
</p>

---

[Features](#-key-features) • [Installation](#-installation) • [Usage](#-usage-instructions) • [Model Details](#-technical-architecture)

</div>

## ✨ Key Features

- 🕒 **Real-Time Detection**: Lightning-fast processing for webcam feeds or static images.
- 👥 **Multi-Face Support**: Simultaneously detect and classify multiple people in a single frame.
- 🎯 **Deep Learning Core**: Uses pre-trained Caffe and TensorFlow models for robust performance.
- 🏷️ **Age Binning**: Classifies age into 8 distinct ranges: `(0-2)`, `(4-6)`, `(8-12)`, `(15-20)`, `(25-32)`, `(38-43)`, `(48-53)`, and `(60-100)`.
- 🚻 **Gender Estimation**: High-precision binary gender classification (Male/Female).

---

## 🛠️ Installation

Ensure you have Python 3.x installed on your system.

1. **Clone the project**
   ```bash
   git clone https://github.com/your-username/Age-Detector-From-Face.git
   cd Age-Detector-From-Face
   ```

2. **Install Dependencies**
   ```bash
   pip install opencv-python numpy
   ```

---

## 🚀 Usage Instructions

The script supports both real-time webcam detection and processing of individual image files.

### 🌐 Real-Time Webcam
Run the script without arguments to activate your default camera:
```bash
python face.py
```

### 🖼️ Static Image Processing
To analyze a specific image file, use the `--image` flag:
```bash
python face.py --image girl1.jpg
```

> **Note**: Press `q` while the detection window is active to exit.

---

## 🏗️ Technical Architecture

This project utilizes the **OpenCV DNN (Deep Neural Network)** module to load and run pre-trained models.

### 1. Face Detection
- **Model**: SSD (Single Shot Detector) with ResNet-10 backbone.
- **Files**: `opencv_face_detector_uint8.pb` (weights) and `opencv_face_detector.pbtxt` (config).

### 2. Gender Classification
- **Architecture**: A simple CNN designed by Gil Levi and Tal Hassner.
- **Files**: `gender_net.caffemodel` and `gender_deploy.prototxt`.

### 3. Age Prediction
- **Architecture**: CNN optimized for age group classification.
- **Files**: `age_net.caffemodel` and `age_deploy.prototxt`.

---

## 📂 Project Structure

```text
Age-Detector-From-Face/
├── age_net.caffemodel        # Age model weights
├── age_deploy.prototxt       # Age model config
├── gender_net.caffemodel     # Gender model weights
├── gender_deploy.prototxt    # Gender model config
├── face.py                   # Main application logic
└── ... (test images)
```

---

<div align="center">
  <sub>Built with ❤️ by Antigravity</sub>
</div>
