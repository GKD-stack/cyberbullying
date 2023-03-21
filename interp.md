---
layout: default
title: Interpretations 
nav_order: 7
---

# Interpretations

## Technical Interpretation 
As a recap, the result of the model will be a score from a scale of 1 to 100, where a higher score indicates one is more likely to be a victim.

### Thresholds: How Are They Made? 
There will be 2 thresholds used to classify each score. The thresholds will be determined based off of the training data and the outcomes of cyberbullying incidents examined manually by the Instagram team. A score of 0 should correspond to no evidence of cyberbullying. A score of 100 will encapsulate all behaviors that have previously lead to the highest form of complaint at Instagram. 

The potential victim’s interpretation will also vary by the thresholds the model’s risk score output surpasses. 

There will be two thresholds used to classify the score the model outputs. 

### Thresholds: What Happens At Threshold 1? 
If a score surpasses the first threshold, the victim (and other account holders) will be warned they are a potential victim of cyberbullying, provided educational resources about cyberbullying, and reminded of the actions they can take to mitigate it, including blocking and flagging accounts. It will also be clarified that this warning is a probability based on recent activity, not a certainty with human judgment involved.  The user will have the opportunity to either confirm whether this warning is accurate or not, which will help eventually improve the accuracy of the model. Essentially, this warning will be portrayed as a preventative measure based on probability. Therefore, it should not lead to any rash actions or interventions by the user where they file complaints against others or a guardian who starts an intervention. 

### Thresholds: What Happens At Threshold 2? 
If a score surpasses the second threshold, then actions that were recommended to the user are automatically done (e.g., another account with high inappropriate activity is temporarily blocked until a human looks at the situation) and the user will be notified. At this stage, the actions by Instagram will not be portrayed as a warning, but as actions that occurred due to a significantly high-risk score. The same resources provided after the first threshold will be directly provided again alongside more stringent optional measures such as filing a complaint to Instagram about a particular user. 

The user still has the opportunity to provide feedback about whether this was a false positive, which will help refine our model. 
