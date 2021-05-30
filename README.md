## CS 103 Data Science :computer: :atom:
#### Arvilyn Mellizas BSCS 3A :woman_technologist:

# Python Programming :snake: :panda_face:
## Review Problems :bookmark_tabs:

#### Part 1

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
     
      print(max(precip["precip_2002"]))
      
      3.2

      max2002 = precip[precip["precip_2002"] == 3.2] 
      print(max2002)
      
        months  precip_2002  precip_2013 seasons
      4    May          3.2         2.66  Spring
     
     :heavy_check_mark: One containing the month with the maximum value in 2013
     
      print(max(precip["precip_2013"]))
      
      18.16

      max2013 = precip[precip["precip_2013"] == 18.16]
      print(max2013)
      
        months  precip_2002  precip_2013 seasons
      8   Sept         1.52        18.16    Fall

    c). Compare these two new dataframes

     :heavy_check_mark: Do they occur in the same season?  :cherry_blossom: :sun_with_face: :fallen_leaf: :snowflake:
     
       max2002 = precip[precip["precip_2002"] == 3.2] 
       print(max2002)
      
        months  precip_2002  precip_2013 seasons
      4    May          3.2         2.66  Spring
      
      
       max2013 = precip[precip["precip_2013"] == 18.16]
       print(max2013)
      
        months  precip_2002  precip_2013 seasons
      8   Sept         1.52        18.16    Fall

     No, the maximum precipitation value of **2002** occured in the **spring season** :cherry_blossom:, while the maximum precipitation value of **2013** occured in **fall season** :fallen_leaf:.
     
     :heavy_check_mark: What do you notice about the precipitation value for the maximum month in 2013, as compared to that same month in 2002?
     
      print("Precipitation value for the maximum month in 2013")
      display(precip.iloc[8])
      
      Precipitation value for the maximum month in 2013
      months          Sept
      precip_2002     1.52
      precip_2013    18.16
      seasons         Fall
      Name: 8, dtype: object
    
    As the data shows, the precipitation value of 1.25 in the month of September 2002 increased in the same month in year 2013 which rose to the value of 18.16.
      
   d). Using the columns for months and the precipitation for 2013, create a plot of **Average Monthly Precipitation in 2013 for Boulder, Co.**
   
     :heavy_check_mark: Recall that you can select a column as a pandas series using `dataframe["column"]`.
     
     :heavy_check_mark: If needed, review how to create matplotlib plots with lists, and then substitute the list names with series selected from the pandas dataframe.
     
      import matplotlib.pyplot as plt
      
      print("Line graph")
      l = precip.plot(x = "months", y = "precip_2013", kind = "line", color = "purple")
      l.set_title("Average Monthly Precipitation in 2013 for Boulder, Co.", color = "white")
 
      plt.xlabel("Month")
      plt.ylabel("Precipitation Value")
      
      l.tick_params(axis = "x", colors = "white")
      l.tick_params(axis = "y", colors = "white")
      l.xaxis.label.set_color("white")
      l.yaxis.label.set_color("white")
      plt.show()
      
     ![image](https://user-images.githubusercontent.com/62274346/120106775-013b1500-c191-11eb-9494-8ea008dcc1a3.png)


#### Part 2

- Analyze, perform and answer the following questions/situations.

   1. Calculate the sum of 10.8, 12.2, and 0.2, store it in the variable **total**, then display the **total's value**.
  
      ![image](https://user-images.githubusercontent.com/62274346/120106897-64c54280-c191-11eb-91f8-6a0f3e3cf27b.png)


   2. Evaluate the expression 3 * (4-5) with and without parentheses. Are the parentheses redundant?

      ![image](https://user-images.githubusercontent.com/62274346/120106990-be2d7180-c191-11eb-89c3-b692535c7ded.png)
      
      The parenthesis is redundant if removing it yields the same results. Based on the output, it yields different results when there is parenthesis and if there's not. Thus, parenthesis is not redundant.


   3. Evaluate the expressions 4 ** 3 ** 2, (4 ** 3) and 4 ** (3 ** 2). Are any of the parentheses redundant?

      ![image](https://user-images.githubusercontent.com/62274346/120107020-da311300-c191-11eb-8b05-65a9dbd4e512.png)
      
      Parenthesis is redundant in the expression `4 ** (3 ** 2)` since it has the same result as the expression `4 ** 3 ** 2`.


   4. What does the following print statement display? `print('int(5.2)', 'truncates 5.2 to', int(5.2))`

      ![image](https://user-images.githubusercontent.com/62274346/120107172-938fe880-c192-11eb-9fec-12326ca5f848.png)
      
      ***truncates*** means discard
      
      
   5. For any of the operators **!=**, **>=**, or **<=**, show that the syntax error occurs if you reverse the symbols in a condition. 

      ![image](https://user-images.githubusercontent.com/62274346/120107198-ac000300-c192-11eb-8c44-02ffcdab0268.png)


   6. Use all six comparison operators to compare the values 5 and 9. Display the values on one line using print.

     ![image](https://user-images.githubusercontent.com/62274346/120112401-40c12b80-c1a8-11eb-88db-7d116b7a4524.png)


   7. For the values 47, 95, 88 and 84 calculate the minimum, maximum and range.
   
      ![image](https://user-images.githubusercontent.com/62274346/120107286-19139880-c193-11eb-9ab0-065a55c13033.png)

   8. Use the `NumPy` function arange to create an array of 20 even integers from 2 through 40, then reshape the result into a 4-by-5 array.

      ![image](https://user-images.githubusercontent.com/62274346/120107549-fd5cc200-c193-11eb-966b-1d15f85be66b.png)









