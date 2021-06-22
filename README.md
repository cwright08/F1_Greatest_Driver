Repository for Formula 1, Greatest Ever Driver Blog Post
Analysis to accompany article found at 
https://chrisw08.medium.com/f1s-greatest-driver-ever-what-does-the-data-say-f64e16bf8246

**Project Description & Motivation:**
This project conducts a simple analysis on Formula 1 data from 1950-2020 in an attempt to explore driver statistics and attempt to do some basic modelling of results. 
The project also forms a key submission for the Udacity Data Science Nanodegree program 2021. Please note this is a personal project and not attributable to any organisation or employer. 

**Acknowledgements:**
Thanks must be provided to the dataset curator Vopani (https://www.kaggle.com/rohanrao) and the ultimate source Ergast API http://ergast.com/mrd. Thanks also to the Udacity team 

**Data Required:**
The data used can be found on the project Github page and is sourced from Kaggle https://www.kaggle.com/rohanrao/formula-1-world-championship-1950-2020.

I used the following datasets for my analysis:
-drivers: file containing driver specific information
-results: file containing information on race results
-standings: file containing information on driver championship standings
-races: file containing information on races
-lap_times: file containing individual laptimes
-constructor_standings: file containing constructors overall championship standings
-constructors: file containing constructor information. 

**Code Files:**
All analysis can be found in the 'Data Science Blog.ipynb' on the project GitHub page https://github.com/cwright08/F1_Greatest_Driver

**Business Questions:**
The questions I set out to answer initially were
1A) Who is the greatest driver ever using traditional 'absolute metrics', such as total race wins
1B) Who is the greatest driver ever using more 'relative' metrics such as wins per start
2) How have F1 lap times changed from the early days to now - note this question did not yield any interesting results and thus was not included in the blog post
3) Can you predict the championship winner using results of the first 10 races of the season. 

**Data Cleansing: Null Values & Categorical Fields**
In this analysis there was only one instance when it became neccessary to handle Null values in the dataset, occuring on line 38 in the modelling tab. Here, we are attempting to pull in the constructors final championship standings from the previous season. However, if the given season is the constructors first season in the championship, or they did not compete in the previous season, they will not have a value for this and this will return null. I decided to simply fill these nulls with zeros for my analysis and modelling, as zero is not possible for the other constructors, this effectively signifies a constructors first season consistently. 

For this analysis, I did not explicitly require categorical variable handling as there were no cateogrical variable required for my model. However, to fulfil the project objectives, I have added a short fuction in the appendix which demonstrates this capability. It takes a list of categorical variables and non categorical variables in a dataframe as input, and returns a dataframe with the categorical variables correctly encoded for use in a model. This code utilises some code from the 'Putting it all together' section of the Udacity Data Science Nanodegree section 1. 

**Libraries and technology:**
- Python 3.8 on Anaconda
- Pandas
- Numpy
- Matplot lib
- SckitLearn


