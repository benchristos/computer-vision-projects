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




# Road Lane Detection and Departure Warning

## 1. Project Title
**Road Lane Detection and Departure Warning Using Computer Vision**

## 2. Problem Statement
Lane detection is an important application of computer vision in advanced driver assistance systems. Detecting road lane markings can help identify lane boundaries and support lane-departure warning systems. However, variations in road markings, lighting conditions, image quality, and road appearance can make lane detection challenging.

This project explores road lane detection using image processing techniques. The current implementation detects candidate lane-line segments but requires further improvement to reliably identify both lane boundaries.

## 3. Objective
The main objectives of this project are:
- To detect road lane markings from road images.
- To preprocess images for improved lane detection.
- To identify edges and candidate lane-line segments.
- To estimate lane boundaries using detected line segments.
- To develop a basic lane-detection status system.
- To explore the concepts behind lane-departure warning systems.

## 4. Dataset
The project uses a road-line image dataset containing road images for lane-detection experiments.

- **Dataset format:** Image files
- **Dataset usage:** Testing image preprocessing, edge detection, and lane-line identification.
- **Image used in the current test:** One road image resized to 960 × 1280 pixels.
- **Dataset source:** The dataset archive used in Google Colab.

The dataset name, original source, and license should be added here once verified.

## 5. Methodology
The project follows these steps:

1. **Image loading:** Load a road image using OpenCV.
2. **Image resizing:** Resize the image to 960 × 1280 pixels for processing.
3. **Grayscale conversion:** Convert the image to grayscale to simplify image processing.
4. **Gaussian blurring:** Reduce image noise before edge detection.
5. **Canny edge detection:** Identify strong edges that may correspond to road markings.
6. **Region of interest (ROI):** Apply a polygon mask to focus processing on a selected region of the road image.
7. **Hough line detection:** Use the Probabilistic Hough Transform to identify candidate line segments.
8. **Lane-line filtering:** Separate candidate segments according to their slopes and horizontal positions.
9. **Boundary estimation:** Estimate a left lane boundary from candidate line segments.
10. **Output generation:** Draw detected lines, display the detection status, and save the output images and test report.

## 6. Tools and Libraries Used
- **Python:** Main programming language.
- **OpenCV:** Image processing, edge detection, line detection, and drawing.
- **NumPy:** Numerical calculations and array operations.
- **Matplotlib:** Displaying road images and detection results.
- **Google Colab:** Cloud-based coding and execution environment.

## 7. Results
The project successfully performed image preprocessing, edge detection, region-of-interest masking, and candidate line-segment detection.

The current test produced the following results:

- Input image dimensions: 960 × 1280 pixels.
- Detected left boundary: Estimated.
- Right-side candidate line segments: 11.
- Reliable right boundary: Not detected.
- Detection status: `LANE DETECTION INCOMPLETE`.
- Output images and a test report: Generated successfully.

The results demonstrate the basic image-processing and line-detection workflow. However, both lane boundaries have not yet been reliably detected, so the lane-departure warning feature requires further development and validation.

## 8. Conclusion
This project demonstrates the use of Python and OpenCV for basic road lane detection using computer vision. Techniques such as grayscale conversion, Gaussian blurring, Canny edge detection, region-of-interest masking, and the Probabilistic Hough Transform were implemented to identify candidate lane markings.

The current implementation estimates the left lane boundary but does not reliably detect the right boundary. Future improvements can include better region-of-interest selection, filtering of irrelevant line segments, perspective transformation, and testing on additional road images under different conditions.

This project provides a foundation for learning about lane detection and the development of driver-assistance technologies. It is an experimental educational project and is not suitable for real-world driving decisions in its current state.

## Project Structure

```text
Road_Lane_Detection/
├── README.md
└── results/
    ├── lane_detection_output.jpg
    ├── lane_warning_preview.jpg
    └── test_report.txt
```

