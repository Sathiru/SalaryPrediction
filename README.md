# Salary Prediction Portfolio
## Problem Definition:
The purpose of this project is to predict the salary based on various factors like jobtype, degree, subject major in terms of education, type of industry, years of experience and miles from metropolis.

## Motivation:
 - Can be used by organisation to set tha salary range for employees and a reference point while creating new job posting.
 - Can be used by the government to analyse the trends in job market/economy growth and salary range to the corresponding.
 - Can be a reference for any individual who is in the job to verify for validation or for applying new jobs.

## Datasets:
**train_features.csv:** Each row represents an observation for each individual job posting. The "jobId" column is unique to each job posting and the other columns are the different features of the job postings. The file has eight(8) columns.

**train-salaries.csv:** Each row is a unique job posting with its corresponding salary. The file contains two (2) columns. The file is combined with train_features.csv to train the machine learning models.

**test_features.csv:** Similar to train_features.csv, each row in this file is metadata for each individual job posting. The file has eight (8) columns and is used to predict the new salaries.

## Features Description:

JobId: Primary Key - unique identifier for each job posting

companyId: Foreign Key - unique identifier for each company corresponding to the job posting

jobType: Job level (e.g janitor, manager, CEO)

degree: Educational level (e.g Bachelor, Doctoral)

major: Subject major in education (e.g. Businesss, Literature, engineering)

industry: field or industry of the job posting (e.g engnieering, oil, finance)

yearsExperience: years of experience in that job(industry/domain)

milesFromMetropolis: distance away from the metropolis, in miles(mi)

salary: salary paid for the job, in thousands US dollars; target variable

## Data Preprocessing:

**Cleaning and Explanatory Data Analysis

Checked for null values

Checked for duplicate values

Check for outliers Deleted the rows with salary < 0. Calculated the quantile value for 75% and 25%, the value above 75% - 220,000 are tend to be outliers. Verfied and validated the data as those rows are legidimate and those salary belongs to c-type jobs or from highly paid industry like oil, finance or web.

image

The target variable salary is normally distributed with right skewness, which is due to outliers and verified.

Performed explanatory data analysis to learn more about the relation between each feature and the target variable,

Major versus Salary

![image](images/salary vs major.png)

image
