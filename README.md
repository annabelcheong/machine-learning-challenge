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

There are often more than one variable value (2 or 3 in most cases) for each name parameter, so some of these have been stripped from the analysis. For example, for stellar parameter 'koi_steff', only 'koi_steff_err1' is in the analysis, with 'koi_steff_err2' removed. Overall, this reduces the time for the code to run and improved its accuracy.  

### Findings





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


