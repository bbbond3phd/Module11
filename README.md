# Module11
Module11_Practical Application

## Overview
The purpose of this practical application is to use the CRoss Industry Standard Process for Data Mining (CRISP-DM) process as a methodological framework from which program participants are to derive a recommendation for a fictitious client attempting to predict the price of automobiles based on a large historical dataset with several auto features.

CRISP-DM is comprised of six phases: business understanding, data understanding, data preparation, modeling, evaluation and deployment. In this practical application all phases but the deployment phase are utilized. Throughout the Jupyter notebook markdowns were used to explain each step of the process as I worked through the process towards presenting findings and providing recommendations.

In this repository, a brief summary of findings from the Modeling phase will presented along with recommendations for the client.

## Summary
A thorough modeling process was undertaking for this practical application in effort to identify a champion model that clearly provides actionable insights for the client. In this instance a ridge model using a highly curated dataset provided an output that outperformed other models based on the evaluation criteria of mean squared error and R-squared or intercept depending on the model method used.

Findings:
1. Odometer: The odometer reading (auto mileage) has a significant impact on the predicted price. Cars with lower mileage tend to have higher prices.

2. Year (of Manufacture): The year plays a crucial role in predicting the price. Newer cars usually command higher prices, while older cars may have lower prices.

3. Condition: The condition of the car affects its price. Cars rated in excellent condition have higher prices compared to those in poorer condition.

4. Cylinders (number of): The number of cylinders in the engine can influence the price, with larger engines typically found in higher-priced vehicles.

5. Fuel_Type: The type of fuel used by the vehicle can affect its price. For example, electric or hybrid vehicles have higher prices.

6. Title Status: The title status impacts price, with clean titles typically associated with higher prices compared to salvage titles.

7. Transmission Type: The type of transmission (e.g., automatic, manual) may influence the price, with certain transmission types being preferred and therefore commanding higher prices.

8. Vehicle Type: The type of vehicle (e.g., sedan, SUV, truck) can also affect its price, with certain types being more desirable and thus having higher prices.

9. Manufacturer: The manufacturer code represents different car brands, and certain brands may have higher perceived value, leading to higher prices.

Overall, the model suggests that these features collectively contribute to predicting car prices. By analyzing these features, the used car business can gain insights into how each characteristic affects the pricing of vehicles in their inventory. This information can be valuable for setting competitive prices, understanding market trends, and making informed decisions about buying and selling used cars.


![GitHub Test](Ridge_Plot.png)
![GitHub Test](Ridge_Plot.png)
