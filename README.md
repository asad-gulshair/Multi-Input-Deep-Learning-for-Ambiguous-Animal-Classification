# Multi-Input-Deep-Learning-for-Ambiguous-Animal-Classification
 Multi-Input Deep Learning for Ambiguous Animal Classification
This project explores the **Ambivision dataset**, a unique optical illusion dataset designed for ambiguous animal classification. The dataset includes **eye coordinates, bounding boxes, viewing direction, and animal labels**, making it well-suited for research on **Explainable AI (XAI)** and challenging visual perception problems.

The primary goal of this project is to design a **multi-input deep learning model** that integrates:
- Image features from EfficientNet
- Spatial keypoints (eye coordinates)
- Directional vectors

We apply **attention masks** to highlight informative regions of the images, allowing the model to better interpret ambiguous animal visuals.

---

## Key Features
- Multi-input model: Combines **image data** with **spatial features** (keypoints + vectors).
- Attention-based preprocessing to enhance relevant visual cues.
- Trained using **EfficientNetB4** backbone with augmentation and regularization.
- Achieved **55–60% accuracy**, showing potential for further improvements.

---

## Dataset
**Ambivision Dataset** – Ambiguous optical illusion dataset for animal classification.  
Includes annotations for:
- Eye coordinates
- Bounding boxes
- Viewing directions
- Animal labels

*Citation:* [ArXiv preprint: Ambivision Dataset](https://arxiv.org/abs/2505.21589)

---

## Model Architecture
- **Image Branch:** EfficientNetB4 for visual features
- **Mask Branch:** Attention masks generated from keypoints
- **Vector Branch:** Directional vectors + keypoints (8D feature)
- **Fusion:** Concatenation of all features followed by fully connected layers
- **Loss:** Binary cross-entropy / focal loss
- **Metrics:** Accuracy, AUC

---

## Results
- Validation Accuracy: **~55–60%**
- Demonstrates feasibility of combining spatial + visual data for ambiguous classification.
- Opens pathways for research in **XAI and visual perception**.
