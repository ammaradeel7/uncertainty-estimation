# uncertainty-estimation
## The Problem
Uncertainity estimation in neural network decisions is a major issue in safety critical applications such as auto driving cars and medical science.It is important that a model learns to say no in an unsure decision rather than giving wrong decisions with high confidence.
## Our Proposed Solution
Ensemble approaches are good for capturing model uncertainty as different outputs of the individual models when observed closely can give a better knowledge about uncertainity as the difference in the outputs can be compared.<br/>
But training multiple models is also computationally expensive and hence we use a Bayesian neural network to learn a distribution of the weights, from where we can sample as many models as we need.<br/>
Now to quantify model uncertainty we find the difference between the individual entropy of the model outputs, and the entropy of the averaged outputs of the ensemble.If the difference between these entropies is zero, the ensemble is highly certain.This can be used as a measure of the confidence of the ensemble.We have thresholded the difference to 0.1 ie the model outputs certain if the difference is below 0.1. <br/>
The MNIST dataset is used and the pictures of the digits on which the model ouputs uncertain were found to be unusual, or not a usual looking digit with respect to structure.

## To sum up:

•We Implement a Bayesian Neural network using Variational Inference and evidence lower bound.<br/>
• Sampled N neural networks from the learned distribution to create an ensemble.<br/>
• Implemented a measure of uncertainty to display confidence in the classification.
