# Predicting loan approval status

## Project/Goals

* Build a loan approval model
* Develop the model into a Pipeline
* Create a Flask app for the Pipeline
* Deploy the Flask app to the cloud

## Hypothesis

Applicants with a low risk of default seem the most likely to recieve loan approval. Some typically factors in default analysis are:
* Credit history and score
* Income
* Debt-to-income ratio
* Employment History
* Loan amount and term

## EDA 

* None of the features showed a normal distribution
* The income features (as is typical) and the LoanAmount variable were right skewed
* The Loan_Amount_Term feature is left skewed and is a discrete numerical feature
* All of the continuous numerical variables have extreme values that can be reduced by log transformation


## Process

1. Hypothesis Generation – understanding the problem better by brainstorming possible factors that can impact the outcome
2. Clean and Split – handling missing values, then splitting the dataset into training and test sets that are random and representative
3. Data Exploration – looking for patterns in the data
4. Feature Engineering – modifying existing variables and creating new ones for analysis
5. Model Building – making a predictive model on the data
6. Deployment - test api and deploy to the cloud

## Results/Demo

For the logistic regression model, there was no difference in f1-scoring between the paramaters found by the gridsearchCV and a cross-validation with the default settings. The model performance stayed consistent when applied to the test data, resulting in the following scores:
* Accuracy: 0.85
* Precision: 0.83
* Recall: 0.99
* F1 Score: 0.90

These results mean the model is excellent at determining applicants who will recieve a loan approval, but does occasional predict approval for those who should denied.

The pipelines (both test and full) have yet to be fully developed, which is holding up the testing of the api and the cloud deployment.

## Challenges 

This project has a lot of moving parts, and harmonizing them is a challenge. A strong understanding of each piece is necessary for producing a smooth running product. This strong understanding is gained through intentional design and experimentation that takes time, and time is a limited resource.

## Future Goals

Next stages for this project:
* Further design and debugging of test_pipeline
* Completion of Flask API testing
* Deployment to Heroku
* Completion of full Pipeline
* Redesign flask app as a simple demo
* Develop flask app with UI for presenting multiple model demos

(Experimentation)
* Completion of XGBoost model
* Add unsupervised learning to feature engineering
* Dockerize and deploy model to AWS with free tiers
* Deploy model to Modal with free credits