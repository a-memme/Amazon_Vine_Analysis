# Amazon_Vine_Analysis
## Overview of Analysis 
Using Apache Spark to access large-scale data files (amazon review data) via AWS, and performing ETL on this Amazon Product Review data using PySpark and storing in a RDS. Data was then edited and cleaned to check for biases with use of Pandas - this aspect of the analysis was crucial in providing insight on paid vs unpaid reviews in quantity and quality.

## Results
### Vine Reviews 
*See image below to reference values*
- The number of paid kitchen reviews are substantially smaller in quantity vs unpaid reviews (1207 paid, 97,839 unpaid).
- There were a total of 509 five-star vine reviews, while non-vine (unpaid) reviews saw a total of 45,858 five star reviews.
- Although there was a substantially larger number of non-vine total reviews and five-star reviews vs. those seen in the vine reviews, the percentage of five star reviews in both categories were relatively close in proportion. Paid reviews had 42.17% 5 star reviews while unpaid reviews had 46.87% 5 star reviews. 

<img width="442" alt="paid_vs_unpaid" src="https://user-images.githubusercontent.com/79600550/122697098-9bcbc880-d212-11eb-94d5-6cda69b0b5af.png">
