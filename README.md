# 🚗 KITTI Object Detection using YOLOv8

## 📖 Project Overview
This project implements an object detection system using YOLOv8 on the KITTI dataset (YOLO format).

The objective of this project is to detect road objects such as:
- Car
- Pedestrian
- Van
- Cyclist
- Truck
- Tram
- Misc
- Person_sitting

This project is inspired by the Tesla Autopilot Clone – Object Detection implementation.

---

## 📂 Dataset
- Dataset Name: KITTI Dataset (YOLO Format)
- Format: YOLO annotation format
- Split: Train and Validation
- Images with bounding box labels

---

## 🛠 Technologies Used
- Python
- YOLOv8 (Ultralytics)
- PyTorch
- OpenCV
- Kaggle Notebook (GPU - Tesla P100)

---

## 🚀 Installation

Install required package:

pip install ultralytics

---

## 🧠 Model Implementation

### Training the Model

from ultralytics import YOLO

model = YOLO("yolov8n.pt")

model.train(
    data="data.yaml",
    epochs=10,
    imgsz=640,
    batch=16
)

### Prediction

model.predict(
    source="valid/images",
    save=True
)

---

## 📊 Results

- Model trained for 10 epochs
- mAP50 ≈ 0.70
- Successful detection of cars, trucks, pedestrians, and other objects
- Output images saved in:

runs/detect/predict/

Example output image is included in this repository.

---

## 📈 Performance Metrics

- Precision
- Recall
- mAP50
- mAP50-95

Validation results show effective multi-class object detection.

---

## ⚠️ Challenges Faced

- Dataset path configuration in Kaggle
- Understanding YOLO directory structure
- Managing GPU session runtime

---

## 🔮 Future Improvements

- Increase training epochs
- Use larger YOLOv8 models (yolov8m / yolov8l)
- Hyperparameter tuning
- Real-time video detection

---

## 👩‍💻 Author

Guru Vaishnavi Sankaranarayanan  
Final Year – Electronics and Communication Engineering  
Object Detection Project Submission
