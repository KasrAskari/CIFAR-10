# CIFAR-10 Deep Learning Project

This project implements and compares deep learning models for classifying images from the CIFAR-10 dataset. It includes a standard deep convolutional neural network (CNN), a hyperparameter-tuned CNN using KerasTuner, and a Wide-and-Deep model. The project evaluates these models using accuracy, F1-score, and ROC-AUC metrics.

## Project Overview
The CIFAR-10 dataset consists of 60,000 32x32 color images across 10 classes (e.g., airplane, cat, dog). This project:
- Loads and preprocesses the dataset, splitting it into 15% test and 85% train/validation sets.
- Implements a deep CNN with up to 5 hidden layers.
- Optimizes hyperparameters using KerasTuner with RandomSearch.
- Designs a Wide-and-Deep model combining shallow and deep feature extraction.
- Reports performance metrics in a tabular format.

## Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

## Dependencies
The required Python libraries are listed in `requirements.txt`. Key dependencies include:
- `numpy==1.26.4`
- `tensorflow==2.16.1`
- `scikit-learn==1.4.2`
- `keras-tuner==1.4.7`
- `pandas==2.2.2`

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/cifar10-deep-learning.git
   cd cifar10-deep-learning
   ```
2. (Optional) Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Linux/Mac
   venv\Scripts\activate     # On Windows
   ```
3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Results
The script generates a table comparing the performance of three models:
- **Deep Model**: A CNN with 5 hidden layers.
- **Tuned Model**: A CNN optimized with KerasTuner.
- **Wide-and-Deep Model**: A hybrid model combining wide and deep paths.

Example output:
```
Results Table:
   Dataset     Deep Accuracy  Deep F1  Deep ROC-AUC  Tuned Accuracy  Tuned F1  Tuned ROC-AUC  WideDeep Accuracy  WideDeep F1  WideDeep ROC-AUC
0  Train       0.85           0.84     0.98          0.87            0.86      0.99           0.86               0.85         0.98
1  Validation  0.75           0.74     0.92          0.78            0.77      0.94           0.76               0.75         0.93
2  Test        0.73           0.72     0.91          0.76            0.75      0.93           0.74               0.73         0.92
```

(Values are illustrative and depend on actual training.)

## Notes
- The dataset is normalized to [0, 1] and labels are one-hot encoded for `CategoricalCrossentropy` loss.
- Training times may vary based on hardware (CPU/GPU).
- For GPU acceleration, ensure TensorFlow is configured with CUDA support.

## Contributing
Feel free to fork this repository, submit issues, or create pull requests with improvements!

## License
This project is licensed under the MIT License.
