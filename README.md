# Exploratory Data Analysis (EDA) of King County Home Sales

## Objectives

This is my first EDA project and I will explore the King County Homes Sales data set. It includes homes sold between May 2014 and May 2015 in King County area. 
With this initial investigations I will gain insight into the dataset and will come up with advice to my imaginary client with respect to her specified requirements.   

## Business case

I assume to work for a client, Nicole Johnson, who is willing to buy a house in a lively and central neighbourhood in middle price class. At the end of the EDA I will provide her with information about the best timing to buy and which area would be the best to aim for. 

## Explanation of individual variables for King County Data Set

|Columns name | Description |
|---- | ------------- |
|house_id|unique identified for a house|
|date | house was sold|
|price| is prediction target|
|bedroomsNumber| # of bedrooms|
|bathroomsNumber| # of bathrooms|
|sqft_livingsquare|footage of the home|
|sqft_lotsquare|footage of the lot|
|floorsTotal|floors (levels) in house|
|waterfront| House which has a view to a waterfront|
|view| quality of view|
|condition| How good the condition is ( Overall )|
|grade| overall grade given to the housing unit, based on King County grading system|
|sqft_above|square footage of house apart from basement|
|sqft_basement|square footage of the basement|
|yr_built|Built Year|
|yr_renovated|Year when house was renovated|
|zipcode| zip|
|lat|Latitude coordinate|
|long|Longitude coordinate|
|sqft_living15|The square footage of interior housing living space for the nearest 15 neighbors|
|sqft_lot15|The square footage of the land lots of the nearest 15 neighbors|

## Workflow:

* Data Cleaning:  
  
  * Remove empty spaces in column names
  * drop columns that are not needed or redundant (such as sale id)
  * change data types if needed (convert numerical features to float)

* Exploratory Data Analysis to answer business question  
  
  * descriptive statistics to identify outliers
  * check for distribution of numerical features
  * correlation matrix to check for correlation and scatter plots to check relation of numerical features to target feature (price)

* Definition of  initial questions and hypotheses 

| Question | Hyothesis |
| ---------|-----------|
| Which lively and central area is still affordable for a budget in middle price range?| The closer to the city center, the more expensive| 
|Does timing affect the price?| House prices fluctuate over the year and are lowest in seasons with low number of solds|
|Do some areas have a better price performance?| Some areas offer a lower price per sqft|

* Selecting only houses that are of interest for the client   
  
  * remove houses that are outside the interquartile range (IQR) to select only houses in the middle price range
  * select only central houses (which are in a 3 miles radius around the city center)
  * check correlation of price and distance to city center in these selected houses 
  * visualization of houses in area of interest on geomap showing the prices 

* When is the best timing to buy? Plotting price and number of house sales by month

* Ranking of cheapest areas 
* Ranking of best price per sqft
* Identification of areas with best price-performance ratio by living space and grade of the house 

## Conclusion/ Summary:

* The middle price range in King County is between 322000-645000$, when taking the interquartile range of the prices of all house sales in King County. Within a radius of 3 miles around the city center, it is still possible to find affordable houses in a middle-price range budget. 
* House prices fluctuate over the year and some seasons are higher priced than others. By plotting average prices by months of the two last years, it seems that february-april is the highest priced season. Although house prices are dependent on several factors e.g. market factors like demand, offer or economic factors like employment rate, which were not considered in this short-term analysis. 
* House prices around the city center do not correlate with proximity to city center. Some neighbourhoods are more popular than others. 
* Zipcode 98144 has the lowest price per sqft 
* Zipcode 91809 has the highest price per sqft
* Most houses with a low price per sqft are located east to the city center 
* Zipcode 98116 (West Seattle) offers the best graded houses AND biggest living space for the smallest price


## Recommendations
* Radius of 3 miles around the city center offers affordable homes
* Consider to buy in West Seattle or East of the city centre to get more living space and good grade at lowest price
* Best timing to buy is in January or from May-September to avoid highly-priced seasons





