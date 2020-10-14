# Animal-Shelter-Predictability

## Executive Summary:
Shelters are places where animals who have been misplaced from their homes can take refuge and be safe until they can find their new owners. Many animals are victims of harsh abuse and abandonment; they are left scarred for their entire lifetime. However, even through shelters, there are animals that are never adopted! Our project aims to figure out what characteristics make an animal more or less likely to be adopted, and what animals are most at-risk to being euthanized or forever lacking a home.

To tackle this project, we have acquired a large dataset with features ranging from the color and breed of an animal to the age and condition of an animal upon being brought into the shelter. We are tackling two problems: a classification problem to determine what outcome an animal will have based on our features and a regression problem to determine how many days an animal will stay in the shelter based on our features. In our classification problem, we will be utilizing Multinomial Bayesian Classification and Decision Trees. In our regression problem, we will be utilizing Ridge, Lasso and Decision Trees. To hypertune and optimize our models, we will be using grid search to find what parameters are best suited for each algorithm.

## Problem Statement
The topic of our project is trying to predict the outcomes of animals when they come into the animal shelter. Millions of animals enter shelters every year, so we are trying to determine what features an animal has makes it more or less likely to be adopted, euthanized, transferred to another facility, fostered, etc. We are also trying to use those features to predict the length of stay of an animal in the shelter.

## Significance of the Problem
This area is important because of the yearly 6.5 million animals that go into a shelter, only about half actually get adopted, and 1.5 million get euthanized (according to the ASPCA). Many animals never get to find their own permanent home. Insight into the features that make an animal “adoptable” or not could identify groups of animals that may need more attention, and thus improve the long-term outcomes of those at-risk groups.

## Summary of Steps
In summation, we obtained animal shelter data online for the Austin Animal Center, and cleaned up the data by dropping unnecessary columns: Animal ID, Animal Name, Date of Birth, "Outcome Subtype. We merged the intake date and outcome data into one column, "Days In," that represents that amount of days an animal was in the shelter, so we were then able to remove even more columns: Intake Date, Intake Time, Outcome Date and Outcome Time.

Since we are tackling two problems, a classification problem on the Outcome Type and a regression problem on the amount of days an animal was in a shelter, we used Recursive Feature Elimination to find the most important features for each target variable. In both problems we split the training and testing sets with a 75:25 ratio and trained our models using the training sets.

In our classification problem, we used the K-nearest neighbor, Decision tree, and Bernoulli naive bayesian algorithms, looking at the Accuracy and F1-Score. We then hypertuned these models using GridSearchCV. The results performed similarly, even with GridSearchCV. They performed with a 50%-60% accuracy rate.

In our regression problem, we used the Linear Regression, Ridge, Lasso, and Decision Tree algorithms, and then hypertuned these models using GridSearchCV. Even after hypertuning, the algorithms produced poor results on the testing set.

## Conclusion
For the classification model, it works averagely, but could be better. Perhaps, taking in more descriptive feature variables would help as well (such as chips), etc.

Based on the findings for our regression problem to determine how long an animal would stay in a shelter based on our feature variable, we conclude that we simply need more significant features to test with. Currently, we have a huge sample size with over 100,000 samples, but we are not able to make a very accurate model with the features we have right now. We recommend for future work looking for features that take into account popular pet breeds in the area or more features concerning the animal's physical appearance, such as weight or loss of limbs.

We also would like to possibly gather a dataset with more normal distribution of features. This would help in the hypothesis testing but may also help in the models.
