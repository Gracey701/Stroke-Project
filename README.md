# Stroke Data Analysis
### Author: Grace Seo
## Business Problem
Objective is to advertise a production model to an insurance stakeholder which would potentially save costs and help avoid insuring customers who would cost more due to experiencing strokes based on their health data.
## Methods 
- Univariate and multivariage graphs were implemented to explore the data and understand the relationships between the features and target variable, in this case whether the patient has had a stroke or not. 
- Using a heatmap served as a building block for more detailed graphs which gave rise to multivariate graphs showing the distributions of certain features
- Figure 1 shows that there is a correlation of glucose level based on whether the patient has had heart disease or not as well as strokes. With this observation, the stakeholder can determine what groups of insured to avoid insuring. 
- Figure 2 shows slight differences in age of individuals who have had strokes along with hypertension. From this the stakeholders can be wary of older clients.

- Preprocessing steps were run to make a preprocessor to use for models and tuning parameters to improve the efficiency. 
- KNN and Random Forest models were used with the preprocessor and multiple sample balancing methods were used, such as SMOTE, Random undersampling, and Random oversampling. 

- Metrics observed with this classification model included precision, recall, accuracy, and AUC scores, along with the rates of true negatives and positives and false negatives and positives. 
- Priority amongst all these metrics after tuning the models is to lower false negative rates, as those indicate customers who were falsely listed as not having strokes. 
- Insuring false negatives would mean believing the insured was healthy and would not have a stroke, but later on will which would cost more for the insurer.
- Undersampling gave the best results with lower false negatives and higher true positives. 
- With the final knn and random forest models, PCA of 95% and feature engineering were fit onto the training data. 
- Despite the addition of PCA and feature engineering, they did not improve the models and the best model found was the random forest model (figure 3).
## Results
### Figure 1
![Average Glucose](https://user-images.githubusercontent.com/113087687/202593741-4412bcaa-6bd2-4201-94ab-a5cf1f8a8a2e.png)

Those who have had heart disease have higher glucose levels. Those with heart disease and high glucose level seem to get strokes. Stakeholders should try to avoid clients with heart disease and high glucose levels.
### Figure 2
![image](https://user-images.githubusercontent.com/113087687/206609811-8032df39-a3bf-49ac-8f8d-8750c6e328fd.png)

Shows slight difference between the two groups of pos and neg hypertension w/ stroke. Younger people seem to be more healthy. Stakeholders should take caution insuring older clients, especially with hypertension.
### Figure 3
![Best Model (2)](https://user-images.githubusercontent.com/113087687/202595301-715f0506-5252-43ef-968a-ba4360c00c47.png)

Low false negative rate of 0.19 and high true positive rate of 0.81, indicating this is a decent model to use.
## Conclusions
Random forest gave the best model after some hyperparameter tuning of max_depth and n_estimators, along with random undersampling. This optimal model gave the false negative rate of 0.15 and true positive rate of 0.85, best amongst all other model versions of both KNN and Random forest. Though the accuracy may not be the best, lower false negative and higher true positive rates would definitely be more prioritized by the stakeholders wanting to insure people who would cost less.
