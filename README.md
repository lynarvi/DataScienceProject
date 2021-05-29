## CS 103 Data Science 
#### Arvilyn Mellizas BSCS 3A

# Python Programming
## Review Problems

- Import data files into pandas dataframe, using precip-2002-2013-months-seasons.csv which is available for download at https://figshare.com/articles/dataset/Earth_Analytics_Bootcamp_Pandas_Dataframes_Teaching_Subset/6934286?file=12710621

      import pandas as pd
      precip = pd.read_csv("D:/precipitation.csv")

  a). Use the `.describe()` method to summarize the precipitation values in the dataframe (e.g. precip_2002_2013). Note the maximum values in 2002 and 2013.

      precip.describe()
      
      ![image](https://user-images.githubusercontent.com/62274346/120074311-cbcdf300-c0ce-11eb-8654-31ae202bf969.png)



