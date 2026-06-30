# 🚗 Autonomous Self-Driving Car using Deep Learning

An end-to-end **Self-Driving Car** project that predicts steering angles from front-facing camera images using NVIDIA's Convolutional Neural Network architecture. The model is trained on driving data collected from a simulator and deployed in real-time using a Flask + Socket.IO server.

---

## 📌 Project Overview

This project demonstrates how Deep Learning can be used for autonomous driving by learning steering behavior directly from camera images.

The workflow includes:

- Data preprocessing
- Data balancing
- Image augmentation
- CNN model training
- Model evaluation
- Real-time deployment in a driving simulator

---

## ✨ Features

- 🚘 End-to-End Steering Angle Prediction
- 🧠 NVIDIA CNN Architecture
- 📸 Image Preprocessing Pipeline
- 🎨 Data Augmentation
- ⚖️ Dataset Balancing
- 📊 Training & Validation Visualization
- 💾 Trained Model (.h5)
- 🌐 Real-time Car Control using Flask & Socket.IO

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Albumentations
- Flask
- Socket.IO
- Eventlet
- PIL (Pillow)

---

## 📂 Project Structure

```
Self-Driving-Car/
│
├── TEAM WIZARDS.ipynb        # Model training notebook
├── drive.py                  # Real-time inference server
├── model.h5                  # Trained CNN model
├── track/
│   ├── IMG/
│   └── driving_log.csv
├── screenshots/
└── README.md
```

---

## 🧠 Model Architecture

The project uses the **NVIDIA End-to-End Self Driving Car CNN**, consisting of:

- 5 Convolutional Layers
- ELU Activation Functions
- Fully Connected Layers
- Regression Output (Steering Angle)

The model predicts a continuous steering angle directly from input images.

---

## 📊 Dataset

Training data consists of:

- Center camera images
- Left camera images
- Right camera images
- Steering angle
- Throttle
- Brake
- Speed

Images are collected using the Udacity Self-Driving Car Simulator.

---

## 🔄 Data Preprocessing

Before training, every image undergoes:

- Crop unnecessary regions (sky & car hood)
- RGB → YUV conversion
- Gaussian Blur
- Resize to **200 × 66**
- Pixel normalization

---

## 🎨 Data Augmentation

To improve model generalization, the following augmentations are applied:

- Random Translation
- Random Zoom
- Random Rotation
- Brightness Adjustment
- Horizontal Flipping
- ShiftScaleRotate Transformations

---

## ⚖️ Dataset Balancing

Since driving datasets contain many straight-driving images, histogram-based balancing is performed to reduce bias toward straight steering.

---

## 🏋️ Model Training

The notebook includes:

- Train / Validation split
- Batch Generator
- Online Data Augmentation
- CNN Training
- Validation Loss Monitoring

The trained model is saved as:

```
model.h5
```

---

## 🚀 Real-Time Deployment

The `drive.py` script:

- Loads the trained model
- Receives images from the simulator
- Preprocesses incoming frames
- Predicts steering angle
- Calculates throttle
- Sends commands back to the simulator using Socket.IO

---

## ▶️ Installation

Clone the repository

```bash
git clone https://github.com/your-username/self-driving-car.git
```

Navigate into the project

```bash
cd self-driving-car
```

Install dependencies

```bash
pip install tensorflow
pip install opencv-python
pip install flask
pip install eventlet
pip install python-socketio
pip install pillow
pip install albumentations
pip install pandas
pip install matplotlib
```

---

## ▶️ Running the Project

### Step 1

Train the model using

```
TEAM WIZARDS.ipynb
```

or use the provided

```
model.h5
```

### Step 2

Start the inference server

```bash
python drive.py
```

### Step 3

Launch the Udacity Self-Driving Car Simulator and connect to the server.

The vehicle will begin driving autonomously using the trained CNN model.

---

## 📈 Results

The model successfully learns steering behavior from camera images and can autonomously navigate tracks in the simulator with real-time steering predictions.

---


## 🚀 Future Improvements

- Lane Detection Integration
- Object Detection (YOLO)
- Traffic Sign Recognition
- Semantic Segmentation
- Adaptive Cruise Control
- Reinforcement Learning
- Real-world Vehicle Deployment

---

## 📚 Learning Outcomes

This project demonstrates:

- Computer Vision
- Image Processing
- Deep Learning
- Convolutional Neural Networks
- Regression using CNN
- Data Augmentation
- Flask Deployment
- Socket Programming
- Real-time AI Inference

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a new feature branch
3. Commit your changes
4. Push your branch
5. Open a Pull Request

---

## 👨‍💻 Author

**Ankush Kumar**

B.Tech CSE | AI & Machine Learning Enthusiast

If you found this project helpful, don't forget to ⭐ the repository!
