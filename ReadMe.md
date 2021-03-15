# Credit Card Fraud Detection
###### by Ibrahim Patel




![Alt Text](https://media.giphy.com/media/5GoVLqeAOo6PK/giphy.gif)
## Executive Summary

## Contents
1. [Introduction](#introduction)
    - [Problem Statement](#problem_statement)
    - [Dataset](#dataset)
2. [Analysis](#analysis)
    - [Data Cleaning](#data_cleaning)
    - [Exploratory Data Analysis](#exploratory_analysis)
    - [Modeling](#modeling)
    - [Results](#results)

## Introduction <a name="introduction"></a>


<p></p>

<p></p>

### Problem Statement <a name="problem_statement"></a>



### Dataset <a name="dataset"></a>
Here is a link to the dataset :
https://www.kaggle.com/unsdsn/world-happiness

This dataset is from Kaggle.com. 

## Analysis <a name="analysis"></a>

### Data Cleaning <a name="data_cleaning"></a>

Thankfully this dataset did not contain any null values. Overall this dataset was clean from the start which is a good thing for us. 

### Exploratory Data Analysis <a name="exploratory_analysis"></a>


<p>
Below is the distribution of the "Freedom" feature. The Freedom feature is a measure of how much an individual is able to conduct themself based on their free will.
</p>







### Modeling <a name="modeling"></a>
I took a Supervised Learning Regression approach when doing this problem. I used many different classification models such as Adaboost, XGBoost, Decision Trees, and Random Forest.

![Alt Text](https://media.giphy.com/media/1zi2FQvx8c6jXZB9dm/giphy.gif)



### Results <a name="results"></a>

 
 

<p>Now that we have seen the results of the model, lets see how different features played a role in predicting the happiness score.</p>



<p></p>
Here is the feature importance for the XG Boost model after it has been tuned. We can see that there are a few slight differences that are hard to spot right away. We can see that the "Family" feature is just very slightly less "important" than it was in our vanilla model. Also in our vanilla model, it showed that " Freedom" was the 3rd highest ranked score on feature importance. However, the XG Boost model after tuning shows that "Dystopia Residual" is the 3rd highest while "Freedom" is ranked 4th highest. 
<p></p>

<p></p>


The final model I will be going into today is the Gradient Boosting model. Once again a picked a few different hyperparameters I could mess with to see how I can improve my results. Once again my results improved ever so slightly. I received an R-Squared of 0.86 which means my model is obtaining 86% of the information needed to predict the "Happiness Score". However, the thing I find most intriguing about this model is its feature importance.








