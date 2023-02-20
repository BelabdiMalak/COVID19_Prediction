# COVID19_Prediction

## Introduction

Using Deep Learning and Machine Learning Techniques, I tried to answer the following question :  
"Does the food diet influence the cumulative numbers of contaminations and deaths due to COVID-19 ?"

## Data

We will use two different databases, the first one (found on link : https://www.ecdc.europa.eu/en/publications-data/download-todays-data-geographic-distribution-covid-19-cases-worldwide) contains a lot of information on daily contaminations and deaths due to COVID-19 as well as numbers cumulated by country between the month of March and the month of December 2020.

The second one “Dietary Intake Estimates” , (found on website : https://www.globaldietarydatabase.org/) gives a huge amount of data on food diet by country, by sub-region, and globally. The observation period is between 1990 and 2018.

## Steps

The problem should be devided into two parts, the first one answers the question concerning deaths only, and the second one concerns the cumulative numbers.

Here are the steps I followed :

- Analyse, correct, encode and scale the two datasets.
- Merge Covid base and Diet Base.
- Choose the appropriate model. This problem belongs to the Supervised Learning, specificly the numerical regression. I have tested the most popular and appropriate models and compared their performance (Linear Regression, Decision Trees, Random Forsets and Artificial Neural Networks).

## Remarks

- The initial Covid base covers two different periods : before the vaccination occured and after. The vaccination criteria will obviously affect the results. I have devided the data according to these two periods. Results weren't coherent for the period before vaccination and the amount of data weren't sufficient. Therfor, I have done the resolution only for the second period.
- The Covid base includes a considerable amount of outliers, it's not suitable to ignore these information and remove all of them. These values might represent the period where deaths and contamination numbers were epic. For this reason, I kept most of them and deleted the furthest points.
- Equally, the Diet base contains a few number of outliers for every food product. I replaced them with maximal or minimal value.

## Results

1. Cumulative numbers prediction

We compared models based on their "r2_score" value. Artificial Neural Networks and Random Forests registered the best values (0.903 and 0.901 respectively).

2. Deaths prediction

Equally to the previous prediction, ANN and Random Forests models has the best values of r2_score (0.72 and 0.739 respectively).

## Ideas to improve the project

- Our model is tested on a clean dataset (x_test and y_test), because we have deleted the outliers before predicting the new values. To test the real performance of our model, we better keep outliers for the testing dataset.
- To make this project more significant, we can classify data according to continents (not countries). Because continents present a big variety of food diets. We predict deaths and cumulative numbers for every continent. We can compare the direct effect of food diet on the Covid-19 contaminations.
