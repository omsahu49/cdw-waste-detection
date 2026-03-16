# 🏗️ Construction & Demolition Waste Object Detection

[![YOLOv8](https://img.shields.io/badge/Model-YOLOv8s-blue)](https://ultralytics.com)
[![Kaggle](https://img.shields.io/badge/Platform-Kaggle-20BEFF)](https://kaggle.com)
[![GPU](https://img.shields.io/badge/GPU-Tesla%20T4-green)](https://kaggle.com)
[![mAP50](https://img.shields.io/badge/mAP50-70.93%25-orange)](https://kaggle.com)

*By **Om Sahu** | BCA AI & Data Analytics | LNCT Group of Colleges, Bhopal*

A deep learning model I built to automatically detect and classify **Construction & Demolition (C&D) waste** from images using **YOLOv8** object detection.

---

## 🎯 Problem Statement

Construction and demolition sites generate massive amounts of waste including rebar, bricks, PVC pipes, wires, and cementitious debris. Manual sorting of this waste is slow, expensive, and hazardous. This project automates waste detection using computer vision to help improve recycling and waste management efficiency.

---

## 🗂️ Classes Detected

| Class | Description |
|-------|-------------|
| 🔩 **rebar** | Steel reinforcement bars |
| 🧱 **brick** | Brick fragments and pieces |
| 🪨 **cementitious_debris** | Concrete and cement chunks |
| 🔵 **PVC** | PVC pipes and plastic material |
| 🔌 **wires** | Electrical wires and cables |

---

## 📊 Model Performance

| Metric | Score |
|--------|-------|
| **mAP50** | **70.93%** |
| **mAP50-95** | 56.03% |
| **Precision** | 81.32% |
| **Recall** | 67.57% |

### Per-Class mAP50:
| Class | mAP50 |
|-------|-------|
| wires | 83.53% |
| brick | 72.42% |
| PVC | 57.29% |
| cementitious_debris | 38.79% |
| rebar | 28.12% |

---

## 🗄️ Datasets Used

I merged 3 public datasets to improve model accuracy:

| Dataset | Images | Source |
|---------|--------|--------|
| CONVR2022 | ~1000 | [Roboflow Universe](https://universe.roboflow.com/convr2022/construction-item) |
| Mendeley CDW | 400 | [Mendeley Data](https://data.mendeley.com/datasets/24d45pf8wm/2) |
| SpringerNature | 400+ | [Figshare](https://springernature.figshare.com/articles/dataset/A_benchmark_dataset_for_class-wise_segmentation_of_construction_and_demolition_waste_in_cluttered_environments/28573229) |

---

## 🛠️ Tech Stack

- **Model:** YOLOv8s (Ultralytics)
- **Platform:** Kaggle (Tesla T4 GPU)
- **Language:** Python 3.12
- **Libraries:** Ultralytics, Roboflow, OpenCV, Matplotlib
- **Format:** COCO → YOLO conversion for Mendeley & SpringerNature datasets

---

## 🚀 How to Run

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/cdw-waste-detection
cd cdw-waste-detection
```

### 2. Install dependencies
```bash
pip install ultralytics roboflow
```

### 3. Run detection on any image
```python
from ultralytics import YOLO

model = YOLO('cdw_best_model.pt')
results = model.predict('your_image.jpg', conf=0.5)
results[0].show()
```

---

## 📁 Project Structure

```
cdw-waste-detection/
│
├── cdw-object-detection-v2.ipynb   # Main Kaggle notebook
├── README.md                        # Project documentation
└── detection_results.png            # Sample detection output
```

---

## 🔍 Sample Detection

> Model detecting **rebar** and **wires** from construction site images with bounding boxes and confidence scores.

---

## 📈 Training Details

| Parameter | Value |
|-----------|-------|
| Epochs | 100 |
| Image Size | 640×640 |
| Batch Size | 16 |
| Optimizer | AdamW |
| Learning Rate | 0.001 |
| GPU | Tesla T4 |
| Training Time | ~45 min |

---

## 🎓 About Me

**Om Sahu**
- 🎓 BCA (AI & Data Analytics) — 1st Year
- 🏫 LNCT Group of Colleges, Bhopal
- 💼 Freelance AI/ML Developer
- 🤖 Kaggle Competitor
- 📍 Bhopal, Madhya Pradesh, India

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).

---

*Built with ❤️ by Om Sahu using YOLOv8 and Kaggle GPU*

"Available for freelance projects — contact: [abc730244@gmail.com]"
