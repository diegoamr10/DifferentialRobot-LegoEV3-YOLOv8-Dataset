# LEGO EV3 Object Detection Dataset for YOLOv8
This repository contains a custom dataset designed for training and evaluating YOLOv8 object detection models using images of LEGO EV3 robots.
The dataset was created specifically for computer vision experiments, robotic tracking, and the study of chaotic trajectories such as the Rössler and Lorenz systems.

---

## 📂 Dataset Description
The dataset includes:

- **High-resolution images** of a LEGO EV3 robot from different angles.
- **Multiple lighting conditions** and backgrounds.
- **Annotated bounding boxes** following YOLO format.
- **Consistent class labeling**, ideal for training detection models.
  
This dataset is suitable for:
- Robot tracking projects  
- Real-time object detection  
- Machine learning experiments with LEGO robotics  
- YOLOv5/YOLOv8 training pipelines  

---

## 🏷 Classes
The dataset currently includes the following class:
- Lego (Mindstorm EV3 Brick)

---
🚀 Usage
1. Clone the repository
  git clone https://github.com/diegoamr10/DifferentialRobot-LegoEV3-YOLOv8-Dataset.git
  cd DifferentialRobot-LegoEV3-YOLOv8-Dataset

2. Install Ultralytics (YOLOv8)
pip install ultralytics

3. Train YOLOv8 with this dataset
yolo detect train data=dataset.yaml model=yolov8m.pt epochs=100 imgsz=640

Notes:
dataset.yaml defines the path to train/val images and class names.
You may use yolov8n.pt, yolov8s.pt, yolov8m.pt, etc.

For faster training:
  yolo detect train data=dataset.yaml model=yolov8n.pt epochs=50 imgsz=640

4. Run Inference Using the Trained Model (best.pt)

Predict on a folder:
  yolo detect predict model=best.pt source=images/

Predict on a video:
  yolo detect predict model=best.pt source=video.mp4

Predict using a webcam:
  yolo detect predict model=best.pt source=0

📁 Folder Structure (Example)
  Dataset/
  │── images/
  │   ├── train/
  │   ├── val/
  │── labels/
  │   ├── train/
  │   ├── val/
  │── dataset.yaml
  │── best.pt   (optional: trained model)
---

## 👥 Authors
D. A. Mata Robles, R. C. Martínez-Montejano, R. C. Martínez-Montejano, J. J. Jaime-Rodriguez

--- 

## 🙌 Acknowledgments
D.A.M.R and L.J.O.G. thank the Potosino Council of Science and Technology (COPOCYT) for the support provided through Trust Project 23871, from the 2023-01 Call.
---
