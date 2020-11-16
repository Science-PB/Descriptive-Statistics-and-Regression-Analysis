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

The results of the five-
number summary can be
interpreted as follows, for
Diameter (in inches) the range of
the dataset is 8.3 to 20.6 with
25% of the data falling below 11, 50% falling below 12.9 and 75% falling below 16. For Height
(in feet), the range of the dataset is 63 to 87 with 25% of the data falling below 72, 50% falling
below 76 and 75% falling below 80. Our last tree attribute of Volume (in cubic feet) resulted in a
range of 10.2 to 77 with 25% of the data falling below 19.1, 50% falling below 24.2 and 75%
falling below 38.3.

<img width="386" alt="Screen Shot 2020-11-16 at 6 47 50 PM" src="https://user-images.githubusercontent.com/66921930/99321660-54c0c380-283c-11eb-8fa3-616cb5eaedf1.png">


From this we can see that of the three different tree attributes Volume appears to be the
one most prone to exhibiting outliers as the majority of the data points fall well below the max.
Height gives the impression of a more symmetric normal distribution with Diameter showcasing
more of a right-skewed distribution Overall, the five-number summary provides a satisfactory
numerical overview of the dataset allowing a foundational understanding of the main points
regardless of the quantity of variables in a data frame.

# The Power of Graphs

It is a common viewpoint that the use of graphs leads to an increased understanding and a
heightened portrayal of patterns and/or trends in a dataset. Utilizing the same “trees” data from
before, Figures 4, 6, 8 and 10, will present the data as a straight-line regression, a histogram and
density plot, a boxplot and finally as normal probability plots. What we can expect from these
graphical depictions is to visually be able to assess if a normal distribution exists for each of the
various attributes.
Single Line Regression is a statistical method utilized to summarize and study the
relationship between two quantitative variables (Penn State, 2018). This is done through the use
of a scatter plot which visually demonstrates if the relationship between the variables is positive,
negative, curvilinear or if no discernable relationship exists (Bluman, 2018, p.563). In the R code
provided in Figure 3, the use of the pairs function allows for the identification of linear
relationships for each variable combination in the dataset. Extrapolating this and focusing on
three main variable combinations, the abline function is applied to add a regression line with the
linear model (lm) function identifying the intercept and slope, as shown in Figure 4.
What Figure 4 showcases is that there is a positive relationship between each of the
variable combinations, however certain variables have a stronger linear correlation to each other.
In the case of the trees dataset, when Diameter is the dependent variable and Volume the
independent variable, a strong correlation exists as the residuals, or distance between the actual
value and predicted value are low. For the remaining showcased linear regressions, Diameter vs
Height and Height vs Volume, there is much less correlation between the two variables and the
residuals are much higher, meaning the fit is less ideal and the prediction of the dependent from
the independent will not be as promising.

<img width="681" alt="Screen Shot 2020-11-16 at 6 51 22 PM" src="https://user-images.githubusercontent.com/66921930/99321857-c39e1c80-283c-11eb-802c-61b37b7c2110.png">


While single line regression focused on comparing two variables within a dataset a
histogram is used to represent the distribution of data amongst a single variable. There are
multiple ways to showcase this, two popular methods being frequency and density. Density plotsaid in displaying where values are concentrated over an interval, this bears an advantage in that it
better represents the distribution shape as it is not affected by the bars of a histogram (The Data
Visualisation Catalogue, n.d.).
As represented in the R code in Figure 5, the probability function is inserted into the
histogram (hist) function to enable the histogram to plot density instead of frequency on the y-
axis. A density plot is then enabled through the use of the line function which superimposes it on
the histogram. What the histogram and density plots for the “trees” dataset end up showcasing is
a visual representation of the positively skewed Diameter and Volume variables with a roughly
normally distributed Height variable, further enforcing what was ascertained numerically from
the five-number summary. The histogram and density plots for “trees” can be seen in Figure 6. In
addition to the skew the Volume plot, displays a steep drop in the distribution leading to a
possible implication of the presence of outliers. Verification of the presence of outliers will be
able to be confirmed through the use of a boxplot.

<img width="652" alt="Screen Shot 2020-11-16 at 6 53 58 PM" src="https://user-images.githubusercontent.com/66921930/99322048-28f20d80-283d-11eb-8e5c-50408b302df1.png">
<img width="626" alt="Screen Shot 2020-11-16 at 6 54 04 PM" src="https://user-images.githubusercontent.com/66921930/99322049-298aa400-283d-11eb-8e90-688d6be7a951.png">

A boxplot is a graph that relies on the elements of a five-number summary. What it tells
the viewer is whether the distribution is symmetric, positively, or negatively skewed. It does this
through both the median location as well as the line length (Bluman, 2018, p.170). According to
the boxplot results for the “trees” dataset shown in Figure 8 with R coding provided in Figure 7,
it can be deduced that the sample trees diameters and volumes are positively skewed, while their
height is roughly symmetric. In addition to this, it is important to note the existence of an outlier
in the Volumes data which could indicate an experimental error as well as cause disruptions in
the analysis of the data as it affects both the mean and median.

<img width="662" alt="Screen Shot 2020-11-16 at 6 55 37 PM" src="https://user-images.githubusercontent.com/66921930/99322166-5e96f680-283d-11eb-9347-bb1f1e76e1f7.png">

Another way of assessing whether or not a dataset is distributed approximately normal is
to use a normal probability plot (Engineering Statistics Handbook, n.d.). By applying the R code
in Figure 9 and implementing the function for a Q-Q plot which sets two sets of quantiles against
one another, the results in Figure 10 provide a quick visual to whether an assumption made on
the dataset being normally distributed is true. The assumption is that if both sets of quantiles originated from the same distribution the points of the scatterplot should form a relatively
straight line (Ford, 2015). A Simulation dataset is also included as a part of the visual to provide
a baseline. What we can interpret from Figure 10, is that both the Height and Diameter variables
have a noticeably more normal distribution than that of Volume, in that the points fall closer to a
straight line. The presence of outliers also is detectable in the Volume data from the Q-Q plot.

<img width="631" alt="Screen Shot 2020-11-16 at 6 56 57 PM" src="https://user-images.githubusercontent.com/66921930/99322243-93a34900-283d-11eb-802f-86f50e73d2ea.png">
<img width="656" alt="Screen Shot 2020-11-16 at 6 57 04 PM" src="https://user-images.githubusercontent.com/66921930/99322246-943bdf80-283d-11eb-9b4d-43531b72cc38.png">

# Multiple Regression Analysis

Multiple linear regression analysis has three major uses in statistics. These uses consist of
identifying the strength of the effect independent variables have on a dependent variable, as a
forecaster for how the dependent variable will change when the independent variables are
modified, and as a predictor for trends and future values (Statistics Solutions, 2020). Two sets of
data from R will be utilized to demonstrate the use cases of multiple regression, “Rubber” and
“oddbooks”. There are three variables in the “Rubber” data set, Loss (the abrasion loss in gm/hr),
Hardness (the hardness in Shore units) and Tensile (tensile strength in kg/sq m) while
“oddbooks” is composed of Thickness (mm), Height (cm), Width (cm), and Weight (g).
A starting foundation when working with any dataset is to understand the main summary
components of the data. Similar to the five-number summary referenced earlier but with the
addition of the mean, the summaries for “Rubber” and “oddbooks” can be found in Figure 11.


