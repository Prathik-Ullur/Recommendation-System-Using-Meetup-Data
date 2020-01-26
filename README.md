# Recommendation-system-using-meetup-data
Recommendation engines are super simple or atleast, they are made to seem super simple by the countless number of online tutorials that uses either a movie or a song dataset. This project focuses on building a recommendation system from scratch - extract real data, structure it and build several recommendation systems


![](https://secure.meetupstatic.com/s/img/7223371979728590/app_download/social/fb/meetup.en.png)

## Task

Recommendation engines are super simple or atleast, they are made to seem super simple by the countless number of online tutorials that uses either a movie or a song dataset. This project focuses on building a recommendation system from scratch - extract real data, structure it and build several recommendation systems.

Meetup is service used to organize events for users with similar interests. Meetup generates revenue from the group owners - the higher the number of members in the groups, the higher the membership fee/revenue. Evidently, any significant improvement in the engagement of the users would result in increased revenue. One of the ways to increase engagement is to personalize the events/groups recommendation in the meetup platform so that users are encouraged to attend more events. In this project, a few recommendation systems were built using the data extracted from the meetup API.

## Evaluation

The recommendation system was evaluated using the Area Under the ROC curve for a fixed recommendation set size.

## Approach 

1. Data Source: Extracted data of Austin, Texas using Meetup API to extract JSON objects of events, groups, rsvp counts etc.

2. Data wrangling to create user-item matrix using implicit feedbacks:

      a. RSVP counts: Number of times a user has attended a group's event
      
      b. TimeDelta: The number of days between a user joined the group and the last event he attended of that group
      
3. Hyperparameter tuning using PySpark on the Databrick platform

4. Final recommendations using the selected hyperparameters


## Results

1.    ALS using RSVP Counts:
            AUC(model): 0.761
            AUC(popular recommendations): 0.837
2.    ALS using TimeDelta:
            AUC(model): 0.809
            AUC(popular recommendations): 0.859


