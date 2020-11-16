# Introduction

The first module of Intermediate Analytics focused on descriptive statistics and regression
analysis. With a concentration on generating data both numerically and graphically, the goal was
to both summarize as well as provide readable graphics as a way to consume a dataset. Utilizing
R as the tool of record, functions to generate various different graphs were applied to assess a
dataset on the diameter, height and volume for a set of 31 felled black cherry trees. In addition,
the use of regression analysis was employed for building multiple regression models assessing
both the accelerated testing of tire rubber and the measurements of twelve books composed of
thickness, height, width and weight. This report will provide the incorporated R coding and
outputs along with assessments of the results of the three aforementioned datasets.
# Descriptive-Statistics-and-Regression-Analysis

Descriptive statistics are an important summary component of a dataset. It can be
manufactured either numerically or graphically and forms a major component of nearly all
quantitative data analysis (A Research Guide, 2019). In particular it helps an audience
understand the tendency, pattern and/or trend of data. Regression analysis is an important
statistical method for identifying whether or not certain variables have an impact and/or
relationship on another. This can be done through a single or simple linear regression which
evaluates one variable’s impact against another, or a multiple regression which evaluates how
two or more variables impact another. What this allows is for predictive analytics to be
conducted. Through five-number summaries, various different graphs and both single and
multiple regression analysis we can evaluate different datasets and have a clearer understanding
of the data’s behavior contained within them.

# Five-Number Summaries

The initial objective from the learning module involved building out a five-number
summary on the R built-in dataset “trees”. Corrections had to be made to the dataset first, which
focused on amending the attribute header of “Girth” to the more appropriately labeled
“Diameter”. With this, both a standard summary was run along with a five-number. Both
summaries are similar with the five-number summary removing the mean and instead focusing
on the median as the “average” indicator. R code for these actions can be found in Figure 1,
while the output of the five-number summary can be seen in Figure 2.


<img width="402" alt="Screen Shot 2020-11-16 at 6 27 08 PM" src="https://user-images.githubusercontent.com/66921930/99321473-dfed8980-283b-11eb-80e4-cfc65d103a04.png">
