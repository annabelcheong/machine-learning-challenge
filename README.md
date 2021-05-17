# machine-learning-challenge
Week 21 Homework
---------------------------
## Exoplanet Exploration Analysis
In the assignment, 4 models were attempted. 

- model1: Deep Learning Model (using neural network)
- model2: Logistic Regression Model
- model3: SVC Model
- model3_improved: SVC Model using GridSearchCV
- model4: Random Forest Model

## Assumptions
The variables (in the rawdata csv file) are defined by the NASA Exoplanet Science Institute in the following link:
https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html

Not all variables are used. For instance, for the project disposition variables, only the koi_disposition was used as the dependent y variable. 

There are many independent variables in the dataset and some work was done to trial and error the accuracy when variables were dropped. Variables which had a positive impact and increased accuracy more significantly were kept in the analysis. For example, koi_duration_err1 increased the accuracy by 0.6% amongst the other dependent variables. Additionally, the Random Forest feature importances was used to help refine the x variable list.

## Findings
The dependent variables selected have a huge impact on the accuracy of the model. 
Similarly, the parameters for the GridSearchCV model also had more of an impact than expected. 

## Test Data Results
Overall, the Random Forest yielded the most accurate model with 90.3% accuracy (test data). 

### Deep Learning (Model1)
The model was compiled but unable to be fitted due to memory constraints on laptop. The code is avaiable in model1.ipynb.
The intention was to have 29 inputs, 1 hidden layer with 6 nodes and 3 possible outputs.
To refine accuracy further, an additional hidden layer could be added on with 6 nodes. 

### Logistic Regression (Model2)
The Logistic Regression model for the fitted data is 84.5% (test data) which is a fairly robust percentage for the general public's use case, assuming they are using the model for curiousity and not used to plan and send rockets up to the exoplanets.

### SVC Model and SVC Model with GridSearchCV (Model3)
- The SVC model itself yielded a 83.9% accuracy (test data).
- The SVC model with GridSearchCV gave a higher value at 88.5% accuracy (test data). 
That is almost a significant 5% increase in accuracy!
It should be made aware that the parameters on GridSearchCV has been further refined to a value which optimised the accuracy; a value of C=250, gamma=0.007 was used to yield the result.

### Random Forest (Model4)
The Random Forest model was most accurate at 90.3% accuracy (test data).
The n_estimator number tend to vary within 1% (n_estimator values between 200 and 400 were used experimentally). In the end, once a high accuracy was attained, the n_estimator was 360. 
This model was the most accurate of all the models performed in this assignment.

---------------------------
## Repository Structure
- FOLDER: Resources
    - exoplanet.csv: CSV file containing the raw data of the exoplanets.

- FOLDER: Models
    - The model folder contains all saved models (produced from the jupyter notebooks in this repository). 
        - model1.sav
        - model2.sav
        - model3.sav
        - model3_withGridSearchCV
        - model4.sav

- FILE: exoplanet.ipynb
    - Cleanup/ Pre-processing and preparation of data. 
    - Train, Test, Split the data. 
    - Scaled the data (X-variables)
    - Encoded the data as follows:
        - 0: CANDIDATE
        - 1: CONFIRMED
        - 2: FALSE POSITIVE
        
- FILE: model1.ipynb
Deep Learning Model code

- FILE: model2.ipynb
Logistic Regression code

- FILE: model3.ipynb
SVC code and SVC with GridSearchCV code

- FILE: model4.ipynb
Random Forest code
