# Coures: 2 Improving Deep Neural Networks: Hyperparameter tuning, Regularization optimization

## Setting up your ML Application Train/dev/test sets

When setting up the NN we have to make a lot of decision in terms of:

* \#of layers we need
* \#of hidden units
* ? learning rate
* ? are the activation functions we need to use for different layers?

When starting out with a new application, it is almost impossible to come up with the right numbers/answers on the first attempt. So in practice applying ML is a highly iterative process, from Idea -&gt; code -&gt; experiment and based on the outcome of the experiment we refine the idea to come up with a better and better network.

![](../.gitbook/assets/image%20%2810%29.png)

{% hint style="success" %}
**Success Factors:**

When setting up your ML, set it up in a train/dev/test model and choose a ratio that is appropriate.

Also make sure that the dev and test sets come from the same distribution.

when the team tells you that they have only a train and a test set, I would just be cautious and think, do they really have a train dev set? Because they're overfitting to the test set.
{% endhint %}

## Bias and Variance

![](../.gitbook/assets/image%20%2825%29.png)

![](../.gitbook/assets/image%20%289%29.png)

### Example of high bias and high variance

this classifier kind of **has high bias** because it was mostly _linear, but you need maybe a curve function_ or quadratic function. And it has **high** **variance**, because it had **too much flexibility** to fit those two mislabel, or those live examples in the middle as well. In case this seems contrived, well, this example is a little bit contrived in two dimensions, but with very high dimensional inputs. You actually do get things with high bias in some regions and high variance in some regions, and so it is possible to get classifiers like this in high dimensional inputs that seem less contrived. So to summarize, you've seen how by looking at your algorithm's error on the training set and your algorithm's error on the dev set you can try to diagnose, whether it has problems of high bias or high variance, or maybe both, or maybe neither. And depending on whether your algorithm suffers from bias or variance, it turns out that there are different things you could try.

![](../.gitbook/assets/image%20%286%29.png)

## Basic recipe for ML

Recommendations:

First ask: Does the algorithm have high bias?   
-&gt; Yes, try bigger network or bigger units, train longer, or use more advanced algo or better NN architecture. Keep in mind that bigger network always helps but training longer doesn't always help but it doesn't hurt. So try these things till you get rid of the bias problem.

![](../.gitbook/assets/image%20%2829%29.png)

if --&gt; No, Next question is:  
Do you have variance problem? 

Once you reduce bias to acceptable amounts then ask, do you have a variance problem? And to evaluate that I would look at dev set performance.   
Are you able to generalize from a pretty good training set performance to having a pretty good dev set performance? And if you have high variance, well, best way to solve a high variance problem is to **get more data**. If you can get it this, you know, can only help.

So for example, if you actually have a high bias problem, getting more training data is actually not going to help. Or at least it's not the most efficient thing to do. 

1. So being clear on how much of a bias problem or variance problem or both can help you focus on selecting the most useful things to try. 
2. Second, in the earlier era of machine learning, there used to be a lot of discussion on what is called the bias variance tradeoff. And the reason for that was that, for a lot of the things you could try, you could increase bias and reduce variance, or reduce bias and increase variance. But back in the pre-deep learning era, we didn't have many tools, we didn't have as many tools that just reduce bias or that just reduce variance without hurting the other one. But in the modern deep learning, big data era, so long as you can keep training a bigger network, and so long as you can keep getting more data, which isn't always the case for either of these, but if that's the case, then getting a bigger network almost always just reduces your bias without necessarily hurting your variance, so long as you regularize appropriately. And getting more data pretty much always reduces your variance and doesn't hurt your bias much.

![](../.gitbook/assets/image%20%2824%29.png)

## How to apply regularization to your network?

If you suspect your neural network is **over fitting your data**. That is you have a **high variance** problem, one of the first things you should try probably _**regularization**_.   
The other way to address high variance, is to get more training data that's also quite reliable. But you can't always get more training data, or it could be expensive to get more data. But adding regularization will often help to prevent overfitting, or to reduce the errors in your network.











