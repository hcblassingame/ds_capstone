# Capstone Project
### Henry Blassingame
### September 2020
---



### Problem
Review of over 100 years of Hurricane Data from the National Weather Service.
Create some visualizations to look at the increase in number of storms and
increase in storm intensity over time.

### Approach
The data set includes storms from 1851 to 2015, with varying degrees of
completeness (and presumably accuracy, especially for the older storms.)
Furthermore, there are problems with the formatting of dates in the dataset,
as well as observation times, which are stored separately from the dates.
Another problem is that Latitude and Longitude are stored as strings, and need
to be re-formatted as numbers and adjustment made for longitudes East and West
of Greenwich.

Data cleanup was performed in two phases: one in Excel, and another in R. One
problem with data cleanup in Excel is that it does not work with dates before 1900.
So, while many tasks (re-formatting times, fixing Latitude and Longitude,
calculating storm categories based on wind speed) are very simple to perform in Excel, the date manipulation was best left to R.

I decided to use Tableau for my data visualization task, since it produces much neater output than R, but also does so more simply.

### Repository Contents:

|Filename              | Description                                           |
|----------------------|-------------------------------------------------------|
| README.md            | This document.                                        |
|Atlantic_Updated.csv  | Hurricane data, cleaning performed in Excel.          |
|Trimmed_data.csv      | Hurricane Data, further processed in R and unused columns removed.|
