# Module11
Module11_Practical Application

## Overview
The purpose of this practical application is to use the CRoss Industry Standard Process for Data Mining (CRISP-DM) process as a methodological framework from which program participants are to derive a recommendation for a fictitious client attempting to predict the price of automobiles based on a large historical dataset with several auto features.

CRISP-DM is comprised of six phases: business understanding, data understanding, data preparation, modeling, evaluation and deployment. In this practical application all phases with the exception of the deployment phase are utilized. Throughout the Jupyter notebook markdowns were used to explain each step of the process as I worked through the process towards presenting findings and providing recommendations.

In this repository, a brief summary of the process used and findings from the Modeling phase will presented along with recommendations for the client.

## Summary
Consulting engagements typically start with a small army of business consultants sitting down with the client in attempts to understand the business question. For this practical application the business question is very simple: provide an analytically backed recommendation for the client explaining which auto features increase car prices. Understanding the business question is vastly different from understanding the business itself.

Once the business question has been clearly defined, the next step is to understand the business. Auto dealerships are retail outlets selling higher priced goods. Like any business, owners must be aware of typical business metrics such as margins, demand, yields, ect. By being aware of which auto features increase sales price, the owner can correctly price the auto for resale or purchase car with higher demand to restock inventory. In this instance the data can be thought of as business, meaning we do not have any back information informing us about the business. 

The dataset to be used for the modeling process contains a large amount of unique rows and approximately a dozen descriptive features of autos. But a brief description of the actual data file is not sufficiant to fulfill the second phase of CRISP-DM, that of understand the data. Understanding the data is the process of investigating the data at the feature and row level. Questions driving this phase include: how many unique data variables in each featuer?, are there outliers?, how much missing data is present,? how to handle missing data?, etc. 

For myself, undstanding the data typically begins with visual reivew of the data. This can be accomplished several ways: run a df.head() command or run a pairplot of integers. Data professionals should be able to visually review and see apparent issues (see the pairplot below). Additional data exploration include running counts of missing data by feature and creating a plot to visualize the size of the issue. Below we can see that the 'size' feature has the largest amount of missing values at over 250,000 rows. Another important discovery is that just under 33,000 rows of 'price' value is equal to 0. Zero is not missing, but simply put, we cannot train or validate a model with target value of $0.00. Investigative steps like the previous examples continued for each of the features.

Outliers impacting corrolation distribution:
![GitHub Test](MissingData.png)


Missing data by feature:
![GitHub Test](MissingData.png)

Understanding the data helps define the scope for the amount of effort needed in preparing the data for use in modeling. Besides fixes for missing values, several features were ommited from the analysis because they would not add any explanitory power to the model. Examples of these features include the vehicle's 'VIN' and the 'state' recording the transaction. Data preparation also includes data transformations. Examples of data transformations include hotone coding for the 'paint_color' feature.

A thorough modeling process was undertaking for this practical application in effort to identify a champion model that clearly provides actionable insights for the client. 
Initial models

In this instance a ridge model using a highly curated dataset provided an output that outperformed other models based on the evaluation criteria of mean squared error and R-squared or intercept depending on the model method used.

## Findings
The proposed client in this practical application is a used car dealership. Their request to to provide a clear understanding of the features that increase car values. Overall findings based on the best performing model (by measure of mean square error) containing the largest number of features resulted in the following recommendations:

1. Odometer: The odometer reading (auto mileage) has a significant impact on the predicted price. Cars with lower mileage tend to have higher prices.

2. Year (of Manufacture): The year plays a crucial role in predicting the price. Newer cars usually command higher prices, while older cars may have lower prices.

3. Condition: The condition of the car affects its price. Cars rated in excellent condition have higher prices compared to those in poorer condition.

4. Cylinders (number of): The number of cylinders in the engine can influence the price, with larger engines typically found in higher-priced vehicles.

5. Fuel_Type: The type of fuel used by the vehicle can affect its price. For example, electric or hybrid vehicles have higher prices.

6. Title Status: The title status impacts price, with clean titles typically associated with higher prices compared to salvage titles.

7. Transmission Type: The type of transmission influences price, with certain transmission types (e.g., automatic) being preferred and therefore commanding higher prices.

8. Vehicle Type: The type of vehicle (e.g., sedan, SUV, truck) can also affect its price, with certain types being more desirable and thus having higher prices.

9. Manufacturer: The manufacturer code represents different car brands, and certain brands have higher perceived value, leading to higher prices.

Overall, the model suggests that these features collectively contribute to predicting car prices. By analyzing these features, the used car business can gain insights into how each characteristic affects the pricing of vehicles in their inventory. This information can be valuable for setting competitive prices, understanding market trends, and making informed decisions about buying and selling used cars.


![GitHub Test](RidgeModel_Results.png)
![GitHub Test](Ridge_Plot.png)
