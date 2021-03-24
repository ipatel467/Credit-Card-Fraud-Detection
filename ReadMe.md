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


This dataset is from Kaggle.com. The names of the columns have been changed from their original form for privacy reasons. 

## Analysis <a name="analysis"></a>

### Data Cleaning <a name="data_cleaning"></a>

Thankfully this dataset did not contain any null values. Overall this dataset was clean from the start so minimal cleaning had to be made. 

<img width="205" alt="Screen Shot 2021-03-16 at 7 38 26 PM" src="https://user-images.githubusercontent.com/52756457/111398207-08be4800-8691-11eb-9d84-07b8a61856ce.png">

<p>We can see that when we try to see the total number of nulls in each column we get a total of 0. This means that there are 0 null values in the dataset. Since the data is clean we can jump right into data preprocessing.</p>

### Exploratory Data Analysis <a name="exploratory_analysis"></a>

Here is a correlation heatmap of the different features in the dataset. We can see that there is no multicollinariety. This is overall a good thing due to multicollinariety being a problem. Multicollinearity is a problem because it undermines the statistical significance of the indpendent varibale. However, this is not a problem I will be facing today due to there being no multicollinerariyt. 

<img width="434" alt="Screen Shot 2021-03-16 at 7 40 09 PM" src="https://user-images.githubusercontent.com/52756457/111398112-da406d00-8690-11eb-8a92-ac79fa7cb970.png">

<p>

</p>







### Modeling <a name="modeling"></a>
I took a Supervised Learning Classification approach when doing this problem. I a few  different classification models such as XGBoost, Decision Trees, and Random Forest.

