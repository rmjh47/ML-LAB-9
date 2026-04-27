# ML-LAB-9
# Lending Club Loan Default Prediction

This project explores publicly available data from **LendingClub.com** to predict whether a borrower will pay back their loan in full. It compares the performance of a single **Decision Tree** against a **Random Forest Classifier**.

## Dataset
The dataset contains lending data from 2007-2010. Key features include:
* **credit.policy**: Whether the customer meets underwriting criteria.
* **purpose**: The reason for the loan (debt consolidation, credit card, etc.).
* **fico**: The FICO credit score of the borrower.
* **not.fully.paid**: The target variable (1 if the loan was not repaid).

## Project Workflow
1. **EDA**: Visualized FICO distributions and loan purposes using Seaborn.
2. **Preprocessing**: Converted categorical features into dummy variables.
3. **Modeling**: Trained both a `DecisionTreeClassifier` and a `RandomForestClassifier` (600 estimators).

## Results

| Model | Accuracy | Class 1 Recall |
| :--- | :--- | :--- |
| **Decision Tree** | ~73% | ~0.23 |
| **Random Forest** | ~85% | ~0.02 |

### Conclusion
The **Random Forest** performed better in terms of overall accuracy. However, the **Decision Tree** was more effective at identifying risky borrowers (higher recall for the "not fully paid" class), whereas the Random Forest was very conservative and missed most defaults.
