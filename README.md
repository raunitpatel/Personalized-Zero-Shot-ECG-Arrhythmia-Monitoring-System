
# Personalized Zero-Shot ECG Arrhythmia Monitoring System

## 📖 Overview

This project implements a **Personalized Zero-Shot ECG Arrhythmia Monitoring System** that leverages domain adaptation techniques to classify and monitor arrhythmias in electrocardiogram (ECG) signals. It focuses on personalized monitoring by adapting models to individual users' data, enabling effective detection of suspicious heartbeats with minimal labeled data. The system is built using Python and Jupyter Notebooks, with a modular structure for data preparation, model training, and inference.

---

## ✨ Features

- **Zero-Shot Learning**: Enables arrhythmia detection with limited or no labeled data for new users.
- **Domain Adaptation**: Adapts models to individual users for personalized performance.
- **Ensemble Classification**: Combines multiple classifiers for robust predictions.
- **Energy-Efficient Detection**: Optimized for computational efficiency during real-time monitoring.
- **End-to-End Pipeline**: Includes data preprocessing, model training, validation, and inference.

---

## 🛠️ Project Structure

The repository is organized into the following key components:


| File/Folder | Description |
| :-- | :-- |
| `Part_a_ECG_beat_extraction.ipynb` | Extracts individual ECG beats from raw signals. |
| `Part_b_ECG_dataset_beat_single_preparation.ipynb` | Prepares datasets with single beats for training and testing. |
| `Part_c_ECG_dataset_beat_trios_preparation.ipynb` | Prepares datasets with beat trios for advanced classification tasks. |
| `Part_d_domain_adaption.ipynb` | Implements domain adaptation techniques for personalized monitoring. |
| `Part_e_domain_adaptation_with_ensemble_classification.ipynb` | Applies ensemble methods for classification. |
| `Part_f_domain_adaptation_with_ensemble_validation.ipynb` | Validates ensemble models on test datasets. |
| `Part_g_inference_for_a_user.ipynb` | Performs inference for a specific user using the trained model. |
| `DL_LAB_REPORT.pdf` | Detailed report describing the methodology and results of the project. |

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.8+
- Jupyter Notebook
- Required Python libraries (see below).


### Installation

1. Clone the repository:

```bash
git clone https://github.com/raunitpatel/Personalized-Zero-Shot-ECG-Arrhythmia-Monitoring-System.git
cd Personalized-Zero-Shot-ECG-Arrhythmia-Monitoring-System
```

2. Install dependencies:

```bash
pip install matplotlib numpy scipy pandas seaborn torch wfdb import_ipynb pytorch
```


### Dataset Preparation

1. Download the [MIT-BIH Arrhythmia Database](https://www.physionet.org/content/mitdb/).
2. Run `Part_a_ECG_beat_extraction.ipynb` to extract single beats and beat trios.
3. Use `Part_b_` and `Part_c_` notebooks to prepare datasets.

---

## 🧪 Usage

### Training

1. Perform domain adaptation using `Part_d_domain_adaption.ipynb`.
2. Train classifiers using the prepared datasets.

### Inference

Run `Part_g_inference_for_a_user.ipynb` to perform inference for a specific user.

---

## 📊 Results

The table below compares the performance of various methods, including CNN-based approaches from previous studies and our proposed personalized zero-shot ensemble classifiers. Metrics such as Accuracy, Specificity, Precision, Recall, and F1-Score are presented.


| **Method** | **Accuracy** | **Specificity** | **Precision** | **Recall** | **F1-Score** |
| :-- | :-- | :-- | :-- | :-- | :-- |
| **CNN** |  |  |  |  |  |
| Kiranyaz *et al.* | 0.959 | 0.971 | 0.842 | 0.888 | 0.864 |
| Zhai *et al.* | 0.968 | 0.976 | 0.879 | 0.920 | 0.899 |
| Li *et al.* | 0.920 | 0.918 | 0.628 | 0.933 | 0.751 |
| **SR-based|  |  |  |  |  |
| SAE-based | 0.947 | 0.968 | 0.779 | 0.794 | 0.786 |
| NPE-based (ours) | 0.947 | 0.968 | 0.779 | 0.800 | 0.790 |
| **CNN|  |  |  |  |  |
| ABS[^9] | 0.977 | **0.995** | 0.956 | 0.825 | 0.886 |
| Baseline (ours) | 0.965 | 0.987 | 0.899 | 0.809 | 0.852 |
| Domain Adaptation (ours) | **0.990** | 0.991 | **0.940** | **0.987** | **0.963** |
| Ensemble (ours) | **0.990** | 0.991 | 0.939 | 0.983 | 0.961 |
| Ensemble (avg.) (ours) | 0.988 | 0.990 | 0.933 | 0.979 | 0.955 |

---



---

## 📚 Documentation

For detailed methodology and experimental results, refer to the `DL_LAB_REPORT.pdf`.
