## Problem Statement:
Whether a user will make an in-app purchase is a problem of high interest to mobile apps in general due to the direct impact on the bottom line. The ability to predict the probability of users purchasing within a certain time window in the future promises various benefits. 

The problem we are solving is to predict the probability of in-app purchase for a 7-day and 14-day time window of 312,568 users of a particular app based on their past behaviors on the app and their receptiveness of marketing communication from the app itself. 

## Data:
We have 2.5 months’ worth of data:

* Attributes: states/attributes of users (eg. time of user account creation)
* Sessions & Events: user's activities on the app
* Message: what messages users received from the app and how they received and responded to them.

The total size of the data we got is 45.25GB.

The target prediction is on the user level (whether a user will make a purchase or not). However, the raw data is not on the readily usable granularity. For instance, in Events dataset, each row records a specific action a user had in a particular session. Therefore, the overall approach we take to extract features is to aggregate raw data to the user level, using, the mean, mode, max value, etc.

## Machine learning method:
We use Random Forest and XGBoost algorithms to build predictive models, using features that are aggregated to user-level. The performance of models is assessed using AUC as the performance metric. Our best model achieved a 0.9765 AUC score. This paper discusses the details about the characteristics of the data, the features we extract, and our model training process.


## Project team:
We are [Hai Vu Le](https://github.com/haivule), (Anna Zeng)[https://github.com/ztzeng], and [Aditi Sharma](https://github.com/AditiSharmaUSFCA). We are all MS in Data Science students at University of San Francisco, Class of 2019.

## Acknowledgement:
We would like to send to:
* [Yannet Interian](https://github.com/yanneta), our professor at University of San Francisco to organize this Kaggle competition for us as the final project of her Advanced Machine Learning course, 2019.

* LeanPlum machine learning pod for providing their real-world data for this project. 

## Notes:
Due to confidentiality, we would not provide the data sets we used here and would not reveal identifiable findings and/or visualization that underlie our machine learning approach. In this repository, we would like to demonstrate our approach and machine learning solution to this important business problem at hand.