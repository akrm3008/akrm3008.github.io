---
layout: archive
title: ""
permalink: /research/
author_profile: true
---



## Research Philosophy

My research philosophy is driven by the two primary motivations :
1. Building solution methods to real world problems which have a social impact 
2. Building solution methods with practical applicability.

To this end, I have foucssed my research in areas like disaster mangement and healthcare which have high social impact. I believe, to increase the applicability of decision models from literature of Operations Research in the real world, they must be able incorporate real-time actionable information. Advances in information processing and machine learning have led to massive improvements in perception tasks of AI like computer vision and natural language processing. Decision models can greatly benifit from these advances as information processed from these AI models are potential sources of actionable information to be incrporated in mathematical models for real-time decision making. In my doctoral research, I used this approach in improving real-time decisions for disaster management. I applied Natural Language Processing on social media to gather actionable information and develop decision models that utilise this information and make optimal decision for disaster planning. Following is a short description of my research.

## Shortage of Essential Commodities during Disasters and Role of Social Media

Shortage of essential commodities is commonly observed when a disaster or epidemic is announced. For instance, shortage of gasoline was observed prior to the landfall of Hurricane Irma in Florida (2017) and  after  the  landfall  of  Hurricane  Sandy  in  New  York/New  Jersey (2012).  When the COVID-19 pandemic unfolded in the United States in March 2020, a large number of stores ran out of essential commodities such as hand sanitizers and face masks.  An accurate prediction and forecasts of the surges in demand and subsequent shortages could help the affected population, authorities, first responders plan better. Social media contains signals for such predictions and forecasts. A lot of people report shortages and their needs during disasters. For instance, during the shortage of PPE's during Covid-19 onset in US #GetmePPE was trending. However the signal for detecting shortage using social media is not so clear in other cases. For instances, the final kind of tweets about gasoline shortage were observed in major cities of Florida during Hurricane: <br />

*"The shelters are full, there is **no gas**. Tornados could happen, and storm surge is predicted. So what are people supposed to do? #Irma"*<br />
*"Insane..95 percent of Florida trying to leave at one time. Roads r slammed. **No gas**. No hotels available. Scared!!!"*<br />
*"Gas stations **out of gas**, water shelves empty, stores and airports closed. Stocked up on food and wine, waiting on irma"*

The following figure describes the spatio temporal distribution of tweets. We wanted to explore if the these tweets can act as sensors for detecting the locations and times of this shortage. The first challenge was to first detect the sensors themselves from the massive amount of information on twitter.

<img align="middle" src="https://akrm3008.github.io/images/web5.png?raw=true" alt="Photo" style="width: 600px; border-radius: 10px; padding: 8px 8px 8px 8px"/> 

## Detecting Social Media Posts that Signal Shortage

We experimented with multiple models to develop a classifier that automates the process of detecting such posts in future disasters. In our case study with Hurricane Irma, we found that sub-topcs identified using correlated topic models served as best features for a [Support Vector Machines](https://github.com/akrm3008/gasoline/blob/master/tweet_classification.R) model beat a [bag-of-words model](https://github.com/akrm3008/gasoline/blob/master/tweet_classification.R) (unigrams with SVM) and a [Recurrent Neural Network](https://github.com/akrm3008/deep-gasoline) architecture in cross validation performace. The 5 unigrams that were part of the best classifier were *"gas, get, line, out, station"*. Topic 1 is about people tweeting that they cannot find gasoline due to Irma. On the other hand, Topic 2 is about people tweeting that gas stations are closed and they need gas. Topic 3 is about no gasoline being there in Miami. Topic 4 is about waiting in line for gasoline because of Irma.492Lastly, topic 5 is about high gasoline prices.

<img align="middle" src="https://akrm3008.github.io/images/web4.png?raw=true" alt="Photo" style="width: 600px; border-radius: 10px; padding: 8px 8px 8px 8px"/> 

## Forecasting Future Shortage of Essential Commodities

Both the number of tweets about gas shortage on a day and the number of gas stations out of gas on the next day in a given city followed a Poisson distribution. We found the the number of tweest along with some other variables like distance from Hurricane, wind speed, evacuation order could prdict the number of gas stations ont the next day using Poisson Regression. There time varying correlation also and ARIMA could explain the variance. We developed a convex hybrid loss function (HLF) that combined ARIMA and Poisson Regression and performed gradient descent on a training set. We could explain greater variance then ARIMA and Poisson Regression using this method and could forecast shortages of gasoline in cities of Florida 1-dy ahead and achieved MAPE of 22% improving over ARIMA (30%) and Poisson Regression (25%).

<img align="middle" src="https://akrm3008.github.io/images/web8.png?raw=true" alt="Photo" style="width: 600px; border-radius: 10px; padding: 8px 8px 8px 8px"/> 


## Localisation of Shortge using Inference on Large Bayesian Networks







## Optimising the Gasoline Search Path for Evacuators 





## Dynamic Supply and Redistribution of Essential Commodities (PPE's) according to changing demand


