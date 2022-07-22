# Amazon_Vine_Analysis

## Overview

This project aims to analyze Amazon reviews for Lawn and Garden products written by members of the paid Amazon Vine program. This program allows manufacturers and publishers to receive reviews for their products after Amazon Vine members receive and test the products at home. This project looks to examine the variances between paid and unpaid reviews, especially in the five star context. 


## Resources

Amazon Reviews: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Lawn_and_Garden_v1_00.tsv.gz

Software: AWS, Google Colab, pgAdmin, PostgreSQL


## Results

In order to conduct the analysis, I first created a DataFrame from the Lawn and Garden review link as shown before:

![dataframe](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/dataframe.png)


I then created four dataframes from the data set:


Customers_Table

![customers_table](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/customers_name_table.png)


Products_Table

![products_table](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/products_table.png)


Review_id_Table

![review_id](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/review_id_table.png)


Vine_Table

![vine_table](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/vine_table.png)


After this, I then uploaded these to tables to pgAdmin:

![pgadmin](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/Screen%20Shot%202022-07-22%20at%203.38.32%20PM.png)


In the next section of this analysis, I examined the paid vs unpaid reviews. Out of 49,088 reviews in the dataset, 48,702 (99%) were unpaid and 386 (<1%) were paid.

![totalreviews](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/reviews.png)


Out of 24,192 five star reviews in the dataset, 24,016(99%) were unpaid and 176 (<1%) were paid.

![fivestar](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/Screen%20Shot%202022-07-22%20at%203.42.26%20PM.png)


Out of 176 total paid Amazon Vine reviews, 45.596% were 5 star reviews.

![fivestarpaid](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/paid%20five%20star.png)


Out of 24,016 total unpaid Amazon Vine reviews, 49.312% were 5 star reviews.

![unpaidfivestars](https://github.com/annietresca/Amazon_Vine_Analysis/blob/main/images/unpaid%20five%20star.png)


## Summary
These reviews suggest that the Amazon Vine program does not create a bias towards five star reviews. If anything, it suggests that reviewers are likely to be close in their examination and review of the product honestly, even if that means not rating it 5 stars. There were slightly fewer 5 star reviews from Amazon Vine members as compared to non members. An additional analysis that could prove insightful is to look for the distribution amongst all star ratings, especially 4 stars. Amazon has recently begun opening Amazon 4-star stores where they sell items that are rated 4 stars and up on their platform. By looking to check the potential bias in 4 star reviews, they could better understand what inventory would be profitable in an in person setting.
