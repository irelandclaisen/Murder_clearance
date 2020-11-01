# Murder_clearance

## Description
In this project, I used data about murder, such as the victim's race, age, gender, where the murder occurred, demographics of the state,
murder weapon, etc. to predict whether a murder will be solved.  This can help with directing resources to help close these harder
to solve murder.

## Context

The murder clearance rate in the US has been hovering around 60% for decades now.  This average belies the fact that many communities see murder
clearance rates significantly below that 60%.  These low clearance rates have dangerous consequences.  

1. This may lead to more crime as if criminals are more likely to think they can get away with the acts, they’re more likely to commit them. 
Additionally the lack of arrests keeps repeat offenders on the streets as well.  
2. It can lead to community distrust, as people think the government aren’t taking these crimes seriously and they may feel abandoned.

There is also a lot of descrepancy between what types of cases are solved and which are not.  My [preliminary data analysis](https://public.tableau.com/profile/julia.nguyen4200#!/vizhome/MurderClearance/Dashboard1) finds that certain 
characteristics of a cases, such as the victim being black or male and the weapon being a gun, correlates with a lower solve rate.  Also certain
states over time have lower solve rates.

There is some evidence that increasing resources can result in higher murder clearance rates.  A [2017 study by 
Braga](https://www.hks.harvard.edu/sites/default/files/centers/rappaport/files/braga_homicideclearance%20v7.pdf) found that when the
Boston police department increased resources for murder investigations, they saw approximately 10% increase in average solve rates.  

By developing this model, we can predict which cases are more likely not to be solved and help by directing resources towards
those harder to solve cases.


## Featured Techniques
 * PostgreSQL
 * Feature Engineering
 * Data Visualization
 * Tableau
 * Balancing Classes
 
 ## Classification Algorithms
  * Logistic Regression
  * Decision Tree
  * Random Forest
  * Naive Bayes
  * XGBoost
  

## Data
Data was taken from murderdata.org and the US census bureau.  To get the data, download the Uniform Crime Report and
Supplementary Homicide Report from [murderdata.org](http://www.murderdata.org/p/data-docs.html), and the [2010 ACS 5-Year PUMS](https://www.census.gov/programs-surveys/acs/microdata/access.2010.html) and [Crosswalk Between 2013 MSAs and 2010 PUMAs](https://usa.ipums.org/usa-action/variables/met2013#description_section).
from the US census bureau.  

To look at some preliminary data analysis, see my [Tableau dashboard](https://public.tableau.com/profile/julia.nguyen4200#!/vizhome/MurderClearance/Dashboard1).


## Model Overview
I ended up using the logisitc regression model for our final model.  Both the logistic regression model and the random forest model worked comparably, but I chose to do more analysis with the logistic regression model because of its higher interpretability.

My logistic regression model was pretty good at predicting whether a murder would be solved, with a precision of 0.90 and recall of 0.74.  It was a little worse at predicting whether a murder will not be solved, with a precision of 0.55 and recall of 0.79.  I wanted a higher recall vs precision, because I think it is more important to find all the cases that are not going to be solved versus avoiding accidentally labeling cases that will be solved incorrectly.

Looking at the coefficients for my model, we can see what sort of attributes of a case that make it harder to solve.  We see that features like victim being male, victim being black, the weapon being a gun, and the crime being gang related have negative coefficients, which suggests that these sorts of crimes are more likely not to be solved.  Meanwhile, features like the victim being female, victim being white, and asphyxiation being the cause of death have positive coefficients, which suggests that crimes with these attributes are more likely to be solved.

We also can look at the coefficients in front of states which can tell us what states should invest more resources into solving their homocides.  For example the coefficient in front of Florida is negative while the coefficient for Delaware is positive, suggesting that a murder is more likely to be solved in Delaware than in Florida

