<h1><center>Movies</center></h1>
<h2><center>What is the most popular type of movie?<br>Does higher budget mean higher revenue?</center></h2>

<h3><center>A Report by Cathal and Marijana<h3></center>

# Introduction

For our Dataset Analysis project, we have chosen a movies dataset from the Github repository. Our choice was based on a common interest we both have, the general area of movies, but also one in which we both have extensive knowledge of. Our analysis will look at movies released between 2000-2015, an analysis of the genre and revenue variables, and will examine the correlation between budget and revenue. 

The dataset we are using here comes from the Udacity--Project-Investigate-TMDB-Movies-Dataset project on GitHub (antra0497, 2018). It is a sample of a much larger dataset from the The Movie Database which contains over 830,000 entries (The Movies Database, 2022).

import matplotlib.pyplot as plt # for plotting graphs
import numpy as np # linear algebra
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)
import seaborn as sns # also for plotting graphs
from datetime import datetime #reformatting date and time variables. 
from scipy import stats
movies_metadata=pd.read_csv('https://raw.githubusercontent.com/antra0497/Udacity--Project-Investigate-TMDB-Movies-Dataset/master/tmdb-movies.csv')
#Our Dataset

The dataset we have selected has 10866 entries and 21 columns. The dataset info is:

movies_metadata.info()

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 10866 entries, 0 to 10865
Data columns (total 21 columns):
 #   Column                Non-Null Count  Dtype  
---  ------                --------------  -----  
 0   id                    10866 non-null  int64  
 1   imdb_id               10856 non-null  object 
 2   popularity            10866 non-null  float64
 3   budget                10866 non-null  int64  
 4   revenue               10866 non-null  int64  
 5   original_title        10866 non-null  object 
 6   cast                  10790 non-null  object 
 7   homepage              2936 non-null   object 
 8   director              10822 non-null  object 
 9   tagline               8042 non-null   object 
 10  keywords              9373 non-null   object 
 11  overview              10862 non-null  object 
 12  runtime               10866 non-null  int64  
 13  genres                10843 non-null  object 
 14  production_companies  9836 non-null   object 
 15  release_date          10866 non-null  object 
 16  vote_count            10866 non-null  int64  
 17  vote_average          10866 non-null  float64
 18  release_year          10866 non-null  int64  
 19  budget_adj            10866 non-null  float64
 20  revenue_adj           10866 non-null  float64
dtypes: float64(4), int64(6), object(11)
memory usage: 1.7+ MB
