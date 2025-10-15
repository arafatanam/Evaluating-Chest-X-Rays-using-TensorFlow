# 🧠 Medical AI – Cardiomegaly Detection using InceptionV3 (TensorFlow)

This project implements a **deep learning model for medical image classification** to detect **Cardiomegaly** (enlarged heart) from chest X-rays using **Transfer Learning** with the **InceptionV3** architecture.  

It follows the workflow demonstrated in the YouTube tutorial:  
🎥 [TensorFlow Course – Building and Evaluating Medical AI Models](https://www.youtube.com/watch?v=8m3LvPg8EuI)

---

## 📁 Project Structure

```

Medical-AI/
│
├── chest_xray.ipynb       # Jupyter Notebook (main code)
├── Cardiomegaly.zip       # Exported trained model (zipped)
└── README.md              # Project documentation

````

---

## 🧩 Overview

This notebook demonstrates how to build, train, evaluate, and visualize a **medical image classification** pipeline using TensorFlow and Keras.  
The task focuses on **binary classification**:
- **Positive class:** Cardiomegaly  
- **Negative class:** No Finding  

---

## ⚙️ Key Features

- ✅ Dataset loading and preprocessing from the **NIH Chest X-ray** dataset (`labels.csv`)
- 🧪 Automatic dataset splitting (Train/Test)
- 🗂️ Balanced class organization (`positive` and `negative` folders)
- 🔄 Data augmentation (rotation, zoom, brightness, translation, contrast)
- 🏗️ Transfer learning using **InceptionV3 (ImageNet pretrained)**
- 📈 Model fine-tuning with early stopping
- 🔍 Evaluation with:
  - Accuracy and loss plots  
  - ROC Curve and AUC calculation  
  - Confidence histograms  
  - Sensitivity and specificity visualization
- 💾 Model exporting for deployment or reuse

---

## 🧠 Model Architecture

The model uses **InceptionV3** (pretrained on ImageNet) as a frozen base for feature extraction, followed by:

- Global Average Pooling
- Dropout layer (0.5)
- Dense output layer (Sigmoid activation for binary classification)

Optimizer: **Adam**  
Loss Function: **Binary Crossentropy**  
Metrics: **Accuracy**

---

## 🧰 Tech Stack

| Library | Purpose |
|----------|----------|
| TensorFlow / Keras | Model building & training |
| NumPy / Pandas | Data processing |
| Matplotlib | Visualization |
| Pillow (PIL) | Image handling |
| Scikit-learn | ROC & AUC computation |
| Graphviz / pydot | Model visualization support |

---

## 📊 Evaluation Metrics

The model is evaluated using:
- **Accuracy (Train & Validation)**
- **Loss (Train & Validation)**
- **ROC Curve & AUC**
- **Sensitivity & Specificity**
- **Confidence Score Distributions**

These visualizations provide insights into the model’s performance and reliability for medical AI applications.

---

## 🧪 Usage

### 1. Open the Notebook
Run the notebook in **Google Colab** (recommended) or Jupyter Notebook.

### 2. Clone the Repository
```bash
!git clone https://github.com/arafatanam/Evaluating-Chest-X-Rays-using-TensorFlow.git
````

### 3. Train and Fine-tune the Model

Execute all cells sequentially.
The notebook handles dataset preparation, model training, and evaluation automatically.

### 4. Export the Model

The trained model is exported to:

```
/content/export/Cardiomegaly/
```

And zipped as:

```
/content/Cardiomegaly.zip
```

---

## 📦 Files to Upload

* `medical_ai_cardiomegaly.ipynb` — Main notebook file
* `Cardiomegaly.zip` — Trained TensorFlow model

These can be used to **reproduce predictions or continue training** on new datasets.

---

## 🚀 Extending the Project

You can easily adapt this notebook for other medical image classification tasks:

* Replace `"Cardiomegaly"` with another finding (e.g., `"Pneumonia"`, `"Edema"`, etc.)
* Update the dataset filtering logic.
* Retrain and export the new model.

---

## 🧑‍🎓 Credits

* **Original Tutorial:** [TensorFlow Course – Building and Evaluating Medical AI Models](https://www.youtube.com/watch?v=8m3LvPg8EuI)
* **Author of Tutorial:** *freeCodeCamp.org*

---

## 📜 License

This project is for **educational and research purposes only**.
It is not intended for clinical or diagnostic use.

---

**⭐ If you found this project useful, consider giving it a star on GitHub!**