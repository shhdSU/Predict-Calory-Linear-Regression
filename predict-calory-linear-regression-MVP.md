# Calory Prediction Using Linear Regression MVP
## Objective
The objective of this project is predicting food calories based on some nutritions such as: Carbohydrates, Cholesterol, and Sodiums.
## Preprocessing 
First, we scraped [Trader Joe's](traderjoes.com/home) and [Sprouts](https://www.sprouts.com/) groceries websites for data collecting, then apply EDA by dropping unnecessary columns that contain a lot of null values and combining some of them. As a result,  we were able to reduce the number of columns from approximately 43 to 14 columns.
## Findings
After obtaining the correlations between features and target, we present them in the below heatmap

<img src = 'https://github.com/shhdSU/Predict-Calory-Linear-Regression/blob/main/Images/MVP%20Heatmap.png'  width="660" height="600" />

As shown above, there is a high correlation between __TOTAL_FAT__ and your target(__CALORY__), which means there is a probability that our model will depend on __TOTAL_FAT__ to predict the calories.
<br/><br>
As the start step, we chose to build the __OLS__ model and train it on our features, then display the model summary as shown below

<img src = 'https://github.com/shhdSU/Predict-Calory-Linear-Regression/blob/main/Images/MVP%20OLS%20Summary.png'  width="350" height="600" />
We concluded that the OLS model gives us a high R-Square which is good! , but it indicates that we may have overfitting; and as a next step, we will check on overfitting, then due to our dataset size we will apply the Cross-Validation approach in several models in order to get accurate results.
