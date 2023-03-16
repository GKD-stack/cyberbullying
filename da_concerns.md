---
layout: default
title: Data Analysis Concerns and Solutions  
nav_order: 5
---
The first ethical data analysis concern is that our data will generate inconclusive evidence that may lead to unjustified results. Both network analysis, natural language processing techniques, and our overall predictive algorithm “produce probable yet inevitably uncertain knowledge” that “may be insufficient to motivate action” (Mittelstadt et al.). Particularly, within these techniques, it is plausible that correlations that are not significant can influence the final outcome. For example, there could be a weak correlation between age and the number of followers and since a higher number of followers allows for more exposure, the result would be a higher risk score for cyberbullying. However, this relationship does not account for the context that younger people do not know as many people as older teenagers so age is not significantly correalted with cyberbullying and shouldn’t be given additional weight. 

The response to this ethical concern is that there are many variables collected and multiple thresholds that mitigate the likelihood of incorrectly classifying certain users as potential victims of cyberbullying. Therefore, weak correlations among few variables are unlikely to hold sinigifcant weight in the algorithm. The multiple thresholds will also allow for real life intervention by either the user or the Instagram team to report whether a classification is false. Furthermore, in this scenario, we allow false positives at the expense of false negatives because it is more ethical to falsely let a user know they may be the target of cyberbullying than to let a user be cyberbullied with no ackonweldgement since the former minimizes total harm. 

The second ethical data analysis concern is that our data analysis will have tranformative effects which will artificially affect how we see the world and proceed to modify its social organisation (Mittelstadt et al). These transformative effects may appear unnoticed because they are not physical, not abundant, and gradual to take place. Nevertheless, this project identifies victims and over time will create a profile of a victim and what cyberbullying consists of. These transformative effects are unethical because they could lead to challenges for informational privacy since our model does not allow the data subjects to abide by their own privacy norms and over time the users’ “value or insightfulness is only established through processing”. 

The solution to the transformative effects is multifaceted. Instead of allowing the model to gradually shape one’s view of the world, if it is consistently monitored and reevaluated when its performance metrics start to become lackluster, then the model will continue to be a somewhat accurate representation of the world, rather than the other way around. Furthermore, a consistent update to the training data, perhaps every three months, would ensure newer trends are encapsulated in the model. As mentioned before, a yearly model evaluation, retraining, and potentially reevaluating the predictors will keep the model consistent with its target users, platform, and place in society. A feedback mechanism where users can immediately provide their thoughts on the performance of the cybersecurity feature is also quick way of gathering public perception that could assist model makers on a more regular basis. The opt in and opt out features of the data collection and usage of the cybersecurity feature also addresses the informational privacy challenge for the individual by allowing the individual to decide the degree of involvement in this personal feature. 