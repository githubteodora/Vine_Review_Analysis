# Amazon Vine Review Analysis

 - What is Amazon Vine? <br>
Amazon provides Vine members with free products that have been submitted to the program by participating vendors. Vine reviews are the independent opinions of the Vine Voices. The vendor cannot influence, modify or edit the reviews. Amazon does not modify or edit Vine reviews, as long as they comply with the posting guidelines. A Vine review is identified with the green stripe Customer review from the Amazon Vine Program.

## Overview of the analysis: 
This analysis reveals if any positivity bias exists for reviews in the Amazon Vine program. <br>
The dataset used for the analysis is available via the link below: <br>
[Musical instruments reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Musical_Instruments_v1_00.tsv.gz)

## Tools and Software used:
 - Google Colab
 - pySpark
 - Python 3 (Pandas)
 - SQL (Postgres, pgAdmin)
 - AWS (RDS, S3)

### ETL Workflow: 
 1. In AWS, create a PostgresDB; 
 2. In Google Colab, use pySpark to read a csv file, create tables and append them to the AWS database; 
 3. In pgAdmin, create an AWS server, confirm the availability of the data in the tables and run SQL queries;
 4. In Google Colab, transform and analyze the vine and non-vive reviews;

### Code for reference:
 - for steps 1 and 2: [Deliverable 1](https://github.com/githubteodora/Vine_Review_Analysis/blob/main/Amazon_Reviews_ETL.ipynb)
 - for steps 3 and 4: [Deliverable 2](https://github.com/githubteodora/Vine_Review_Analysis)

## Results: 

 - How many Vine reviews and non-Vine reviews were there? --> There were 60 vine and 14477 non-vine reviews in the dataset.
 - How many Vine reviews were 5 stars? --> 34 of the vine reviews gave a 5-star rating.
 - How many non-Vine reviews were 5 stars? --> 8212 of the non-vine reviews gave a 5-star rating.
 - What percentage of Vine reviews were 5 stars? --> 57%
 - What percentage of non-Vine reviews were 5 stars? --> 57% as well

## Summary:
The analysis could not confirm the existence of any positivity bias for reviews in the Vine program for the chosen dataset (musical intruments). It would be interesting to explore other dataset with non-niche products. 
