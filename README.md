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



# Traffic Sign Recognition Using CNN

## 1. Project Title
**Traffic Sign Recognition Using Convolutional Neural Network (CNN)**

## 2. Problem Statement
Traffic sign recognition is an important task in intelligent transportation systems and autonomous driving. Traffic signs provide essential information about speed limits, road conditions, warnings, and traffic regulations. Manually identifying traffic signs can be challenging in different lighting and road conditions. Therefore, an automated system is needed to recognize traffic signs accurately from images.

## 3. Objective
The main objective of this project is to develop a deep learning model using a Convolutional Neural Network (CNN) to classify traffic sign images into 43 different categories. The project aims to train and evaluate the model using a traffic sign dataset and measure its performance on unseen test images.

## 4. Dataset
This project uses the **German Traffic Sign Recognition Benchmark (GTSRB)** dataset.

- Training images: 39,209
- Test images: 12,630
- Number of classes: 43
- Image input size: 30 × 30 pixels
- Image format: RGB

The dataset contains images representing different traffic signs, such as speed limits, warning signs, and prohibition signs. The images are resized and normalized before being used by the CNN model.

Dataset source: [GTSRB – German Traffic Sign Recognition Benchmark](https://benchmark.ini.rub.de/gtsrb_dataset.html)

## 5. Methodology
The project was developed using the following steps:

1. **Dataset Preparation:** Loaded the traffic sign images and their corresponding class labels.
2. **Preprocessing:** Resized images to 30 × 30 pixels, converted them into RGB format, and normalized pixel values to the range 0–1.
3. **Data Splitting:** Divided the training dataset into training and validation sets.
4. **Model Development:** Built a CNN architecture containing convolutional layers, max-pooling layers, a flatten layer, dense layers, and a dropout layer.
5. **Model Training:** Trained the CNN model for 10 epochs using the training dataset.
6. **Validation:** Evaluated the model on the validation dataset to monitor its performance.
7. **Testing:** Evaluated the trained model on 12,630 separate test images.
8. **Performance Analysis:** Generated a classification report, confusion matrix, and CSV file containing actual labels, predicted labels, correctness, and prediction confidence.
9. **Model Saving:** Saved the trained model in Keras format for future use.

## 6. Tools and Libraries Used
- **Python** – Programming language
- **Google Colab** – Development and execution environment
- **TensorFlow and Keras** – CNN model development and training
- **NumPy** – Numerical operations and array processing
- **Pandas** – Dataset and CSV file handling
- **Matplotlib** – Visualization of training results
- **Seaborn** – Confusion matrix visualization
- **Scikit-learn** – Classification report, confusion matrix, and evaluation metrics
- **Pillow (PIL)** – Image processing

## 7. Results
The trained CNN model achieved the following results:

| Evaluation Metric | Result |
|---|---:|
| Validation Accuracy | 99.46% |
| Test Accuracy | 95.41% |
| Total Test Images | 12,630 |
| Correct Predictions | 12,050 |
| Incorrect Predictions | 580 |
| Average Prediction Confidence | 97.43% |

The model achieved 99.46% accuracy on the validation dataset and 95.41% accuracy on the separate test dataset. The confusion matrix was generated to examine classification performance across the 43 traffic sign classes.

The project also produced a saved Keras model and a CSV file containing the test prediction results.

## 8. Conclusion
This project demonstrates how a Convolutional Neural Network can be used to recognize and classify traffic signs from images. The model achieved 95.41% accuracy on the separate test dataset, demonstrating its ability to classify many traffic sign images correctly.

The project helped develop practical knowledge of image preprocessing, deep learning, CNN architecture, model training, evaluation, and visualization. In the future, the system could be improved through data augmentation, further model optimization, and testing under different real-world lighting and weather conditions.

**Author:** Ben Christos Thomas

**Project Type:** Computer Vision / Deep Learning

**Model:** Convolutional Neural Network (CNN)
