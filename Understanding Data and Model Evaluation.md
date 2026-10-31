# Day 4 — Understanding Data and Model Evaluation

## 1. What is Data?
Data is a collection of facts or information.

Examples: Names, ages, marks, prices and temperatures.

## 2. What is a Dataset?
A dataset is an organised collection of data, usually arranged in a table.

## 3. Rows and Columns
- **Row:** One record or one example.
- **Column:** One type of information about the records.

### Example

| Student | Age | Marks |
|---|---:|---:|
| Asha | 19 | 85 |
| Ravi | 20 | 72 |
| Maya | 18 | 91 |

- Each student represents one row.
- Student, Age and Marks are columns.
- The complete table is a dataset.

## 4. Why is Data Important?
Machine learning models learn patterns from data.

If data is incorrect, incomplete or unsuitable, the model may produce poor results.

## 5. What is Model Evaluation?
Model evaluation is the process of checking how well a trained model performs.

### Why do we evaluate models?
- To measure model performance.
- To identify weaknesses.
- To compare different models.
- To check performance on unseen data.

## 6. Training vs Testing

- **Training data:** Data used to teach the model.
- **Testing data:** Data used to check the model's performance on unseen examples.

### Basic workflow

Dataset → Training Data → Model Training → Testing Data → Evaluation

## 7. Common Evaluation Metrics

| Metric | Meaning |
|---|---|
| MAE | Average absolute prediction error |
| MSE | Average squared prediction error |
| RMSE | Square root of MSE |
| R² | Measures how well a regression model explains variation in the target |

## 8. Model Comparison
Model comparison means testing different models and comparing their performance using the same evaluation process.

Examples:
- Linear Regression
- Decision Tree
- Random Forest

## 9. Understanding Model Performance

| Training Accuracy | Testing Accuracy | Possible Problem |
|---|---|---|
| 98% | 55% | Overfitting |
| 45% | 42% | Underfitting |
| 90% | 88% | Good generalization |

- **Overfitting:** The model learns the training data too specifically and performs poorly on unseen data.
- **Underfitting:** The model fails to learn important patterns, even from training data.
- **Good generalization:** The model performs well on both training and unseen data.

## 10. Research Flow

Problem → Dataset → Training → Testing → Evaluation → Comparison → Conclusion

## Practice Questions

1. What is data?
2. What is a dataset?
3. What is the difference between rows and columns?
4. What is the difference between training and testing data?
5. Why do we evaluate machine learning models?
6. Name four common evaluation metrics.
7. What is model comparison?
8. What is the difference between overfitting and underfitting?
9. A model has 98% training accuracy and 55% testing accuracy. What might be the problem?

