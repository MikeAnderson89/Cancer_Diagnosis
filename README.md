# 🧬 Cancer Diagnosis: Malignant vs. Benign Tumors

## 📄 Overview

This notebook explores a supervised classification task using diagnostic data to distinguish between **malignant** and **benign** tumors. The dataset comes from [Kaggle](https://www.kaggle.com/datasets/erdemtaha/cancer-data) and includes 569 samples with 30 numerical features derived from digitized images of breast masses.

The analysis covers:
- 🔍 Exploratory data analysis
- ⚙️ Data preprocessing
- 🧪 Outlier detection with Mahalanobis distance
- 🔁 Feature transformation (Box-Cox)
- 🧠 Model training (Random Forest, Linear Regression)
- 📊 Performance evaluation

## 🧠 Objectives

- **Primary goal**: Predict whether a tumor is malignant (`1`) or benign (`0`) using structured diagnostic features.
- **Secondary tasks**: Feature transformation, anomaly detection, and exploratory unsupervised clustering.

## 📦 Features

Each sample includes:
- **Mean**, **standard error**, and **worst** values for 10 base features:
  - `radius`, `texture`, `perimeter`, `area`, `smoothness`, `compactness`, `concavity`, `concave points`, `symmetry`, `fractal dimension`
- Total of 30 continuous features
- Binary target: `diagnosis` (`M` mapped to `1`, `B` to `0`)

## 🔧 Preprocessing

- Null and redundant column removal
- Label encoding (`diagnosis`)
- Box-Cox transformations for normalization
- Mahalanobis distance for multivariate outlier detection
- Standard scaling for model readiness

## 🧪 Modeling Techniques

1. **Random Forest Classifier**
   - Baseline performance metrics: accuracy, precision, recall, F1-score
2. **Linear Regression**
   - Used here for exploratory purposes and imputation modeling
3. **K-Means Clustering**
   - Helps assess natural groupings in the data and supports subtype discovery

## 📈 Visualizations

- Distribution plots for all features
- KDE-enhanced histograms
- Cluster visualizations (when applicable)

## 📂 File Structure

- `Cancer_Diagnosis.ipynb`: Main analysis notebook
- `Cancer_Data.csv`: (Expected to be downloaded using `kagglehub`)
- Custom helper functions:
  - `boxcox_transformation_array`, `mahalanobis_outlier_removal`, etc.

## 🚀 How to Run

1. Clone this repo or download the notebook.
2. Make sure you have Kaggle credentials configured for `kagglehub`.
3. Run all cells sequentially. All dependencies are handled via standard packages:
   ```bash
   pip install numpy pandas seaborn matplotlib scikit-learn kneed kagglehub
   ```

## 📌 Notes

- Box-Cox transformations require strictly positive data, hence the `+1e-6` shift.
- Mahalanobis distance is used for robust multivariate outlier detection.
- This project can be extended for feature selection, hyperparameter tuning, or deep learning pipelines.

## 📬 Author

**Mike Anderson**  
*Principal Data Scientist | ML Specialist*  
📧 mikeanderson0289@gmail.com  
🔗 [www.mikeandersondata.com](http://www.mikeandersondata.com)
