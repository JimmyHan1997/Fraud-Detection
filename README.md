# Fraud-Detection
Jimmy Han COMP647

## Dataset
This project uses the Kaggle [Credit Card Fraud Detection dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud).
Please download `creditcard.csv` from Kaggle and place it in the repository root folder before running the code.

## Steps Implemented
1. **Data Preprocessing**
   - (a) *Cleaning*: removed duplicate rows.  
   - (b) *Missing data*: applied median imputation (though the dataset has no missing values).  
   - (c) *Outliers*: clipped the `Amount` feature at the 1st and 99th percentiles.  

2. **Exploratory Data Analysis (EDA)**
   - Visualized distribution of transaction amounts.  
   - Checked class imbalance (fraud vs non-fraud).  
   - Simple correlation exploration.  

3. **Decision Tree Model**
   - Used `DecisionTreeClassifier(max_depth=5, class_weight="balanced")`.  
   - Trained on 80% of the dataset, tested on 20%.  
   - Balanced class weights to handle severe fraud/non-fraud imbalance.  

4. **Evaluation**
   - Printed classification report and confusion matrix.  
   - Computed ROC-AUC.  
   - Plotted ROC curve.  
   - Visualized top levels of the decision tree.  
