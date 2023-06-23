# Case-studay_Lead-Scoring-Assignment

Summary

The model building and prediction is being done for company X Education and to find ways to convert potential users. We will further understand and validate the data to reach a conclusion to target the correct group and increase conversion rate. Let us discuss steps followed:

1.	EDA:
•	Quick check was done on % of null value and we dropped columns with more than 30% missing values.
•	We also saw that the rows with the null value would cost us a lot of data and they were important columns. So, instead we replaced the NaN values with 'not provided'. 
•	Since India was the most common occurrence among the non-missing values, we imputed all not provided values with India.
•	We also worked on numerical variable, outliers and dummy variables.


2.	Train-Test split & Scaling : 

•	The split was done at 70% and 30% for train and test data respectively. 
•	We have done min-max scaling on the variables (TotalVisits,' 'Total Time Spent on Website,' and 'Page Views Per Visit')l

3.	Model Building 

•	RFE was used for feature selection.
•	Then RFE was done to attain the top 15 relevant variables. 
•	Later the rest of the variables were removed manually depending on the VIF values and p-value.
•	A confusion matrix was created, and overall accuracy was checked which came out to be almost 80%1%.

4.	Model Evaluation

•	Sensitivity – Specificity

If we go with Sensitivity- Specificity Evaluation. We will get :

	On Training Data

o	The optimum cut off value was found using ROC curve. The area under ROC curve was 0.87.
o	After Plotting we found that optimum cutoff was 0.42 which gave 

Accuracy 79%
        Sensitivity 79.65%
        Specificity 78.53%. 

	Prediction on Test Data

o	We get 

Accuracy 78.93%
Sensitivity 78.53%
Specificity 79.30%


•	Precision – Recall: 
                                     
                                If we go with Precision – Recall Evaluation 

	On Training Data

o	With the cutoff of 0.35 we get the Precision & Recall of 79.29% & 70.22% respectively.
o	So to increase the above percentage we need to change the cut off value. After plotting we found the optimum cut off value of 0.44 which gave 

Accuracy 81.80%
Precision 75.71%
Recall 76.32%

	Prediction on Test Data

o	We get 

Accuracy 80.57%
Precision 74.87%
Recall 73.26%

5.	So if we go with Sensitivity-Specificity Evaluation the optimal cut off value would be 0.42
&
If we go with Precision – Recall Evaluation the optimal cut off value would be 0.042


CONCLUSION

TOP VARIABLE CONTRIBUTING TO CONVERSION:
•	LEAD SOURCE:
o	Total Visits
o	Total Time Spent on Website
•	Lead Origin: 
o	Lead Add Form
•	Lead source: 
o	Direct traffic 
o	Google 
o	Welingak website
o	Organic search 
o	Referral Sites
Last Activity:
•	Do Not Email_Yes
•	Last Activity_Email Bounced
•	 Olark chat conversation


The Model seems to predict the Conversion Rate very well and we should be able to give the Company confidence in making good calls based on this model.
