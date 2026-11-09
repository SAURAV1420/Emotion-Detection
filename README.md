# 🎭 Real-Time Facial Emotion Detection using Deep Learning

An AI-powered computer vision application that detects and classifies human facial expressions in real-time from webcam video streams using OpenCV and Deep Convolutional Neural Networks (CNNs).

---

## 📌 Overview

This project implements an end-to-end facial emotion recognition pipeline:
1. **Face Detection**: Localizes human faces in real-time video frames using OpenCV Haar Feature-based Cascade Classifiers.
2. **Preprocessing**: Normalizes face regions of interest (ROI) to grayscale $48 \times 48$ dimensions matching training inputs.
3. **Emotion Classification**: Passes ROI through a multi-layer Convolutional Neural Network trained to classify emotions across 5 emotional states.

### 🎯 Supported Emotion Classes:
- 😡 **Angry**
- 😊 **Happy**
- 😐 **Neutral**
- 😢 **Sad**
- 😲 **Surprise**

---

## 🚀 Features

- **⚡ Real-Time Inference**: High-framerate face detection and emotion prediction on live webcam feed.
- **🧠 Pre-trained Deep Learning Model**: Ready-to-use pre-trained weights (`Emotion_Detection.h5`) included.
- **🔄 Modern Compatibility**: Built with cross-compatibility support for TensorFlow 2.x and `tf-keras`.
- **🛠 Transfer Learning Ready**: Includes `train.py` pipeline with MobileNet transfer learning architecture on the FER2013 dataset.

---

## 📂 Project Structure

```text
├── Emotion_Detection.h5             # Pre-trained CNN model weights
├── haarcascade_frontalface_default.xml # OpenCV Haar Cascade face detector
├── test.py                          # Real-time webcam emotion detection script
├── train.py                         # MobileNet transfer learning training script
├── requirements.txt                 # Pinned project dependencies
├── .gitignore                       # Git exclusion rules
└── README.md                        # Documentation
```

---

## 🛠 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/SAURAV1420/Emotion-Detection.git
cd Emotion-Detection
```

### 2. Create and Activate Virtual Environment
```bash
# macOS / Linux
python3 -m venv .venv
source .venv/bin/activate

# Windows
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

---

## 💻 Usage

### Run Real-Time Emotion Detection:
```bash
python test.py
```
- A window titled **"Emotion Detector"** will open showing your webcam feed with green bounding boxes and detected emotion labels above each detected face.
- Press **`q`** on your keyboard while the video window is focused to safely terminate and release the webcam.

---

## 🏋️ Training Custom Models

To train or fine-tune models on the Facial Expression Recognition (FER-2013) dataset:

1. Download the dataset from Kaggle:
   - [Challenges in Representation Learning: Facial Expression Recognition Challenge](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data)
2. Update the training and validation directory paths in `train.py`.
3. Run training:
```bash
python train.py
```

---

## 🧰 Tech Stack

- **Python 3.9+**
- **TensorFlow / Keras** (`tf-keras`)
- **OpenCV (`opencv-python`)**
- **NumPy**

---

## 📄 License & Attribution

Based on the PyPower emotion detection project tutorial: [YouTube Tutorial](https://youtu.be/PulKlAZRoAY).
Open-source under the MIT License.
