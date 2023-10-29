# Book Weight Prediction Project

## Table of Contents
1. [Introduction](#Introduction)
2. [Summary of the Dataset](#Summary-of-the-Dataset)
3. [Machine Learning Pipeline](#Machine-Learning-Pipeline)
4. [Results](#Results)


## Introduction
This project aims to predict the weight of books into 3 categories: Light, Normal, and Heavy. The model serves various purposes such as shipping optimization, inventory management, and customer recommendations.

## Summary of the Dataset
### Columns: 
The dataset contains 28 columns, each with varying data types—object, float64, and int64.

- **Object columns**: authors, categories, description, edition, etc.
- **Float64 columns**: bestsellers-rank, dimension-x, dimension-y, etc.
- **Int64 columns**: id, isbn13, etc.

### Null Values:
- `bestsellers-rank`, `description`, and `dimension-x` have notable null values.
- `edition`, `index-date`, and `publication-place` are almost entirely null.

## Machine Learning Pipeline

### Data Preprocessing
We've managed missing values with strategic imputations and handled categorical variables using encoding techniques. Outliers were identified and appropriately dealt with to ensure they did not skew the model.

### Feature Transformation
Our pipeline includes steps for feature selection, reducing dimensionality where necessary, and transforming text data via text vectorization methods such as TF-IDF.

### Classification Model
The core of this project is a Logistic Regression model designed to predict the weight of a book into 5 classes: Very Light, Light, Average, Heavy, Very Heavy.

### Hyperparameter Tuning
We've employed a rigorous grid search to identify the best hyperparameters for our model, ensuring it performs optimally for the task at hand.

### Evaluation
The model is evaluated using various metrics, but we focus on the Accuracy and Confusion Matrix to gauge its performance. 

## Results

### Model Used
For this project, the classification model used is Logistic Regression.

### Accuracy
Our model achieved an overall accuracy of 66%.

### Confusion Matrix
The confusion matrix helps us to understand the classification performance of the model in detail. Below is the confusion matrix for the model's predictions:

| Actual\Predicted | Light   | Normal |  Heavy  | 
|------------------|---------|--------|---------|
| Light            |  3058   |  2494  |   76    |   
| Normal           |   896   |  8165  |  452    |   
| Heavy            |   53    |  2769  |  2037   |   

Each cell in this table represents the number of samples for the corresponding class. For example, there were 3058 instances where both the actual and predicted class was "Light".

