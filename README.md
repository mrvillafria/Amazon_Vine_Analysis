# Amazon Vine Analysis

## Overview of Project
For this week's project, we will be looking at Big Data and Cloud Services. Big Data is data that has more variety and is generating at high volumes quickly. Spark has become the leading technology for handling big data. This will allow us to process and analyze data quickly and at a massive scale. We will also be using Google Colab since it is hosted in the cloud. This makes it easier to read datasets that are from the cloud as well. Our data will be pulled from Amazon's Simple Storage Service (S3).

### Purpose
The purpose of this week's project is help businesses optimize their marketing efforts at BigMarket. The project will be to analyze Amazon reviews written by members of the paid Amazon Vine program. Amazon Vine members are delivered products and are required to publish a review. We will be using PySpark to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. We will then be using PySpark to analyze our data to determine if there is any bias toward favorable Vine member reviews. 

## Results

In order for us to determine if there was a bias of Vine Reviews, we created a dataframe from our Amazon review data that had 6 columns:
1. review_id: The unique ID of the review.
2. star_rating: The 1-5 star rating of the review.
3. helpful_votes: Number of helpful votes.
4. total_votes: Number of total votes the review received.
5. vine: Review was written as part of the Vine program.
6. verified_purchase: The review is on a verified purchase.

We filtered the dataframe to retrieve rows where the total_count was greater or equal to 20 and also filtered to show reviews that are more likely to be helpful. We created two more dataframes based on if the review was a Vine review (paid) or non-Vine review (unpaid).

#### Number of Reviews
##### Vine Reviews
![paid_reviews](/Resources/paid_reviews.PNG)

##### Non-View Reviews
![unpaid_reviews](/Resources/unpaid_reviews.PNG)

#### Number of 5 Star Reviews
##### Vine 5 Star Reviews
![paid_five_star_reviews](/Resources/paid_five_star_reviews.PNG)

##### Non-View 5 Star Reviews
![unpaid_five_star_reviews](/Resources/unpaid_five_star_reviews.PNG)

#### Percentage of 5 Star Reviews
##### Vine 5 Star Review Percentage
![paid_reviews_percentage](/Resources/paid_reviews_percentage.PNG)

##### Non-View 5 Star Review Percentage
![unpaid_reviews_percentage](/Resources/unpaid_reviews_percentage.PNG)

## Summary
In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.