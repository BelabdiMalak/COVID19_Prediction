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
- The Covid base includes a considerable amount of outliers, it's not suitable to ignore these information and remove all of them. These values might represent the period where deaths and contamination numbers were epic.
