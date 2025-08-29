# 👁️ Eye Disease Detection using YOLOv8

## 📖 Overview
This project focuses on detecting eye diseases, particularly **glaucoma**, by analyzing the **Cup-to-Disc Ratio (CDR)** in retinal fundus images.  
It uses **YOLOv8 Object Detection** to automatically detect and localize:  

- **Optic Disc**  
- **Optic Cup**  
- **Cup-to-Disc structures for ratio analysis**  

---

## 🛠️ Tools & Frameworks
- **YOLOv8 (Ultralytics)** – Object detection  
- **PyTorch** – Model training backend  
- **Detectron2** – Optional experiments  
- **OpenCV** – Visualization & preprocessing  
- **scikit-learn** – Metrics (Precision, Recall, Accuracy)  
- **Matplotlib** – Plotting results  

---

## 🏋️ Training Approach

### 1. Dataset Preparation
- Unzip dataset (`gg.zip`) into `train/`, `valid/`, and `test/` folders  
- YOLO format labels (`.txt`) for each image  

### 2. YAML Configuration
```yaml
train: dataset10/train/images
val: dataset10/valid/images
test: dataset10/test/images
nc: 3
names: ['Cup Disc', 'Optic Cup', 'Optic Disc']
###3. Model Training

Base model: YOLOv8m

Epochs: 50

Image size: 640×640


##  Results

Validation Accuracy: ~90%

Average IoU: ~0.70

mAP@0.5: ~0.88

Precision: ~0.89

Recall: ~0.87
