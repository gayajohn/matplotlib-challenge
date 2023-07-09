# Module 5 Assignment: Plotting in Python

-----------------
Table of Contents
-----------------

Pymaceuticals Folder which contains

  - Pymaceuticals_script.ipynb file. This is the main script.
 
  
  - data folder with contains the .csv files used in the script

       - Mouse_metadata.csv
    
       - Study_results.csv
    
    
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

-------------------
Challenge Objective
-------------------

The objective of our analysis is to look at data of mice who are receiving various medical treatments and analyse the efficacy of the drugs on reducing tumour volume. The actual analysis is perfomed in the .ipynb script, and results and conclusions are reported at the top of the script file. 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

----------
References
----------

Here are the references used in my code:

1) To learn how to find and print duplicate rows:

   https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.duplicated.html

   https://stackoverflow.com/questions/14657241/how-do-i-get-a-list-of-all-the-duplicate-items-using-pandas-in-python

   https://www.geeksforgeeks.org/find-duplicate-rows-in-a-dataframe-based-on-all-or-selected-columns/

   Code referenced:

   duplicate_rows = merged_data[merged_data.duplicated(subset = ("Mouse ID", "Timepoint"))]
   

2) To learn how to drop rows:

   https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop.html
   
   https://stackoverflow.com/questions/13851535/how-to-delete-rows-from-a-pandas-dataframe-based-on-a-conditional-expression
   
   Code referenced:

   clean_mouse_data = merged_data.drop(merged_data[merged_data["Mouse ID"] == duplicate_mouse_ID[0]].index)



3) To learn how to summarize stats in one line of code:

   https://pandas.pydata.org/docs/getting_started/intro_tutorials/06_calculate_statistics.html

   https://sparkbyexamples.com/pandas/pandas-groupby-aggregate-explained/#:~:text=In%20Pandas%2C%20the%20aggregate(),apply%20aggregation%20functions%20to%20it.

   Code referenced:

   agg_regimen_summary_stats = regimen_data[["Tumor Volume (mm3)"]].agg(["mean", "median", "var", "std", "sem"])

   

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
