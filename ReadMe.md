# Credit Card Fraud Detection
###### by Ibrahim Patel

![Alt Text](
https://media.giphy.com/media/QxAcaW5HgmqYmW5QNh/giphy.gif)

## Executive Summary

For this project I will mainly focus on detecting cases of fraud from a transactions dataset. The supermajority of transcations recorded are NOT fraud cases. Less than 0.2% of all transactions are recorded are identified as fraudulent. I will creating a machine learning model that will be able to detect and indentify transactions as fraudllent. 



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

In 2019 alone there have been roughly 165 million records of credit card fraud. This has more than doubled since the year 2017. I thought it would be interesting to create a machine learning model that could detect fraudulent transaction. 

### Dataset <a name="dataset"></a>
Here is a link to the dataset : https://www.kaggle.com/mlg-ulb/creditcardfraud 


This dataset is from Kaggle.com. 

## Analysis <a name="analysis"></a>

### Data Cleaning <a name="data_cleaning"></a>

Thankfully this dataset did not contain any null values. Overall this dataset was clean from the start so minimal cleaning had to be made. 

<img width="205" alt="Screen Shot 2021-03-16 at 7 38 26 PM" src="https://user-images.githubusercontent.com/52756457/111398207-08be4800-8691-11eb-9d84-07b8a61856ce.png">

<p>We can see that when we try to see the total number of nulls in each column we get a total of 0. This means that there are 0 null values in the dataset. </p>

### Exploratory Data Analysis <a name="exploratory_analysis"></a>


<img width="434" alt="Screen Shot 2021-03-16 at 7 40 09 PM" src="https://user-images.githubusercontent.com/52756457/111398112-da406d00-8690-11eb-8a92-ac79fa7cb970.png">

<p>

</p>







### Modeling <a name="modeling"></a>
I took a Supervised Learning Regression approach when doing this problem. I used many different classification models such as Adaboost, XGBoost, Decision Trees, and Random Forest.

![Alt Text](https://media.giphy.com/media/1zi2FQvx8c6jXZB9dm/giphy.gif)



### Results <a name="results"></a>


<img width="424" alt="Screen Shot 2021-03-16 at 7 52 58 PM" src="https://user-images.githubusercontent.com/52756457/111398459-82eecc80-8691-11eb-9cb1-7cc4fc2391c8.png">

<img width="358" alt="Screen Shot 2021-03-16 at 7 26 34 PM" src="https://user-images.githubusercontent.com/52756457/111397699-eaa41800-868f-11eb-94a5-ff4f8829a513.png">


<img width="360" alt="Screen Shot 2021-03-16 at 7 26 01 PM" src="https://user-images.githubusercontent.com/52756457/111398022-964d6800-8690-11eb-9169-99127b5cc2f8.png">





<img width="384" alt="Screen Shot 2021-03-16 at 7 25 39 PM" src="https://user-images.githubusercontent.com/52756457/111398042-a8c7a180-8690-11eb-9b7a-bb9b515af1a7.png">





<img width="429" alt="Screen Shot 2021-03-16 at 7 53 38 PM" src="https://user-images.githubusercontent.com/52756457/111398479-8c783480-8691-11eb-8522-3d01c72f19f4.png">

<img width="424" alt="Screen Shot 2021-03-16 at 7 54 11 PM" src="https://user-images.githubusercontent.com/52756457/111398488-926e1580-8691-11eb-8cab-e05425a95d98.png">



 

<p>Now that we have seen the results of the model, lets see how different features played a role in detecting credit card fraud.</p>

<img width="481" alt="Screen Shot 2021-03-16 at 7 26 16 PM" src="https://user-images.githubusercontent.com/52756457/111398000-89c90f80-8690-11eb-81b1-1ee6be647b5f.png">



<img width="486" alt="Screen Shot 2021-03-16 at 7 25 49 PM" src="https://user-images.githubusercontent.com/52756457/111398029-a06f6680-8690-11eb-8f14-ab272639d54c.png">


<img width="480" alt="Screen Shot 2021-03-16 at 7 26 51 PM" src="https://user-images.githubusercontent.com/52756457/111398052-b2510980-8690-11eb-9c80-ef1276915afe.png">


<p></p>


<p></p>










