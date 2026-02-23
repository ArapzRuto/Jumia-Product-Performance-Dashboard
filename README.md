#**Jumia Product Performance Dashboard**

##**Data cleaning and preparation**

-The product column was converted into  text

-Current price and old price were converted into numeric

-Product category changed into text

-Review and rating changed to numeric

-The dataset had no duplicates

##**Data Enrichment**

The following columns were created to facilitate data analysis

**Discount Amount (KSh)**: Old Price minus Current Price =C2-B2

**% Discount** = Amount/Old Price =(D2/C2)

**Rating Category**:
=IFS(H3<3,"Poor",AND(H3>=3,H3<4.5),"Average",      H3>=4.5,"High")

o	Poor for ratings below 3

o	Average for ratings between 3 and 4.4

o	Excellent for ratings of 4.5 and above

**Discount Category:**

=IF(E2<20%,"Poor Discount",IF(E2>=40%,"High Discount","Medium Discount"))

-Low Discount for discounts below 20%, 	

-Medium Discount for discounts between 20% and 40%

-High Discount for discounts above 40%

#**Data Analysis**

**Descriptive Analysis**

![Descriptive Analysis](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Descriptive%20Analysis.jpg)
	
**Trend and Relationship Analysis**

1.The relationship between discount percentage and number of reviews

![Discount percentage Vs number of reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/The%20relationship%20between%20discount%20percentage%20and%20number%20of%20reviews.jpg)

Deeper discounts do not drive higher ratings. Instead, Medium Discount products outperform others in customer satisfaction. In contrast, high-discount items carry a higher risk of poor ratings, possibly because quality expectations are not met despite the low price.

2.The relationship between rating and number of reviews

![Rating Vs number of reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher%20discounts%20lead%20to%20increased%20customer%20engagement.jpg)

Customers are highly motivated to purchase and leave feedback when a High Discount is present. This suggests that while people are buying because of the discounts, the product experience itself is meeting expectations but not necessarily exceeding them.

3.Whether higher discounts lead to increased customer engagement

![Discounts Vs customer engagement](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher%20discounts%20lead%20to%20increased%20customer%20engagement.jpg)

High discounts are the primary driver of customer engagement, accounting for 55% of the total 112 reviews collected. Despite this high volume of interaction, the vast majority of feedback is categorized as "Average," representing 68.7% of all ratings. Ultimately, the data indicates that while aggressive pricing successfully generates 
review quantity, it does not proportionally increase high customer satisfaction.

4. Whether higher-rated products tend to have more reviews

![Higher-rated products Vs reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher-rated%20products%20tend%20to%20have%20more%20reviews.jpg)

Most products with high review volumes fall into the "Average" rating category. Ratings naturally stabilize as more diverse feedback is collected.

##**Product Performance Analysis**

**Identify:**

-The top 10 products with the highest discounts


![Top 10 products with the highest discounts](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/The%20top%2010%20products%20with%20the%20highest%20discounts.jpg)

•	The top 10 products with the most reviews

![Top 10 products with the most reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Top%20products%20by%20number%20of%20reviews.jpg)

•	The top 5 highest-rated and bottom 5 lowest-rated products

![Top 5 highest-rated Vs bottom 5 lowest-rated products](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/The%20top%205%20highest-rated%20and%20bottom%205%20lowest-rated%20products%20.jpg)

•	A comparison between high-discount and low-discount products based on average rating and number of reviews

 ![comparison between high-discount and low-discount products based on average rating and number of reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/A%20comparison%20between%20high-discount%20and%20low-discount%20products%20based%20on%20average%20rating%20and%20number%20of%20reviews.jpg)

#**Dashboard Design**

##**Dashboard Requirements**

Create a single interactive Excel dashboard containing the following sections:

**Overview**

 ![Overview](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Overview.jpg)

**Product Performance Analysis**

**Top products by rating**

![Top products by rating](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Top%20products%20by%20rating.jpg)

**Top products by number of reviews**

![Top products by number of reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Top%20products%20by%20number%20of%20reviews.jpg)

**Top products by discount percentage**

 ![Top products by discount percentage](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher-rated%20products%20tend%20to%20have%20more%20reviews.jpg)

##**Trend Analysis**

•	Visualizations showing discount percentage versus reviews

![Higher-rated products Vs reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher-rated%20products%20tend%20to%20have%20more%20reviews.jpg)
 
•	Visualizations showing rating versus reviews

![Higher-rated products Vs reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher-rated%20products%20tend%20to%20have%20more%20reviews.jpg)
 
**Product Categories**

•	Breakdown of products by rating category

![Higher-rated products Vs reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher-rated%20products%20tend%20to%20have%20more%20reviews.jpg)
 
•	Breakdown of products by discount category

![Higher-rated products Vs reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher-rated%20products%20tend%20to%20have%20more%20reviews.jpg)
 
#**Dashboard**
 
![Higher-rated products Vs reviews](https://github.com/ArapzRuto/Jumia-Product-Performance-Dashboard/blob/main/Whether%20higher-rated%20products%20tend%20to%20have%20more%20reviews.jpg)
