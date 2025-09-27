# 🦴 Bone Fracture Detection using Deep Learning  

## 📌 Overview  
This project applies CNN (ResNet50 transfer learning) and YOLOv8 for detecting and classifying 10 types of bone fractures using the Human Bone Fractures Multi-modal Image Dataset (HBFMID).  

## 🚀 Models Implemented  
- ✅ **CNN with ResNet50** – Baseline classifier (~56% accuracy)  
- ✅ **YOLOv8 (Nano)** – Best-performing model with real-time detection (**mAP50 = 86%**)  

## 📂 Dataset  
Dataset: **Human Bone Fractures Multi-modal Image Dataset (HBFMID)**  
[Kaggle Link](https://www.kaggle.com/datasets/orvile/human-bone-fractures-image-dataset-hbfmid/data)  

**Classes:**  
Comminuted, Greenstick, Healthy, Linear, Oblique Displaced, Oblique, Segmental, Spiral, Transverse Displaced, Transverse  

## ⚙️ Installation  
```bash
git clone https://github.com/yourusername/Fracture-Detection-Project.git
cd Fracture-Detection-Project
pip install -r requirements.txt
```

## ▶️ Usage  
1. Run the notebook:  
```bash
jupyter notebook notebooks/Project.ipynb
```

2. Train YOLOv8:  
```python
from ultralytics import YOLO
model = YOLO("yolov8n.pt")
model.train(data="data.yaml", epochs=50, imgsz=512, batch=4)
```

## 📊 Results  
- CNN (ResNet50) → **~56% accuracy**  
- YOLOv8 (Nano) → **mAP50 = 86%, mAP50-95 = 48%**  

## 📌 Conclusion  
- YOLOv8 outperforms CNN in both accuracy and robustness.  
- Feasible for **real-time fracture detection**.  
- Future improvements: larger dataset, fine-tuning hyperparameters, and ensemble methods.  

