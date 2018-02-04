#!/usr/bin/python

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

Senior_Employees14 = pd.read_csv("~/Senior employees 2014.csv")
print(Senior_Employees14)

Senior_Employees14.describe()

Senior_Employees14.head(2)

Senior_Employees14.tail(2)

Senior_Employees14.sample(2)

# Enable IPython to display matplotlib graphs.
%matplotlib inline

# We will read in the file like we did in above but I’m going to tell it to treat the date column as
# a date field (using parse_dates ) so I can do some re-sampling later.

Senior_Employees14 = pd.read_csv("~/Senior employees 2014.csv", parse_dates=['ApplicableDate'])
Senior_Employees14.head()

#Now that we have read in the data, we can do basic and quick analysis
Senior_Employees14.describe()

# We get NAN for many attributes because the value is missing or not applicable

Senior_Employees14.tail(2)

Senior_Employees14.sample(2)

%matplotlib inline

Senior_Employees14['Salary'].describe() # We look here at a single column (salary)

#Plotting some data

#We have our data read in and have completed some basic analysis. Let’s start plotting it.

#First remove some columns to make additional analysis easier.
employees = Senior_Employees14[['ApplicableDate','JobTitle','OrganisationalUnit', 'Salary', 'PensionContribution']]

employees.head()

Pension_group = employees.groupby('PensionContribution')
Pension_group.size()


Pension_total = Pension_group.sum()
Pension_total

my_plot = Pension_group.plot(kind='bar')
