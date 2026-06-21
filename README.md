Enhanced Recovery After Surgery (ERAS) DID Analysis
This project analyzes whether implementing an Enhanced Recovery After Surgery (ERAS) protocol reduced average hospital length of stay (LOS) using a Difference-in-Differences (DID) approach.
Project Overview
Treatment group: Hospital B, which implemented ERAS starting in 2015.
Control group: Hospital A, which did not use ERAS.
Outcome: Average hospital length of stay (LOS) in days.
Study period: 2010–2019, with a focused comparison on 2014 and 2015 for the DID estimate.
Methods
The analysis includes:
Loading the dataset from eras_df.csv.
Exploring the data and printing the head of the dataset.
Plotting LOS trends for Hospital B.
Plotting LOS trends for both hospitals to assess the parallel trends assumption.
Restricting the dataset to 2014–2015.
Calculating within-hospital changes in LOS.
Computing the Difference-in-Differences estimate.
Creating treatment and time indicator variables.
Fitting a linear regression model with an interaction term.
Extracting the ATT from the interaction coefficient.
Expected Result
The ATT is approximately -0.75 days, meaning ERAS reduced average LOS by about 0.75 days (about 18 hours) at Hospital B compared to what would have been expected without ERAS.
Files
notebook.Rmd — R Markdown notebook containing the full analysis.
eras_df.csv — Dataset used for the analysis.
Requirements
This notebook uses the following R packages:
dplyr
ggplot2
How to Run
Open notebook.Rmd in RStudio.
Make sure eras_df.csv is in the same directory.
Knit or run the notebook to reproduce the analysis and plots.
Notes
The DID approach assumes the parallel trends condition holds before treatment.
The interaction term in the regression model (treat:time) is the ATT.# ersa