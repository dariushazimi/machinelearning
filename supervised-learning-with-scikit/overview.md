# Overview

## Supervised Learning vs Unsupervised Learning

Supervised learning uses labeled data and when there are no labeled data, we call it unsupervised learning.

Classification & Regression are Supervised Learning concepts, whereas Clustering \(k-means, hierarchical\) and Dimensionality Reduction are Unsupervised Learning concepts.

Supervised Learning is also known as representative, and Unsupervised predictive.

Grouping images or texts is always Classification. Labeling is a whole another concept of in itself, within Data Science and outside of ML.

Class & Reg can be linear, nonlinear or logistic.

An example of supervised learning is when a teacher or a parent supervises the learning process by providing model examples and feedback on quizzes.

![](../.gitbook/assets/image%20%2832%29.png)

Where as with an unsupervised learning you are on your own trying to figure things out. Imagine being in the wild and trying to figure out which types of fruits you can eat vs the poisonous ones.

![](../.gitbook/assets/image%20%2830%29.png)

## **Supervised learning**

Supervised learning aka predictive modelling is the process of making predictions using data.  ie.e if my dataset is set of email message, my Supervised learning task might be to predict whether each email is spam or non-spam. This is a supervised learning, because there is a specific outcome we are trying to predict. 

In supervised learning we make prediction based on a _**specific**_ outcome. I.e Predict survival on the titanic. 

In supervised learning we have Predictor variables / features and a target variable.

Goal: 

* Make future predictions \(Predict the target variable, given the predictor variables., say will a customer click on an add or not?\)
* Automate time-consuming task \(doctor's diagnosis\)

our goal with supervised learning is to build models that **generalize** to new data however we often aren't able to truly  measure how well our models will perform on out-of-sample \(new\) data does that mean that we're forced to just guess how well our models are likely to do thankfully there are option to for model evaluation procedures which allow us to estimate how well our models are likely to perform on out-of-sample data using our existing labelled data these procedures will help us to choose which value of K is best for kN and to choose whether K and N or logistic regression is a better choice for our particular task  in the meantime I've linked to a few resources that might be helpful to you first is the nearest neighbor section of the scikit-learn user guide it can help you to understand the available nearest neighbor algorithms and how to use them effectively also worth reviewing is the  class documentation for que neighbors classifier it's useful to become familiar with the structure of the class documentation since all classes are documented in the same manner.

At very high level, here are the two main steps of supervised learning: 

1. you train a machine learning model using your existing labeled data. Labeled data is data which has been labeled with the outcome, which in the case of the email example,  is whether each message is ham or spam. This is called "model training" because the model is learning the relationship between the attributes of the data and the outcome. These attributes  might include the message text, the number of embedded links, the length of the message, and so on.  
2. Second, you make predictions on new data for which you don't know the true outcome. In other words, when a new email message arrives, you want your trained model to accurately predict whether the email is ham or spam without a human examining it. 

{% hint style="info" %}
To summarize these two steps, you could say that the model is learning from past examples, made up of inputs and outputs, and then applying what it has learned to future inputs in order to predict future outputs.
{% endhint %}

| **Task type** | **Target variable** |
| :--- | :--- |
| Classification | is categorical \(spam or legit\) and unordered |
| Regression | is ordered and continuous \(like price of houses\) |

classification problem is predicting whether an email is spam or ham in ****contrast a regression problem is one in which the response being predicted is **ordered** and **continuous** such as the price of a house or the height of a person when looking at iris dot target you might be wondering how you can tell that his is a classification problem and not a regression problem since all you can see is the numbers 0 1 & 2 the answer is you actually cannot tell the difference as a machine learning practitioner you have to understand how your data is encoded and decide whether your response variable is suited for regression or classification in this case we know that the number is 0 1 & 2 represent unordered categories unless we know to use classification techniques and not regression techniques in order to solve this problem .

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

![](../.gitbook/assets/image%20%2817%29.png)

{% hint style="info" %}
Book: "An Introduction to Statistical Learning" by Trevor Hastie and Rob Tibshirani.
{% endhint %}

{% hint style="info" %}
* [x] Book: [An Introduction to Statistical Learning](http://www-bcf.usc.edu/~gareth/ISL/) \(section 2.1, 14 pages\)
* [x] Video: [Learning Paradigms](http://work.caltech.edu/library/014.html) \(13 minutes\)
{% endhint %}





