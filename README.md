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
The costs and effects of crime touches everyone to some degree. With the increased wave of crime seen within the city of NYC, the city is trying to reduce these costs and effects for its population. They hypothesize that different community programs might help, however they do not know which programs will create the most positive impact.

We have been hired to analyze NYC population demographics and crime data to provide helpful information for the city so they can better examine the social impact of crime in their city. Knowing this social impact, will help them better determine how to allocate their resources amongst these community programs and create a healthier NYC.

To do this, we will first explore the data we have collected, including complaints of criminal activity logged by the NYPD, the location, various demographics of the victims and suspects, location data, income, and more. Preliminarily, we suspect that the highest predictor of crime will be location, and will therefore build supervised models to predict both the Borough of New York City the complaint is filed in, and the precinct that reponds to the complaint. 

After this, we will conduct an unsupervised model on the data, to try and identify any other less obvious trends that would be beneficial to conduct further studies on in follow up data collection and analysis projects.


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
This step was conducted repeatedly throughout the course of the project, with the most significant EDA conducted at the very end of the project. The first steps of analysis were done using conventional methods, exploring the dataset as imported, searching for strong learners to pass into an estimator for the sake of classification/regression modelling. 

Following this (and as a result of poor accuracy scores in modelling), an attempt at Unsupervised modeling was begun, in order to better understand the data we are working with. This was done in multiple steps:

- First, an attempt at a KMeans cluster was undertaken. However, given the immense size of the data, this proved to require prohibitively large time requirements, given the dealine of our project deliverables. 

- In response to this, a sample of about 35% of the data was taken in order to complete this study with the time remaining. Using the elbow method, several values of k in a kmeans were conducted, as well as a DBScan. However, these proved to return very poor silhouette scores. This was suspected to be because the data was just so complex that the model was unable to properly measure correlations.

- Therefore, the model was simplified using a Principle Component Analysis to 10 features, which were then passed once again into a KMeans Analysis, after again using the elbow method. This resulted in greatly imporved results.


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

1) Supervised Model Conclusions

- We can use the coefficients created from our linear regression model to make some tentative observations regarding current law enforcement practices.  For example, as this data was taken from 2018, it’s no surprise that marijuana possession complaints were used by the model to assess how many arrests were made.  The publicly available arrest data can confirm that this crime constituted a high number of arrests.  In particular, it may be said that these types of complaints may be made less frequently without already being attached to an arrest.

- We also have some data that seems to have an inverse effect on the expected numbers of arrests, such as complaints made for motorcycle theft.  This is also expected, as there are frequently reports made for certain crimes without arrests to go with them.
Population demographic data is also included within, which may show some indication of how the demographics of the people that live in an area can affect the rates of law enforcement, independent of the frequency of the occurrence of crime.


2) Unsupervised Model Conclusions:

- Looking at the similarity of boroughs with the total count of complaints in New York, there appears to be unique features that separate the clusters that my model created.

- Stronger than this is the Latitude and Longitude coordinates, which clearly show the separation of each cluster. Given that many of these clusters are touching, I do think it likely that some other features separate these clusters clearly along location lines. 

- Despite the relatively poor performance of the classification model in the Neighborhood Analysis Notebook, this result is a clear indication that location is an imortant feature to identify differences in the impact of crime in New York - specifically, according to the map created above.

*Important Caveat to these findings - due to processing and time limitations, this study had to be done on a small sampling of the entire data. This analysis would ideally be done on the entirety of the dataset, to hopefully find even stronger correlations.*

2) Modeling Conclusions:

- HERE LIES THE TEXT THAT WILL ONE DAY DESCRIBE OUR MODEL IN ALL ITS GLORY


-----------
## Next Steps
- Sadly, the income information that was drawn for this project was merely an estimation that was too general to yield helpful results. However, it is still highly suspect to be a strong predictor of the number of and type of crimes committed. Perhpas following more recent Census and IRS data to the specific regions given above, we can analyze these differences to evaluate their effects on crime.

- This data is clearly showing differences based on these geographic locations. I would recommend a thorough survey of each of these 8 regions displayed (as cluster 8, the 9th cluster, is practically not visible on the plot). An analysis of their specific traits for comparison would be helpful here. In addition, a study of each region's specific history, local laws/leaders, current events, and even a consultation with individuals knowledgeable about the areas of each cluster would lead to more advanced insight, and should likely be the primary direction of a followup study.