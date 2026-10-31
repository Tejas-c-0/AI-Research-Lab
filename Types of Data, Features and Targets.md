# Day 5 — Types of Data, Features and Targets

## 1. What are Data Types?
Data types describe what kind of information is stored in a dataset.

Two common types are:

- **Numerical Data:** Information represented using numbers.
- **Categorical Data:** Information represented using groups or categories.

## 2. Numerical Data
Numerical data contains measurable or countable values.

Examples:
- Age: 20
- Marks: 85
- Salary: 25,000
- Temperature: 32.5°C

## 3. Categorical Data
Categorical data represents labels or groups.

Examples:
- City: Bangalore, Mumbai, Chennai
- Department: CSE, ECE, AIML
- Grade: A, B, C

## 4. What are Features and Targets?

In a dataset:

- **Features:** Input information given to a machine learning model to help it make a prediction.
- **Target:** The actual value that we want the model to predict.

### Example 1: Student Marks Prediction

| Study Hours | Previous Marks | Attendance | Final Marks |
|---:|---:|---:|---:|
| 2 | 65 | 80% | 70 |
| 4 | 75 | 90% | 82 |
| 6 | 85 | 95% | 92 |

- Study Hours → Feature
- Previous Marks → Feature
- Attendance → Feature
- Final Marks → Target

The model learns patterns from these examples and predicts final marks for a new student.

## 5. Example 2: House Price Prediction

| Area (sq. ft.) | Bedrooms | Bathrooms | Location | House Price |
|---:|---:|---:|---|---:|
| 1000 | 2 | 1 | Bangalore | 40 lakh |
| 1500 | 3 | 2 | Mumbai | 60 lakh |
| 1200 | 2 | 2 | Chennai | 50 lakh |

**Features:**
- Area
- Number of bedrooms
- Number of bathrooms
- Location

**Target:**
- House Price

The model uses the features to learn how house prices vary and predicts the price of a new house.

## 6. How Features and Targets Work

Features → Machine Learning Model → Predicted Target

During training, the model learns using examples with known target values.

During prediction, we provide new features, and the model estimates the target.

## 7. Why Do We Need to Understand Data Types?

Understanding data types helps us:
- Organise datasets.
- Identify numerical and categorical information.
- Identify features and targets.
- Prepare data for machine learning.

## Important Points to Remember

- Numerical data = Numbers.
- Categorical data = Labels or groups.
- Features = Input information.
- Target = Value we want to predict.
- A target contains actual values during training; the trained model predicts values for new examples.