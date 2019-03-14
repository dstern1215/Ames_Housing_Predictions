
# Project: Ames Dataset House Price Prediction
_Author: Daniel Stern_

## Problem Statement

The process of buying or selling a house is something that most have at least some familiarity with. _"Location, Location, Location!"_ is a frequently cited axiom, but is it actually true in practice? And what about all of the other significant and peripheral features of a house?

Using the Ames Housing Dataset (consisting of 2930 observations, and 82 variables), this project will explore the importance of certain housing features, and attempt create a model that predicts the value of a given home based on those features. Based on that model, the end user will be able to focus on the most important features of a home relative to its final Sale Price, to aid in their effort to increase ROI.

The model's performance will ultimately be judged on Root Mean Squared Error (RMSE), which can be interpreted as

> The square root of the variance of the residuals. RMSE is a good measure of how accurately the model predicts the response, and it is the most important criterion for fit if the main purpose of the model is prediction. [Source](https://www.theanalysisfactor.com/assessing-the-fit-of-regression-models/)

## Executive Summary

The enclosed technical report analyzes the Ames Housing Dataset to see which features have the strongest relationship with Sale Price. The report contains detailed plots of most of the relevant attributes, as well as an in-depth analysis of many of the features. 

The report ultimately concludes that Overall Quality rating and SF/Area pertaining to living area are the most important factors, and recommends focusing on increasing the quality of some of the other Quality-related attributes (such as Kitchen and Exterior) to most effectively increase the value of the home.

### Contents:
- [Notebook 1 (Cleaning Training Data)](https://git.generalassemb.ly/dstern1215/project-2/blob/master/DanielStern_Ames/Code/Notebook1_CleaningTrainingData.ipynb)
- [Notebook 2 (EDA of Features)](https://git.generalassemb.ly/dstern1215/project-2/blob/master/DanielStern_Ames/Code/Notebook2_EDAofFeatures.ipynb)
- [Notebook 3 (Manual Feature Engineering)](https://git.generalassemb.ly/dstern1215/project-2/blob/master/DanielStern_Ames/Code/Notebook3_ManualFeatureEngineering.ipynb)
- [Notebook 4 (Variance Thresholding)](https://git.generalassemb.ly/dstern1215/project-2/blob/master/DanielStern_Ames/Code/Notebook4_VarianceThreshold.ipynb)
- [Notebook 5 (Functions for matching Test data with Train)](https://git.generalassemb.ly/dstern1215/project-2/blob/master/DanielStern_Ames/Code/Notebook5_FunctionsForMatchingTestWithTrain.ipynb)
- [Notebook 6 (Modeling)](https://git.generalassemb.ly/dstern1215/project-2/blob/master/DanielStern_Ames/Code/Notebook6_Modeling.ipynb)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**Total SF**|float|test/train|An aggregate of all columns labeled with 'SF' in the dataset.
|**Total Living Space**|float|test/train|Sum of 'Total SF' and 'Gr Liv Area'.
**Qual_LivingArea** |float|test/train|A metric that combines Overall Quality and Total Living Space. Calculated as:<br /> ```(starter['Total Living Space'] / 1000) * (starter['Overall Qual'])```

## Conclusions & Recommendations

After analyzing the data, a lot of the variables tend to be co-linear with each other, and deliver redundant information. A house's Overall Quality and living space (which can be determined by a number of co-linear varibles) have the greatest impact on a house's Sale Price.

Clear trends between several "Quality"-related variables (namely Kitchen Quality, Exterior Quality, Garage Quality, Basement Quality and Fireplace Quality) were also discovered, as well as the date that a house was remodeled. Since these features can be more directly improved upon compared to "Overall Quality", it is recommended that potential sellers/investors focus on upgrading the "Quality" of a home, to have the greatest potential impact on ROI.