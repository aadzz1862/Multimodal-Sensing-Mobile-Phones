# Multimodal-Sensing-Mobile-Phones

This project implements anomaly detection in motion sensor data collected from a mobile device. The data is gathered using the **Sensor Logger App**, capturing signals from the **Accelerometer** and **Gyroscope** sensors. The primary goal is to detect deviations in movement patterns when a person is distracted.

To achieve this, the project employs:
- ✅ Socket Programming (Flask) for real-time sensor data collection  
- ✅ Principal Component Analysis (PCA) for dimensionality reduction and feature extraction  
- ✅ Dynamic Time Warping (DTW) for time-series similarity measurement  
- ✅ One-Class SVM for anomaly detection  
- ✅ Dash & Plotly for real-time visualization  

The system compares reference movement data (without distractions) with test movement data (with distractions) to identify anomalous behavior.

---

## 📌 Anomaly Detection Using PCA, DTW, and Socket Programming

### 🚀 Project Overview
This project collects **real-time sensor data** from a mobile device and applies **machine learning techniques** to detect anomalies in movement patterns. The data is collected using the **Sensor Logger App**, processed via **Socket Programming (Flask)**, and analyzed using **PCA**, **DTW**, and **One-Class SVM**.

### 🔧 Technologies Used
- **Python** 🐍  
- **Flask** (for real-time data collection via Socket Programming)  
- **Dash & Plotly** (for live visualization)  
- **Pandas & NumPy** (for data processing)  
- **Matplotlib** (for data visualization)  
- **SciKit-Learn** (for machine learning models)  
- **Dynamic Time Warping (DTW)** (for time-series similarity analysis)  
- **Principal Component Analysis (PCA)** (for dimensionality reduction)  
- **One-Class SVM** (for anomaly detection)

### 📂 Dataset
The data consists of **accelerometer** and **gyroscope** readings collected under two conditions:

1. **Reference Data (`accelerometerref.csv`)** - Normal movement without distractions.  
2. **Original Data (`accelerometer.csv`)** - Movement with distractions (phone calls, direction change, sitting).

### 📊 Features Extracted
1. **PCA Features** – Extracted using covariance matrix decomposition.  
2. **DTW Features** – Calculated using time-series comparison.  
3. **Combined Features** – PCA + DTW for enhanced anomaly detection.

### 📡 Live Data Streaming (Socket Programming)
The system continuously streams **real-time sensor data** from the mobile device using **Flask** and buffers the incoming data for processing. Data is saved to:
- `gyroscope.csv`
- `accelerometer.csv`

---

## ⚡ How to Run the Project

### 1️⃣ Install Dependencies
```sh
pip install -r requirements.txt
```

2️⃣ Run Flask Server for Real-Time Data Collection
```sh
python app.py
```
3️⃣ Run Data Processing & Anomaly Detection
```sh
python anomaly_detection.py
```
4️⃣ View Live Graphs (Dash App)
```sh
python dashboard.py
```

Open http://localhost:8000 in your browser to view the real-time sensor data.

📊 Results
The system successfully detected anomalous movement patterns when distractions (calls, sitting, direction changes) were introduced.
PCA helped reduce dimensionality, improving classification efficiency.
DTW effectively identified deviations in movement trends.
The One-Class SVM model flagged unusual behavior based on extracted features.
🛠️ Future Improvements
Integrate deep learning models (e.g., LSTMs) for better sequence prediction.
Deploy a real-time mobile application instead of using Flask.
Improve sensor fusion techniques for more accurate anomaly detection.

