# machine-learning-challenge
Week 21 Homework
---------------------------
## Exoplanet Exploration Analysis
In the assignment, 3 models were attempted. 

model1: Deep Learning Model (using neural network)
model2: Logistic Regression
model3: SVC Model
model3_improved: SVC Model using GridSearchCV

### Assumptions
The variables (in the rawdata csv file) are defined by the NASA Exoplanet Science Institute in the following link:
https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html

Not all variables are used. For instance, for the project disposition variables, only the koi_disposition was used as the dependent Y variable. 

There are many dependent variables in the dataset and some work was done to trial and error the accuracy when variables were dropped. Variables which had a positive impact and increased accuracy more significantly were kept in the analysis. For example, koi_duration_err1 increased the accuracy by 0.6% amongst the other dependent variables. 

### Findings
The dependent variables selected have a huge impact on the accuracy of the model. 
Similarly, the parameters for the GridSearchCV model also had more of an impact than expected. 

## Test Data Results

# Deep Learning (Model1)





# Logistic Regression (Model2)
The Logistic Regression model for the fitted data is 84.5% (test data) which is a fairly robust percentage for the general public's use case, assuming they are using the model for curiousity and not used to plan and send rockets up to the exoplanets.

# SVC Model and SVC Model with GridSearchCV (Model3)
The SVC model itself yielded a 83.9% accuracy (test data).
When the GridSearchCV was implemented on using the SVC model, the accuracy was 88.5%. That is almost a significant 5% increase in accuracy!
It should be made aware that the parameters on GridSearchCV has been further refined to a value which optimised the accuracy; a value of C=250, gamma=0.007 was used to yield the result.

---------------------------
## Repository Structure
### FOLDER: Resources
- #### cumulative.csv
CSV file containing the raw data of the exoplanets.

### FILE: exoplanet_ETL.ipynb
- 

### FILE: model1.ipynb


### FILE: model2.ipynb


### FILE: bestmodel.h5


