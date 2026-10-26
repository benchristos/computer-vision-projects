# computer-vision-projects
Implementation of five Computer Vision projects using Python and OpenCV.



# Road Pothole Detection Using Computer Vision
## 1. Project Title
**Road Pothole Detection Using Computer Vision**

## 2. Problem Statement
Potholes on roads can create safety risks for drivers and passengers and contribute to vehicle damage. Manual road inspection can be time-consuming and may not identify every pothole efficiently. Computer vision and deep learning can help automatically detect potholes from road images.

## 3. Objective
The main objective of this project is to develop a computer vision system that detects potholes in road images using the YOLOv8 object detection model. The system identifies potholes and marks their locations with bounding boxes, helping demonstrate how automated road-condition monitoring can be performed.

## 4. Dataset
A pothole image dataset containing images and XML annotation files was used.

- **Total images:** 665
- **Training images:** 532
- **Validation images:** 66
- **Testing images:** 67
- **Object class:** Pothole

The XML annotations were converted into YOLO format, which contains normalized bounding-box coordinates. The dataset was divided into training, validation, and testing sets.

## 5. Methodology
The project was completed using the following steps:

1. **Dataset preparation:** Extracted the dataset and inspected the road images and XML annotations.
2. **Annotation processing:** Converted XML bounding-box annotations into YOLO format.
3. **Dataset splitting:** Organized the images and labels into training, validation, and testing folders.
4. **Model training:** Trained the YOLOv8n object detection model for 30 epochs.
5. **Model validation:** Evaluated the trained model using the validation dataset.
6. **Model testing:** Evaluated the best model on the separate test dataset.
7. **Prediction:** Tested the trained model on a road image and generated bounding boxes around detected potholes.
8. **Evaluation and documentation:** Recorded the test metrics, saved the trained model, and prepared the project files.

## 6. Tools and Libraries Used
- **Python:** Main programming language
- **Google Colab:** Cloud-based development and training environment
- **Ultralytics YOLOv8:** Object detection model and training framework
- **PyTorch:** Deep learning framework used by YOLO
- **OpenCV:** Image processing
- **NumPy:** Numerical operations
- **Matplotlib:** Image visualization
- **XML processing:** Reading the dataset's annotation files

## 7. Results
The trained model was evaluated on 67 test images containing 193 annotated pothole instances.

| Evaluation Metric | Test Result |
|---|---:|
| Precision | 80.57% |
| Recall | 65.28% |
| mAP@50 | 77.60% |
| mAP@50–95 | 47.94% |

A sample prediction on `img-594.jpg` produced five pothole detections.

The results demonstrate that the model can identify potholes in road images. However, the recall and stricter mAP score indicate that there is room for improvement.

## 8. Conclusion
This project demonstrates the use of computer vision and deep learning for pothole detection using YOLOv8n. The model was trained, validated, and tested on an annotated pothole dataset. It successfully generated pothole detections with bounding boxes and achieved a test mAP@50 of 77.60%.

Future improvements could include training with more diverse road images, tuning model parameters, improving recall, and evaluating the model under different lighting and road conditions. The system is a prototype that demonstrates the potential of automated road-condition monitoring and is not a replacement for professional road inspection.

## Project Files
- `best.pt` — Trained model weights
- `results/pothole_detection_result.jpg` — Sample pothole detection image
- `results/test_report.txt` — Test evaluation report
- `README.md` — Project documentation



