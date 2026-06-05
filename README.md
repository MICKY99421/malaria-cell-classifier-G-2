# malaria-cell-classifier-G-2
CNN-based malaria cell classifier using transfer learning with ResNet18 and MobileNetV2.
# Malaria Cell Classifier

## Project Overview

This project uses Deep Learning and Transfer Learning to classify microscopic blood cell images as:

- Parasitized
- Uninfected

The goal is to support laboratory technicians by automatically flagging suspicious cells for further review.

---

## Problem Statement

Malaria diagnosis often requires trained technicians to manually inspect blood smear slides under a microscope.

This process is:

- Time-consuming
- Labor-intensive
- Susceptible to fatigue

This project explores the use of Convolutional Neural Networks (CNNs) to automate classification of individual blood cell images.

---

## Dataset

NIH Malaria Cell Images Dataset from Kaggle.

Dataset contains approximately 27,500 labeled cell images.

Classes:

- Parasitized
- Uninfected

Dataset source:

https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria

---

## Models Used

### ResNet18

Transfer learning using pretrained ImageNet weights.

### MobileNetV2

Lightweight architecture optimized for faster inference.

---

## Preprocessing

- Resize images to 224 × 224
- Normalize using ImageNet mean and standard deviation
- Training augmentation:
  - Horizontal flips
  - Rotations
  - Brightness adjustments

---

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Special attention was given to Recall because false negatives are particularly dangerous in malaria screening.

---

## Explainability

Grad-CAM was used to visualize image regions influencing model predictions.

---

## Deployment

A Gradio web application allows users to:

- Upload cell images
- View predicted class
- View confidence score

---

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/malaria-cell-classifier.git
```

Navigate to the project:

```bash
cd malaria-cell-classifier
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Application

Run:

```bash
python gradio_app.py
```

Open the generated local URL in your browser.

---

## Disclaimer

This tool is for decision support only and should not replace the judgement of a trained health professional.

---

## Future Improvements

- Validation on Ghanaian clinical data
- Whole-slide analysis
- Confidence calibration
- Clinical validation studies

---

## Author

Your Name
