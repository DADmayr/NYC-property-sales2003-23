# Analysis of New York City Property Sales (Jan 2003 - Mar 2023)
Project to practice Python and tableau skills.

## The Project
During a trip to New York City in 2023, I visited the Tenement Museum. The museum looks at tenements (i.e. buildings offering living space for rent) in NYC in both the past and the present. In doing so it also looks at who owns buildings and how this affects the living conditions of those who live in the buildings. This made me look for data on properties in NYC and eventually prompted me to analyse the property sales data made available by the NYC Department on Finance. The key questions I was interested in were:
+ Does price development differ throughout NYC’s five boroughs and if so, how does it differ?
+ Do factors such as property size or type of use affect prices?
+ Did outside effects such as financial or health crisis impact property sales?

## The Data
The data is open, administrative data collected and made available by the NYC Department of Finance, an official governmental source. It is provided separately per year and borough (Manhattan, Bronx, Brooklyn, Queens, Staten Island) for past years. Furthermore rolling sales data is available for the past 12 months, i.e. at the time of retrieval for April 2022 – March 2023. Data is provided in the form of .xlsx (from 2018) or .xls files (until 2017).

Data for the period 2003 – 2022 was downloaded [here](https://www.nyc.gov/site/finance/taxes/property-annualized-sales-update.page). 
Rolling sales data was downloaded [here](https://www.nyc.gov/site/finance/taxes/property-rolling-sales-data.page). 
The data is complemented by a [glossary of terms](https://www.nyc.gov/site/finance/taxes/glossary-property-sales.page) and a [building classification codes list](https://www.nyc.gov/assets/finance/jump/hlpbldgcode.html). 
All data was accessed and retrieved on 7 May 2023.

The volume of the data exceeds GitHub’s upload limits and is therefore not made available here. 

In addition to the data from the NYC Department of Finance a shapefile (GeoJSON) was downloaded [here](https://cartographyvectors.com/map/508-new-york-city-boroughs-ny). 
The shapefile was accessed on 2 June 2023.

## The Results of the Analysis
Key results of the analysis are visualised in a tableau storyboard [here](https://public.tableau.com/app/profile/daniela.dietmayr/viz/NewYorkCityPropertySales2003-23/NYCpropertyprices2003-23).

Before key results were visualised with tableau, analysis of the data with Python yielded the following results: 
+ There are significant gaps in the data, in particular with regards to variables on property size in number of units (residential, commercial, and total) and land/gross square feet. Therefore, these variables proved less useful in explaining and predicting sale prices than intended when sourcing the data.
+ A significant number of observations recorded by the NYC Department of Finance falls into the category of ownership transfers at sale prices of 0 US$. The share of ownership transfers is lowest in Manhattan (18%) and highest in Brooklyn (35%).
+ Neither linear regression analysis nor cluster analysis explains property prices very well. This may however be due to the gaps in the data mentioned above.
+ Cluster analysis does however unveil insights about the age of properties sold across boroughs and how the boroughs differ. For instance, in Manhattan and the Bronx most properties sold are old (44% and 48% respectively) while Staten Island has by far the highest share of new properties sold (47%).
+ Time series analysis showed that price development since 2003 differed significantly across boroughs, prices are by far highest in Manhattan. 
+ Time series analysis also showed that property use (primarily residential vs. non-residential) has a significant impact on property prices with non-residential sales being both higher and more volatile. 
+ Last, but not least the effects of the global financial crisis after the crash of Lehman Brothers in 2008 and the Covid-19 pandemic are visible in the data. At the same time, the data also unveils an interesting detail about Staten Island: while all other boroughs seemed to be impacted by the Covid-19 pandemic, Staten Island did not see a drop in property prices.
