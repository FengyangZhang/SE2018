# Course Project for Software Engineering Course 2018
----

Members: Fengyang Zhang (fz2ds), Yutong Wang (yw4ku)

By adding some slight perturbations to the input of a neural network classifier, one can easily fool even the most sophisticated model. The perturbation is easy to compute using gradient descent.

Although lots of efforts are put into defense against the adversarial examples, no defense method has been proven to be robust in all cases. 

Standard attacks apply gradient descent to maximize the loss of the network, instead of minimize it, on a given image to generate an adversarial example for a certain neural network. Such **optimization** methods require a useful gradient signal to succeed. When a defense obfuscates gradients, it breaks this gradient signal and causes optimization based methods to fail.

In our project we studied the paper [Towards Deep Learning Models Resistant to Adversarial Attacks](https://arxiv.org/pdf/1706.06083.pdf), run experiments on that.