## Safety Notice
This project is intended for educational purposes only. It must not be used as a real-world lane-departure warning or vehicle safety system without substantial further development and validation.






# Fruit Counting Using OpenCV

## 1. Project Title
**Fruit Counting Using OpenCV**

## 2. Problem Statement
Counting fruits in images manually can be time-consuming. Computer Vision techniques can help identify objects in images and estimate their number automatically. This project uses OpenCV to detect fruit-shaped regions in images through image processing and contour detection.

## 3. Objective
The main objective of this project is to implement a basic fruit-region detection system using Python and OpenCV. The system processes fruit images, detects candidate regions, draws bounding boxes around them, and reports the number of detected regions.

## 4. Dataset
The project uses a fruit image dataset containing **359 images across nine categories**:

- Apple
- Banana
- Cherry
- Chickoo
- Grapes
- Kiwi
- Mango
- Orange
- Strawberry

The images were uploaded to Google Colab and extracted into category-specific folders. The original dataset download link should be added here.

**Dataset structure:**
- `apple fruit/`
- `banana fruit/`
- `cherry fruit/`
- `chickoo fruit/`
- `grapes fruit/`
- `kiwi fruit/`
- `mango fruit/`
- `orange fruit/`
- `strawberry fruit/`

## 5. Methodology
The project follows these Computer Vision steps:

1. **Image acquisition:** Load fruit images from the dataset.
2. **Image resizing:** Resize images to 400 × 400 pixels.
3. **Grayscale conversion:** Convert the images from colour to grayscale.
4. **Noise reduction:** Apply Gaussian blur to reduce image noise.
5. **Thresholding:** Use Otsu's thresholding method to separate foreground and background regions.
6. **Contour detection:** Detect external contours in the binary image.
7. **Contour filtering:** Ignore contours with an area of 1,000 pixels or less.
8. **Bounding-box drawing:** Draw green rectangles around the remaining regions.
9. **Region counting:** Count the detected regions and save the results in a CSV file.

## 6. Tools and Libraries Used
- **Python:** Main programming language.
- **OpenCV:** Image processing, thresholding and contour detection.
- **Pandas:** Storing and exporting detection results.
- **Matplotlib:** Displaying and visualising fruit detection outputs.
- **Google Colab:** Cloud-based development and testing environment.
- **GitHub:** Project storage and version control.

## 7. Results
The system was tested on one sample image from each of the nine fruit categories.

| Fruit category | Detected regions |
|---|---:|
| Apple | 1 |
| Banana | 1 |
| Cherry | 2 |
| Chickoo | 1 |
| Grapes | 3 |
| Kiwi | 1 |
| Mango | 1 |
| Orange | 2 |
| Strawberry | 1 |
| **Total** | **13** |

The results show that the algorithm can identify candidate image regions and display bounding boxes. However, detected regions are not necessarily equal to the actual number of fruits.

**Performance evaluation:** The current implementation reports detected-region counts. Ground-truth fruit counts have not been established, so accuracy, precision, recall and counting error cannot yet be reliably calculated.

## 8. Conclusion
This project demonstrates a basic Computer Vision approach to fruit-region detection using OpenCV. Techniques such as grayscale conversion, Gaussian blur, Otsu thresholding and contour detection were implemented and tested on nine fruit categories.

The results demonstrate the working image-processing pipeline. However, the system has limitations when dealing with complex backgrounds, overlapping fruits, shadows and differences in lighting. Future improvements could include colour-based segmentation, watershed segmentation or a trained object-detection model to improve detection and counting reliability.

## Project Files
- `fruit_counting.py` — Python source code.
- `requirements.txt` — Required Python libraries.
- `results/fruit_detection_results.csv` — Detection results.
- `dataset/README.md` — Dataset information.

## How to Run
Install the required libraries:

```bash
pip install -r requirements.txt
```

Ensure that the dataset is downloaded and extracted into the expected folder structure. Update the dataset path in the source code if necessary, then run:

```bash
python fruit_counting.py
```




