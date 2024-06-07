# Description : 

#* Project phases : 


* preprocessing : 
we read each folder which represents a seperate paper file, each paper file have a list of algorithms performance in 30 function with different dimensions 10,30,50,100. We read each paper files and then divide each paper into dimensions after that we divide each file into 14 rows and we computed the AVG and STD for each row, so we got a 14 values from each file which represent an algorithm performance in specific function for a dimension. We used dictionaries to read files, we found all files with .txt extensions so we stored the files into dictionaries and then we implemented the formulas to Get the required AVG and STD for each row inside each file in different dimensions and at the end we extracted the sublist inside each dictionary and we export the values into CSV files. After that we had a seperate files for each dimensions in each row which included all papers from 1 to 12, and all function from 1 to 30 and each csv file had all required values which are each single paper performance in each single function. 
As a final results we have a many csv files as a datasets Dim 10 from 1 to 14, Dim 30 from to 14, Dim 5o from 1 to 14, Dim 100 from 1 to 14.





* Normality and Outliers Checking : 
We implemented a normality and outliers checking using data visualizations, for normality we used QQ plot and Histogram and for outliers checking we used Boxplot. we have a seperate juypter notebook for each operation which include the normality for all datasets and outliers checking for all datasets generated from the Preprocessing phase.






* Friedman and Wilcoxon Testing : 
at first the target from this project is to find if there is a significant difference between the performance of algorithms in papers so we need to determine a null hypothesis at the first, so we can assume that our null hypothesis is that there is a difference between the algorithms performance so if the tests results prove that it should be correct 
we implemented friedman rank test on each dataset and then we determined the ranking for each paper. regarding to our data we are representing the AVg for error values so the last ranking value should be the best performer so we selected p10 as a highest one and we used it as a control method to implement the wilcoxon test as a second phase so for that reason we implemented wilcoxon and we found that the result that there  a difference between the control method (P10) and other papers in performance.
we implemeted wilcoxon and friedman in different Jyupter notebooks a seperate one for each dimension from 1 to 14









* adjusting p-values 
here we implemented the wilcoxon test based on the control method which are determined based on friedman and then we got a P-value for each separate paper according on different methods such as : The Bonferroni, The Holm procedure, The Holland procedure, The Hochberg procedure, The Hommel procedure
we implemented the adjusting p-values in a different jyupter notebook which included all Dimension(10-100) in all rows(1-14) 
