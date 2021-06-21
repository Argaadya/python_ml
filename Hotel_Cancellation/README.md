# Predicting Hotel Booking Cancellation

## Data

The data come from [Antonio et. al (2019)](https://www.sciencedirect.com/science/article/pii/S2352340918315191). Due to privacy concern, the data has been anonymized after being extracted from the hotels PMS (Payment Management Services) databases. Both hotels are located in Portugal: resort hotel (H1) at the resort region of Algarve and city hotel (H2) at the city of Lisbon. Both datasets comprehend bookings due to arrive between the 1st of July of 2015 and the 31st of August 2017, including bookings that effectively arrived and bookings that were canceled.

![](asset/hotel_grid.png)


## Problem

26.4% of all hotel transactions are being cancelled. If the management can predict a cancellation, they can confirm to the customer days before the arrival date and make the room available for another customer, thus generating more revenues.

## Model Evaluation

We trained **Decision Tree** and **Random Forest** model to classify if a transaction will be a canceled book. We have also use grid search to find the optimal hyper-parameter for Random Forest with the following search space:

| Hyper-Parameter | Options |
| :---: | :---: | 
| Number of estimators | 100, 500, 1000 | 
| Maximum number of features | 2, 5, 15, square root of n, log2 of n | 
| Minimum sample to split | 1, 2, 5 | 
| Maximum depth of tree | None, 2, 5, 10 | 

The following is the summary of the model performance:

| Model | Accuracy | Recall | Precision | F1 Score | 
| :---: | :---: | :---: | :---: | :---: | 
| Decision Tree | 0.791 | 0.623 | 0.632 | 0.627 | 
| Initial Random Forest | 0.804 | 0.601 | 0.876 | 0.713 | 
| Tuned Random Forest | 0.809 | 0.608 | 0.880 | 0.720 | 
