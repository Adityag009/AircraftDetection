# Aircraft Detection

This repository contains the implementation of an aircraft detection model using YOLO (You Only Look Once). The model is trained on a custom dataset of various aircraft types and tested on aircraft videos to detect and classify aircraft effectively.

## Project Overview

The goal of this project is to detect and classify aircraft in video footage using a deep learning-based object detection approach. The YOLO model was trained on a dataset containing images of multiple aircraft types, including **Il-76**, **J10**, **J15-J16**, **KJ-2000**, and **Mig-21**.

## Model Training Details

The YOLO model used for this project is **YOLOv10l**, which consists of:

- **461 layers**
- **25,727,162 parameters**
- **126.4 GFLOPs**

### Training Metrics

The model was evaluated on a validation dataset, and the results are as follows:

| Class       | Images | Instances | Precision (P) | Recall (R) | mAP@50 | mAP@50-95 |
|-------------|--------|-----------|---------------|------------|--------|-----------|
| **All**     | 44     | 54        | 0.864         | 0.739      | 0.850  | 0.736     |
| Il-76        | 7      | 7         | 0.754         | 0.714      | 0.786  | 0.786     |
| J10          | 10     | 17        | 0.691         | 0.529      | 0.649  | 0.541     |
| J15-J16      | 9      | 9         | 1.000         | 0.743      | 0.922  | 0.757     |
| KJ-2000      | 10     | 10        | 0.994         | 0.800      | 0.949  | 0.875     |
| Mig-21       | 8      | 11        | 0.882         | 0.909      | 0.942  | 0.723     |

### Inference Speed

- **Preprocessing Time:** 0.2ms per image
- **Inference Time:** 7.0ms per image
- **Postprocessing Time:** 0.1ms per image

## Outputs

### Videos

The trained model was tested on various aircraft videos. The following video outputs demonstrate the model's ability to detect and classify aircraft in real-time:

 `output_videoA.mp4`

## Repository Contents

- `AircraftDetection.ipynb`: Jupyter Notebook containing the model training and testing code.
- `bestMulti.pt`: The trained YOLO model weights.
- Video outputs of model inference on test data.
