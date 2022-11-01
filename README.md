# Online Fraud Detection
### Goal
Blossom Bank's goal is to create a machine learning model that can foresee online payment fraud.
### ProjectOverview
According to Infosecurity Magazine, fraud cost the entire economy £3.2 trillion in 2018. For some businesses, fraud losses could account for more than 10% of total costs. Such huge losses motivate companies to seek out novel strategies for preventing, detecting, and eliminating fraud. Machine learning is now the most efficient technological method for preventing financial fraud and I was able to:
- Perform exploratory data analysis in python.
- Perform feature engineering.
- Perform Model selection, training, and validation.
- Perform Model evaluation
- Give recommendations to Blossom Bank based on insights from data. 

![](https://github.com/ChristianaBolanle/Bolanle-Christiana_portfolio/blob/main/Images/pie%20chart%20online%20fraud%20detection.PNG)
![](https://github.com/ChristianaBolanle/Bolanle-Christiana_portfolio/blob/main/Images/Heat%20map%20Online%20Fraud%20Detection.PNG)

This Readme section is to walk you through my codes and processes and will be useful to Data Analysts and Scientist. For the Stakeholder's report and insights, check the Stakeholders Report PDF or watch the presentation https://www.canva.com/design/DAFQbtCFOFs/GxAJ3rSMa5zVykcX12s5sw/view?utm_content=DAFQbtCFOFs&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton The dataset used was provided by Blossom Bank, a UK based bank. The transactional data set contained 10 columns and 1,048,575 rows.

## METHODOLOGY
1. Cleaning the data by removing unnecessary rows or/and columns, conducting exploratory data analysis, obtaining the pertinent insights, and presenting the data set using the best visualisation charts are the next steps.
2. By encoding categorical variables, feature engineering is being performed. This suggests that important category columns need be converted into numerical columns in order to be included or used in the machine learning model.
3. Performed model deployment and selection. To help the bank prevent losing money to fraud, it is necessary to interpret the modelling results, identify the model that fits the data the best and is realistic in post-production, and then offer business strategies.

## Data Cleaning and Exploratory Data Analysis
This project was conducted using Jupyter Notebook. I found no missing cell(s) and that the datatypes (columns) were of the required type after loading the requisite libraries. I then performed exploratory data analysis, gaining pertinent insights as I went along generating the appropriate visualisation charts. The data was then displayed using pairplots, heatmaps, pie charts, distribution charts, boxplots, histograms, and box plots. For more technical information. please consult the jupyter Notebook file, and for business summary and recommendations, please consult the Stakeholders report file.
## Feature Engineering
Due to my observation that categorical columns would not be processed during the deployment of the models, I decided to change them to numerical values (encoding). The 'nameOrg' and 'nameDest' columns were eliminated because they played no significant role in our models, and I encoded the 'type' column by creating dummy columns.

## Results and Model Evaluation
I used the Linear Regression, Random Forest, and Decision Tree supervised machine learning models for classification and regression. The Random Forest model was the most effective at identifying fraudulent transactions. Additionally, the confusion matrix revealed that it had the best post-production outcome;
- Random Forest performed exclusively well on the dataset, the accuracy is 99% which is similar to Decision Tree.
- Both Recall and Precision are also very good, **Recall** is 81% on test data which means that we don't have a large amount of False Positives.
- **Precision** on the testing data is ~98%, which means that we only have about 2% of False Positives. This is great, because as a company, we want to avoid predicting fraudulent transactions that will later turn out to be non-fraudulent.
- **Accuracy** on the testing data is ~99.97% which means that the model correctly predicts almost 5/5 of the transactions.This means that we will not miss out on any potential non-fraudulent transaction.
- **F1 Score**: The F1 score on the testing data is ~87%, which is great since it takes into account both False Positives and False Negatives.
The Random Forest Model is obviously the best model out of the 3.The heatmap shows the details of predicting fraudulent transactions with the Random Forest Model.While 294 transactions were actually fraudulent as predicted (True positive TP), 65 transactions were actually fraudulent even with the fact that it was predicted to be non-fraudulent (False negative FN). 5 transactions were actually non-fraudulent even when it was predicted to be fraudulent(False positive FP). 314148 transactions were actually non-fraudulent as predicted (True negative TN). In relation to accuracy, Random Forest Model is the most accurate.
