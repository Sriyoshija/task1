# Task1 Data Cleaning and Preprocessing
When creating this code, I focused on transforming the raw **Titanic dataset** into a clean, structured format suitable for machine learning.
I followed these steps:

1. Load Data and Spot Missing Values:
I imported the necessary tools: pandas for data analysis, numpy for numerical work, and seaborn/matplotlib for visualizations.
After loading the Titanic dataset from the CSV file into a DataFrame called df, I printed the Total Number of passengers and the list of missing values in each column.

2. Clean Up Missing Data:
Ages: Filled out empty age slots with the median age (28) to avoid skewed results.
Cabins: I deleted the entire Cabin column because most data was missing.
Embarked: For the 2 missing boarding ports, I used "S" (Southampton), the most common port.

3. Feature Engineering & Encoding:
I created a binary 'IsFemale' column from 'Sex' (1 for female, 0 for male) and dropped the original 'Sex' column to reduce redundancy. For 'Embarked', I used one-hot encoding to create Port_C, Port_Q, and Port_S columns, avoiding ordinal bias between ports.  

4. Feature Scaling: 
I standardized Age and Fare using StandardScaler to ensure equal weight in ML models. This transforms values to have a mean of 0 and standard deviation of 1.  

5. Drop Unnecessary Columns: 
I removed PassengerId, Name, and Ticket —these identifiers and text-based features lack predictive value for survival analysis.  

6. Data Visualization (Correlation Heatmap): 
Generated a heatmap to visualize feature correlations, highlighting relationships like higher fares correlating with survival.  

7. Final Data Check:  
At final I have printed the cleaned dataset’s dimensions and displayed sample rows to confirm readiness for modeling.
