![](https://cdn-images-1.medium.com/max/800/1*NI9v47AHXmtwu2jv2cvWCg.jpeg)

# Metropolitan Trends Analysis for Home Improvement Spending in 2015 and
Projection for 2017

## Analysis in Python Pandas and Graphs in Plotly & Seaborn

**The Data Set**: from [Joint Center for Housing Studies at
Harvard](http://www.jchs.harvard.edu/research-areas/reports/demographic-change-and-remodeling-outlook).
I used a subset of the same data set in my [previous
post](https://medium.com/@manjula.mishra/home-remodeling-analysis-turned-excel-data-handling-in-python-e1115f8302e4)
published in [Towards Data Science](https://towardsdatascience.com/).

**Features of Interest in This Data Set:**

* 25 US metropolitan areas
* Median income: 2015
* Median home value: 2015
* ‘Discretionary’ (kitchen, bathroom, room additions, and outside attachments),
‘Replacement’(exterior, interior, and system and equipments), and
‘Other’(disaster repair, improvements to lot or yard) home improvement
expenditure categories
* Total expenditure on home improvement in 2015
* Projected Real Annual Percent Change, 2017

**Key Takeaways From My Analysis:**

* Interactive graphs for a closer look at the numbers
* Discretionary and replacement spending show negative relation
* Median home value and median income are (obviously) highly correlated related
* Average expenditure per owner (on home improvement) and median home value don’t
tell the whole story
* 2015 home improvement expenditure trends and 2017 projected
* Correlation matrix
* Attached Jupyter notebook at the end to see the raw work

Let’s start digging into analysis now. Below is the correlation matrix table for
various features. It’s interesting to see a **negative correlation** between
median income and percent of expenditure on replacement category, while median
income and expenditure on discretionary home improvement shows a **positive
correlation**. Does it mean more people like remodeling their kitchen/bath/ or
add another room/outdoor attachment as their income increase? Or items on
replacement category do not need to changed? Or homeowners like modernizing
their homes as the income increases? Interesting hypotheses, but I didn’t
analyze enough data to conclude any of that.

![](https://cdn-images-1.medium.com/max/800/1*g2htkeMxlwwN8jrk5DBBbQ.png)

The graph below shows the intensity of correlations. Some of the negative
correlations are surprising to me. For example, median home value and
expenditure on replacement category. It will be interesting to investigate if
spending on beautifying the interiors like kitchen or/and adding more rooms
drives the home value up. This is out of scope of my analysis in this post.

![](https://cdn-images-1.medium.com/max/800/1*PbaBFFVM7fO2XAT2sSpokg.png)

First graph show a clearly negative relationship between discretionary versus
replacement expenditure percentages. Discretionary expenditure includes kitchen,
bathroom and outdoor patio etc, while replacement expenditure consists of items
like roofing, windows, insulation. From the chart, it looks like that homeowner
can afford/choose to spend on either one category not both.

Some metropolitan areas are more expensive/valued more than the others. It’s
clear that cities with higher median income have more expensive housing.

Since we just talked about the median home value and incomes, it would be
interesting to see the average per home owner spending on home improvements in
the same metropolitan areas. Looking at the graph, the average per owner
spending looks flatter.

The above graph doesn’t show average per owner spending very clearly. So I
plotted it below :

The home improvement spending in 2015 and projections for 2017 almost perfectly
overlaps for all 25 metropolitan areas. It’s both good or bad news for the
businesses. Good news because the market looks stable without any shock and
speculation, but on the other hand it also means less chances of extra growth or
spurt in the market.

The above graph compelled me to plot the projected real annual percentage change
in the graph below. Milwaukee, WI and Kansas City, MO project the highest growth
while Houston, TX and and Miami, FL show negative projections.

My Jupyter notebook showing the dataset and raw work.

* [Data Science](https://towardsdatascience.com/tagged/data-science?source=post)
* [Housing
Market](https://towardsdatascience.com/tagged/housing-market?source=post)
* [Excel](https://towardsdatascience.com/tagged/excel?source=post)
* [Pandas](https://towardsdatascience.com/tagged/pandas?source=post)
* [Plotly](https://towardsdatascience.com/tagged/plotly?source=post)

### [Manjula Mishra](https://towardsdatascience.com/@manjula.mishra)

Data Scientist in Training, Masters in Economics

### [Towards Data Science](https://towardsdatascience.com/?source=footer_card)

Sharing concepts, ideas, and codes.
