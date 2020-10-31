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
 * Logistic Regression
 * 

## Data
Data was taken from murderdata.org and the US census bureau.  To get the data, download the Uniform Crime Report and
Supplementary Homicide Report from murderdata.org, and the 2010 ACS 5-Year PUMS and Crosswalk Between 2013 MSAs and 2010 PUMAs
from the US census bureau.  


## Model Overview
