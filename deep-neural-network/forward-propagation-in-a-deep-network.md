---
description: What are hyperparameters?
---

# Parameters vs Hyperparameters

Parameters of your model include W\(1\), b\(1\), etc... but there are other parameters which are called hyperparameters and play a key role in the model as well.

Examples are hyperparameters are:

* Learning rate alpha \(a\)
* Number of iterations
* Number of hidden layer L
* hidden units, n\(super1\), n\(super 2\), ....
* Choice of your activation function

these are all parameters that control W and B so we call these hyper parameters because it is the hyper parameters that somehow determine the final value of the parameters W and B that you end up with.

when you're starting on the new application it's difficult to know in advance exactly what's the best value of the hyper parameters so what often happen is you just have to try out many different values and go around this cycle your trial some value really try five hidden layers with this many number of hidden units implement that see if it works and then iterate so the title of this slide is that apply deep learning is very empirical process and empirical process is maybe a fancy way of saying you just have to try a lot of things and see what works another effect I've seen is that deep learning today is applied to so many problems ranging from computer vision to speech recognition to natural language processing to a lot of structured data applications such as maybe a online advertising or web search or product recommendations and so on and what I've seen is that first I've seen researchers from one discipline any one of these try to go to a different one and sometimes the intuitions about hyper parameters carries over and sometimes it doesn't so I often advise people especially when starting on a new problem to just try out a range of values and see what works.

Every few months try a different value for your hyperparameters and see if that makes a difference in getting better results.

![](../.gitbook/assets/image%20%2814%29.png)



{% hint style="info" %}
Each activation has a different derivative. Thus, during back propagation you need to know which activation was used in the forward propagation to be able to compute the correct derivative.
{% endhint %}



