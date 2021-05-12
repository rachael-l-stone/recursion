# recursion
worksample

Recursion Worksample
Rachael Stone

With limited context it is hard for me to determine exactly what is defined as healthy and what is unhealthy. My assumptions will be Healthy = mock and nan, Unhealthy - UV Inactivated SARS-CoV-2 and  Active SARS-CoV-2.

Model selection

1.a) What is your chosen approach/model(s), and why did you choose it?

My first assumption is that a rules based approach does not meet the needs of the business. 

For a situation like this, I like to usually start with a few very simple approaches to a model (such as linear regression and decision trees) for interpretability. If a simple model does not seem to work significantly well for the purposes of the business then I will continue on to more complicated methods that may have better results.  

In this situation I will be using a simple decision tree. I weighed the decision tree as if it were a balanced dataset because it gave me better precision and less error.

For best results, I think that I would need more context around the data and a more complex model could improve this model. I would start with random forest and then look in to other approaches.


1.b) What assumptions does your method make about the features?

The training set is considered as the root of the decision tree
Features are preferred to be categorical - (even though most of my data is continuous my chosen method can still give me good insights to the data)
The tree will make it’s splits according to the gini index unless otherwise specified
Samples are distributed recursively


1.c) How well does your approach discriminate between healthy and disease states of the provided Data?

The accuracy of the model is pretty high. After looking into the confusion matrix and classification report, we can see that the model is pretty good at identifying when the disease condition is “healthy” but it is not as good at identifying when it is “diseased”.

Confusion Matrix:

Classification Report:


Model generalization

2.a) How well does your model(s) generalize to different plates, experiments, or cell types?
The model doesn’t seem to generalize well to different plates, experiment, or cell types at this time. With some adjustments it may be able to perform better.

2.b) If you were provided new data from new experiments (i.e. HRCE-3 and VERO-3), how would you expect your model(s) to perform?

I would expect it to perform similarly to above. It would probably do fairly well but be better at determining those sites that are unhealthy rather than healthy.


Treatment scoring

3.a) What are the top 20 compounds, as determined by your measure of "rescue"?


3.b) What are the strengths and weaknesses to your selected approach to scoring treatment conditions?

Strengths: Easy to interpret, data doesn’t have to be a specific shape to get scores, provides a simple and effective visual representation of how scoring works, can work with numerical and categorical features to get score

Weaknesses: Can over fit if you don’t trim, can take some time to compute scores 

3.c) Would you judge the treatment predictions/scores to be necessary and/or sufficient to conclude the treatment effectively rescues the disease effect (makes disease look like healthy)? Why or why not?

I would not say that the treatment predictions are sufficient to conclude the treatment effectively rescues the disease effect. I would say that more experimentation would be necessary to judge if a treatment is effective in “rescues”. The sample sizes are relatively small.

Although, it does appear that the treatments are not effective in rescues. The percentage of those that are “rescues” in each treatment group was small in comparison to the percentage of those that are not “rescues”.

