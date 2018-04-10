# Course Project for Software Engineering Course 2018
----

Members: Fengyang Zhang (fz2ds), Yutong Wang (yw4ku)

By adding some slight perturbations to the input of a neural network classifier, one can easily fool even the most sophisticated model. The perturbation is easy to compute using gradient descent.

Although lots of efforts are put into defense against the adversarial examples, no defense method has been proven to be robust in all cases. 

Standard attacks apply gradient descent to maximize the loss of the network, instead of minimize it, on a given image to generate an adversarial example for a certain neural network. Such **optimization** methods require a useful gradient signal to succeed. When a defense obfuscates gradients, it breaks this gradient signal and causes optimization based methods to fail.

However, a recent paper: [Obfuscated Gradients Give a False Sense of Security: Circumventing Defenses to Adversarial Examples](https://arxiv.org/abs/1802.00420) showed that maybe we shouldn't rely on these obfuscated gradient methods too much because it can be circumvented.

![Robustness of some proposed defenses](https://image.jiqizhixin.com/uploads/editor/e3f874e5-b05e-4ed6-aa3c-e6a8aaae160d/943562.png)

From the table we see that only one paper can largely increase the robustness of a model, which is [Towards Deep Learning Models Resistant to Adversarial Attacks](https://arxiv.org/abs/1706.06083).

After this, the paper also gives some suggestions on new rules to assess defense methods.

However, the obfuscated gradient problem stated in this paper is, said by some researchers, just another name for gradient masking problem, which has been tackled by [Ensemble Adversarial Training: Attacks and Defenses](https://arxiv.org/abs/1705.07204). This is not fully accepted by the authors.

We will investigate the methods of gradient masking and obfuscated gradients, try to formally explain them and see if they have any relationship with each other, then we will study the suggestions made in the paper about how to came up with new rules to assess defense methods' robustness.
