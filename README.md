# Final-Project

## Topic
Our goal is to find if we can predict a home's value based on certain features.

## Source of Data

## Questions we want to answer
We want to find what features of a home have the most impact on the price.

## Description of data preprocessing

### Unsupervised Learning

- The first objective is to read and clean the data. The two things that need to happen when it comes to running an unsupervised learning model is there shouldn't be and nan's and each value type needs to be in number format.
	Luckily for us, our data set had 0 null values and only one column that wasn't a numerical data type. For additional data cleaning we deleted a few duplicate rows.
- The main objective of our unsupervised machine learning model was to find correlation between features then confirm their correlation with explained variance ratio.

### Supervised Learning
 
- Using linear regression, the initial test was run with our entire dataset which has dimensions of 21613 x 21 and our initial test yielded a variance below 50%.
- The second test the size of the feature selection was narrowed down from 21613 x 21 to 21613 x 6, by random feature selection. This random feature selection yielded a variance of 63%.
- Eventually, we used a heatmap correlation to find the heaviest features in terms of weight on price. With the new features selected we were able to capture 86% of our original data.

## Recommendation for future analysis

We think that in future analysis, it would be helpful to see how other factors affect home values. Originaly we wanted to see how things like crime, school ratings, unemployment rate, and other non-physical attributes affect the value. We had a tough time finding good data for these things, but with more time, think it would helpful to add to our original findings.

## What we would have done differently


