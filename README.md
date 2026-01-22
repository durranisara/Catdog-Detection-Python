# Cat vs Dog Image Classification using CNN

This repository implements a Convolutional Neural Network (CNN) for binary image classification of cats and dogs using Keras. The model is trained on labeled image data and predicts whether a given image belongs to the **cat** or **dog** class.

The project uses a simple CNN architecture with image preprocessing, training, validation, and evaluation pipelines.

---

## ✨Features

- Binary image classification (Cat vs Dog)
- CNN built using Keras Sequential API
- Image preprocessing with ImageDataGenerator
- Training, validation, and evaluation support
- Model weight saving and loading
- Single image prediction

---

## 📁Dataset

The dataset consists of images of cats and dogs. Due to the large size of the dataset, images are **not included** in this repository.

You can use publicly available datasets such as:

- Kaggle Cats vs Dogs Dataset

---

## 🗂 Directory Structure

After downloading and organizing the dataset, the directory structure should look like this:
CAT-DOG-CNN
├── data
│ ├── train
│ │ ├── cats
│ │ │ └── cat.1.jpg
│ │ └── dogs
│ │ └── dog.1.jpg
│ ├── validation
│ │ ├── cats
│ │ └── dogs
│ └── evaluation
│ ├── cats
│ └── dogs
├── cat_dog_1.h5
├── main.py
└── README.md


---

##🧠 Model Architecture

The CNN model consists of the following layers:

- Convolutional Layer (32 filters, 3×3, ReLU)
- Max Pooling Layer (2×2)
- Convolutional Layer (32 filters, 3×3, ReLU)
- Max Pooling Layer (2×2)
- Flatten Layer
- Fully Connected Dense Layer (128 units, ReLU)
- Output Layer (1 unit, Sigmoid)

### Compilation Details

- Loss Function: `binary_crossentropy`
- Optimizer: `Adam`
- Metric: `accuracy`

---

## Training Details

- Image size: 224 × 224
- Batch size: 64
- Epochs: 8
- Data augmentation:
  - Rotation
  - Zoom
  - Shear
  - Horizontal flip

Training and validation are performed using directory-based generators.

---

## Installation & Setup
### Install required dependencies:
```bash
pip install numpy keras tensorflow
```
### Model Training

Run the training script to train the CNN model.
The trained weights will be saved as:
```bash
cat_dog_1.h5
```
### Evaluation & Prediction
The model supports prediction on:

-A complete evaluation directory

-Individual images

Prediction output:
```bash
0 → Cat

1 → Dog
```
### Results
The model achieves good accuracy on the validation set and performs reliably on unseen evaluation images. Performance vary depending on dataset size, image quality, and training duration.


