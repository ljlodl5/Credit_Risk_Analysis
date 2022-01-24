# Credit_Risk_Analysis

## Overview 
The purpose of the challenge is to use supervised models to determine classification of customer loan risk (low vs. high) in order for an organization to determine whether and under what terms to extend credit to an individual or cohort. 
Before making that decision, we need to analyze the best predictive model in order to ensure that decisions made are based on an appropriate sensitivity (true positives and negatives) and that oversampling or undersampling of data points does not constrain resources (time/$),    
or attempt to achieve results that do not align with the expected company experience.  

As a side note one can draw a parallel searching for optimal model selection is like making orange juice with multiple different-sized mesh 'filters'. The consumer (much like a low risk-adverse organization) may prefer no pulp, or the individual (or high-risk adverse organization) may prefer pulp. 
Too much filtering/decisioning, or too little filtering/desisioning, between models (or mesh components) can produce an undesireable result for the consumer/organization. In some cases it may be okay to have false reads/microns of pulp in a pulp free container, or false high-risk applications amid a low-risk pool. It can become quite expensive and time consuming 
to manage a model/product with a return that has near 0 parts outside of true positives and negatives. And if the consumer can't feel it between the teeth, well it may be time to pick the mesh filter/model and use it going forward and allow some false-reads to go through.    
Therefore, it is important to choose the model that predicts the appropriate dependency in a timely and cost-effective manner.   

## Results 
Enclosed are the accuracy and precision results of the six models 

### Random OverSample Model
![Exhibit1](https://github.com/ljlodl5/Credit_Risk_Analysis/blob/main/Random%20Sampling.PNG)

### SMOTE Model

![Exhibit2](https://github.com/ljlodl5/Credit_Risk_Analysis/blob/main/Smote%20Sampling.PNG)

### Cluster Model

![Exhibit3](https://github.com/ljlodl5/Credit_Risk_Analysis/blob/main/Cluster%20Sampling.PNG)

### SMOTEENN Model

![Exhibit4](https://github.com/ljlodl5/Credit_Risk_Analysis/blob/main/Smoteen%20Sampling.PNG)

### Random Forest Ensemble 

![Exhibit5](https://github.com/ljlodl5/Credit_Risk_Analysis/blob/main/Balanced%20Random%20Forest%20Sampling.PNG)

### Easy Ensemble 

![Exhibit6](https://github.com/ljlodl5/Credit_Risk_Analysis/blob/main/Easy%20Ensemble%20Classifier.PNG)



## Summary 
My opinion is that none of these models are ideal, but all may be adequate for the purpose of extending loans. Part of the issue is that the pool of high-risk applications is considerably lower than that of low risk.
In the over and under sampling models (SMOTE, Random, Cluster) and over/under sampling model (SMOTEENN) the accuracy does not exceed 70%. Even if we reached close to 100% accuracy, the high risk loans count would not be that much higher. So one can assume even in the most accurate model, the low-risk category would largely outweigh the high-risk category. 
In addition, the precision value is extremely low for high-risk, lending F1 (sensitivity to precision comparison) to be extremely low for all models when it comes to evaluating high risk so there are a lot of false values occurring, but the pool is virtually skewed toward low-risk creditors regardless. 
The expectation is that a company is trying to make sound loans, or sound terms on loans--not exactly a decision requiring extreme precision or sensitivity.  

This begs the question on how far does a company need to spend in $/time to find a sensitivity score or F1 high enough for a small pool of high-risk individuals?
As stated above having microns of pulp among gallons or orange juice can be perfectly adequate for selling 'pulp free' juice. A quest for total precision and accuracy may not be necessary in order for a company to act.  

When looking at the ensembles: Balanced Random Forest and Easy Ensemble the accuracy rates go up ~80% and 93%, respectively but the precision score is low, and thus the F1 score remains low as well. 
If the company had unlimited resources and was an extremely low-risk company, then I may be more inclined to choose the Easy Ensemble model as accuracy and F1 for both low and high risk is a little higher, though it is noteworthy that it takes longer and greater $ for the models to execute and may not be worth the small benefit of higher precision or sensitivity.

It is possible other values needs to be considered in order to glean greater precision, or that a company can make allowances for the expected smaller % of high-risk lenders. 
A parallel demonstration is assessment of risk in insurance companies. For example, a life insurance company is going to take on high-risk individuals at a premium price, as long as they accept enough applications from the lower-risk pool as offet, or reinsure the risk.
The model does not need to be perfect in accuracy or precision/sensitivity, but it needs to ensure the company can forecast risk appropriately enough to obtain revenue while supporting payout committments. 
 
 
