# CIFAR-10
Test various techniques to assess impact on CIFAR10 accuracy.

# Introduction
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
CIFAR-10 is not an easy dataset to classify.

One of the current checked-in scripts produced 91.93% accuracy against the test dataset.

![Result](assets/images/accuracy_result.png)


Please see [accuracy_log.md](accuracy_log.md) for accuracy result for each script in this repo.
