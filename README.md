# 🧠 CIFAR-10 Deep Learning Project

A deep dive into image classification using the CIFAR-10 dataset. This project implements and compares multiple deep learning architectures — including a standard CNN, a hyperparameter-tuned CNN (via KerasTuner), and a custom Wide-and-Deep model — to evaluate performance on classification tasks using **Accuracy**, **F1-score**, and **ROC-AUC**.

---

## 📦 Overview

CIFAR-10 is a classic image classification dataset containing **50,000 32×32 color images** across **10 categories** (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck).  
You can find more about the dataset [here](https://keras.io/api/datasets/cifar10/).

This project includes:

- 🔹 Data preprocessing and splitting (85% train/val, 15% test)
- 🔹 A standard deep CNN with up to 5 hidden layers
- 🔹 Hyperparameter tuning via `KerasTuner` using `RandomSearch`
- 🔹 A Wide-and-Deep model combining shallow and deep features
- 🔹 Metric evaluation in tabular format (Accuracy, F1, ROC-AUC)

---

## 🚀 Quick Start

### ✅ Prerequisites
- Python 3.8+
- `pip` package manager

### 📥 Installation

1. **Clone the repo:**
   ```bash
   git clone https://github.com/KasrAskari/CIFAR-10
   cd CIFAR-10
   ```

2. **(Optional) Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate        # On Linux/Mac
   venv\Scripts\activate           # On Windows
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

---

## 📚 Dependencies

Main libraries used:

- `numpy==1.26.4`
- `tensorflow==2.16.1`
- `scikit-learn==1.4.2`
- `keras-tuner==1.4.7`
- `pandas==2.2.2`

(See `requirements.txt` for full list.)

---

## 📊 Results

The following table compares performance across models:

```
Results Table:
   Dataset     Deep Accuracy  Deep F1  Deep ROC-AUC  Tuned Accuracy  Tuned F1  Tuned ROC-AUC  WideDeep Accuracy  WideDeep F1  WideDeep ROC-AUC
0  Train       0.85           0.84     0.98          0.87            0.86      0.99           0.86               0.85         0.98
1  Validation  0.75           0.74     0.92          0.78            0.77      0.94           0.76               0.75         0.93
2  Test        0.73           0.72     0.91          0.76            0.75      0.93           0.74               0.73         0.92
```

📌 *Values are sample outputs. Final results depend on training runs.*

---

## 📝 Notes

- Images are normalized to `[0, 1]`.
- Labels are one-hot encoded for use with `CategoricalCrossentropy`.
- Model training time may vary depending on hardware (CPU vs. GPU).
- For best performance, ensure TensorFlow is CUDA-enabled if using a GPU.

---

## 🤝 Contributing

Pull requests are welcome! Feel free to fork the project, open issues, or suggest improvements.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
