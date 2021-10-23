# Calory Predictor Linear Regression Final Report


## Abstract 
Being healthy should be part of your overall lifestyle. Living a healthy lifestyle can help prevent chronic diseases and long-term illnesses. 
The goal of this project is to predict food calories based on their nutrients using Linear Regression as a part of machine learning.

## Data Description 
We choose [Sprouts](https://www.sprouts.com/) and [Trader Joe's](https://www.traderjoes.com/home) websites to scrape their nutrients' data. Sprouts 
is a supermarket chain offers a wide selection of natural and organic foods, while Trader Joe's is a national chain of neighborhood grocery stores, 
but our target is their own grocery online store websites. The features of our dataset include the following: __TOTAL_FAT__, __SATURATED_FAT__, __TOTAL_CARBOHYDRATE__, 
__FIBER__, __SUGARS__, __PROTEIN__, __CALCIUM__, __IRON__, __POTASSIUM__, __(TOTAL_FAT+SATURATED_FAT)__, __(TOTAL_CARBOHYDRATE_SQ)__ and our target is __CALORY__. <br/>

As a result, the total columns are 12, and 1720 rows. <br/>

## Algorithms

### Models Evaluation and Selection 
We have been evaluate the data over more than 5 models using Cross-Validation approach, which are: __Linear Regression__, __Polynomial (from degree 2 until 9)__ , __Lasso__, __Ridge__, __Elastic Net__, and __Gradient Boosting Regressor__.
Accordingly, we choose __Gradient Boosting Regressor__ because it has the greatest __R<sup>2</sup>__. 


### Feature Engineering 
We tried 11 attempts to optimize the model's score, and we approved 3 of them.

1. Sum the __SATURATED_FAT__ and __TOTAL_FAT__ features as an additional feature. 
2. Drop the __SODIUM__ feature.
3. Squared the __TOTAL_CARBOHYDRATE__ as an additional feature.

### Best Model Scores
with 11 features.

#### Training
__R<sup>2</sup>__: 0.94<br/>
__MAE__ : 12.6 

#### Testing
__R<sup>2</sup>__ : 0.89<br/>
__MAE__ : 12.4 

## Tools
Here the basic tools we used in our project: <br/>
Technologies: python, and Jupyter Notebook with python libraries:

- EDA
  - pandas
  - matplotlib
  - numpy
  - seaborn
- Web Scraping
  - BeatuifulSoup
  - Selenium
- Linear Regression
  - statsmodels
  - scikit-learn

## Communication 
The provided slides, and calory predictor webpage.

## Conclusion 
We aim to improve the healthy life of people who cares and track their calories; to achieve that we used Linear Regression algorithm to predict the food calories, by training and testing our model on the extracted data.
