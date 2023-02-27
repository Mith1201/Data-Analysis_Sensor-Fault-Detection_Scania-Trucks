# Data-Analysis_Sensor-Fault-Detection_Sacnia-Trucks
Performing EDA and model building to find an optimum predictive classification model.

## Problem statement.
### Data: Sensor Data

The system in focus is the Air Pressure system (APS) which generates pressurized air that are utilized in various functions in a truck, such as braking and gear changes.

- The datasets positive class corresponds to component failures for a specific component of the APS system.

- The negative class corresponds to trucks with failures for components not related to the APS system.

- The problem is to reduce the cost due to unnecessary repairs. So it is required to minimize the false predictions.

![image](https://user-images.githubusercontent.com/102762042/221452154-a4a0730b-baa0-4faf-b04b-47ad69e1044e.png)

Cost 1 = 10 and Cost 2 = 500 

- The total cost of a prediction model the sum of `Cost_1` multiplied by the number of Instances with type 1 failure and `Cost_2` with the number of instances with type 2 failure, resulting in a `Total_cost`. In this case `Cost_1` refers to the cost that an unnessecary check needs to be done by an mechanic at an workshop, while `Cost_2` refer to the cost of missing a faulty truck, which may cause a breakdown. 
- `Total_cost = Cost_1 * No_Instances + Cost_2 * No_Instances.`

- From the above problem statement we could observe that, we have to reduce false positives and false negatives. More importantly we have to **reduce false negatives, since cost incurred due to false negative is 50 times higher than the false positives.**

### Challenges and other objectives
- Need to Handle many Null values in almost all columns
- No low-latency requirement.
- Interpretability is not important.
- misclassification leads the unecessary repair costs.

## Final Result
![image](https://user-images.githubusercontent.com/102762042/221452445-89bd0dfb-1697-4d7e-acc7-ed3a0f67e58a.png)

![image](https://user-images.githubusercontent.com/102762042/221452550-0a5a53ba-a6a6-4b81-bdb9-946cc736c143.png)

### The best Model is XGBoost Classifier with 99.6% accuracy and cost of 2950 ###

