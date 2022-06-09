# Predicting-Ted-Talks-Views
Founded in 1984 by Richard Salman as a nonprofit organization that aimed at bringing experts from the fields of Technology, Entertainment, and Design together, TED Conferences have gone on to become the Mecca of ideas from virtually all walks of life.

The main objective is to build a predictive model, which could help in predicting the views of the videos uploaded on the TEDx website.

# Problem Statement:
TED is a non-profit devoted to spreading ideas, usually in the form of short, powerful talks (18 minutes or less). TED began in 1984 as a conference where Technology, Entertainment and Design converged, and today covers almost all topics from science to business to global issues, in more than 100 languages. 

The given TED talks dataset has relevant details such as Title of talk, Speakers details, comments, native languages, topics, description etc. for around 4000 TED Talks. The goal is to identify the factors driving interest of people in Talks and build a model to predict number of views for a given TED talk.

# Approach taken:
After importing relevant python Libraries, dataset file was loaded, and I gathered basic details about dataset. Then started with the data preparation and cleaning (i.e., Handling Missing values, checking outliers etc.). After data cleaning stage, univariate analysis for each variable was done, followed by bivariate analysis to explore the relationships between two variables using Pair plots, Correlation Matrix etc. Also, used data visualization tools to get better grasp of underlying trends and patterns. 
Extracted features form textual and categorical variables. Transformed predictor variables using MinMaxScaler. Using correlation matrix, SelectKBest filter method and Sequential Forward selection method, selected important features for modelling. Built simpler models and did evaluation using MAE score. Also, performed Hyper-parameter tuning of XGBoost and randomForest models.


# Challenges Faced:
1. Ways to include information contained in non-numerical features while model building.
2. Identifying and Eliminating sources of Data Leakages.

# Conclusion:
During EDA, found out the factors driving the views on a given TED Talk. After model building, achieved average Test MAE of ~550K views. Best performing model was XGBoost after tuning with Best MAE score of ~542K views on test dataset. Based on above, following features turned out to be most important:
1.	Average of views of all topics for a Talk.
2.	Number of Languages in which a Talk is available for viewing.
3.	How many days ago a talk was published? (i.e, Days for which it was available for viewing online).
