# The Impact of Food Deserts and Unemployment on Homicide Rates in Baltimore City
Homicide has been linked to factors such as poverty and economic inequality. In 2019, there were [347 homicides in Baltimore](https://www.cnn.com/2019/12/31/americas/baltimore-2019-homicides/index.html), breaking the record for killings per capita. We wanted to analyze whether there are other significant variables more present in Baltimore that could lead to such a high homicide rate.

What are the socioeconomic factors that affect Baltimore’s high homicide rate, and what actions can the local government take?

After researching more about specific conditions in Baltimore, we found that [20 percent of Balitmore residents live in food deserts](https://www.umaryland.edu/gogreen/news/food/combating-the-urban-food-desert.php). A food desert is roughly defined as a location where there is no access to affordable nutritious foods like fruits, vegetables, and whole grains. Since a high population of Baltimore residents live in food deserts, we narrowed down our question:

Could food deserts be a cause of the high homicide rate in Baltimore?

We analyzed several other factors, including more common factors such as unemployment, for comparison.
### Findings
1. Higher % of area covered by food desert →  higher % of deaths due to homicide 
More Food Deserts →  More Unhealthy Foods/Less Healthy Foods →  More Aggression, Stress, And Anxiety → More Homicides 
2. Higher % of unemployment →  higher % of deaths due to homicide 
### Suggestions
1. Government promotes programs that helps citizens afford healthy foods → citizens eat healtier → less aggression and stress → fewer homicides
2. Government impliments career development programs to help citizens find jobs → citizens can afford more nutrious food → less aggression → fewer homicides


# Significance



# Data
We chose to analyze the [2017 Neighborhood Health Profile Data](https://health.baltimorecity.gov/neighborhoods/neighborhood-health-profile-reports) from the Baltimore City Health Department. It is comprehensive and contains data about major health outcomes for 55 Community Statistical Areas in the city of Baltimore. Although this data is from 2017, it is still relevant because Baltimore has a long history of high homicide rates. 

We looked at these factors: 
- Median household income <br>
Median annual household income, according to the Baltimore Neighborhood Indicators Alliance
- % living below Federal Poverty Level <br>
Percentage of families that earned less than the Federal Poverty Level in the past 12 months
- % of Adults with Less than a HS Diploma <br>
Percentage of adults 25 years of age or older with less than a high school diploma
- % of Area Covered by Food Desert <br>
Percentage of land area covered by food desert, as defined by the Center for a Livable Future
- Vacant Lot Density <br>
Number of vacant lots per 10,000 housing units
- Unemployment <br>
Percentage of population 16 years of age or older in the labor force that are unemployed

Two factors of special interest are vacant lot density and percent of area covered by food desert.
## Vacant Lot Density
We were interested in looking at the number of vacant lots in different neighborhoods in Baltimore. Vacant lots are small areas of land that are not being occupied or used. It is usually neglected and, in many cases, houses were on these lots, but they fell into disrepair and were demolished. 

They disrupt a neighborhood's sense of community and lower property values. There are significantly more vacant lots in poorer neighborhoods, which could possibly contribute to higher homicide rates.
## Percent of Area Covered by Food Desert
The [Center for a Livable Future](https://clf.jhsph.edu/about-us/news/news-2012/new-improved-food-desert-map) defines food deserts: 
- An area where the distance to a supermarket is more than one quarter of a mile
- The median household income is at or below 185% of the Federal Poverty Level
- Over 40% of households have no vehicle available 

We were interested in this data because a food desert represents a location where resources are scarce and healthy habits are hard to maintain. This could possibly impact homicide rates in Baltimore.
# Analysis
First, we conducted a multiple linear regression between all the variables to determine which variables were statistically significant. 
![alt_text](https://github.com/AndrealZhang/Food_Deserts_and_Homicide_Rates_in_Baltimore_City/blob/master/initial%20multiple%20regression.png)

The R squared from this initial analysis is around 70%, meaning that around 70% of the data can be displayed using this model. However, the only variables that are statistically significant with a p value of less than 0.05 are unemployment, % of area covered by food desert, and vacant lot density. 

Then we modified our model to only include the statistically significant variables.
![alt_text](https://github.com/AndrealZhang/Food_Deserts_and_Homicide_Rates_in_Baltimore_City/blob/master/final%20multiple%20regression.png)

The R squared is around the same and the significance F decreased, meaning that there is a very high probability that unemployment, % of area covered by food desert, and vacant lot density impact the % of deaths due to homicides. However, looking at the correlation, 
![alt_text](https://github.com/AndrealZhang/Food_Deserts_and_Homicide_Rates_in_Baltimore_City/blob/master/correlation.png)
there is a very low correlation between vacant lot density and % of deaths due to homicides. This information is supported with this scatterplot: 
![alt_text](https://github.com/AndrealZhang/Food_Deserts_and_Homicide_Rates_in_Baltimore_City/blob/master/vacantlotscatter.png)
Only around 6% of the data can be explained by this model, meaning that vacant lot density does not have a significant effect on homicide rates.

Next, we can analyze another scatterplot.
![alt_text](https://github.com/AndrealZhang/Food_Deserts_and_Homicide_Rates_in_Baltimore_City/blob/master/fooddesertscatter.png)
Looking at the impact of the percent of area covered by food deserts on the percent of deaths due to homicides, around 36% of the data can be represented by this model. Although this number may seem small, it is important to remember that there are multiple factors that can impact homicide rates and one factor affecting around 36% of the homicide rates is significant. 

Similarly, looking at the scatterplot of the impact of unemployment on the percent of deaths due to homicides, there is clearly a relationship between two variables as this model represents around 56% of the data.
![alt_text](https://github.com/AndrealZhang/Food_Deserts_and_Homicide_Rates_in_Baltimore_City/blob/master/unemploymentscatter.png)

# Summary
1. FOOD DESERT: Higher average percentage of food desert in certain neighborhoods in Baltimore, higher average percentage of deaths due to homicide in those neighborhoods
2. UNEMPLOYMENT: Higher average of unemployment in certain neighborhoods in Baltimore, higher average percentage of deaths due to homicide in those neighborhoods

# Future Plan

