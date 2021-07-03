# Company-Potential-leads
Leads which can be used by the company to target potential leads



Approach followed:
1.Importing important libraries.

2.Load and over look on the Data given
  a.	Shape of the dataset
  b.	Inspect the different columns in the dataset
  c.	Check the info to see the types of the feature variables and the null values present
  d.	summary and dtypes in the dataset.

3. Data Cleaning:
  a.	First step to clean the dataset, i removed the redundant variables/features.
  b.	After removing the redundant columns, i found that some columns had label as ‘Select’ which means the customer has chosen not to answer this question. The ideal value to replace this label would be null value as the customer has not opted any option. Hence,i changed those labels from ‘Select’ to null values.
  c.	Removed columns which had more than 45% missing values
  d.	For remaining missing values, i have imputed values with maximum number of occurrences for a column.
  e.	Discovered one column is has two identical label names in different format (capital letter and small letter). i fixed this issue by changes the labels names into one format.

4. Data Transformation:
  a.	Mapped 0 and 1 to yes and no variables.
  b.	Changed the multicategory labels into dummy variables and binary variables into ‘0’ and ‘1’.
  c.	Checked the outliers and created bins for them.
  d.	Removed all the redundant and repeated columns.

5. Data Preparation:
  a.	Split the dataset into train and test dataset and scaled the dataset.
  b.	Ploted a heatmap to check the correlations among the variables.



6. Model Building and testing the model:
  a.	I built the model with rfe count 15 and manually compared the model evaluation with respect to P values and VIF values and choose our final model with 10 variables as has more stability and accuracy than the other.
  b.	For the final model I checked the optimal probability cut-offs by finding points and checking the accuracy, sensitivity and specificity.
  c.  Found one convergent points and we chose that point for cut-offs and predicted our final outcomes.
  d.	Checked the precision and recall with accuracy, sensitivity and specificity for our final model and the trade-offs.
  e.	Prediction made now in test set and predicted value was recoded.
  f.	Model evaluation on the test set by checking the accuracy, recall/sensitivity 
  g.	I found the score of accuracy and sensitivity from our final test model is within acceptable range.
  h.	Gave lead score to the test dataset for indication that high lead score are hot leads and low lead score are not hot leads.

7. Conclusion:
Learning gathered are below:
  a.	Test set is having accuracy, recall/sensitivity in an acceptable range.
  b.	In business terms, This model is has stability and accuracy with adaptive environment skills. Means it will adjust with the company’s requirement changes made in coming future.
  c.	Top features for good conversion rate:
    1.Tags_Lost to EINS
    2.Tags_Closed by Horizzon
    3.Total Time Spent on Website
  d.	Top 3 variables that need improvement to convert a lead are:
    1.	Lead Source_Welingak website
    2.	Last Notable Activity_Had a Phone Conversation
    3.	Tags_Ringing
