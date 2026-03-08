# Transfer Learning Image Classification Project

## Overview

This project demonstrates **Transfer Learning** for image classification using two approaches:

1. Feature Extraction
2. Fine-Tuning

Transfer learning allows us to use a pre-trained deep learning model and adapt it to a new dataset. This reduces training time and improves performance when the dataset is small.

---

## Dataset

The project uses **ImageNet-pretrained deep learning models** for transfer learning. ImageNet is a large-scale dataset containing **over 1 million labeled images across 1000 classes** and is commonly used to pre-train convolutional neural networks.

In this project, models such as **VGG16, ResNet50, or MobileNet** are loaded with **pre-trained ImageNet weights**. These learned visual features (edges, textures, shapes, objects) are then reused for the new classification task.

The working dataset is divided into:

* Train set
* Validation set
* Test set

Image preprocessing techniques such as **resizing, normalization, and augmentation** are applied before training.

---

# Approach 1: Feature Extraction

In feature extraction, we use a **pre-trained CNN model** as a fixed feature extractor. The convolutional base of the model is frozen and only the final classification layers are trained.

### Steps

1. Load a pre-trained model (such as VGG16 / ResNet50 / MobileNet).
2. Freeze all convolutional layers.
3. Add custom dense layers for classification.
4. Train only the newly added layers.
5. Evaluate the model.

### Advantages

* Faster training
* Requires less data
* Prevents overfitting

---

# Approach 2: Fine-Tuning

Fine-tuning is an advanced transfer learning technique where we unfreeze some of the deeper layers of the pre-trained model and retrain them along with the classifier.

### Steps

1. Load the pre-trained model.
2. Freeze most of the early layers.
3. Unfreeze top layers of the network.
4. Train the model with a low learning rate.
5. Evaluate performance.

### Advantages

* Higher accuracy
* Better adaptation to the dataset

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* OpenCV

---

## Project Structure

```
project/
│
├── dataset/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── feature_extraction_model.ipynb
├── fine_tuning_model.ipynb
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository:

```
git clone <your-repo-link>
cd project
```

Install dependencies:

```
pip install -r requirements.txt
```

---

## Run the Project

### Feature Extraction

```
python feature_extraction_model.py
```

### Fine-Tuning

```
python fine_tuning_model.py
```

---

## Results

The project compares the performance of:

* Feature Extraction
* Fine-Tuning

Metrics used:

* Accuracy
* Loss
* Confusion Matrix

---

## Conclusion

Transfer learning significantly improves model performance when working with limited datasets. Feature extraction provides fast results while fine-tuning helps achieve better accuracy.

---

## Author

Tejesh Yewale
