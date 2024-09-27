# COVID-19 Outcome Prediction

This project aims to predict whether a person will recover or not from COVID-19 symptoms based on pre-defined standard symptoms, following guidelines given by the World Health Organization (WHO).

## Project Overview

The dataset used contains daily-level information on the number of affected cases, deaths, and recoveries from the novel coronavirus, available from January 22, 2020. This is a time-series dataset, and the number of cases on any given day is cumulative.

### Key Features
- **Country**: Where the person resides.
- **Location**: The specific region within the country.
- **Age**: The age group classification, based on WHO standards.
- **Gender**: Male or Female.
- **Visited Wuhan**: Whether the person visited Wuhan, China.
- **From Wuhan**: Whether the person is from Wuhan, China.
- **Symptoms**: Six coded fields for different symptom families.
- **Time Before Symptoms Appear**
- **Result**: Recovery (0) or Death (1).

## Required Classifiers
The following classifiers were used in this project:
1. **K-Nearest Neighbors (KNN)**
2. **Logistic Regression**
3. **Naive Bayes**
4. **Decision Trees**
5. **Support Vector Machines (SVM)**

Each classifier was evaluated based on various metrics, including precision, recall, F1-score, and ROC/AUC curves.

## Installation

To run this project, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/COVID-19-outcome-prediction.git
    ```

2. Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the dataset (`data.csv`) and place it in the root folder.

## Usage

1. Open the Jupyter Notebook or Colab Notebook for the classifier you want to test.
2. Follow the notebook steps:
   - Import Libraries
   - Load the dataset
   - Split the dataset into Training, Validation, and Testing sets.
   - Train the model using the training set.
   - Tune hyperparameters using Grid Search.
   - Evaluate the model using various metrics.

## Findings

- **K-Nearest Neighbors**: Achieved its best result with `K=3`. The training and testing data metrics align well.
- **Logistic Regression**: Performed well in both training and testing, especially in accuracy and recall, but precision and F1 scores were lower for class 1.
- **Naive Bayes**: This model struggled due to the assumption of feature independence, making it unsuitable for this problem.
- **Decision Trees**: Achieved high accuracy but showed a tendency to overfit.
- **Support Vector Machines**: Considered the best-performing model, with a test accuracy of 95%.

## Conclusion

SVM and Decision Trees were the top-performing classifiers, with SVM being the most reliable due to its resistance to overfitting. KNN and Logistic Regression also performed adequately, while Naive Bayes was not suitable for this problem.
