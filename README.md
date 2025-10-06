# AIPI 590 - XAI - Explainable Deep Learning

## Explainable AI for Assistive Object Recognition

This project explores how explainable deep learning techniques can be used to understand and improve the behavior of computer vision models in assistive technology contexts. Using a pretrained ResNet-50 model, Grad-CAM and its variants (Grad-CAM++ and Score-CAM) are applied to visualize which regions of an image most influence the model’s predictions.

## Objective

The goal is to examine whether a pretrained image classifier focuses on meaningful object regions when identifying common household items that accessibility tools might need to recognize, such as a mug, phone, laptop, door, chair, book, and backpack.
By comparing Grad-CAM variants, we gain insight into how model attention differs and how explainability contributes to trust and interpretability in assistive AI systems.

## Methods

- Model: Pretrained ResNet-50 (ImageNet weights)

- Explainability Techniques:

    - Grad-CAM (baseline)

    - Grad-CAM++ (sharper localization)

    - Score-CAM (context-aware smoothing)

- Dataset: 7 manually selected images of everyday objects (sourced from Unsplash). Each image was preprocessed, classified, and visualized using the three Grad-CAM methods.


## Findings

- The model generally attends to relevant object regions, such as the keyboard on a laptop or the rim of a mug.

- Grad-CAM++ produced the most precise focus regions, while Score-CAM gave smoother but broader context coverage.

- Even when misclassified (e.g., door classified as refrigerator), the model still focused on the right object region.

- Explainability tools like Grad-CAM can increase transparency and trust in accessibility-focused AI applications.

## How to Run

- Open the notebook directly in Google Colab by clicking this badge: [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ailina-aniwan/xai-explainable-deep-learning/blob/main/gradcam_analysis.ipynb)

- Run all cells in order.

- The Grad-CAM heatmaps will be displayed within the notebook.