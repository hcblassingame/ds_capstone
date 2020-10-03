---
title: "Hurricane Track & Intensity Investigation"
author: "Henry Blassingame"
date: "02 OCTOBER 2020"
output:
  html_document
---

# Capstone Project
### Henry Blassingame
### September 2020
---



### Problem
- Review of over 100 years of Hurricane Data from the National Weather Service.
Create some visualizations to look at the increase in number of storms and
increase in storm intensity over time.

- Compare Linear Regression to Random Forest to see which one performs better at predicting the number of storms per year.

### Approach
The data set includes storms from 1851 to 2015, with varying degrees of
completeness (and presumably accuracy, especially for the older storms.)
Furthermore, there are problems with the formatting of dates in the dataset,
as well as observation times, which are stored separately from the dates.
Another problem is that Latitude and Longitude are stored as strings, and need
to be re-formatted as numbers and adjustment made for longitudes East and West
of Greenwich.

Due to the incompleteness of much of the data before 1900, this was removed before visualization and analysis.

### Tools Used in the Project

#### Data Cleanup and Manipulation
- Excel
- RStudio

Data cleanup was performed in two phases: one in Excel, and another in R. One
problem with data cleanup in Excel is that it does not work with dates before 1900.
So, while many tasks (re-formatting times, fixing Latitude and Longitude, calculating storm categories based on wind speed) are very simple to perform in Excel, the date manipulation was best left to R.

Due to the incompleteness of much of the data before 1900, this was removed before visualization and analysis.

#### Visualization
- RStudio
- Tableau

The visualizations for landfall on the US coast and the bar and whiskers plot of landfall wind speeds by state were based on Giovanni Maccioni's Kaggle page (https://www.kaggle.com/gi0vanni/analysis-on-us-hurricane-landfalls/report),  but modified based on my own data cleanup and manipulation, and to modify several other aspects.

The graph of number of storms per year broken down by category/strength is a link to a previous project I completed in Tableau.


#### Machine Learning
The challenge with this data was to try to find a good fit for Machine Learning, and to decide on which method made the most sense. The data did not lend itself to predicting direction (without some heavy manipulation to derive this from the coordinates and next/previous observations) or even storm strength. At the end, the simplest metric to determine was how many storms there would be in a given year based on the data.

This was modeled using both Linear Regression and Random Forest models, and the residuals from both were plotted, showing a higher correlation between the data and the Random Forest model.




### Repository Contents:

|Filename              | Description                                           |
|----------------------|-------------------------------------------------------|
| README.md            | This document.                                        |
|Atlantic_Updated.csv  | Hurricane data, cleaning performed in Excel.          |
|Atlantic.csv          | Hurricane Data in its raw format, prior to any scrubbing|
|BLASSINGAME_CAPSTONE.rmd | R Markdown file for the project                    |
|BLASSINGAME_CAPSTONE.html | knitted output of the project                     |