![Alt Text](https://media.giphy.com/media/1zi2FQvx8c6jXZB9dm/giphy.gif)



### Results <a name="results"></a>

It is hard to tell which type of model will perform best for the data, so it is best to create multiple different models. After creating a few different credit card detection models, now compare them to each other. 

However, before jumping right into the results, we will quickly go over the modeling steps. 

Here is a random forest model. 
At the top of the cell there is a %%time which will time how long it will take for the code to execute. 

After doing that we will instantitate the random forest classifier and tune some parameters. We will set the criterion to entropy because it is a measure of the randomness in the information being processed. The higher the entropy, the harder it is to draw any conclusions from that information.

The max depth parameter is the limit up to what depth every tree in the random forest will grow to.

The final parameter I tuned was n_estimators. This is the number of trees that will be built before taking the maximum voting or averages of predictions. Higher number of trees gives  better performance but makes also makes the code slower.
<img width="424" alt="Screen Shot 2021-03-16 at 7 54 11 PM" src="https://user-images.githubusercontent.com/52756457/111398488-926e1580-8691-11eb-8cab-e05425a95d98.png">

After setting the parameters to the model the next step is to fit the model with the training data. After doing this we will use the model to get test metrics such as accuracy, precision, and recall.


The random forest model scored a 99.9% accuracy, 92.4% precision, and 74.4% recall. 

Precision is   is the number of correctly-identified members of a class divided by all the times the model predicted that class. The precision score 92.4% which means that 92.4% of the results are relevant.

Recall is 74.4% which means that 74.4% of total relevant results were correctly classified by your algorithm.

Below is a confusion matrix of the Random Forest model. This table may seem daunting, but it is quite simple once broken down. A confusion matrix helps us indentify True Positive, True Negatives, False Positives, False Negatives. Below will a quick explaination of the postivives and negatives in refrence to our Credit Card transaction data.

- True Positive: Model labels a transaction as "Fraud", and is correct.
- False Positive: Model labels a transaction as "Fraud", and is incorrect.
- True Negative: Model labels a transaction as "Not Fraud", and is correct.
- False Negative :Model labels a transaction as "Fraud", and is incorrect.

<img width="384" alt="Screen Shot 2021-03-16 at 7 25 39 PM" src="https://user-images.githubusercontent.com/52756457/111398042-a8c7a180-8690-11eb-9b7a-bb9b515af1a7.png">


Above is the confusion matrix of the Random Forest model. This may look a little confusing, but it is not that crazy. 

If we look at the 2 darker blue squares those are the True Positive and True Negative outputs. These 2 blue squares represent correct classifiying done by the model. So what does this mean? This means that our true positive were label correctly 100% of the time and our True Negatives were labeled correctly 74% of the time. These are pretty good results.  

The lighter squares are the False Positives and Negatives. The very light blue square on the bottom left is False Negative. The model predicted a falsoe negative 26% of the time. This means the model reported a transaction as not fraud when the tranasction is actually fraudalent. 


<img width="424" alt="Screen Shot 2021-03-16 at 7 52 58 PM" src="https://user-images.githubusercontent.com/52756457/111398459-82eecc80-8691-11eb-9cb1-7cc4fc2391c8.png">



<img width="429" alt="Screen Shot 2021-03-16 at 7 53 38 PM" src="https://user-images.githubusercontent.com/52756457/111398479-8c783480-8691-11eb-8522-3d01c72f19f4.png">



<img width="358" alt="Screen Shot 2021-03-16 at 7 26 34 PM" src="https://user-images.githubusercontent.com/52756457/111397699-eaa41800-868f-11eb-94a5-ff4f8829a513.png">

Above is the confusion matrix of the XGBoost Classifier model.

If we look at the 2 darker blue squares those are the True Positive and True Negative outputs. These 2 blue squares represent correct classifiying done by the model. So what does this mean? This means that our true positive were label correctly 100% of the time and our True Negatives were labeled correctly 82% of the time. These are pretty good results.  

The lighter squares are the False Positives and Negatives. The very light blue square on the bottom left is False Negative. The model predicted a falsoe negative 18% of the time. This means the model reported a transaction as not fraud when the tranasction is actually fraudalent. 

<img width="360" alt="Screen Shot 2021-03-16 at 7 26 01 PM" src="https://user-images.githubusercontent.com/52756457/111398022-964d6800-8690-11eb-9169-99127b5cc2f8.png">

Above is the confusion matrix of the Decision Tree Classifier model.

If we look at the 2 darker blue squares those are the True Positive and True Negative outputs. These 2 blue squares represent correct classifiying done by the model. So what does this mean? This means that our true positive were label correctly 100% of the time and our True Negatives were labeled correctly 80% of the time. These are pretty good results.  

The lighter squares are the False Positives and Negatives. The very light blue square on the bottom left is False Negative. The model predicted a falsoe negative 20% of the time. This means the model reported a transaction as not fraud when the tranasction is actually fraudalent. 


 

<p>Now that we have seen the results of the model, lets see how different features played a role in detecting credit card fraud.</p>

### Decision Tree
<img width="481" alt="Screen Shot 2021-03-16 at 7 26 16 PM" src="https://user-images.githubusercontent.com/52756457/111398000-89c90f80-8690-11eb-81b1-1ee6be647b5f.png">
Above are all the features included in the Decsion Tree Classifier model. Each feature is given an importance score that shows its relevant importance in helping the model reach its target answer. 


We can see that V17 is the most important feature in the Decision Tree model by a significant amount. V14 is about 1/4th the size of V17. This is saying that V17 is almost 4x more important than V14.

### Random Forest
<img width="486" alt="Screen Shot 2021-03-16 at 7 25 49 PM" src="https://user-images.githubusercontent.com/52756457/111398029-a06f6680-8690-11eb-8f14-ab272639d54c.png">
The plot above shows the importance of each feature in the Random Forest model. Just by looking at it we can see that some of these are a lot more important in the Random Forest model than they were in the decision tree model.

We can see that V14 has the highest importance score and V17 has the 2nd highest importance score. We can also see that the Random Forest gives importance to multiple difference features reather than giving a couple features heavy importance like in the decison tree model. 
### XGBoost
<img width="480" alt="Screen Shot 2021-03-16 at 7 26 51 PM" src="https://user-images.githubusercontent.com/52756457/111398052-b2510980-8690-11eb-9c80-ef1276915afe.png">
 Finally here are the feature importance scores for the XGBoost classifier. The XGboost model takes alot of importance from the V17 feature and the V14 feature is 2nd most important just like the decision tree model.
 
<p></p>
One interesting thing I noticed was that the feature V10 is 3rd most important for all the models tested. I am not sure why that is the case, but it is defentiely interesting to bring up. This would require more investigation into the feature V10.
<p></p>










