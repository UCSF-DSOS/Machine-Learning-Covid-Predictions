## Description

This repository contains materials for a hands-on workshop introducing supervised machine learning with Python and scikit-learn. Using COVID-19 clinical data from Carbon Health and Braid Health, participants explore how symptoms, comorbidities, vital signs, and other predictor variables can be used to estimate the probability of a positive or negative COVID-19 test.

The workshop builds on earlier exercises using Python, pandas, and SQL to explore COVID testing data. Here, the focus shifts from querying and summarizing data to using that data to build classification models with scikit-learn. Participants work through the process of preparing data for machine learning, selecting predictor and outcome variables, building models, and examining model output.

The goal of the workshop is to develop practical machine learning skills rather than to build a highly predictive model for COVID-19. Although some symptoms or combinations of symptoms may correlate with test results, the COVID dataset is used primarily as a way to explore how data and algorithm choices influence a machine learning model. The techniques introduced here can be applied to other datasets and classification problems.

## Objectives

Through a series of hands-on exercises with Python, pandas, SQL, and scikit-learn, participants will learn to:

- Identify predictor and outcome variables for a supervised machine learning task
- Prepare tabular data for use with scikit-learn
- Handle missing values prior to building a machine learning model
- Convert categorical and Boolean values into numerical representations
- Explore relationships between predictor variables and outcomes using SQL and pandas
- Build a classification model using scikit-learn
- Use a random forest model to estimate the probability of an outcome
- Examine how training data and algorithm choice influence model output
- Use small datasets to investigate how machine learning models work

### Prerequisites

This workshop is intended for participants who have intermediate programming experience with Python and SQL. Participants should be comfortable working with Python variables, lists, loops, and pandas DataFrames and should have some experience writing SQL queries.

Participants without this background may still find it useful to read through the materials, watch the accompanying workshop recording, or attend the workshop to become familiar with the concepts and techniques.

### Instructor

Geoffrey Boushey is a computational and research data science specialist at UCSF and a member of the Library's Data Science and Open Scholarship team. Geoff teaches courses and provides consultations on foundational programming, data analysis, and AI techniques including Python, SQL, Unix, and Version Control.

## Data

This workshop uses data from the Coronavirus Disease 2019 (COVID-19) Clinical Data Repository made available by Carbon Health and Braid Health.

[https://covidclinicaldata.org](https://covidclinicaldata.org)

The dataset includes COVID-19 test outcomes along with patient characteristics such as symptoms, comorbidities, and vital signs. These variables provide an example classification problem in which information about an observation is used to estimate the probability of an outcome.

### Loading Data For Workbooks

To run the notebooks for this workshop, you'll need to copy the data from the covidclincaldata repostitory into a local data repository in your jupyter workspace. Alternatively, you can load the data directly from the csv links in the repository. Techniques for this are covered in "Intro to Python Part 2" and "Analyzing Data with SQL and Python". 

https://github.com/mdcollab/covidclinicaldata/tree/master/data/

### Data Citation

```bibtex
@dataset{2020covidclinicaldata,
  author =       {Carbon Health and Braid Health},
  title =        {Coronavirus Disease 2019 (COVID-19) Clinical Data Repository},
  howpublished = {Accessed from \url{https://covidclinicaldata.org/.}},
  year =         2020,
  version =      {10-20-2020}
}
```

## Workbooks

### [query-estimates.ipynb](query-estimates.ipynb)

This workbook uses SQL, Python, and pandas to investigate the frequency of positive and negative COVID-19 tests associated with different symptoms, comorbidities, and vital signs.

### [rf-estimates.ipynb](rf-estimates.ipynb)

This workbook uses scikit-learn to build a machine learning model that estimates the probability of a positive or negative COVID-19 test based on symptoms and other predictor variables.

The goal is not to produce a highly predictive COVID-19 model, but to introduce techniques for analyzing a dataset using scikit-learn, random forests, and other machine learning algorithms.

### [clean-data.ipynb](clean-data.ipynb)

This workbook contains code for preparing the COVID-19 data for use with scikit-learn. It demonstrates how to read data from multiple CSV files into a pandas DataFrame, handle missing values, convert positive and negative test results and other categorical values into numerical representations, and write the prepared data to a CSV file for use in a machine learning model.

### [rf-sample-data.ipynb](rf-sample-data.ipynb)

This workbook builds and populates a scikit-learn model using a very small dataset. Although the four-row dataset is too small to produce reliable predictions, it provides an opportunity to examine how changes in training data and algorithm choice can influence model output.

### [sql-query-page.ipynb](sql-query-page.ipynb)

This workbook provides a workspace for ad hoc SQL queries and pandas operations for exploring the COVID-19 dataset.
