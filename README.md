# **Instrumental Variable Analysis with Machine Learning**

## Overview
This analysis pretends to explore the application of a machine learning approach to a specific study, "The Long Term Effects of Africa's Slave Trade", to improve its results and interpretation. 

Applying machine learning to study the long-term effects of Africa's Slave Trade brings significant advantages. It handles complex data well, capturing non-linear relationships. By building predictive models and analyzing data, it can be revealed hidden patterns to understand better the impact nuances. Additionally, machine learning integrates diverse data sources, offering a comprehensive understanding across regions and populations, enhancing analysis depth and breadth.

## The Study

The study "The Long Term Effects of Africa's Slave Trade" by Nathan Nunn (2008) examines how the slave trades continue to affect Africa’s economy. Africa’s economic struggles in the late 20th century
stem from exploitation via slavery and colonialism. Previous studies connect colonialism to underdevelopment but lack empirical research on Africa’s slave trades. This paper aims to bridge this
gap by estimating exported slaves from Africa and studying their impact on current economic development

This analysis utilizes shipping records and historical documents to estimate the number of slaves exported from each African country during the slave trades. Combining this with contemporary economic data, it examines the correlation between historical slave exports and current economic performance. To assess causality, it employs instrumental variable analysis based on geographic distances from major slave markets, ensuring a robust analytical framework for exploring the slave trades’ long-term economic effects.

The findings reveal a significant negative relationship between the number of slaves exported from African countries during the slave trades and their current economic development. Those demonstrate that regions most affected by the slave trades are among the poorest today.

The study can be found in this link: https://www.jstor.org/stable/25098896

## Instrumental Variable using Machine Learning

### Method

This empirical exercise explores the application of Double Lasso Regression to the study while still incorporating the IV approach. 

Double Lasso Regression employs a two-step approach to enhance causal inference. It is a variable selection and regularization technique that helps to estimate causal effects and identify relevant variables in high-dimensional datasets. It can be particularly useful in this study because there may be many potential confounding variables and the goal is to identify the causal effect of the slave trade on economic performance.

### Objectives

1. To identify which variables (e.g., historical factors, socio-economic indicators) are most important in explaining the economic long-term effects.
2. To mitigate confounding bias and identifies variables that are likely to be causally related to the outcome of interest.
3. To make the model more interpretable and reduces overfitting.

### Data Sources

For Double Lasso analysis in the context of the long-term effects of Africa's slave trade, it is necessary the following data:

Outcome Variable: Economic developmnet measurement (real per capita GDP in 2000) used in the original analysis. Other years can be considered for this exercise. In addition, other development indicators can be considered such as health outcomes, social indicators, etc.

Treatment Variable: Information of the intensity or presence of the slave trade in different regions or countries in Africa. In the study, the instrumental variable used is distance from the trade route.

Covariates: A wide range of covariates including historical data (e.g., pre-slave trade economic indicators, population density), geographic factors, cultural factors, and any other variables that might affect both the treatment (slave trade) and the outcome.

*Some of the data mentioned before is already considered in the original study.*

## This Repository

This repository contains our analysis of the study "The Long Term Effects of Africa's Slave Trade."

This repository includes:

1.  The ReadMe file.
2.  The data: (slave_trade_QJE_New_Data.xlsx). This xlsx file includes not only the variables from the original dataset but also adds new variables that represent the log GDP for the period 2001 - 2022 and an average of GDP the same period.
3. The replication code of the original paper in Python and HTML versions. The replication uses the original varibles and the variables added.
4. The code used to create a more precise analysis, through Double Lasso, of the impact of the slave trade exposure on the current economic outcomes in African countries. Python and HTML versions are available
5. A template of the presentation of the analysis.
6. A complete report of the analysis.


