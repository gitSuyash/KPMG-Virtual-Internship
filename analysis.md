## Analysis of the Customer Demographics and their Transactions

The ```customer demographics table``` alone doesn't convey any information about the transactions made by the customers. Therfore, we synchronise the transactions data along with customer demographics data using the common ```customer_id```'s present in both the tables.
<br>
For all the customers about whom we have their transaction history, we set a ```target``` label for them:
* 0 for customers who made less than 7 transactions, considered as Normal Customers
* 1 for customers who made more than 7 transactions, considered as High Value Customers

This data preparation step will help us make our analysis more convenient and target specific. 

### Customer-Target Distribution

![image.png](attachment:17b8947b-010c-4ca9-8cf0-a99477ed4aa9.png)

##### Interpretations:
* 2279 customers belong to ```label 0```
* 1210 customers belong to ```label 1```
* 65.3% customers constitute to ```label 0``` while 34.7% customers constitute to ```label 1```

### High value customers for each gender

![image.png](attachment:28ebbcd3-7f4e-4aa9-9bca-dc00469e28de.png)

##### Interpretations:
 Among all the high value customers:
* ```49.2%``` of the customers are ```Female```
* ```48.4%``` customers are ```Male```
* While ```2.4%``` of the customers belong to ```unknown``` category

### Job Industry Category

![image.png](attachment:53922392-3126-404b-957f-87bfed475914.png)

##### Interpretations:

* ```Manufaturing``` Industry has highest number of customers with ```label 0```.
* ```Financial Services``` & ```Manufacturing``` Industry have highest and almost same number of customers belonging to ```label 1```.
* The ```Telecommunications``` industry has least number of customers for each label.

### High Value Customers in each State

![image.png](attachment:521ad873-f724-46d0-affa-86188b52fcdd.png)

##### Interpretations:
* 54.5% of the high value customers come from ```NSW``` 
* While 21.7% & 23.9% of the high value customers belong to ```QLD``` & ```VIC``` respectively

### Customer's Property Valuation Variance

![image.png](attachment:0b59bb48-f289-4648-b576-06903027fc3c.png)

##### Interpretations:

* It is observed that customers having ```property valuation``` between 7 to 10 are crucial for both ```label 0``` as well as ```label 1``` 

### Customer's Tenure

![image.png](attachment:96c4c49d-426b-4cd0-8550-ac09fcff5d6e.png)

##### Interpretations:

* There is not much clear differnce in number of customers belonging to label 0 for different tenure
* The highest number of customers belonging to label 1 have tenure of 7

### Postcode Effect

![image.png](attachment:3e65fd0d-d124-4985-8c5c-7eb2dfa1d0b9.png)

##### Interpretations:

* The above graph represents the top 15 postcodes and number of high value customers for each postcode.
* ```2153``` Postcode has ```highest number``` of high value customers 

### Impact of Past 3 year purchases

![image.png](attachment:b3a8223e-32a7-4a9a-bfe0-ed287fb0c6cd.png)

##### Interpretations:
* There's no such difference in average bike realated purchases for each target.

### Difference due to Wealth Segments

![image.png](attachment:838515ff-5f5d-473e-bf07-38a68585e865.png)

##### Interpretations:

* For ```label 0``` or Normal Customers:
 1. 49.14% customers belong to ```Mass Customer``` Segment
 2. 24.62% customers belong to ```Affluent Customer``` Segment
 3. 26.24% customers belong to ```High Net Worth``` Segment
<br>
* For ```label 1``` or High Value Customers:
 1. 51.57% customers belong to ```Mass Customer``` Segment
 2. 23.97% customers belong to ```Affluent Customer``` Segment
 3. 24.46% customers belong to ```High Net Worth``` Segment