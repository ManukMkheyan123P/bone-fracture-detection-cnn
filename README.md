
# 🦴 Bone Fracture Detection Using CNN

### Deep Learning | Computer Vision | TensorFlow | Keras

A computer vision project focused on bone fracture classification and localization using custom Convolutional Neural Networks (CNNs).

The project explores three different deep learning approaches without using YOLO.

## 🎯 Project Objectives

The main goal is to develop CNN-based models capable of analyzing bone X-ray images and learning patterns associated with fractures.

The project includes three tasks:

1. **Multiclass Classification** — Classify X-ray images into different categories.
2. **Binary Classification** — Predict whether an image belongs to a fracture or non-fracture category.
3. **Bounding Box Regression** — Predict the approximate location of a fracture using bounding box coordinates.

## 🧠 Deep Learning Models

### 1. Multiclass Classification

A custom CNN architecture is used to classify X-ray images into multiple categories.

- Convolutional Neural Network (CNN)
- Batch Normalization
- Max Pooling
- Dense Layers
- Dropout
- Softmax Activation
- 10 Output Neurons

The model uses the first annotated object class from each nonempty annotation file.

### 2. Binary Classification

A CNN model is trained to distinguish between two categories:

- Fracture
- Non-Fracture

**Model characteristics:**
- Sigmoid activation
- Binary classification output
- Adam optimizer
- Early stopping

In the current implementation, annotation class `2` is treated as non-fracture, while other annotated classes are treated as fracture.

Images with empty annotation files are skipped.

### 3. Bounding Box Regression

A CNN-based regression model predicts the approximate location of a fracture.

**Predicted coordinates:**

- `x_center`
- `y_center`
- `width`
- `height`

The model uses:

- Convolutional layers
- Batch normalization
- Max pooling
- Global average pooling
- Sigmoid output
- Mean Squared Error (MSE) loss

The current implementation predicts one bounding box based on the first annotated fracture object.

## 📊 Dataset

The project uses the Bone Fractures Detection dataset.

Dataset structure:

```text
Bone Fractures Detection/
│
├── train/
│   ├── images/
│   └── labels/
│
├── valid/
│   ├── images/
│   └── labels/
│
└── data.yaml
```

Images are resized to **128 × 128 pixels** and normalized to the range `[0, 1]`.

The annotation files use YOLO-style normalized bounding box coordinates.

Dataset files are not included in this repository.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| TensorFlow | Deep learning framework |
| Keras | Neural network development |
| OpenCV | Image preprocessing |
| NumPy | Numerical operations |
| Pandas | Data manipulation |
| Matplotlib | Data visualization |
| Jupyter Notebook | Model experimentation |

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/bone-fracture-detection-cnn.git
cd bone-fracture-detection-cnn
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Prepare the dataset

Place the dataset inside the project directory.

### 4. Run the notebook

```bash
jupyter notebook notebooks/bone_fracture_detection.ipynb
```

## 📈 Model Training

The models are trained using:

- Image preprocessing and normalization
- Training and validation datasets
- CNN feature extraction
- Adam optimization
- Early stopping to reduce overfitting

Model performance can be analyzed using training and validation metrics.

## 🔍 Current Limitations

- Models are experimental and require further evaluation.
- Binary classification currently excludes empty annotation files.
- Bounding box regression predicts only one annotated object.
- A separate held-out test evaluation is not included.
- The dataset's class mapping must be verified before interpreting predictions.
- The models are not intended for clinical diagnosis.

## 🚀 Future Improvements

- Improve classification performance.
- Experiment with data augmentation.
- Evaluate models on a separate test dataset.
- Add confusion matrices and classification reports.
- Visualize predicted bounding boxes.
- Compare custom CNNs with transfer learning models.
- Develop a Flask-based web application for image predictions.

## 👨‍💻 Author

**Manuk Mkheyan**

Machine Learning & Python Developer

**GitHub:** [ManukMkheyan123P](https://github.com/ManukMkheyan123P)

### Skills Demonstrated

`Python` `Deep Learning` `CNN` `TensorFlow` `Keras` `Computer Vision` `Image Classification` `Regression`

---

⭐ If you find this project interesting, consider giving it a star!
