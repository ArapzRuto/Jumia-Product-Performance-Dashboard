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

-Average Current price	1,186.89

-Average Old price	1811.107

-Average % Discount	0.367141

-Average rating	3.894643
	
**Trend and Relationship Analysis**

1.The relationship between discount percentage and number of reviews

%Discount	Count of Review
0.0126382306477093-0.112638230647709	13
0.112638230647709-0.212638230647709	7
0.212638230647709-0.312638230647709	12
0.312638230647709-0.412638230647709	20
0.412638230647709-0.512638230647709	48
0.512638230647709-0.612638230647709	11
0.612638230647709-0.712638230647709	1
Grand Total	112

Deeper discounts do not drive higher ratings. Instead, Medium Discount products outperform others in customer satisfaction. In contrast, high-discount items carry a higher risk of poor ratings, possibly because quality expectations are not met despite the low price.
•	The relationship between rating and number of reviews
Rating Category	Count of Review
Average	77
High	23
Poor	12
Grand Total	112

Customers are highly motivated to purchase and leave feedback when a High Discount is present. This suggests that while people are buying because of the discounts, the product experience itself is meeting expectations but not necessarily exceeding them.
•	Whether higher discounts lead to increased customer engagement
Discount Category	Count of Review
High Discount	62
Medium Discount	32
Poor Discount	18
Grand Total	112

High discounts are the primary driver of customer engagement, accounting for 55% of the total 112 reviews collected. Despite this high volume of interaction, the vast majority of feedback is categorized as "Average," representing 68.7% of all ratings. Ultimately, the data indicates that while aggressive pricing successfully generates review quantity, it does not proportionally increase high customer satisfaction.
•	Whether higher-rated products tend to have more reviews
Sum of Review	Rating Category			
Discount Category	Average	High	Poor	Grand Total
High Discount	526.00	77.00	147.00	750.00
Medium Discount	203.00	249.00	16.00	468.00
Poor Discount	209.00	5.00	6.00	220.00
Grand Total	938.00	331.00	169.00	1438.00
•	
Most products with high review volumes fall into the "Average" rating category. Ratings naturally stabilize as more diverse feedback is collected.

Product Performance Analysis
Identify:
•	The top 10 products with the highest discounts
The top 10 products with the highest discounts 	
Product	Sum of DiscountAmount
32PCS Portable Cordless Drill Set With Cyclic Battery Drive -26 Variable Speed	2393.00
5-PCS Stainless Steel Cooking Pot Set With Steamed Slices	2585.00
Angle Measuring Tool Full Metal Multi Angle Measuring Tool	1399.00
Electric LED UV Mosquito Killer Lamp, Outdoor/Indoor Fly Killer Trap Light -USB	1418.00
LASA 3 Tier Bamboo Shoe Bench Storage Shelf	2452.00
LASA Aluminum Folding Truck Hand Cart - 68kg Max	1946.00
LASA FOLDING TABLE SERVING STAND	1526.00
LASA Stainless Steel Double Wall Mount Soap Dispenser - 500ml	1721.00
LED Eye Protection  Desk Lamp , Study, Reading, USB Fan - Double Pen Holder	1670.00
MultiFunctional Storage Rack Multi-layer Bookshelf	1880.00
Grand Total	18990.00

•	The top 10 products with the most reviews
The top 10 products with the most reviews 	
Products	Sum of Review
100 Pcs Crochet Hook Tool Set Knitting Hook Set With Box	39.00
120W Cordless Vacuum Cleaners Handheld Electric Vacuum Cleaner	69.00
137 Pieces Cake Decorating Tool Set Baking Supplies	55.00
3D Waterproof EVA Plastic Shower Curtain 1.8*2Mtrs	44.00
53 Pieces/Set Yarn Knitting Crochet Hooks With Bag - Pansies	32.00
Angle Measuring Tool Full Metal Multi Angle Measuring Tool	26.00
Creative Owl Shape Keychain Black	26.00
Electronic Digital Display Vernier Caliper	49.00
Punch-free Great Load Bearing Bathroom Storage Rack Wall Shelf-White	36.00
Simple Metal Dog Art Sculpture Decoration For Home Office	26.00
Grand Total	402.00

