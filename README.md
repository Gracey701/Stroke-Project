# Stroke Data Analysis
### Author: Grace Seo
## Business Problem
Objective is to advertise a production model to an insurance stakeholder which would potentially save costs and help avoid insuring customers who would cost more due to experiencing strokes based on their health data.
## Methods 
Univariate and multivariage graphs were implemented to explore the data and understand the relationships between the features and target variable, in this case whether the patient has had a stroke or not. Using a heatmap served as a building block for more detailed graphs which gave rise to a multivariate graph showing the distribution of average glucose levels grouped by having heart disease or stroke as shown below (figure 1). 
This graph shows that there is a correlation of glucose level based on whether the patient has had heart disease or not as well as strokes. With this observation, the stakeholder can determine what groups of insured to avoid insuring. 
From here, preprocessing steps were run to make a preprocessor to use for models and tuning parameters to improve the efficiency. KNN and Random Forest models were used with the preprocessor and multiple sample balancing methods were used, such as SMOTE, Random undersampling, and Random oversampling. With all the tuning and testing what was prioritized was lower false negative rates as those indicate customer who were falsely listed as not having strokes. Insuring false negatives would mean believing the insured was healthy and would not have a stroke, but later on will which would cost more for the insurer. With both the KNN and Random Forest models, undersampling gave the best results with lower false negatives and higher true positives.  With the undersampling method, further tuning was done while comparing the training and testing data results to prevent overfitting while reducing false negatives. Furthermore, with the final knn and random forest models, PCA of 95% and feature engineering were fit onto the training data. Despite the addition of PCA and feature engineering, they did not improve the models and the best model found was the random forest model (figure 2).
## Results
### Figure 1
![Average Glucose](https://user-images.githubusercontent.com/113087687/202593741-4412bcaa-6bd2-4201-94ab-a5cf1f8a8a2e.png)
### Figure 2
![Best Model (2)](https://user-images.githubusercontent.com/113087687/202595301-715f0506-5252-43ef-968a-ba4360c00c47.png)
## Conclusions
Random forest gave the best model after some hyperparameter tuning of max_depth and n_estimators, along with random undersampling. Thought the accuracy may not be the best, lower false negative and higher true positive rates would definitely be more prioritized by the stakeholders wanting to insure people who would cost less.
