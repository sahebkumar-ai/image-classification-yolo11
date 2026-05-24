
![23](https://github.com/user-attachments/assets/0489766c-359e-4cf2-b10d-09849cab5ba5)

# 🚀 YOLO11 Image Classification System

A professional AI-powered image classification project built using Ultralytics YOLO11 for custom dataset training and inference.

---

## 📌 Overview

This project demonstrates image classification using the YOLO11 Classification model.  
The model is trained on a custom dataset and performs accurate predictions on input images.

The system supports:
- Custom dataset training
- Image classification inference
- Batch image prediction
- Result visualization and saving

---

## ✨ Features

- YOLO11 Classification Model
- Custom Dataset Training
- High-Speed Inference
- Batch Image Prediction
- Automatic Result Saving
- Easy-to-Use Pipeline

---

## 🛠️ Tech Stack

- Python
- Ultralytics YOLO11
- PyTorch
- OpenCV

---

## 📂 Project Structure

```bash
YOLO11-Image-Classification/
│
├── custom_dataset/
├── test_images/
├── runs/
│   └── classify/
│
├── main.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

```bash
git clone https://github.com/your-username/YOLO11-Image-Classification.git

cd YOLO11-Image-Classification

pip install ultralytics
```

---

## ▶️ Training

```python
from ultralytics import YOLO

# Load pretrained classification model
model = YOLO("yolo11s-cls.pt")

# Train model
results = model.train(
    data="custom_dataset",
    epochs=10,
    imgsz=640
)
```

---

## 🔍 Inference

### Single Image Prediction

```python
from ultralytics import YOLO

model = YOLO("runs/classify/train/weights/best.pt")

results = model(
    "test_images/0.jpg",
    save=True,
    imgsz=640,
    conf=0.5
)

results[0].show()
```

---

### Batch Prediction

```python
results = model("test_images", save=True)
```

---

## 📊 Model Workflow

- Load pretrained YOLO11 classification model
- Train on custom dataset
- Generate best model weights
- Perform inference on test images
- Save classified output results

---

## 📈 Applications

- Plant Disease Classification
- Medical Image Classification
- Product Recognition
---

## 💡 Future Improvements

- Real-time webcam classification
- Web deployment using Streamlit
- GPU optimization
- Larger custom datasets
- Model performance tuning

---
