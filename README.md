# My-Data-Science-Blog-Post
The goal of this project is to identify the factors on which the perception of good governance depends.
We will analyze how corruption, legislation, political activity and civil society can have an influence on the effectiveness of governance. 
The model will need to make predictions about the outcomes of governance if certain factors on which it depends undergo changes.
The data was taken from the World Bank Databank Website, https://databank.worldbank.org/, (Worldwide_Governance_Indicators, 2020).
In this site, select Databases (at the left screen) and for Topic(in right): Social Developement, then press Apply filter. 
The data has already undergone a standardization process.
The database structure was adapted for the project.
The database used, called Governance_Data_M2.csv, has the following structure:
-	on rows – the countries (211 countries)
-	on columns – the indicators
Meaning of the names of the columns:

GE.EST - Government Effectiveness: Estimate
CC.EST - Control of Corruption: Estimate
PV.EST - Political Stability and Absence of Violence/Terrorism: Estimate
RL.NO.SRC - Rule of Law: Number of Sources
RQ.EST - Regulatory Quality: Estimate
RL.EST - Rule of Law: Estimate
VA.EST - Voice and Accountability: Estimate
 
The distribution diagrams show that the variables have normal distributions.
The linear correlation matrix shows the degree of correlation of each factor with the target variable, GE.EST. From these matrices it is observed that the most important variables for prediction are RL.EST, RQ.EST and CC.EST with a degree of correlation of over 90%. The other two variables PV.EST and VA.EST have a high degree of correlation of over 70%.
Only one factor indicates a negative correlation, RL.NO.SRC – the number of sources for the rule of law is negatively correlated with GE.EST – the efficiency of government. This suggests that a high efficiency of government is associated with a lower number of sources for the rule of law.
RMSE on the training set is 0.27 and RMSE on the test set is 0.31. Higher RMSE on the test set suggests a little overfitting, not very much, which means that the model generalizes well, reasonably well.
We train a simple linear regression model for two important features: CC.EST and RL.EST.
In the first model for CC.EST, the RMSE on the training set is 0.41 and the RMSE on the test set is 0.38.
In the second model for RL.EST, the RMSE on the training set is 0.34 and the RMSE on the test set is 0.38.
Compared to our full model, these two models perform worse because they use less information.
I believe that this model could make some predictions about the effectiveness of governance if other variables were changed.

