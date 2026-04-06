# 🎥 Human Violence Detection using CNN-LSTM

This project implements a Deep Learning system to detect violent activities (e.g., Punching) in video sequences using a hybrid **CNN-LSTM** architecture.

## 🚀 Key Features
- **Spatial Feature Extraction:** Uses a pre-trained **ResNet18** (CNN) to extract features from individual video frames.
- **Temporal Modeling:** Uses **LSTM** layers to understand the sequence of actions over time.
- **Explainable AI (XAI):** Integrated **Grad-CAM** heatmaps to visualize which part of the video triggered the detection.
- **Real-time Overlay:** Automatically labels videos with "Violence" or "Normal" along with a confidence score.

## 📊 Dataset
The model is trained on the **UCF101** dataset, focusing on:
- **Normal Class:** Cricket Shot
- **Anomaly/Violence Class:** Punching

## 🛠️ Tech Stack
- **Framework:** PyTorch
- **Computer Vision:** OpenCV
- **Visualization:** Matplotlib, Seaborn
- **Development:** Kaggle (T4 GPU)

## 📈 Results
- **Training Loss:** Reduced from 0.37 to ~0.02.
- **Output:** See the `results/` folder for demo videos.
