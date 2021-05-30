## CS 103 Data Science 
#### Arvilyn Mellizas BSCS 3A 

# Python Programming 
## Review Problems

#### Part 1

- Import data files into pandas dataframe, using precip-2002-2013-months-seasons.csv which is available for download at https://figshare.com/articles/dataset/Earth_Analytics_Bootcamp_Pandas_Dataframes_Teaching_Subset/6934286?file=12710621

![image](https://user-images.githubusercontent.com/62274346/120113415-fa220000-c1ac-11eb-96ae-254b13b36efa.png)


  a). Use the `.describe()` method to summarize the precipitation values in the dataframe (e.g. precip_2002_2013). Note the maximum values in 2002 and 2013.
  
  ![image](https://user-images.githubusercontent.com/62274346/120113454-1d4caf80-c1ad-11eb-90fc-db98dc9f79bd.png)

    
   b). Use indexing to create two new dataframes:
       
   - One containing the month with the maximum value in 2002

   ![image](https://user-images.githubusercontent.com/62274346/120113493-44a37c80-c1ad-11eb-9857-253a9ffc8821.png)
   
   ![image](https://user-images.githubusercontent.com/62274346/120113516-6c92e000-c1ad-11eb-8a7a-bad6dc5b0bd9.png)

   ![image](https://user-images.githubusercontent.com/62274346/120113565-9c41e800-c1ad-11eb-8057-9500e928aafc.png)

     
   - One containing the month with the maximum value in 2013

   ![image](https://user-images.githubusercontent.com/62274346/120113590-baa7e380-c1ad-11eb-9d58-6e043d8b5c9b.png)


   c). Compare these two new dataframes

   - Do they occur in the same season?  
     
      ![image](https://user-images.githubusercontent.com/62274346/120113565-9c41e800-c1ad-11eb-8057-9500e928aafc.png) 
      ![image](https://user-images.githubusercontent.com/62274346/120113590-baa7e380-c1ad-11eb-9d58-6e043d8b5c9b.png)

     No, the maximum precipitation value of **2002** occured in the **spring season**, while the maximum precipitation value of **2013** occured in **fall season** .
     
   - What do you notice about the precipitation value for the maximum month in 2013, as compared to that same month in 2002?
     
      ![image](https://user-images.githubusercontent.com/62274346/120113703-3efa6680-c1ae-11eb-9523-c2a122587bf8.png)


   As the data shows, the precipitation value of 1.25 in the month of September 2002 increased in the same month in year 2013 which rose to the value of 18.16.
      
   d). Using the columns for months and the precipitation for 2013, create a plot of **Average Monthly Precipitation in 2013 for Boulder, Co.**
   
   - Recall that you can select a column as a pandas series using `dataframe["column"]`.
     
   - If needed, review how to create matplotlib plots with lists, and then substitute the list names with series selected from the pandas dataframe.
     
      ![image](https://user-images.githubusercontent.com/62274346/120113726-605b5280-c1ae-11eb-9229-33a1de0b152a.png)
      
      ![image](https://user-images.githubusercontent.com/62274346/120113746-7e28b780-c1ae-11eb-92ff-9be88bb83c1c.png)
      
      ![image](https://user-images.githubusercontent.com/62274346/120106775-013b1500-c191-11eb-9494-8ea008dcc1a3.png)


#### Part 2

- Analyze, perform and answer the following questions/situations.

   1. Calculate the sum of 10.8, 12.2, and 0.2, store it in the variable **total**, then display the **total's value**.
  
      ![image](https://user-images.githubusercontent.com/62274346/120112644-40756000-c1a9-11eb-9338-6fbfe0672045.png)


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
   
      ![image](https://user-images.githubusercontent.com/62274346/120112764-c1ccf280-c1a9-11eb-8e28-382e2afb0819.png)

   8. Use the `NumPy` function arange to create an array of 20 even integers from 2 through 40, then reshape the result into a 4-by-5 array.

      ![image](https://user-images.githubusercontent.com/62274346/120107549-fd5cc200-c193-11eb-966b-1d15f85be66b.png)









