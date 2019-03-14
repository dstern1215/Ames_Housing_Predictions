{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "\n",
    "# Project: Ames Dataset House Price Prediction\n",
    "_Author: Daniel Stern_\n",
    "\n",
    "## Problem Statement\n",
    "\n",
    "The process of buying or selling a house is something that most have at least some familiarity with. _\"Location, Location, Location!\"_ is a frequently cited axiom, but is it actually true in practice? And what about all of the other significant and peripheral features of a house?\n",
    "\n",
    "Using the Ames Housing Dataset (consisting of 2930 observations, and 82 variables), this project will explore the importance of certain housing features, and attempt create a model that predicts the value of a given home based on those features. Based on that model, the end user will be able to focus on the most important features of a home relative to its final Sale Price, to aid in their effort to increase ROI.\n",
    "\n",
    "The model's performance will ultimately be judged on Root Mean Squared Error (RMSE), which can be interpreted as\n",
    "\n",
    "> The square root of the variance of the residuals. RMSE is a good measure of how accurately the model predicts the response, and it is the most important criterion for fit if the main purpose of the model is prediction. [Source](https://www.theanalysisfactor.com/assessing-the-fit-of-regression-models/)\n",
    "\n",
    "## Executive Summary\n",
    "\n",
    "The enclosed technical report analyzes the Ames Housing Dataset to see which features have the strongest relationship with Sale Price. The report contains detailed plots of most of the relevant attributes, as well as an in-depth analysis of many of the features. \n",
    "\n",
    "The report ultimately concludes that Overll Quality rating and SF/Area pertaining to living area are the most important factors, and recommends focusing on increasing the quality of some of the other Quality-related attributes (such as Kitchen and Exterior) to most effectively increase the value of the home.\n",
    "\n",
    "Link to \n",
    "### Contents:\n",
    "- [Notebook 1](./Code/Notebook1_CleaningTrainingData.ipynb)\n",
    "- [Notebook 2](./Code/Notebook2_EDAofFeatures.ipynb)\n",
    "- [Notebook 3](./Code/Notebook3_ManualFeatureEngineering.ipynb)\n",
    "- [Notebook 4](./Code/Notebook4_VarianceThreshold.ipynb)\n",
    "- [Notebook 5](./Code/Notebook5_FunctionsForMatchingTestWithTrain.ipynb)\n",
    "- [Notebook 6](./Code/Notebook6_Modeling.ipynb)\n",
    "- [Conclusions and Recommendations](#Conclusions-and-Recommendations)\n",
    "\n",
    "## Data Dictionary\n",
    "\n",
    "|Feature|Type|Dataset|Description|\n",
    "|---|---|---|---|\n",
    "|**Total SF**|float|test/train|An aggregate of all columns labeled with 'SF' in the dataset.\n",
    "|**Total Living Space**|float|test/train|Sum of 'Total SF' and 'Gr Liv Area'.\n",
    "**Qual_LivingArea** |float|SAT|A metric that combines Overall Quality and Total Living Space. Calculated as:<br /> ```(starter['Total Living Space'] / 1000) * (starter['Overall Qual'])```\n",
    "\n",
    "## Conclusions & Recommendations\n",
    "\n",
    "After analyzing the data, a lot of the variables tend to be co-linear with each other, and deliver redundant information. A house's Overall Quality and living space (which can be determined by a number of co-linear varibles) have the greatest impact on a house's Sale Price.\n",
    "\n",
    "Clear trends between a house's Kitchen Quality and Exterior Quality were also discovered, as well as the date that a house was remodeled. Since these features can theoreticall be improved"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.0"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
