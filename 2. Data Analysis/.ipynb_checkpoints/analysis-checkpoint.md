## Analysis of the Customer Demographics and their Transactions

The ```customer demographics table``` alone doesn't convey any information about the transactions made by the customers. Therfore, we synchronise the transactions data along with customer demographics data using the common ```customer_id```'s present in both the tables.
<br>
For all the customers about whom we have their transaction history, we set a ```target``` label for them:
* 0 for customers who made less than 7 transactions, considered as Normal Customers
* 1 for customers who made more than 7 transactions, considered as High Value Customers

This data preparation step will help us make our analysis more convenient and target specific. 

### Customer-Target Distribution

![image.png](../images/fig1.png)

##### Interpretations:
* 2279 customers belong to ```label 0```
* 1210 customers belong to ```label 1```
* 65.3% customers constitute to ```label 0``` while 34.7% customers constitute to ```label 1```

### High value customers for each gender

![image.png](../images/fig2.png)

##### Interpretations:
 Among all the high value customers:
* ```49.2%``` of the customers are ```Female```
* ```48.4%``` customers are ```Male```
* While ```2.4%``` of the customers belong to ```unknown``` category

### Job Industry Category

![image.png](../images/fig3.png)

##### Interpretations:

* ```Manufaturing``` Industry has highest number of customers with ```label 0```.
* ```Financial Services``` & ```Manufacturing``` Industry have highest and almost same number of customers belonging to ```label 1```.
* The ```Telecommunications``` industry has least number of customers for each label.

### High Value Customers in each State

![image.png](../images/fig4.png)

##### Interpretations:
* 54.5% of the high value customers come from ```NSW``` 
* While 21.7% & 23.9% of the high value customers belong to ```QLD``` & ```VIC``` respectively

### Customer's Property Valuation Variance

![image.png](../images/fig5.png)

##### Interpretations:

* It is observed that customers having ```property valuation``` between 7 to 10 are crucial for both ```label 0``` as well as ```label 1``` 

### Customer's Tenure

![image.png](../images/fig6.png)

##### Interpretations:

* There is not much clear differnce in number of customers belonging to label 0 for different tenure
* The highest number of customers belonging to label 1 have tenure of 7

### Postcode Effect

![image.png](../images/fig7.png)

##### Interpretations:

* The above graph represents the top 15 postcodes and number of high value customers for each postcode.
* ```2153``` Postcode has ```highest number``` of high value customers 

### Impact of Past 3 year purchases

![image.png](../images/fig8.PNG)

##### Interpretations:
* There's no such difference in average bike realated purchases for each target.

### Difference due to Wealth Segments

![image.png](../images/fig9.png)

##### Interpretations:

* For ```label 0``` or Normal Customers:
 1. 49.14% customers belong to ```Mass Customer``` Segment
 2. 24.62% customers belong to ```Affluent Customer``` Segment
 3. 26.24% customers belong to ```High Net Worth``` Segment
 
* For ```label 1``` or High Value Customers:
 1. 51.57% customers belong to ```Mass Customer``` Segment
 2. 23.97% customers belong to ```Affluent Customer``` Segment
 3. 24.46% customers belong to ```High Net Worth``` Segment