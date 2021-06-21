# Predicting Hotel Booking Cancellation

## Data

The data come from [Antonio et. al (2019)](https://www.sciencedirect.com/science/article/pii/S2352340918315191). Due to privacy concern, the data has been anonymized after being extracted from the hotels PMS (Payment Management Services) databases. Both hotels are located in Portugal: resort hotel (H1) at the resort region of Algarve and city hotel (H2) at the city of Lisbon. Both datasets comprehend bookings due to arrive between the 1st of July of 2015 and the 31st of August 2017, including bookings that effectively arrived and bookings that were canceled.

![](asset/hotel_grid.png)


## Problem

26.4% of all hotel transactions are being cancelled. If the management can predict a cancellation, they can confirm to the customer days before the arrival date and make the room available for another customer, thus generating more revenues.

## Model Evaluation

We trained **Decision Tree** and **Random Forest** model to classify if a transaction will be a canceled book. We have also use grid search to find the optimal hyper-parameter for Random Forest with the following search space:



The following is the summary of the model performance:

