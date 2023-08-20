# Holiday Package Acceptence by Avengers on Holiday !

# Members
 - Aulia Pramesthi
 - Jonathan Geraldin 
 - Chairunnissa 
 - Kinanti Salsabila
 - Galih Jaya 
 - Tanda Jatiningsih

# Work Environment

 - Tools
 [JupyterLab](https://jupyter.org/try)

 - Dataset
 [Holiday Package Prediction](https://www.kaggle.com/datasets/susant4learning/holiday-package-purchase-prediction)

# Background 

 - Low product acceptance/conversion rate and high marketing costs due
   to contacting customers at random, while penetration rate for holiday
   packages continue to grow.


# Objective
 - Create a model classification to predict potential product acceptance with a higher accuracy and higher conversion rate.

# Goals
- Increase product conversion rate and lowers marketing costs
 
# Data and Assumed

**Dataset Description:**
The dataset has 4888 rows, 20 columns and **1 target ** variable `ProdTaken`

- `CustomerID` : Unique number of each customer
- `ProdTaken` : Whether the customer has ever taken the package offered
- `Age` : Age
- `TypeofContact` : How does the agent contact the customer
- `CityTier` : City level
- `DurationOfPitch` : The duration of pitching to the customer
- `Occupation` : Occupation
- `Gender` : Gender
- `NumberOfPersonVisiting` : How many family members to bring
- `NumberOfFollowups` : How many follow ups are done to the customer
- `ProductPitched` : Type of product offered
- `PreferredPropertyStar` : Rating of the property that the customer wants
- `MaritalStatus` : Status
- `NumberofTrips` : Number of trips taken by the customer
- `Passport` : Passport
- `PitchSatisfactionScore` : Customer satisfaction score on pitching
- `OwnCar` : Own a vehicle
- `NumberOfChildrenVisiting` : Number of young children going
- `Designation` : Customer designation
- `MonthlyIncome` : Income per month
  

# Data Analytics

 - ### Exploratory Data Analysis (EDA)
	Separating between numerical and categorical columns.
		
		numericals = ['Age', 'DurationOfPitch', 'NumberOfPersonVisiting', 'NumberOfFollowups', 'NumberOfTrips', 'PitchSatisfactionScore', 'NumberOfChildrenVisiting', 'MonthlyIncome']

		categoricals = ['ProdTaken', 'TypeofContact', 'CityTier', 'Occupation', 'Gender', 'ProductPitched', 'PreferredPropertyStar', 'MaritalStatus', 'Passport', 'Designation']


	- Univariate Analysis
	
		Based on the results of the univariate analysis of the numericals columns, some insights can be drawn such as:
	    - DurationOfPitch, NumberOfTrips and MonthlyIncome columns have a positively skewed data distribution, which indicates that there are outliers in the data and also the mean value is greater than the median value.
	    - Age column has an almost normal distribution.
	    - CustomerID column has a very wide distribution because there are unique values for each data.
	    - In the form of boxplot visualisation above for the numericals category, it can be concluded that there are several columns whose distribution has outliers, namely the DurationOfPitch, NumberOfPersonVisiting, NumberOfFollowups, NumberOfTrips and MonthlyIncome columns.
	    - What should be followed up during data pre-processing is handling empty columns, Replacement, handling outliers, and Normalisation/Standardisation.

		
	- Multivariate Analysis
	
		The insights obtained based on the correlation heatmap that has been plotted are:
		- There is a positive correlation between `ProdTaken` and `Passport`, where **there is a possibility that if a customer already has a passport, the customer is more likely to take the product offered**.
		- There is a moderately strong positive correlation between `Age` and `MonthlyIncome`, where **there is a possibility that if a customer has an older age, it is more likely that the customer has a larger income**.
		- There is a moderately strong positive correlation between `NumberOfFollowups` and `NumberOfPersonVisiting`, where **it is likely that a customer who invites more than 1 person is more likely to listen to the pitch**.
		- There is a very strong positive correlation between `NumberOfChildrenVisiting` and `NumberOfPersonVisiting`.
		- In addition, there are several other correlations both positive and negative, but it can be said that these correlations are fairly weak.


- ### Business Insight
	Customer who have Passport, have bigger conversion rate.
	
	Customer are more interested in BASIC Holiday Package.

	With more FollowUps after pitching the product at least 5 Time or more. Have a higher Change customer to buy Holiday Package. 

	Customers with Executive and Senior Manager titles, purchased more holiday packages.

	Customer who live at City Tier 2 and 3. More interested to buy Holiday Package.

	Age between 18 - 25yo more likely to buy the package holiday than other. 
	
- ### Data Cleansing & Preprocessing
	- Missing Value, Value Replacement and Handling Duplicate Value 
		### Missing Value
		Handling missing values starts with identifying which columns have missing values, followed by analysing the distribution of the data (stage 1)

		Columns that have missing data are Age, TypeofContact, DurationOfPitch, NumberofFollowups, PreferredPropertyStar, NumberOfTrips, NumberOfChildrenVisiting and MonthlyIncome.

		### Value Replacement
		Handling Value Replacement  in Gender, MaritalStatus, ProductPitched and Occupation columns.
		- For the Gender column, there is a value that we changed from Fe Male to Female.
		- For the MaritalStatus column, the values Unmarried and Divorce are changed to Single.
		- For the ProductPitched column, the product Standard is changed to Basic.
		-  For the Occupation column, for the job as a Freelancer is changed to Small Business.
		
		### Handling Duplicate Value
		Making sure that there are no duplicated data is one of the aspect of understanding the data itself.
		
		After checking the Duplicate Value without using the Customer ID column. There are 141 rows that have duplicate values.

		To handle the duplicate values, we will delete those rows. Before deleting the duplicate column, the dataset has **4888 rows** and after deleting the duplicate values, the number of rows becomes **4747 rows**.
	
	- Split Data Train and Test
		In a basic two-part data split, the training data set is used to train and develop models. Training sets are commonly used to estimate different parameters or to compare different model performance. The testing data set is used after the training is done.
		
		In this dataset we split the train and test data 80: 20. With results for Data Train (3797, 19) (3797,) and Data Test (950, 19) (950,)
		
	- Outlier Handling
	- Feature Encoding
	

- ### Classification Model
		



# Conclusion

Customers who we consider potential to purchase Holiday Packages

1. Customer who have Passport.
2. Customer who live at City Tier 2 and 3.
3. Customers with Executive and Senior Manager titles.
4. Get at least 5 times follow-up.
5. Age between 18 - 25yo.

# Business Recomendation

1. We recommend the Marketing Team to make more offers on
on Basic and Deluxe Products to customers.
2. Prioritise the Single age group with Teenage Age (18-25 years old) with a field duration under 20 minutes.
3. Doing a marketing strategy with a max. call duration of 20 minutes, will
have a greater chance for customers to take the product offered. With a more effective and concise way of offering.
4. Providing coupons or additional discounts to customers who are already
provide additional coupons or discounts to customers who are married, to increase the number of customers who buy holiday packages from the
from that group.
5. The company's marketing team should offer packages based on the customer's monthly income and job title.

