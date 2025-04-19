# My-Data-Science-Blog-Post
DataScitentist_Blog_Post: Good governance, bad governance

Libraries used
The libraries were used in this project are in the requirements file.
You can install the packages listed in the requirements.txt file:
open terminal or command prompt and navigate to the directory containing requirements.txt file, then run:
pip install –r requirements.txt

The problem that arises is to provide a model against which government officials can check their future decisions.
Problems to solve:
1.	How well do the variables chosen in the project explain the variation in the resulting variable, governance effectiveness?
2.	What is the project error?
3.	To what extent can only one of the independent variables with a strong positive correlation influence the dependent variable, governance effectiveness.
4.	How to check the model over time, if it needs updates or retrain?.
5.	How to retrain the model?

Summary of the results
The results can be read at:
https://medium.com/@bt07moc/good-governance-bad-governance-f80df4e610a9

Source of data:
The data was taken from the World Bank Databank Website, https://databank.worldbank.org/, (Worldwide_Governance_Indicators, 2020).
In this site, select Databases (at the left screen) and for Topic(in right): Social Developement, then press Apply filter. 

 Acknowledgements

Detailed documentation of the WGI, interactive tools for exploring the data, and full access to the underlying source data available at www.govindicators.org.The WGI are produced by Daniel Kaufmann (Natural Resource Governance Institute and Brookings Institution) and Aart Kraay (World Bank Development Research Group). Please cite Kaufmann, Daniel, Aart Kraay and Massimo Mastruzzi (2010). "The Worldwide Governance Indicators: Methodology and Analytical Issues". World Bank Policy Research Working Paper No. 5430 (http://papers.ssrn.com/sol3/papers.cfm?abstract_id=1682130). The WGI do not reflect the official views of the Natural Resource Governance Institute, the Brookings Institution, the World Bank, its Executive Directors, or the countries they represent.

The files in the repository:
1.	The database used, called Governance_Data_M2.csv, has the following structure:
-	on rows – the countries (211 countries)
-	on columns – the indicators
The data has already undergone a standardization process.
The database structure was adapted for the project.
Meaning of the names of the columns:
GE.EST - Government Effectiveness: Estimate
CC.EST - Control of Corruption: Estimate
PV.EST - Political Stability and Absence of Violence/Terrorism: Estimate
RL.NO.SRC - Rule of Law: Number of Sources
RQ.EST - Regulatory Quality: Estimate
RL.EST - Rule of Law: Estimate
VA.EST - Voice and Accountability: Estimate
 
2.	Metadata
It includes an explanation of each variable in the database used in the project.

3.	Requirements.txt file
It includes the list of libraries used in the analysis.

Brief description of the model
The distribution diagrams show that the variables have normal distributions.
The linear correlation matrix shows the degree of correlation of each factor with the target variable, GE.EST. From these matrices it is observed that the most important variables for prediction are RL.EST, RQ.EST and CC.EST with a degree of correlation of over 90%. The other two variables PV.EST and VA.EST have a high degree of correlation of over 70%.
Only one factor indicates a negative correlation, RL.NO.SRC – the number of sources for the rule of law is negatively correlated with GE.EST – the efficiency of government. This suggests that a high efficiency of government is associated with a lower number of sources for the rule of law.
RMSE on the training set is 0.27 and RMSE on the test set is 0.31. Higher RMSE on the test set suggests a little overfitting, not very much, which means that the model generalizes well, reasonably well.
We train a simple linear regression model for two important features: CC.EST.
In the first model for CC.EST, the RMSE on the training set is 0.41 and the RMSE on the test set is 0.38. 
Compared to our full model, this model perform worse because they use less information.
I believe that this model could make good predictions about the effectiveness of governance using the variables mentioned above.