•	The top 5 highest-rated and bottom 5 lowest-rated products
The top 5 highest-rated and bottom 5 lowest-rated products 	
Top 5 Products	Sum of Rating(Out of 5)
Angle Measuring Tool Full Metal Multi Angle Measuring Tool	7.80
Anti-Skid Absorbent Insulation Coaster  For Home Office	5.00
Bedroom Simple Floor Hanging Clothes Rack Single Pole Hat Rack - White	5.00
Classic Black Cat Cotton Hemp Pillow Case For Home Car	5.00
Creative Owl Shape Keychain Black	7.80
DIY File Folder, Office Drawer File Holder, Pen Holder, Desktop Storage Rack	5.00
Konka Healty Electric Kettle, 24-hour Heat Preservation,1.5L,800W, White	5.00
LASA Aluminum Folding Truck Hand Cart - 68kg Max	5.00
Peacock  Throw Pillow Cushion Case For Home Car	5.00
Simple Metal Dog Art Sculpture Decoration For Home Office	7.80
Grand Total	58.40
Bottom 5 Products	Sum of Rating(Out of 5)
5-PCS Stainless Steel Cooking Pot Set With Steamed Slices	2.10
7-piece Set Of Storage Bags, Travel Storage Bags, Shoe Bags	2.20
Artificial Potted Flowers Room Decorative Flowers (2 Pieces)	2.20
Electric LED UV Mosquito Killer Lamp, Outdoor/Indoor Fly Killer Trap Light -USB	2.10
Wall-mounted Sticker Punch-free Plug Fixer	2.00
Grand Total	10.60

•	A comparison between high-discount and low-discount products based on average rating and number of reviews
 A comparison between high-discount and low-discount products based on average rating and number of reviews  
Row Labels	Average of Rating(Out of 5)	Count of Review
High Discount	3.76	62
Medium Discount	4.17	32
Poor Discount	3.86	18
Grand Total	3.89	112

Dashboard Design
Dashboard Requirements
Create a single interactive Excel dashboard containing the following sections:
Overview

Total number of products 	112
Average rating 		3.894643
Average discount percentage	0.367141
 Total number of reviews	112

Product Performance
•	Top products by rating
Top products by rating 	
Top 10 Products	Sum of Rating(Out of 5)
Angle Measuring Tool Full Metal Multi Angle Measuring Tool	7.80
Anti-Skid Absorbent Insulation Coaster  For Home Office	5.00
Bedroom Simple Floor Hanging Clothes Rack Single Pole Hat Rack - White	5.00
Classic Black Cat Cotton Hemp Pillow Case For Home Car	5.00
Creative Owl Shape Keychain Black	7.80
DIY File Folder, Office Drawer File Holder, Pen Holder, Desktop Storage Rack	5.00
Konka Healty Electric Kettle, 24-hour Heat Preservation,1.5L,800W, White	5.00
LASA Aluminum Folding Truck Hand Cart - 68kg Max	5.00
Peacock  Throw Pillow Cushion Case For Home Car	5.00
Simple Metal Dog Art Sculpture Decoration For Home Office	7.80
Grand Total	58.40

•	Top products by number of reviews
Top products by number of reviews 	
Top 10 Products	Average of Review
100 Pcs Crochet Hook Tool Set Knitting Hook Set With Box	39.00
120W Cordless Vacuum Cleaners Handheld Electric Vacuum Cleaner	69.00
137 Pieces Cake Decorating Tool Set Baking Supplies	55.00
3D Waterproof EVA Plastic Shower Curtain 1.8*2Mtrs	44.00
52 Pieces Cake Decorating Tool Set Gift Kit Baking Supplies	20.00
53 Pieces/Set Yarn Knitting Crochet Hooks With Bag - Pansies	32.00
53Pcs/Set Yarn Knitting Crochet Hooks With Bag - Fortune Cat	20.00
Electronic Digital Display Vernier Caliper	49.00
Portable Mini Cordless Car Vacuum Cleaner - Blue	24.00
Punch-free Great Load Bearing Bathroom Storage Rack Wall Shelf-White	36.00
Grand Total	38.80

•	Top products by discount percentage
 Top products by discount percentage 	
Top 10 Products	Sum of %Discount
3PCS Single Head Knitting Crochet Sweater Needle Set	53%
5-PCS Stainless Steel Cooking Pot Set With Steamed Slices	55%
6 In 1 Bottle Can Opener Multifunctional Easy Opener	64%
Angle Measuring Tool Full Metal Multi Angle Measuring Tool	98%
Classic Black Cat Cotton Hemp Pillow Case For Home Car	53%
Creative Owl Shape Keychain Black	110%
LASA 3 Tier Bamboo Shoe Bench Storage Shelf	54%
LASA FOLDING TABLE SERVING STAND	55%
Mythco 120COB Solar Wall Ligt With Motion Sensor And Remote Control 3 Modes	54%
Simple Metal Dog Art Sculpture Decoration For Home Office	100%
Grand Total	694%

Trend Analysis
•	Visualizations showing discount percentage versus reviews
 
•	Visualizations showing rating versus reviews
 
Product Categories
•	Breakdown of products by rating category
 
•	Breakdown of products by discount category
 
Dashboard
 
