# Amazon_Vine_Analysis
## Overview of Analysis 
Using Apache Spark to access large data files via AWS - ETL was performed on Amazon product review data using PySpark and then stored in a structured RDS. Data was then edited and cleaned to check for biases with use of Pandas - this aspect of the analysis was crucial in providing insight on paid vs unpaid reviews in quantity and quality of reviews.

## Results
### Vine Reviews 
*See images below to reference values and paid & unpaid review dataframes (respectively) - see Vine_Review_Analysis.ipynb for full code*
- The number of paid kitchen reviews are substantially smaller in quantity vs unpaid reviews (1207 paid, 97,839 unpaid).
- There were a total of 509 five-star vine reviews, while non-vine (unpaid) reviews saw a total of 45,858 five star reviews.
- Although there was a substantially larger number of non-vine total reviews and five-star reviews vs. those seen in the vine reviews, the percentage of five star reviews in both categories were relatively close in proportion. Paid reviews had 42.17% 5 star reviews while unpaid reviews had 46.87% 5 star reviews. 

<img width="442" alt="paid_vs_unpaid" src="https://user-images.githubusercontent.com/79600550/122697098-9bcbc880-d212-11eb-94d5-6cda69b0b5af.png">

<img width="635" alt="unpaid_review" src="https://user-images.githubusercontent.com/79600550/122699690-da17b680-d217-11eb-9a04-77a00d31ab39.png">

<img width="640" alt="paid_review" src="https://user-images.githubusercontent.com/79600550/122699697-ddab3d80-d217-11eb-9055-669292c9e180.png">

## Summary
Although the incentive in paid reviews (i.e vine reviews) poses a realistic possibility for positive bias, it appears as though it hasn't played too significant of a role here as the percentage of five-star reviews within both vine and non-vine review groups are close in value. Furthermore, the percentage of positive reviews is actually higher in the non-vine group vs. paid vine group of reviews, providing greater confidence that positive bias hasn't posed as a significant factor. 

An extension to this analysis that could be performed to help control for biases further would be to filter only for reviews with verified purchases. This seems to be an obvious factor when trying to determine whether a review could be genuine or not - controlling for this factor would help paint a more reliable picture of both paid and non-paid reviews given all reviews have been written by customers who have proof of purchase.


*Note - the error redndered when writing the review_id_df to the RDS occurred only because it was ran twice - the image below shows the data fully loaded in postgreSQL with no issues*

