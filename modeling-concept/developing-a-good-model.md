# Developing a good model

There are different ways to approach the problem:

![](../.gitbook/assets/image%20%2829%29.png)

Here are some examples of choosing the right approach

![](../.gitbook/assets/image%20%289%29.png)

### Confusion Matrix

![](../.gitbook/assets/image.png)

![](../.gitbook/assets/image%20%2814%29.png)

### Bloom's Taxonomy

![](../.gitbook/assets/image%20%2815%29.png)

### Data Preparation

![](../.gitbook/assets/image%20%2841%29.png)

### K-Fold Cross-Validation Method

![](../.gitbook/assets/image%20%283%29.png)

### AWS Mechanical Turk

The name Mechanical Turk was inspired by "[The Turk](https://en.wikipedia.org/wiki/The_Turk)", an 18th-century chess-playing [automaton](https://en.wikipedia.org/wiki/Automaton) made by [Wolfgang von Kempelen](https://en.wikipedia.org/wiki/Wolfgang_von_Kempelen) that toured Europe, beating both [Napoleon Bonaparte](https://en.wikipedia.org/wiki/Napoleon_Bonaparte) and [Benjamin Franklin](https://en.wikipedia.org/wiki/Benjamin_Franklin). It was later revealed that this "machine" was not an automaton at all, but was, in fact, a human [chess master](https://en.wikipedia.org/wiki/Chess_master) hidden in the cabinet beneath the board and controlling the movements of a humanoid dummy. Likewise, the Mechanical Turk online service uses remote human labour hidden behind a computer interface to help employers perform tasks that are not possible using a true machine.

### Hyperparameters vs Parameters

![](../.gitbook/assets/image%20%2812%29.png)

![](../.gitbook/assets/image%20%2820%29.png)

### Why GPUs?

![](../.gitbook/assets/image%20%284%29.png)

### Model design

1. Select a model that is a good fit for the objective
2. Choose the proper ML approach for your objective \(regression, binary classification, etc.\) \( you need to know about your algo and data\)
3. Choose proper evaluation strategies for your model based on your objective
4. Know the steps for training a model

### Data Preparation 

1. Understand concepts of Training Data and Testing Data
2. Identify potential biases introduced in an insufficient split strategy
3. Know when to use sequential splits versus randomized splits and what additional measures could be used to increase training data value. Sequential split is what we would use for time-series data. Perhaps we want to carve off the last 3 months as our test data sets. In other cases we would use randomized splits or k-fold to make sure we have good data for both training and test datasets.



### Model Training 

1. Multiple options for training: SageMaker Console, Apache Spark, Custom Code visa SDK, Jupyter Notebook
2. Be familiar with default data types SageMaker algorithms support and the recommended format for best performance 
3. Know the difference between a Hyper parameter and Parameter
4. understand the repository and container image concept for SageMaker training
5. Understand the process if you wish to provide your own algorithm
6. Understand the process for using Apache Spark to interact with SageMaker

{% embed url="https://docs.aws.amazon.com/sagemaker/latest/dg/your-algorithms.html" %}

{% embed url="https://docs.aws.amazon.com/machine-learning/latest/dg/amazon-machine-learning-key-concepts.html" %}

{% embed url="https://d1.awsstatic.com/whitepapers/aws-managing-ml-projects.pdf" %}







