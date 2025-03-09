# **YuNet Face Detection**

## **1. Project Overview**
This project focuses on **face detection and recognition** using **OpenCV's YuNet model**. The goal is to detect and recognize faces in images and videos while improving accuracy through **data preprocessing, augmentation, and model training**.

---

## **2. Data Preparation**
### **A. Loading and Labeling Data**
- The dataset consists of multiple **face images** stored in subdirectories, where:
  - Each **subfolder represents a person**.
  - Images are read, converted to grayscale, and stored as **NumPy arrays**.
  - A **dictionary maps each person to a numerical label**.

### **B. Data Augmentation**
To improve model generalization, **data augmentation** is applied:
- **Flipping**: Creates a horizontally flipped version of each face.
- **Gaussian Blur**: Introduces slight blurring for variation.
- **Brightness & Contrast Adjustments**: Simulates lighting changes.

### **C. Splitting the Dataset**
- The dataset is split into **training (80%)** and **testing (20%)** subsets.

---

## **3. Face Detection & Recognition**
### **A. Face Detection using OpenCV's YuNet**
- **YuNet (OpenCV’s deep-learning-based face detector)** is used for detecting faces in:
  - Images
  - Video streams
  - Webcam feeds

- **Key Features of YuNet:**
  - Lightweight and optimized for **real-time face detection**.
  - Provides **bounding box coordinates** of detected faces.

### **B. Feature Extraction**
- Extracts **facial embeddings** from detected faces.
- These embeddings are used for **recognition/classification**.

---

## **4. Model Training & Evaluation**
### **A. Training a Face Recognition Model**
- A classifier (e.g., **SVM, k-NN, or Deep Learning models**) is trained using extracted facial embeddings.
- The trained model can **predict the identity of detected faces**.

### **B. Performance Metrics**
- **Accuracy Score**: Measures model performance.
- **Confusion Matrix**: Evaluates misclassifications.
- **Inference Speed**: Measures real-time detection efficiency.

---

## **5. Real-Time Face Detection & Recognition**
- The trained model is **deployed** for real-time face detection using:
  - **Live webcam feed**
  - **Video files**
  - **Pre-loaded images**
- The system draws **bounding boxes** around detected faces and labels them.

---

## **6. Insights & Applications**
- **Security & Surveillance**: Real-time monitoring and authentication.
- **Attendance Systems**: Automated face-based attendance tracking.
- **Smart Devices**: Integration into **IoT** applications.

---

## **7. Next Steps**
- Optimize model performance with **transfer learning**.
- Improve accuracy using **larger datasets** and **advanced augmentation**.
- Deploy as a **Flask API** for easy integration into applications.

