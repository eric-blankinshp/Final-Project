
Unserpervised Learning 

- The first objective is to read and clean the data. The two things that need to happen when it comes to running an unserpervised learning model is there shouldn't be and nan's and each value type needs to be in number format. 
	Luckily for us, our data set had 0 null values and only one column that wasn't a numerical data type. For additional data cleaning we deleted a few duplicate rows. 

- The main objective of our unserpervised machine learning model was to find coorelation between features then confirm their coorelation with explained variance ratio. 
	
	The initial test was run with our entire dataset which has dimensions of 21613 x 21 and our initial test yeilded a variance below 50%. 
	The second test the size of the feature selection was narrowed down from 21613 x 21 to 21613 x 6, by random feature selection. This random feature selection yeilded a variance of 63%.
	Eventually, we used a heatmap coorelation to find the heaviest features in terms of weight on price. With the new features selected we were able to capture 86% of our original data. 

With the feature selection, we were now in a position to start using our predictive model.  
	

	
















Prediction Model Notes 

Supervised learning deals with labeled data. 
	An example of supervised learning might be to predict, based on data from previous patients, whether a new patient has diabetes.

Regression is used to predict continuous variables.

