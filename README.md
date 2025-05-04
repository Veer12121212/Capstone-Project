# Capstone-Project
Project Summary Only — No Code or Data Due to NDA
# Automated Facial Recognition Attendance Monitoring System

**Capstone Project — Indian School of Business (ISB)**  
**Sponsor Company**: Confidential (as per NDA)  
**Team Members**: Charchit Tailong, Jatin Dhawan, Nitin Sethi, Nehal Singh, Virendra Singh

---

## 🎯 Objective

To design and deploy a robust, AI-powered attendance monitoring system using CCTV video feeds for industrial environments. The system aims to automate attendance tracking with high accuracy and low manual intervention, especially in challenging conditions like helmet use, poor lighting, and shift-based entry.

---

## 🧠 Problem Context

Traditional attendance systems like biometric and manual logs are ineffective in industrial settings due to:
- Helmet/safety gear obscuring faces
- Poor lighting and video quality
- High volume of simultaneous entries
- Network/power instability

---

## ⚙️ Technical Overview

### 📦 Data Sources:
- CCTV Videos (in-gate and out-gate footage)
- Structured metadata (employee IDs, names, departments)
- Mobile-clicked high-quality face images

### 🧪 Feature Engineering:
- Face cropping & manual labeling from video
- Data augmentation (blur, flip, noise, brightness adjustments)
- Timestamp extraction and mapping
- Super-resolution on low-quality CCTV images

### 🔍 Models Used:
- **Face Detection**: MTCNN, YOLOv8
- **Embedding Generation**: FaceNet, ArcFace
- **Classifier**: Support Vector Machine (SVM)

### 🧮 Evaluation:
- Accuracy: Up to 86.96% with MTCNN-FaceNet-SVM pipeline
- Precision/Recall: Improved through augmentation and embedding normalization

---

## 🖥️ Dashboard

A Streamlit-based attendance dashboard visualizes:
- Daily/weekly attendance
- Department-wise distribution
- In-time/out-time trends
- Late comers, absentees, and short-duration workers

---

## ☁️ Deployment

- **Frontend**: Streamlit
- **Backend**: Python scripts for detection, embedding, classification
- **Infrastructure**: AWS EC2 for hosting, with future scope for AWS Lambda for EOD processing

---

## ✅ Key Achievements

- Automated system capable of 85–90% recognition in industrial CCTV footage
- Augmented training data to simulate low-res, real-world conditions
- Reduced administrative burden with structured CSV outputs for payroll integration
- Non-intrusive, fully automated model with adaptability to new employee entries

---

## 🔒 Disclaimer

This repository intentionally excludes real client data, proprietary video/image assets, and internal documentation due to a binding **Data Security Agreement**.  
All code and demonstrations will use **mocked/synthetic data** for representation purposes only.

---

## 📚 How to Use This Project (If Replicated Publicly)

1. Replace `data/` with synthetic images & video clips.
2. Run preprocessing scripts in `scripts/`.
3. Use `models/` to train and save SVM classifiers.
4. Launch `streamlit_app.py` to see a demo of the dashboard.

---

For questions, collaboration, or a more detailed walkthrough, please contact the project contributors.
