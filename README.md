## CS 103 Data Science 
#### Arvilyn Mellizas BSCS 3A

# Python Programming
## Review Problems

- Import data files into pandas dataframe, using precip-2002-2013-months-seasons.csv which is available for download at https://figshare.com/articles/dataset/Earth_Analytics_Bootcamp_Pandas_Dataframes_Teaching_Subset/6934286?file=12710621

      import numpy as np
      import pandas as pd
      precip = pd.read_csv("D:/precipitation.csv")
      print(precip)
      
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

  a). Use the `.describe()` method to summarize the precipitation values in the dataframe (e.g. precip_2002_2013). Note the maximum values in 2002 and 2013.

      precip.describe()
      
            precip_2002	precip_2013
      count	12.000000	12.000000
      mean	1.156667	2.845833
      std	0.961101	4.953130
      min	0.020000	0.270000
      25%	0.380000	0.582500
      50%	1.125000	1.265000
      75%	1.505000	2.345000
      max	3.200000	18.160000
    
   b). Use indexing to create two new dataframes:
       
     :heavy_check_mark: One containing the month with the maximum value in 2002
     
      col = precip["precip_2002"]
      max2002 = col.max()
      print(max2002)
      
      3.2
     
     :heavy_check_mark: One containing the month with the maximum value in 2013
     
      col2 = precip["precip_2013"]
      max2013 = col2.max()
      print(max2013)
      
      18.16

    c). Compare these two new dataframes

     :heavy_check_mark: Do they occur in the same season?
     
     
     :heavy_check_mark: What do you notice about the precipitation value for the maximum month in 2013, as compared to that same month in 2002?
     
      print("Precipitation value for the maximum month in 2013")
      display(precip.iloc[8])
      
      Precipitation value for the maximum month in 2013
      months          Sept
      precip_2002     1.52
      precip_2013    18.16
      seasons         Fall
      Name: 8, dtype: object

      
      



