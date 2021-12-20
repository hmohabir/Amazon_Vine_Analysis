# Amazon_Vine_Analysis
Module 16 Big Data

## Overview of the analysis

The purpose of this analysis is to review Amazon reviewsthat are written by paid Amazon Vine members. Amazon reviews for US Furniture purchase was chosen:
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Furniture_v1_00.tsv.gz.
Extract Transform Load was done in Google Collab. and the data was loaded into PostgresSQL. Also, Vine analysis was done.

## Resources: 

https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Furniture_v1_00.tsv.gz
PySparks
Google Collaboratory
PostgresSQL

## Results

First, the data was obtained to begin the analysis from the Amazon reviews weblink above: 

![PySpark data](https://github.com/hmohabir/Amazon_Vine_Analysis/blob/main/1%20Spark.PNG)

From this data, the Customer ID and count was then obtained. Other important information obtained includedproduct ID, Product title and review information. This was then loaded into a Vine table:

![Vine table](https://github.com/hmohabir/Amazon_Vine_Analysis/blob/main/5%20Vine%20table.PNG)

The data was then sent to Amazon RDS for further transformation. Tables were created in PostgresSQL, connected to Amazon AWS to capture relavant data.

![Postgres tables](https://github.com/hmohabir/Amazon_Vine_Analysis/blob/main/6%20PostgresSQL.PNG)

A couple of pieces of information were obtained. The vine(paid) and non-vine(non-paid) reviews were compared.

The toyal number of Vine and Non-vine reviews were 136 and 18019 respectively.
The number of Vine and non-vine reviews obtained were 74 and 8482 respectively.
The percentage of 5-star vine and non-vine reviews were 54 and 47 percent respectively.

## Summary

Over 99% of reviewers are non-vine.
Over 99% of 5-star reviews are also non-vine.
However, not all 5-star reviews are non-vine.

The Amazon vine analysis provided a agreeable 5-star dataset.

Additional analysis shows that there are a total of 421 vine reviewed products in this category.After an inner join of vine reviews and non-vine for a full dataset, we see that the total vine reviews for vine product is 2775, while non-vine is 7914.  This shows that the vine reviews is still favorable and worthwhile.
