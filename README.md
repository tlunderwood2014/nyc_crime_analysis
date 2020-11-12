# Project_5
## New York Crime Anaysis

-----------
### Table of Contents
[Executive Summary](https://git.generalassemb.ly/johnlawless/Project_5/#executive-summary)

[Folder Structure](https://git.generalassemb.ly/johnlawless/Project_5/#folder-structure)

[Problem Statement](https://git.generalassemb.ly/johnlawless/Project_5/#problem-statement)

[Data Acquisition](https://git.generalassemb.ly/johnlawless/Project_5/#data-acquisition)

[Data Description](https://git.generalassemb.ly/johnlawless/Project_5/#data-description)

[Software Requirements](https://git.generalassemb.ly/johnlawless/Project_5/#software-requirements)

[Data Cleaning Steps](https://git.generalassemb.ly/johnlawless/Project_5/#data-cleaning-steps)

[Exploratory Data Analysis](https://git.generalassemb.ly/johnlawless/Project_5/#exploratory-data-analysis)

[Data Processing](https://git.generalassemb.ly/johnlawless/Project_5/#data-processing)

[Engineer Features](https://git.generalassemb.ly/johnlawless/Project_5/#engineer-features)

[Modeling](https://git.generalassemb.ly/johnlawless/Project_5/#modeling)

[Evaluation](https://git.generalassemb.ly/johnlawless/Project_5/#evaluation)

[Conclusion](https://git.generalassemb.ly/johnlawless/Project_5/#conclusion)

[Next Steps](https://git.generalassemb.ly/johnlawless/Project_5/#next-steps)


-----------
## Executive Summary
---
The costs and effect of crime touches everyone to some degree. We have been hired by a client who is interested in learning more about the social impact of crime in New York City. To do this, we are first conducting a study to identify any trends we can find: what factors play a significant role in increasing the occurence of crime in the city?

To do this, we will first explore the data we have collected, including complaints of criminal activity logged by the NYPD, the location, various demographics of the victims and suspects, location data, income, and more. Preliminarily, we suspect that the highest predictor of crime will be location, and will therefore build supervised models to predict both the Borough of New York City the complaint is filed in, and the precinct that reponds to the complaint. 

After this, we will conduct an unsupervised model on the data, to try and identify any other less obvious trends that would be beneficial to conduct further studies on in follow up data collection and analysis projects.

**ORIGINAL The purpose of this project is to examine the social impact of crime in New York City by predicting its occurance. With this prediction the city can properly allocate resources to facilitate a healthier community with less crime. **

aksfakjdsfa


-----
## Folder Structure
```
|__ code
|   |__ part_1_data_cleaning.ipynb      
|   |__ part_2.1_eda_crimes.ipynb
|   |__ part_3_preprocessing_and_feature_engineering.ipynb 
|   |__ part_4_modeling.ipynb 
|__ data
|   |__ data_description.txt
|   |__ complaints_2018_final.csv
|   |__ .csv
|   |__ .csv
|   |__ .csv
|__ images
|   |__ 1_remove_outliers.png
|   |__ 2_numerical_distribution_fit.png
|   |__ 3_categorical_boxplot.png
|   |__ 4_categorical_anova.png
|   |__ 5_corelation_feature_feature.png
|   |__ 6_corelation_feature_feature.png
|   |__ 7_numerical_transformation.png
|   |__ 8_categorical_encoding.png
|   |__ 9_model_coefficient.png
|   |__ 10_numerical_transformation.png
|   |__ 11_error_plot.png
|   |__ age_group_by_sex.png
|   |__ crime_by_amount_type.png
|   |__ crime_by_boro.png
|   |__ crime_distribution_by_neighborhood.png
|   |__ crime_per_boro_2.png
|   |__ felony_vs_misd.png
|   |__ nviolent_per_boro.png
|   |__ suspects_by_age.png
|   |__ suspects_by_sex.png
|   |__ violent_boro.png
|   |__ violent_nonviolent_amounts.png
|__ README.md
```


-----
## Problem Statement
Jasdckjabsdkcjbnc


-----
## Data Acquisition
Jasdckjabsdkcjbnc


-----------
## Data Description
The data was downloaded from [NYafasf](www.asfadsfasdf.com). 

This data is a breakdown of every criminal complaint report filed in NYC by the NYPD in 2018. This data was manually extracted every quarter and reviewed by the Office of Management Analysis and Planning. 

Each record represents a criminal complaint in NYC and includes information abot the type of crime, the location and time of enforcement. In addition, information related to victim and suspect demographics is also included. This data can be used by the public to explore the nature of criminal activity. 

Columns that were added to the originally colelcted data:

| POPULATION | AREA | COUNTY | ZIPCODES | ADJUSTED_GROSS_INCOME | AVG_AGI | TOTAL_INCOME_AMOUNT | AVG_TOTAL_INCOME  | TAXABLE_INCOME_AMOUNT | AVG_TAXABLE INCOME |  

These columns came from.......gsdgsdgdfg

There are 34 features and 91,7456 values within each feature of the used data. Each features, and the description of these features can be found in this [file](./data/data_description.txt). 


-----------
## Software Requirements
- pandas
- numpy
- missingno

Jasdckjabsdkcjbnc


-----------
## Data Cleaning Steps
35 columns were dropped from the original data due to duplicated information, extraneous features, or large amount of null values. 

Missing values in remaining columns were carefully evaluated and replaced as summarized in the table below

**Features with `NaN`**|**Pre-clean Amount**|**Description of `NaN`**|**Replacing Value**|
:-----:                |    :-----:         |            :-----:     |    :-----:        | 
susp_sex               |229263              |Missing or 0 value      |     u             |
susp_race              |229263              |Missing or 0 value      |     unknown       |
susp_age_group         |229263              |Missing or incorrect    |     0             |
vic_age_group          |113                 |Missing or incorrect    |     0             |
vic_race               |113                 |Missing or 0 value      |     unknown       |
vic_sex                |113                 |Missing or 0 value      |     u             |
ofns_desc              |26                  |Missing                 |     unknown       |
pd_cd                  |619                 |Missing                 |     0             |
boro_nm                |630                 |Missing                 |     0             |
prem_typ_desc          |3853                |Missing                 |     unknown       |
patrol_boro            |619                 |Missing                 |     unknown       |
prem_typ_desc          |3853                |Missing                 |     unknown       |
zipcodes               |5401                |Missing                 |     unknown       |
pd_desc                |619                 |Missing                 |     unknown       |


-----------
## Exploratory Data Analysis
Jasdckjabsdkcjbnc


-----------
## Data Processing
Jasdckjabsdkcjbnc


-----------
## Engineer Features
Jasdckjabsdkcjbnc


-----------
## Modeling
Jasdckjabsdkcjbnc


-----------
## Conclusion
asdvavav


-----------
## Next Steps
asdfadsvsdc



