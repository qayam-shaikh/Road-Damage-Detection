# Automated Road Damage Detection

A computer vision project that uses **YOLOv8** to detect and localize road surface damage in images, supporting automated road inspection and infrastructure maintenance.

## Overview

Manual road inspection is time-consuming and difficult to scale. This project applies deep learning–based object detection to identify visible road damage and generate structured predictions for further analysis.

The model detects five categories of road damage using the RDD2022-based dataset.

## Features

- **Multi-Class Detection:** Identifies five types of road damage.
    
- **Bounding Box Localization:** Locates detected damage within road images.
    
- **Transfer Learning:** Uses pretrained YOLOv8m weights for object detection.
    
- **Model Evaluation:** Uses mean Average Precision (mAP) to evaluate detection performance.
    
- **Batch Inference:** Processes multiple test images and generates prediction files.
    
- **Structured Outputs:** Exports detected classes, bounding-box coordinates, and confidence scores in YOLO format.
    

## Damage Categories

|Class ID|Damage Type|
|---|---|
|0|Longitudinal Crack|
|1|Transverse Crack|
|2|Alligator Crack|
|3|Other Corruption|
|4|Pothole|

## Tech Stack

- **Language:** Python
    
- **Computer Vision:** OpenCV
    
- **Deep Learning:** PyTorch
    
- **Object Detection:** Ultralytics YOLOv8m
    
- **Data Processing:** NumPy, Pandas
    
- **Environment:** Jupyter Notebook / Kaggle Notebook
    

## Model Configuration

|Parameter|Configuration|
|---|---|
|Architecture|YOLOv8m|
|Input Resolution|640 × 640|
|Batch Size|16|
|Optimizer|AdamW|
|Learning Rate|0.001|
|Training Epochs|20–30|

The model uses transfer learning from pretrained weights to adapt object detection to road damage categories.

## Workflow

1. **Dataset Preparation:** Load annotated road images and prepare labels in YOLO format.
    
2. **Exploratory Analysis:** Examine class distribution and annotation characteristics.
    
3. **Model Training:** Fine-tune the pretrained YOLOv8m model on road damage images.
    
4. **Model Evaluation:** Assess detection performance using mAP metrics.
    
5. **Batch Inference:** Run predictions on test images.
    
6. **Output Generation:** Save detected classes and normalized bounding-box coordinates as prediction files.
    

## Output Format

Predictions are saved in YOLO format:

```
<class_id> <x_center> <y_center> <width> <height> <confidence>
```

Coordinates are normalized relative to image dimensions.

## Applications

- Automated road condition inspection
    
- Road maintenance planning
    
- Infrastructure damage monitoring
    
- Smart-city analytics
    
- Road damage dataset analysis
    

## Future Improvements

- Video-based road damage detection
    
- Damage severity estimation
    
- GPS-based damage localization
    
- Integration with road maintenance dashboards
    
- Edge-device deployment
    

## Disclaimer

This project is intended for educational and research purposes. Detection results should be validated before being used for operational road maintenance decisions.