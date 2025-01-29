
# **Indian Sign Language Detection using YOLOv5 and YOLOv7**  

## **Overview**  
This repository contains the research work on **Indian Sign Language (ISL) Detection** using **YOLOv5 and YOLOv7**. The project aims to compare the performance of these two object detection models on an ISL dataset, analyzing their accuracy, precision, recall, and real-time detection capabilities.  



🔗 **Model Weights** (Due to file size constraints, model weights are provided via external links):  
- **YOLOv5 Best Model**: [Download Here](#)  
- **YOLOv7 Best Model**: [Download Here](#)  

## **Dataset**  
- **Dataset Name:** Indian Sign Language Detection  
- **Total Images:** 1,748  
- **Classes:** 35 (Alphabets A-Z and Numbers 0-9)  
- **Train/Validation/Test Split:**  
  - **Train:** 1,212 images  
  - **Validation:** 341 images  
  - **Test:** 195 images  
- **Preprocessing:** Images were resized to **640×640** with auto-orientation applied. No data augmentation was performed.  

## **Models Used**  
### **1️⃣ YOLOv5**  
- Faster convergence, lower computational cost.  
- Shows rapid fluctuations in initial epochs but stabilizes faster.  

### **2️⃣ YOLOv7**  
- More stable training with consistent improvement.  
- Requires longer training time but adapts better with more data.  

## **Performance Comparison**  
| Metric  | YOLOv5 | YOLOv7 |
|---------|--------|--------|
| **Precision** | **0.97** (Faster convergence) | **0.97** (Steady improvement) |
| **Recall** | 0.95 | 0.92 |
| **mAP@0.5** | **0.90** | **Moderate (lower than YOLOv5)** |
| **F1 Score** | 0.95 | 0.92 |

## **Installation & Setup**  
### **1️⃣ Clone the Repository**  
```bash
git clone https://github.com/your-username/ISL-YOLO-Comparison.git
cd ISL-YOLO-Comparison
```

### **2️⃣ Install Dependencies**  
```bash
pip install -r requirements.txt
```

### **3️⃣ Running Inference (Real-Time Detection using Webcam)**  
```bash
python detect.py --weights best_yolov7.pt --source 0 --img-size 640 --conf-thres 0.5 --device cpu
```
> Replace `best_yolov7.pt` with `best_yolov5.pt` to run YOLOv5.

## **How to Use the Models**  
### **Training YOLOv5**
```bash
python train.py --img 640 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt
```
### **Training YOLOv7**
```bash
python train.py --img 640 --batch 16 --epochs 70 --data dataset.yaml --weights yolov7.pt
```

## **Research Paper & Findings**  
📄 [Download the Research Paper](./research_paper.pdf)  

The research explores the efficiency of YOLOv5 and YOLOv7 for ISL detection, highlighting their pros and cons. YOLOv5 offers **faster convergence** but struggles with **small datasets**, while YOLOv7 provides **better adaptability** at the cost of longer training times.

## **Limitations**  
- **Dataset Size**: More images could improve model robustness.  
- **Sign Similarities**: Models struggle with visually similar gestures.  
- **Real-Time Performance**: YOLOv7 is more resource-intensive compared to YOLOv5.  

## **Future Scope**  
- Improving dataset diversity for better model generalization.  
- Implementing real-time sign-to-text translation.  
- Optimizing YOLOv7 for real-time efficiency.  

## **Acknowledgments**  
- **YOLOv5 Repo**: [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5)  
- **YOLOv7 Repo**: [YOLOv7 GitHub](https://github.com/WongKinYiu/yolov7)  
- **Dataset**: [Indian Sign Language Dataset - Roboflow](https://universe.roboflow.com/niladri-basu-roy-qnrm4/indian-sign-language-detection/dataset/2)  

## **Contributors**  
👤 **Eric Fernandes**  
📧 Email: ericfergoa@gmail.c0m
🔗 GitHub: [Ericfdes](https://github.com/EricFdes)  

