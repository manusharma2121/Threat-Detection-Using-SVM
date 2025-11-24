# Real-Time Anomaly Detection in Surveillance Videos

This project implements a hybrid Deep Learning and Machine Learning solution to detect anomalies (such as accidents, fighting, or vandalism) in CCTV surveillance footage. It utilizes **ResNet50** for feature extraction and a **Support Vector Machine (SVM)** for classification.

## 🚀 Features
* **Hybrid Architecture:** Combines the feature extraction power of CNNs (ResNet50) with the efficiency of SVMs.
* **Multi-Class Threat Detection:** Capable of identifying 13 different types of anomalies.
* **Real-Time Simulation:** Includes a frame-buffering logic to simulate live video stream analysis.
* **High Accuracy:** Achieved ~88% accuracy on the test set.

## 🧠 Methodology
1.  **Frame Extraction:** The system extracts frames from video files at regular intervals.
2.  **Feature Extraction:** Each frame is passed through a pre-trained **ResNet50** model (ImageNet weights, top layer removed).
3.  **Pooling:** The features from multiple frames are averaged to create a temporal representation of the video segment.
4.  **Classification:** An **SVM (RBF Kernel)** classifies the aggregated feature vector as either "Normal" or a "Threat".

## 📂 Dataset Classes
The model is trained to distinguish between **Normal** activities and the following **Threat** classes:
* Abuse, Arrest, Arson, Assault
* Burglary, Explosion, Fighting
* Road Accidents, Robbery, Shooting
* Shoplifting, Stealing, Vandalism

## 🛠️ Prerequisites

Ensure you have Python 3.8+ installed. You can install the required dependencies using the command below:

```bash
pip install opencv-python numpy pandas scikit-learn tensorflow joblib
