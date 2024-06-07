
# Breast Cancer Detection and Classification Using Ultrasound Images & Classic Machine Learning Algorithms

This repository contains the project developed by Systems and Biomedical engineering students for the Introduction to Machine Learning Course 2024. The project involves predicting and classifying breast cancer using ultrasound images, employing three distinct approaches: Gradient Boosting, AdaBoost, and a Radiomics-based approach.

## Team Members
- Abdallah Magdy
- Muhammad Alaa
- Nouran Mahmoud
- Omar Emad

## Project Overview
Breast cancer is a critical health issue worldwide, and early detection is crucial for improving patient outcomes. This project explores the application of classic machine learning algorithms to classify ultrasound images of breast tissue as normal, benign, or malignant.

### Approaches
1. **Gradient Boosting**: Achieved F1 scores of 0.87 (Normal vs. Cancerous) and 0.902 (Benign vs. Malignant).
2. **AdaBoost**: Achieved F1 scores of 0.84 (Normal vs. Cancerous) and 0.85 (Benign vs. Malignant).
3. **Radiomics-Based Classification**: Achieved an F1 score of 0.922 (Benign vs. Malignant) by extracting and selecting significant features from the images.

## Dataset
The dataset used is the "Breast Ultrasound Images Dataset (BUSI)", which consists of 780 images categorized into three classes: Normal, Benign, and Malignant. This dataset includes images along with segmentation masks for benign and malignant tumors.

## Methods and Experiments
### Data Preprocessing
- **Labeling and Data Loading**: Images were organized into directories and labeled accordingly.
- **Undersampling**: Performed to balance the dataset, with 133 images for each class.
- **Data Splitting**: 90% of data was used for training and 10% for testing.
- **Normalization**: Pixel values normalized to the range [0, 1].
- **Resolution**: Images resized to 64x64 pixels.

### Models
1. **Gradient Boosting Classifier**: Built using weak learners (decision trees), optimizing with grid search or Optuna auto tuner.
2. **AdaBoost Classifier**: Used Logistic Regression as the weak learner, with hyperparameter tuning using Optuna.
3. **Radiomics-Based Approach**: Extracted shape, texture, and edge features, employing Recursive Feature Elimination (RFE) and SMOTE for feature selection and class balancing.

## Results
- **Gradient Boosting**: Achieved robust performance with notable F1 scores.
- **AdaBoost**: Demonstrated excellent discriminative ability.
- **Radiomics-Based Approach**: Provided the highest F1 score, showcasing the potential of feature extraction and selection methods.

## Conclusion
The findings of this project highlight the effectiveness of classic machine learning algorithms in breast cancer detection using ultrasound images. Each approach has its strengths and can be further optimized for better performance.

## Repository Structure
- `notebooks/`: Contains Jupyter notebooks for each approach.
  - `adaptive-boosting-approach.ipynb`
  - `gradient-boosting-approach.ipynb`
  - `radiomics-based-approach.ipynb`
- `report/`: Contains the project report.
- `README.md`: Project overview and instructions.

## How to Use
1. **Clone the repository**:
   ```sh
   git clone https://github.com/OmarEmad101/breast-cancer-detection.git
   cd breast-cancer-detection

2. **Install dependencies**:
   ```sh
   pip install -r requirements.txt

3. **Run the notebooks**: Open the Jupyter notebooks in the `notebooks/` directory to explore the different approaches.

## References
- [Breast Ultrasound Images Dataset (BUSI)](https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset)
