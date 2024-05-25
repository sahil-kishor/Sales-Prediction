# Sales-Prediction
## Predicting Sales on store chains of Rossmann Drug Stores in Europe!

## Promblem Statement:

Imagine yourself as a freelance data scientist ready for the next project adventure. Your task is to select a machine learning project from the list provided or propose an original project idea that resonates with you. Your objective is to identify a specific challenge within the chosen industry domain and design a machine learning solution to address it. Whether you're predicting customer behavior, optimizing processes, or making healthcare more efficient, your project should demonstrate your ability to approach complex problems, preprocess and analyze relevant data, develop and fine-tune models, and interpret results in a meaningful way. Your project will be a testament to your adaptability, curiosity, and aptitude for machine learning.

## Problem Description:

As the Problem Statement Suggested to Perform a Comple Machine Learning Project, so i have carried out the project on Sales Prediction of Rossmann Drug Stores.
Rossmann operates a network of more than 3,000 drug stores across seven European countries. The company faces the challenge of accurately forecasting daily sales for up to six weeks in advance. Sales at Rossmann stores are impacted by various factors, such as promotional activities, competition, school and public holidays, seasonal variations, and local demographics. Due to the diverse circumstances of individual store managers, the accuracy of sales predictions can vary significantly.
Provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

## Data Description:

- **Rossmann Stores Data.csv** - historical data including Sales

- **store.csv** - supplemental information about the stores

## Data fields:
Most of the fields are self-explanatory. The following are descriptions for those that aren't.

- **Id** - an Id that represents a (Store, Date) duple within the test set

- **Store** - a unique Id for each store

- **Sales** - the turnover for any given day (this is what you are predicting)

- **Customers** - the number of customers on a given day

- **Open** - an indicator for whether the store was open: 0 = closed, 1 = open

- **StateHoliday** - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None

- **SchoolHoliday** - indicates if the (Store, Date) was affected by the closure of public schools

- **StoreType** - differentiates between 4 different store models: a, b, c, d

- **Assortment** - describes an assortment level: a = basic, b = extra, c = extended

- **CompetitionDistance** - distance in meters to the nearest competitor store

- **CompetitionOpenSince[Month/Year]** - gives the approximate year and month of the time the nearest competitor was opened

- **Promo** - indicates whether a store is running a promo on that day

- **Promo2** - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating

- **Promo2Since[Year/Week]** - describes the year and calendar week when the store started participating in Promo2

- **PromoInterval** - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

## Tasks Performed:

1. **Importing Data** :- Imported both the dataset into Google Colab notebook and converted in into a Pandas dataframe using Pandas Library

2. **Data Cleaning** :- There were no Null or duplicate values in the Rossman stores data, which means that Rossmann Stores have efficiently managed their data. So no data cleaning process has to be gone through. In the Stor dataset there were no duplicate values but there were high percentage of null values in 'CompetitionDistance' with 0.27% of null values which was replaced by median. Followed by 'CompetitionOpenSinceMonth' and 'CompetitionOpenSinceYear' with 31.75%, 'Promo2SinceWeek', 'Promo2SinceYear' and 'PromoInterval' with 48.79% of null values.

3. **Exploratory Data Analysis** :- Merged both the dataset as 'mergeddf' and plotted the dependent variable and analyzed the distributions of both dependent and independent variables. Checked and visualized the correlation between the dependent and independent variables, and explored the relationships between each pair of variables through various visualization techniques.

4. **Setting Features and Target Variables** :- Created a new dataset from the mergeddf and splitted the dataset into X (by dropping columns such as 'Sales','Store','Date','Year') and y with the sales data. Further splitted the dataset into Training Set and Test Set for Implementing **Supervised Learning Machine Learning** models

5. **Implementing Supervised Machine Learning algorithms** :- Implemented Linear Regression, Lasso Regression, Decision Tree Regression and Support Vector Regression and tested the models on the train and test datasets to get to know the best model to predict the sales.

## Insights on the Analysis:

- Sales are highly correlated to number of Customers.

- The most selling and crowded store type is A.

- StoreType B has the lowest Average Sales per Customer. So i think customers visit this type only for small things.

- StoreTybe D had the highest buyer cart.

- Promo runs only in weekdays.

- For all stores, Promotion leads to increase in Sales and Customers both.

- More stores are opened during School holidays than State holidays.

- The stores which are opened during School Holiday have more sales than normal days.

- Sales are increased during Chirstmas week, this might be due to the fact that people buy more beauty products during a Christmas celebration.

- Promo2 doesnt seems to be correlated to any significant change in the sales amount.

- Absence of values in features CompetitionOpenSinceYear/Month doesn’t indicate the absence of competition as CompetitionDistance values are not null where the other two values are null.

## Conclusion: 

***Train and Test Scores for all Supervised Learning models:***
![Screenshot 2024-05-25 185727](https://github.com/sahil-kishor/Sales-Prediction/assets/159517524/88717387-51a9-438b-bd87-e023f39fe538)

### Random Forest regressor achieved the highest in training and testing score with lowest MAPE as 5.65% showing that it is a highly accurate model. MAE is the average magnitude of error produced by your model, the MAPE is how far the model’s predictions are off from their corresponding outputs on average.


  
## Author

Sahil Kishor

Project : https://github.com/sahil-kishor/Sales-Prediction/blob/main/Machine_Learning_Mid_Course_Assessment_Case_Study.ipynb 

Email : kishorsahil555@gmail.com

LinkedIn : www.linkedin.com/in/sahil-kishor


