# Customer Purchase Prediction Using Machine Learning

## Project Overview

This project uses Machine Learning classification algorithms to predict whether a customer is likely to purchase a product based on their age and estimated salary.

The project compares three classification models and evaluates their performance using multiple evaluation metrics.

## Objectives

- Explore and analyze customer data.
- Check data quality and identify potential outliers.
- Train and compare different Machine Learning models.
- Evaluate model performance using classification metrics.
- Identify the best-performing model based on the F1-score.

## Dataset

The project uses the Social Network Ads dataset.

- **Number of records:** 400
- **Number of columns:** 5
- **Input features:** Age and Estimated Salary
- **Target variable:** Purchased

### Dataset Features

| Feature | Description |
|---|---|
| User ID | Unique customer identifier |
| Gender | Customer gender |
| Age | Customer age |
| EstimatedSalary | Estimated customer salary |
| Purchased | Whether the customer purchased the product (0 or 1) |

The `User ID` column is excluded from model training. The initial experiments use `Age` and `EstimatedSalary` as input features.

## Data Preparation

The following steps were performed:

- Checked for missing values.
- Checked for duplicate rows.
- Inspected data types and feature distributions.
- Checked age and salary values for potential issues.
- Detected potential outliers using the Interquartile Range (IQR) method.
- Split the data into training and testing sets.
- Scaled numerical features for model training.

The dataset contained no missing values or exact duplicate rows in the initial checks. The IQR method did not identify potential outliers in the age or salary features.

## Machine Learning Models

Three classification algorithms were trained and compared:

1. Logistic Regression
2. Decision Tree
3. Random Forest

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

### Results

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Random Forest | 0.910 | 0.865 | 0.889 | 0.877 | 0.930 |
| Decision Tree | 0.890 | 0.821 | 0.889 | 0.853 | 0.939 |
| Logistic Regression | 0.840 | 0.857 | 0.667 | 0.750 | 0.910 |

*Results are based on the current experiment and test split.*

## Best Model

Random Forest achieved the highest accuracy (91%) and the highest F1-score (87.7%) among the three models in this experiment.

Decision Tree achieved the highest ROC-AUC score (93.9%).

Random Forest is therefore the best model according to the F1-score in this experiment, while the final model choice depends on the evaluation metric and the project's objectives.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- Jupyter Notebook

## How to Run the Project

1. Download or clone this repository.
2. Open the notebook `machine-learning-customer-purchase-prediction.ipynb` in Google Colab or Jupyter Notebook.
3. Run the notebook cells in order.
4. Ensure the dataset is accessible when executing the data-loading cell.

## Limitations

- The dataset contains only 400 records.
- The model uses only age and estimated salary as input features.
- Results may differ with other training/testing splits or new customer data.
- These experimental results do not guarantee real-world purchasing behavior.

## Author

**Hayet Mecegguem**

Computer Science Graduate | Master's Student in Artificial Intelligence

Interested in Machine Learning, Data Analysis, and Artificial Intelligence.
