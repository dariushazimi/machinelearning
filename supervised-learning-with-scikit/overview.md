# Overview

## Supervised Learning vs Unsupervised Learning

Supervised learning uses labeled data and when there are no labeled data, we call it unsupervised learning.

## **Supervised learning**

Supervised learning aka predictive modelling is the process of making predictions using data.  ie.e if my dataset is set of email message, my Supervised learning task might be to predict whether each email is spam or non-spam. This is a supervised learning, because there is a specific outcome we are trying to predict. 

In supervised learning we make prediction based on a _**specific**_ outcome. I.e Predict survival on the titanic. 

In supervised learning we have Predictor variables / features and a target variable.

Goal: 

* Make future predictions \(Predict the target variable, given the predictor variables., say will a customer click on an add or not?\)
* Automate time-consuming task \(doctor's diagnosis\)

At very high level, here are the two main steps of supervised learning: 

1. you train a machine learning model using your existing labeled data. Labeled data is data which has been labeled with the outcome, which in the case of the email example,  is whether each message is ham or spam. This is called "model training" because the model is learning the relationship between the attributes of the data and the outcome. These attributes  might include the message text, the number of embedded links, the length of the message, and so on.  
2. Second, you make predictions on new data for which you don't know the true outcome. In other words, when a new email message arrives, you want your trained model to accurately predict whether the email is ham or spam without a human examining it. 

{% hint style="info" %}
To summarize these two steps, you could say that the model is learning from past examples, made up of inputs and outputs, and then applying what it has learned to future inputs in order to predict future outputs.
{% endhint %}

| **Task type** | **Target variable** |
| :--- | :--- |
| Classification | is categorical \(spam or legit\) |
| Regression | is continuous \(like price of houses\) |

#### **Supervised learning Requirements**

For supervised learning you need labeled data 

* Historical data with labels
* Experiments to get labeled data \(see how many click a page gets\)

There are many ways to do supervised learning in python. One of the powerful libraries is scikit learn or sklearn.

Other libraries are: TensorFlow and Keras

## **Unsupervised learning**

Uncovering hidden patterns from unlabeled data.

Unsupervised learning is the process of extracting structure from data or finding a best way to present data. ie.e segmenting the shopper in groups or cluster that have similar characteristics. This is an unsupervised learning tasks because there is no right or wrong answer about how many clusters can be found in the data, which people belong in which cluster or even how to describe each cluster.

* Grouping customers into distinct categories \(clustering\) based on their purchasing behaviour without knowing in advance what these categories maybe. This is known as clustering \(just of the branches of unsupervised learning\)

### **Reinforcement learning**

This is where machines interact with an environment. These reinforcement learning agents can optimize their 

* behaviour based on a given system of rewards and punishments. Similar to what google GO project was able to achieve playing GO.
* Grouping customers into distinct categories \(clustering\) based on their purchasing behaviour without knowing in advance what these categories maybe. This is known as clustering \(just of the branches of unsupervised learning\)

{% hint style="info" %}
Book: "An Introduction to Statistical Learning" by Trevor Hastie and Rob Tibshirani.
{% endhint %}

{% hint style="info" %}
* [x] Book: [An Introduction to Statistical Learning](http://www-bcf.usc.edu/~gareth/ISL/) \(section 2.1, 14 pages\)
* [x] Video: [Learning Paradigms](http://work.caltech.edu/library/014.html) \(13 minutes\)
{% endhint %}