# Parking Slot Occupancy Detection 

## 1. Project Title
**Parking Slot Occupancy Detection Using Computer Vision**

## 2. Problem Statement
Finding available parking spaces in crowded parking areas can be time-consuming and inconvenient. Manual monitoring of parking spaces requires continuous observation and may lead to delays and inaccurate identification of vacant spaces. A computer vision-based system can help identify occupied and vacant parking spaces automatically from images.

## 3. Objective
The main objective of this project is to develop an object detection model that identifies parking spaces as **Occupied** or **Vacant** using the YOLO11 deep learning model. The project aims to automate parking space monitoring, reduce the effort required for manual inspection, and demonstrate the application of computer vision in intelligent parking systems.

## 4. Dataset
The project uses a parking lot image dataset obtained from Kaggle.

- Total images: 150
- Training images: 120
- Validation images: 30
- Annotation format provided: JSON
- Model training annotation format: YOLO
- Classes: Occupied and Vacant

The JSON annotations were converted into YOLO-compatible bounding box labels. The dataset was divided into training and validation sets to train and evaluate the object detection model.

## 5. Methodology
The project was completed using the following steps:

1. **Dataset collection:** Obtained the parking lot image dataset from Kaggle.
2. **Data preparation:** Extracted the dataset and inspected the images and JSON annotations.
3. **Annotation conversion:** Converted the bounding box coordinates into YOLO format and assigned class IDs to Occupied and Vacant parking spaces.
4. **Dataset splitting:** Divided the dataset into 120 training images and 30 validation images.
5. **Model training:** Trained a YOLO11n object detection model for 10 epochs using CPU.
6. **Model evaluation:** Evaluated the trained model using precision, recall, mean Average Precision (mAP), and evaluation plots.
7. **Prediction testing:** Tested the trained model on a validation image and saved the resulting image with detected parking spaces.
8. **Result analysis:** Examined the evaluation metrics, confusion matrix, precision-recall curve, and prediction images.

## 6. Tools and Libraries Used
- **Python:** Main programming language.
- **Ultralytics YOLO11:** Object detection model used for training and prediction.
- **PyTorch:** Deep learning framework used by the model.
- **OpenCV:** Image processing support.
- **JSON:** Reading the original dataset annotations.
- **Google Colab:** Cloud-based environment used for training and evaluation.

## 7. Results
The trained YOLO11n model was evaluated on 30 validation images containing 562 annotated objects.

### Overall Evaluation Results

| Metric | Result |
|---|---:|
| Precision | 88.36% |
| Recall | 91.22% |
| mAP@50 | 92.23% |
| mAP@50–95 | 73.97% |

### Class-wise Results

| Class | Precision | Recall | mAP@50 |
|---|---:|---:|---:|
| Occupied | 93.5% | 94.6% | 97.7% |
| Vacant | 83.2% | 87.8% | 86.7% |

The model was also tested on a validation image named `126.jpg`, where it reported 29 detections classified as Occupied.

The evaluation generated a confusion matrix, precision-recall curve, precision curve, recall curve, F1 curve, and prediction comparison images. These outputs are saved in the project's `results/final_evaluation` directory.

The results indicate good detection performance on the validation dataset. However, the validation set is relatively small, and performance may differ on unseen images or under different lighting and camera conditions.

## 8. Conclusion
This project demonstrates how deep learning and computer vision can be used to detect occupied and vacant parking spaces automatically. The YOLO11n model achieved an overall mAP@50 of 92.23% on the validation dataset. The project provided practical experience in dataset preparation, annotation conversion, object detection model training, evaluation, and result visualization.

In the future, the system could be improved by using a larger and more diverse dataset, testing on live camera footage, and integrating the model into a real-time parking management application.

---

**Project:** Parking Slot Occupancy Detection Using YOLO11  
**Model:** YOLO11n  
**Dataset split:** 120 training images and 30 validation images  
**Environment:** Google Colab
