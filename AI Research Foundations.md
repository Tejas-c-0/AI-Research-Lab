# Day 01 — AI Research Foundations

## 1. What is AI Research?

AI research is a systematic process of investigating problems related to Artificial Intelligence, developing or testing methods, conducting experiments, analysing results, and generating new knowledge or improving existing techniques.

Example: Investigating why a machine learning model performs poorly on a small dataset.

## 2. What is a Research Problem?

A research problem is a clearly defined issue, question, or challenge that requires systematic investigation.

Example: A machine learning model achieves poor prediction accuracy when trained on a limited dataset.

Research question: How can we improve model generalization when training data is limited?

## 3. What is a Research Gap?

A research gap is an unanswered question, limitation, missing investigation, or unexplored area identified through reviewing existing research.

Example: Previous studies have investigated data augmentation on large datasets, but its effectiveness in a particular small-data setting has not been adequately studied.

## 4. What is a Hypothesis?

A hypothesis is a clear, testable prediction about the expected relationship between variables or the outcome of an experiment.

Example: Applying data augmentation to a small training dataset will improve model performance on unseen test data.

- Independent variable: Data augmentation.
- Dependent variable: Model performance.
- Prediction: Performance will improve.

## 5. What is an Experiment?

An experiment is a controlled and systematic procedure designed to test a hypothesis by changing or measuring variables, collecting results, and analysing evidence.

Example:
1. Select a dataset.
2. Split it into training, validation and test sets.
3. Train a model without data augmentation.
4. Train another model with data augmentation.
5. Compare test performance.
6. Repeat with multiple random seeds.
7. Analyse the results.

## Important Research Sequence

Problem → Literature Review → Research Gap → Hypothesis → Experiment → Analysis → Conclusion.

## Important Note

A research experiment does not need to produce a better result to be valuable. Even when a hypothesis is not supported, the findings can contribute useful knowledge.