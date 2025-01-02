This script is designed to predict customer churn using a machine learning model, with steps for importing, preprocessing, training, and analyzing data. The results are saved in a format that can be imported into Power BI for visualization and business insights. Below is a concise description of the process:

Steps and what they mean

1.	Library Importation:
- Imported essential Python libraries for data handling (pandas, numpy), visualization (matplotlib, seaborn), machine learning (scikit-learn), and model persistence (joblib).
2.	Data Importation:
- 	Loaded customer data from an Excel file using the pandas library. Data was read from a specified sheet (vw_ChurnData) into a DataFrame.
3.	Data Preprocessing:
-	Dropped irrelevant columns such as Customer_ID and other fields not useful for modeling.
- 	Encoded categorical variables using LabelEncoder to convert them into numeric values for the machine learning algorithm.
-	Manually mapped the target variable (Customer_Status) into binary values: 0 for "Stayed" and 1 for "Churned."
4.	Data Splitting:
-	Split the data into training (80%) and testing (20%) sets to train and evaluate the model.
5.	Model Training:
-	Trained a Random Forest Classifier using the training dataset. This algorithm is well-suited for handling both categorical and numerical data and accounts for feature importance.
6.	Model Evaluation:
-	Evaluated the trained model on the test data using metrics like confusion matrix, accuracy score, and classification report to measure its predictive performance.
7.	Feature Importance:
-	Analyzed and visualized the importance of individual features using the trained Random Forest model to understand which variables most influence churn predictions.
8.	New Predictions:
-	Imported additional customer data from another Excel sheet (vw_JoinData) for prediction.
-	Encoded this data in the same format as the training set, ensuring consistency.
-	Used the trained model to predict churn probabilities for new data and added predictions to the original dataset.
9.	Export Results:
-	Filtered churned customers and saved the results as a CSV file (Prediction Data.csv). This file can be imported into Power BI.
Integration with Power BI
1.	Data Import:
-	The processed dataset and churn predictions were saved as CSV files, which were imported into Power BI using the data import feature.
-	Power BI allows linking these CSVs for dynamic visualization and analysis.
2.	Visualization:
-	Churn analysis results, including feature importance and predicted outcomes, were visualized in Power BI.
-	Charts, graphs, and dashboards were created to provide actionable insights into customer behavior and churn patterns.
3.	Usage for Business Insights:
-	The predictions helped identify at-risk customers, enabling the business to implement targeted retention strategies.
-	Visualizations highlighted key factors contributing to churn, guiding operational improvements.
This end-to-end process integrates machine learning with business intelligence, offering a robust solution for predictive analytics and decision-making.

