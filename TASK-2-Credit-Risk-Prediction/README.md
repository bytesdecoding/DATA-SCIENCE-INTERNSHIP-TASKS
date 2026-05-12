# Task 2: Credit Risk Prediction
# Credit Risk Prediction using Machine Learning

## Project Overview
This project predicts whether a loan applicant is likely to be approved or default based on applicant details such as income, education, loan amount, and credit history.

The project was developed using Python in Google Colab and implements a machine learning classification model for credit risk prediction.

---

## Objective
The main objective of this project is to:

- Analyze loan applicant data
- Handle missing values in the dataset
- Perform Exploratory Data Analysis (EDA)
- Train a machine learning classification model
- Predict loan approval status
- Evaluate model performance using accuracy and confusion matrix

---

## Dataset
Dataset used: Loan Prediction Dataset from Kaggle

Dataset Link:
https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset

File used:
- `train_u6lujuX_CVtuZ9i.csv`

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Machine Learning Model

The following classification model was used:

- Logistic Regression

---

## Project Workflow

1. Data Collection
2. Data Cleaning
3. Handling Missing Values
4. Exploratory Data Analysis (EDA)
5. Label Encoding
6. Train-Test Split
7. Model Training
8. Prediction
9. Model Evaluation

---

## Data Preprocessing

Missing values were handled using:

- Mean for numerical columns
- Mode for categorical columns

Categorical variables were converted into numerical format using Label Encoding.

---

## Exploratory Data Analysis

The following visualizations were created:

- Loan Amount Distribution
- Applicant Income Distribution
- Education Count Plot

These visualizations helped understand the dataset patterns and feature distributions.

---

## Model Evaluation

The model performance was evaluated using:

- Accuracy Score
- Confusion Matrix
- Classification Report

### Model Accuracy
- Accuracy Achieved: **78.86%**

---

## Results

The Logistic Regression model performed well in predicting loan approval status and achieved good classification accuracy on the testing dataset.

---

## How to Run the Project

1. Open the notebook in Google Colab
2. Upload the dataset file
3. Run all cells sequentially
4. View predictions and evaluation results

---

## Project Structure

```text
Credit-Risk-Prediction/
│
├── Credit_Risk_Prediction.ipynb
├── README.md
└── train_u6lujuX_CVtuZ9i.csv

## Future Improvements

- Improve model accuracy
- Use more machine learning models
- Deploy as a web application

## Author

Ayesha

---

## License

This project is developed for educational purposes.
