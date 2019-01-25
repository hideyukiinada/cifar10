# Overview
CIFAR-10 is not an easy dataset to classify.  Back in 2011, it was believed that [it would be hard to go above 80%](http://karpathy.github.io/2011/04/27/manually-classifying-cifar10/).  Since then, technology has advanced, and in 2018, a paperwas published in which the accuracy was listed as 98.52%.  Despite this, it is a still much harder dataset than MNIST for which reaching 90% accuracy is really easy. I wanted to see how difficult it is to hit a 90% plus mark and what kind of tricks I need to employ.  I started with a plain-vanilla convnet and continued tweaking with different type of techniques and architectures.  Eventually, I was able to hit 91.93% accuracy against the test dataset.

# About CIFAR-10
CIFAR-10 is a dataset that is used to test and/or measure classification performance of a machine learning architecture for images.  The dataset consists of:

| Description | Number of images |
|---|---|
| Training set | 50000 |
| Test set | 10000 |
| Total | 60000 |

Each image is

| Attribute | Value |
|---|---|
| Height | 32 pixels |
| Width | 32 pixels |
| Channels | 3 |

Each image is classified into one of the 10 classes as listed in the [CIFAR-10 homepage](https://www.cs.toronto.edu/~kriz/cifar.html).

# Objectives
CIFAR-10 is not an easy dataset to classify.  Back in 2011, it was believed that [it would be hard to go above 80%](http://karpathy.github.io/2011/04/27/manually-classifying-cifar10/).  Since then, technology has advanced, and [a Kaggle leaderboard in 2015](https://www.kaggle.com/c/cifar-10/leaderboard) shows 22 contentants beat 90% accuracy.  In 2018, [a paper] (https://arxiv.org/abs/1805.09501) was published in which the accuracy was listed as 98.52%.  Despite this, it is a still much harder dataset than MNIST for which reaching 90% accuracy is really easy.

I wanted to see how difficult it is to hit a 90% plus mark and what kind of tricks I need to employ.  I started with a plain-vanilla convnet and continued tweaking with different type of techniques and architectures.  Eventually, I was able to hit 91.93% accuracy against the test dataset.

![Result](assets/images/accuracy_result.png)

I started off with a 2-conv layer and 2 dense layer architecture and got 63.89% which obviously is a very low result (Result #1).  I did a few more tries with this architecture and seeing that I wouldn't hit 90% and decided to add more conv layers.

# Code
All the code is available in this repo(https://github.com/hideyukiinada/cifar10/tree/master/project)
