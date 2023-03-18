---
layout: default
title: Proposed Data Collection 
nav_order: 3
---

# Proposed Data Collection 

User-level data will be collected via Instagram for all factors. All users will have the option to voluntarily provide more detailed information about factors such as their demographics, past cyberbullying history, and current concerns. IThe primary limitation on data collection will be age.

Note: It is possible to derive certain predictors such as age from already existing data. Nevertheless, users will also be asked for these predictors and voluntary responses will be prioritized over inferred ones. 

The following relations will be constructed. 

### Work in Progress 
### Demographic
<center> 
| Variable Name     | Data Type            | Collection Method |
|:-----------------:|:--------------------|:------------------|
| Age               | Integer              | Voluntary         |
| Race              | Categorical          | Voluntary         |
| Sexuality         | Categorical          | Voluntary         |
| Household Income  | Continuous Numeric   | Voluntary         |
| Gender            | Categorical          | Voluntary         |
| User ID           | Categorical          | Instagram         |
| Name              | Categorical          | Instagram         |
| Physical Address  | Categorical          | Voluntary         |
</center>

### Cyberbullying History
| Variable Name                                     | Data Type          | Collection Method |
|:-------------------------------------------------:|:------------------|:------------------|
| Any past incidents                                | Boolean            | Voluntary         |
| Any reported past incidents                      | Boolean            | Instagram         |
| Number of Cyberbullying Experiences in Past Year  | Continuous Numeric | Voluntary         |

<center> 

</center>



### Demographic 
- Age - Integer (v)
- Race - Categorical (v)
- Sexuality - Categorical (v)
- Household Income - Continuous Numeric (v)
- Gender - Categorical (v) 
- User ID - Categorical (p) 
- Name - Categorical (p) 
- Physical Address - Categorical (v)

### Cyberbullying History
- Any past incidents - Boolean (v) 
- Any reported past incidents - Boolean (p)
- Number of Cyberbullying Experiences in Past Year (v)

### Network
- Followers - Integer (p)
- Following  - Integer (p)
- Frequency of Posting - Integer (p)
- Frequency of Highlights and Stories - Integer (p)
- Frequency of Comments - Integer (p)
- Frequency of Direct Messages Sent  - Integer (p)
- Frequency of Direct Messages Recieved - Integer (p)
- Cyberbullying in Online Circle - Boolean (v) 

### Direct Messages (The primary key for this table will be the other party and the data/time the message was sent). This will also include swipe ups from stories. 
- Other User Id(s) - account id (p)
- Message (p)
- Data/Time Sent (p)

### Comments 
- Others User - user id (p)
- Comment - Categorical (p) 
- Data/Time - Date (p)
- Original Post Caption - Categorical (p) 

## Model 
The predictors in demographic, cyberbullying history, and network will be used as inputs in the network analysis, and the results will be statistics such as degree centrality, eigenvector centrality, and community membership. Degree centrality essentially measures the number of followers, which is relevant since more popular accounts may be more prone to cyberbullying due ot more exposure. Eigenvector centrality measures a particular account’s influence in their network through measure such as time spent on viewing their posts or searching their account name. Community membership identifies particular groups who may belong to a marginalized group and be more likely to be targetted through cyberbullying. 

We will also use natural language processing techniques on the predictors in the direct message and comments relations to predict whether a particular comment or message could be classified as “hostile.” The results of this subprocess can be statistics that reveal how many and the frequency of hostile comments, messages that a victim recieves and from who. 

Finally, we will use the results from the subprocesses alongside the predictors in the demographic and cyberbullying history table as inputs for our predictive model. 

The model can take a variety of forms including logistic regression, decision trees, random forests, support vector machines, and neural networks. Since there are not strong existing biases within this data, we will prioritize performance above transparency and choose a neural network model to optimize performance. 

The result of the model will be a score from a scale of 1 to 100, where a higher score indicates one is more likely to be a victim. 

**insert diagram for clarity** 

## Measurement System
There are two primary components of the measurement system: how we plan to measure each variable and how well our variables represent the knowledge we hope to extract. 

First, predictors within the direct messages and comments relations are most likely to suffer from measurement bias since there are discrepancies between how younger and older teenagers communicate and understanding how colloquialisms and context. To combat this, it is vital that training data is representative of teens of different ages, locations, and cultures across the US. Additionally, the training data should be updated consistently to keep up with slang and evolution. The time frame for colloquialism’s change varies and depends upon many factors. Although conservative, we recommend the model be retrained every year. For other factors, if voluntary data is missing, we ought to be able to accurately impute those values based on the profile Instagram has of the user and missingness techniques. 

The second component of the measurement system and potential bias is how well each predictor represents the true knowledge we hope to extract. For example, how well does the number of average comments on one’s post represent the influence of a particular user? There is no technical measurement for this, and to prevent this bias from being a significant hindrance, the model makers ought to work with domain experts to ensure that the proxies are consistent with the project goal. 

## Consent 
By signing up for Instagram, users allow Instagram to monitor many factors, including many of predictors we’ve outlined, as well as create a profile on them. Therefore, their data will be used in the training model through the same privacy measures they agreed to when signing up for Instagram. This project also requests additional information with educational consent, and if a user chooses to provide additional information, they will be explained why specific predictors are requested and what the purpose is. 

For usage, we aim to make this project a cyberbullying feature that users can opt in or opt-out. If a user creates a new account or is young, Instagram will recommend they turn the feature on. 



There will be 2 thresholds used to classify each score. The thresholds will be determined based off of the training data and the outcomes of cyberbullying incidents examined manually by the Instagram team. If a score surpasses the first threshold, then the victim is warned and provided with educational resources and reminded of actions they can take including blocking and flagging accounts. If there are other account holders or if the account has parental controls, then the parents will be notified. If a score surpasses the second threshold, then actions that were recommended to the victim are automatically done, a real person is notified to look more into the case, and the victim will be notified. For example, an account that consisitently sends inappropriate messages will be blocked unless the user unblocks them manually. If there are inconsistencies with this process, the original user can also submit feedback anytime as a false flag. 
