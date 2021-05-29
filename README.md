## CS 103 Data Science 
#### Arvilyn Mellizas BSCS 3A

# Python Programming
## Review Problems

- Import data files into pandas dataframe, using precip-2002-2013-months-seasons.csv which is available for download at https://figshare.com/articles/dataset/Earth_Analytics_Bootcamp_Pandas_Dataframes_Teaching_Subset/6934286?file=12710621

      import pandas as pd
      precip = pd.read_csv("D:/precipitation.csv")

  a). Use the `.describe()` method to summarize the precipitation values in the dataframe (e.g. precip_2002_2013). Note the maximum values in 2002 and 2013.

      precip.describe()
      
         months  precip_2002  precip_2013 seasons
      0     Jan         1.07         0.27  Winter
      1     Feb         0.44         1.13  Winter
      2     Mar         1.50         1.72  Spring
      3     Apr         0.20         4.14  Spring
      4     May         3.20         2.66  Spring
      5    June         1.18         0.61  Summer
      6    July         0.09         1.03  Summer
      7     Aug         1.44         1.40  Summer
      8    Sept         1.52        18.16    Fall
      9     Oct         2.44         2.24    Fall
      10    Nov         0.78         0.29    Fall
      11    Dec         0.02         0.50  Winter
      



