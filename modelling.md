## Modelling

#### Aim: To identify the high value customers given their demographics

We were provided with the three data tables to design a model that accurately labels whether a customer is high valued or normal given its certain demographics. The three data tables were:<br>
1. Transactions Table <br>
2. Customer Demographics Table<br>
3. Customer Address Table 


*The data provided in customer demographics table does not convey any information about the transactions made by customers. To create something meaningful we extract the number of transactions made by each customer and set a target label for the customers who made more than 7 purchases as 1, thus denoting high value customers and label 0 for customers who made less than 7 purchases as Normal Customers.*  

*Also since we have to target new customers about whom we will have no prior transaction history, we need to focus more on those features that are present in test dataset that is produced during Data Quality Analysis process.* 


#### Preparing Data For Modelling

* ```First Name```, ```Last Name``` will be of no use to determine our target variable since we will be provided with new customer data, therefore we can delete these 2 features.
* We will use ```Postcode``` to determine the location of the customers, though ```Address``` feature may provide more accurate location but too many specific locations might introduce noise in model development. Therefore, we will drop ```Address``` feature too.
* Features ```Deceased_indicator``` and ```country``` have same values for all observations.Therefore these doesn't provide any significant information, these can be discarded.
* Separate ```day```, ```month``` and ```year``` from ``DOB``` feature and make 3 new features. Discard ```DOB``` feature.
* ```Job title``` & ```Job industry category``` contain high number of null values represented by *'missing'*
* In ```job title``` feature we have 421 missing features while all other values are less than 50. This needs to be dealt. Therefore we will replace *'missing'* in this feature on the basis of most frequent values for common ```industry category``` & ```wealth segment```.
* ```Job industry category``` contains 560 *'missing'* value, we will replace it by the most frequent category for customers belonging to same ```wealth segment``` and having same ```job title```.
* After the last 2 steps we are left with only 87 *'missing'* value in ```job title``` and ```job industry category features```.
* Features ```Gender```, ```Owns Car```, ```Job Title``` are encoded using ```LabelEncoder```.
* Features ```Job Title```, ```State``` & ```Wealth Segment``` are encoded using ```OneHotEncoder```.
* Final data had ```27 features``` to be used to train a model.


#### Model Development

Modellling is nothing but a mathematical phenomenon representing the data. We have used an ensemble learning model called ```RandomForestClassifier``` to train on data and infer target labels. 

* Random Forest creates subsets of train data and features.
* A decision tree model is fitted on each subset.
* At each node in Decision Tree, random set of features are considered to decide best split.
* Final prediction is made by averaging outcomes of all decision trees.

#### Model Performance

*```Accuracy Score on Train Data: 71.8%```*<br>
*```Accuracy Score on Test Data: 65.2%```*