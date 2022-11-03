# Final-Project

##Tableau
https://public.tableau.com/app/profile/eric.blankinship/viz/HousingDataProject/Story1?publish=yes

## Slides https://docs.google.com/presentation/d/12sqbnzH5KZyljp_qEkTRjAhgdXWHzRi8D435oBrMoss/edit?usp=sharing

## Topic
Our goal is to find if we can predict a home's value based on certain features.

## Source of Data

## Questions we want to answer
We want to find what features of a home have the most impact on the price, and then find if price can be predicted.

## Data Exploration
We went through several different ideas for data. Originally used Census data, but found it difficult to find what we were looking for. After a time, we found a good csv file for homes in Kansas City. We felt there was plenty of homes in the csv to help us make predictions with machine learning. After adding it to a map in Tableau, we found that the homes were actually in Seattle, Washington. Looking more closely, we found that home prices matched the Seattle area more than Kansas City. We felt we could still use it, that it was just mislabled.

## Description of data processing

### Unsupervised Learning
- The first objective is to read and clean the data. The two things that need to happen when it comes to running an unsupervised learning model is there shouldn't be and nan's and each value type needs to be in number format. Luckily for us, our data set had 0 null values and only one column that wasn't a numerical data type. For additional data cleaning we deleted a few duplicate rows.
- The main objective of our unsupervised machine learning model was to find correlation between features then confirm their correlation with explained variance ratio.

### Supervised Learning

- We split the data into training and testing using train test split.
- Using linear regression, the initial test was run with our entire dataset which has dimensions of 21613 x 21 and our initial test yielded a variance 0f ~65%.

<img width="290" alt="Screen Shot 2022-11-01 at 7 25 02 PM" src="https://user-images.githubusercontent.com/106006911/199366478-8a89fec0-6d79-4d30-b759-5d532c42e52e.png">


- The second test the size of the feature selection was narrowed down from 21613 x 21 to 21613 x 6, by random feature selection. This random feature selection yielded a variance of ~54%.

<img width="281" alt="Screen Shot 2022-11-01 at 7 25 16 PM" src="https://user-images.githubusercontent.com/106006911/199366581-d985dc24-7fb6-4ca1-a601-c2fac896ca48.png">


- Eventually, we used a heatmap correlation to find the heaviest features in terms of weight on price. 

<img width="324" alt="featurecoorelation" src="https://user-images.githubusercontent.com/106006911/199366225-a1e581ec-2439-4955-a6c5-8e4ee9d561db.png">


- With the new features selected we were able to reach a variance of ~77%.

![image](https://user-images.githubusercontent.com/106006911/199365939-a1381b82-55ef-4996-bdfe-fff1131abcfb.png)


### Database Connection

We created an AWS instance titled "final-project" in RDS console. Next created a jupyter notebook file in which we imported our data as a csv. After making sure the data was clean, we then used sql alchemy to send the dataframe to our AWS instance in pgAdmin.


## Recommendation for future analysis
We think that in future analysis, it would be helpful to see how other factors affect home values. Originally, we wanted to see how things like crime, school ratings, unemployment rate, and other non-physical attributes affect the value. We had a tough time finding good data for these things, but with more time, think it would helpful to add to our original findings.

## What we would have done differently
