# Pneumonia Detection with Domain Generalization

A deep learning project for **pneumonia detection from chest X-ray images**, with a focus on improving model generalization across different datasets and imaging domains.

The main objective is to develop a model that learns meaningful pneumonia-related visual features rather than relying heavily on dataset-specific patterns, allowing it to perform more reliably on images from unseen domains.

## 📌 Project Overview

Medical imaging datasets can differ significantly because of variations in hospitals, imaging equipment, patient populations, acquisition protocols, and data distributions. A model trained on one dataset may therefore perform well on its training domain but degrade when evaluated on another dataset.

This project investigates **domain generalization and transfer learning** for pneumonia detection by training models on multiple chest X-ray datasets and evaluating their performance on a different, unseen dataset.

## 🎯 Objectives

* Detect pneumonia from chest X-ray images.
* Investigate the effect of domain shifts on model performance.
* Improve generalization across different chest X-ray datasets.
* Compare deep learning architectures for pneumonia classification.
* Evaluate models on unseen data from a different domain.
* Analyze model performance using appropriate classification metrics.

## 🗂️ Datasets

The project uses multiple chest X-ray datasets from different sources/domains.

The datasets include:

* **NIH ChestX-ray14**
* **Stanford CheXpert**
* Additional chest X-ray datasets used for cross-domain evaluation.

The experimental setup uses multiple domains for training and reserves another domain for evaluation to investigate how well the model generalizes to unseen data.

## 🧠 Methodology

The overall workflow consists of:

```text
Chest X-ray Datasets
        ↓
Data Preprocessing
        ↓
Image Resizing & Normalization
        ↓
Data Augmentation
        ↓
Transfer Learning
        ↓
Model Training
        ↓
Cross-Dataset Evaluation
        ↓
Performance Analysis
```

### Data Preprocessing

The preprocessing pipeline includes:

* Image resizing
* Normalization
* Data augmentation
* Dataset organization
* Label preparation
* Handling differences between datasets

### Transfer Learning

Pre-trained deep learning models are used as the foundation for pneumonia classification. Transfer learning allows the models to leverage previously learned visual representations and adapt them to the medical imaging task.

### Models

The experiments include deep learning architectures such as:

* **DenseNet-121**
* **EfficientNetV2S**

DenseNet-121 was particularly useful because of its strong feature reuse, relatively efficient architecture, and suitability for medical image classification.

## 🔬 Domain Generalization Setup

A key part of this project is **cross-domain evaluation**.

Instead of evaluating the model only on images from the same dataset used during training, the model is evaluated on an unseen dataset/domain.

For example:

```text
Domain A ─┐
Domain B ─┼──→ Model Training ──→ Unseen Domain ──→ Evaluation
Domain C ─┘
```

This setup helps investigate whether the model learns general pneumonia-related features rather than memorizing characteristics specific to a particular dataset.

## 📊 Evaluation

Model performance is evaluated using metrics such as:

* Accuracy
* Precision
* Recall
* F1-score
* AUC / ROC-AUC
* Confusion Matrix

Cross-dataset performance is particularly important because conventional in-domain accuracy may not reflect how well a medical AI system performs when exposed to data from another source.

## 📁 Repository Structure

```text
Pneumonia-Detection-with-Domain-Generalization/
│
├── experiment_1.ipynb
├── experiment_epoch_1.ipynb
├── pneumonia_epoch2.ipynb
├── pneumonia-streamlit-app.ipynb
└── README.md
```

### Notebooks

**`experiment_1.ipynb`**
Initial experimentation and model development.

**`experiment_epoch_1.ipynb`**
Training and evaluation experiments across different epochs/configurations.

**`pneumonia_epoch2.ipynb`**
Further model training and experimentation.

**`pneumonia-streamlit-app.ipynb`**
Prototype implementation for deploying the trained pneumonia detection model through a Streamlit interface.

## 🖥️ Streamlit Application

A Streamlit-based prototype is included to demonstrate model inference through a simple user interface.

The application allows a user to provide a chest X-ray image and obtain a model prediction.

```text
X-ray Image
     ↓
Streamlit Interface
     ↓
Trained Deep Learning Model
     ↓
Prediction
```

## 🛠️ Technologies

* Python
* TensorFlow
* PyTorch
* OpenCV
* NumPy
* Pandas
* scikit-learn
* Matplotlib
* Streamlit
* Jupyter Notebook

## 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

* Medical image classification
* Deep learning and transfer learning
* Image preprocessing
* Model training and fine-tuning
* Cross-dataset evaluation
* Domain generalization concepts
* Performance evaluation
* Model visualization
* Deploying ML models with Streamlit

## ⚠️ Disclaimer

This project is developed for **academic and research purposes**. The model is not intended to provide medical diagnosis or replace evaluation by qualified healthcare professionals.

## 👨‍💻 Author

**Muhammad Arslan**

Bachelor of Computer Science
Lahore Garrison University, Pakistan

GitHub: [Muhammad-Arslan6621](https://github.com/Muhammad-Arslan6621)
