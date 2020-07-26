## Data Quality Report

### Overview of Data
* Transactions Table has 20000 observations & 13 features.
* Customer Demographic's Table has 4000 observarions & 13 features.
* Customer Address Table has 3999 observations and 6 features

### Issues with Data

* Incosistency in customer_id column of customer demographic table with respect to the customer address table.
* Presence of null values in various features such as job_title, DOB etc..
* Incosistency in various features regarding the recorded values having same interpretation but different representation. For example, 'Victoria' is represented as 'VIC' or 'V' at some points.
* Some Numerical features are present in the form of string.

*Please ensure the actions to be taken on the null values present in accordance with your data collection technique. Meanwhile we are proceeding forward with steps mentioned below.*


### Dealing with issues for each data:

#### Transactions Dataset:
 1. Null Values:
 <br>
      * The features ```brand```, ```product_line```,
       ```product_class```, ```product_size``` have missing values for same observations and therefore values in these observations are replaced by 'missing'.
      * Null values in ```standard_cost```,
       ```product_first_sold_date``` are replaced by 0.
      * The null values in ```online_order``` are taken to be offline orders and replaced to be 0.
      
 2. Convert necessary string features to numeric data type.
      
#### Customer Demographic Dataset:
 1. Null Values:
      * The null values in ```last_name```,  ```job_title```, ```job_industry_category``` are replaced by'missing'.
      * The null values in ```DOB``` are replaced by ```1970-01-01```
      * The null values in ```tenure``` are replced by 0 
      * Delete the ```default``` column as it does not provide any significant information.
      
 2. Inconsistency in ```gender``` column:
      * Female is represented by 'Female', 'Femal' & 'F'
      * Male is represented by 'Male' & 'M'
      * For all Female we will use 'F'  and for Male we will use 'M'
      
#### Customer Address Dataset:
 1. Null Values:
 <br>
    * No Null Values
 2. Inconsistency in ```state``` column:
 <br>
    * 'VIC', 'Victoria' represent same entity similarly 'NSW', 'New South Wales' also represent same state.
    * We will be using 'VIC', 'NSW' inplace of 'Victoria' & 'New South Wales' respectively.
 
 
*Moving forward, the team will continue with the data cleaning, standardisation and transformation process
for the purpose of model analysis. Questions will be raised along the way and assumptions documented.
After we have completed this, it would be great to spend some time with your data SME to ensure that all
assumptions are aligned with Sprocket Central’s understanding.*