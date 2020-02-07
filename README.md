# Eventum-Junior-Data-Scientst-Task (Airbnb New User Bookings)

## Task Description
An [Airbnb data scientist recruitment challenge](https://www.kaggle.com/c/airbnb-recruiting-new-user-bookings) used as a task by Eventum IT Solutions for Junior Data Scientest recruitment.

## Problem Description
1. Given a list of users along with their demographics, web session records, and some summary statistics. 
2. Required to predict which country a new user's first booking destination will be. 
3. All the users in this dataset are from the USA.
4. A multiclass classification problem where it is required to classifiy input to one of {'US', 'FR', 'CA', 'GB', 'ES', 'IT', 'PT', 'NL', 'DE', 'AU', 'NDF' and 'other'} classifier labels.

## Data Preprocessing
- Dataset is already divided to train and test with ratio 8 : 2 respectively [both are mentioned as the dataset]
- User id dropped from the dataset.
- Date of first booking is dropped from the dataset since this attribute contains ~57% NaN in training set and ~95% in testing set.
- NaN is replaced in the following attributes:

| Attribute               | Value           |
| ----------------------- |:---------------:|
| Age                     | 0               |
| Gender                  | Male            |
| First Affiliate Tracked | Untracked       |

- Dates in the dataset are split to 2 columns:
1. Year
2. Month

- This decision was made so the dates are more descriptive to the classifier.


## Results
| Classifier	                 | Public Score |
|------------------------------|--------------|
| Adaboost	                   | 0.67924      |
| Naive Bayes	                 | 0.67908      |
| Decision Tree	               | 0.59523      |
| **kNN**                      | **0.70635**  |
| Random Forest	               | 0.69315      |
| Logistic Regression	         | 0.68187      |
| **Max Score (Kaggle)**       | **0.88697**  |
| Min non-zero Score  (kaggle) | 0.00757      |

## Notes
- Number of neighbors in kNN = 200.
- Number of estimators in Random Forest = 50 estimator.
- All scores are submitted on Kaggle.

