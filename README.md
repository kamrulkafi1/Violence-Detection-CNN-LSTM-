# 🎥 Human Violence Detection Using CNN-LSTM

This project implements a Deep Learning system designed to detect violent activities (e.g., punching) in video sequences using a hybrid **CNN-LSTM** architecture.

- 🛡️ **Real-Time Human Violence Detection**  
Automated surveillance utilizing a Hybrid CNN-LSTM Architecture.

## 📌 Problem Statement  
Traditional security monitoring requires human operators to monitor hundreds of camera feeds simultaneously, which can lead to fatigue and the risk of missing incidents of physical violence. There is a critical need for an automated system that can "understand" human actions and trigger alerts when aggressive behaviors (e.g., punching) occur, effectively distinguishing them from normal activities.

## 💡 The Solution  
This project implements a Deep Learning system designed for high-accuracy action recognition, using a temporal-spatial approach:

- **Spatial Analysis:** Extracts visual features from individual video frames using a pre-trained CNN.
- **Temporal Analysis:** Analyzes the sequence of movements over time using an LSTM to identify patterns related to violence.
- **Automated Labeling:** Processes raw video and produces a new file with real-time status and confidence scores overlaid on the video frames.

## 🚀 Key Features  
- **Spatial Feature Extraction:** Utilizes a pre-trained **ResNet18** (CNN) to extract features from individual video frames.
- **Temporal Modeling:** Employs **LSTM** layers to understand action sequences over time.
- **Explainable AI (XAI):** Integrates **Grad-CAM** heatmaps to visualize which parts of the video triggered the detection.
- **Real-Time Overlay:** Automatically labels videos as "Violence" or "Normal" along with a confidence score.

## 📊 Dataset  
The model is trained on the **UCF101** dataset, focusing on:
- **Normal Class:** Cricket Shot
- **Anomaly/Violence Class:** Punching

## 🛠️ Tech Stack  
- **Framework:** PyTorch (for model training and GPU acceleration)
- **Deep Learning:** CNN (ResNet18) + LSTM (Long Short-Term Memory)
- **Computer Vision:** OpenCV (for video processing and visualization)
- **Data Science:** NumPy, Scikit-learn (for data splitting and normalization)

## 🏗️ Model Architecture  
The system utilizes a hybrid CNN-LSTM pipeline:

- **Feature Extractor:** A ResNet18 backbone (pre-trained on ImageNet) extracts 512-dimensional feature vectors from sequences of 16 frames.
- **Sequence Processor:** A single-layer LSTM with 256 hidden units processes these vectors to capture motion dynamics.
- **Classifier:** A fully connected layer provides the final probability for "Normal Activity" versus "Violence Detected."

## 🚀 Key Results  
- **100% Test Accuracy:** The model achieved perfect classification on the test set for 'Punch' (Anomaly) versus 'Cricket Shot' (Normal) classes.
- **High Confidence:** Real-world testing shows the model identifies violence with over 99% confidence in clear sequences.
- **Visual Evidence:** An automated script generates labeled videos highlighting detected anomalies.
- **Training Loss:** Reduced from 0.37 to approximately 0.02.
- **Output:** Refer to the `results/` folder for demo videos.
