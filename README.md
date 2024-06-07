# Description : 

Project phases : 


* Preprocessing : 
We read each folder (you can find them in "Results for all papers.zip" file, and then you can change the paths), which represents a separate paper file, each paper file have a list of algorithms' performance in 30 functions with different dimensions 10,30,50,100. We read each paper file and then divide each paper into dimensions, after that we divide each file into 14 rows and we computed the AVG and STD for each row, so we got 14 values from each file which represent an algorithm's performance in a specific function for a dimension. We used dictionaries to read files, we found all files with .txt extensions, so we stored the files in dictionaries and then we implemented the formulas to get the required AVG and STD for each row inside each file in different dimensions and at the end we extracted the sublist inside each dictionary and we export the values into CSV files. After that we had a separate file for each dimension in each row which included all papers from 1 to 12, and all functions from 1 to 30 and each csv file had all required values which are each single paper performance in each single function. 
As final results we have a many csv files as datasets Dim 10 from 1 to 14, Dim 30 from to 14, Dim 5o from 1 to 14, Dim 100 from 1 to 14.





* Normality and Outliers Checking : 
We implemented normality and outliers checking using data visualizations, for normality, we used QQ plot and Histogram and for outliers checking we used Boxplot. We have a separate Juypter notebook for each operation which includes normality for all datasets and outliers checking for all datasets generated from the Preprocessing phase.






* Friedman and Wilcoxon Testing : 
At first, the target of this project is to find if there is a significant difference between the performance of algorithms in papers so we need to determine the null hypothesis, so we can assume that our null hypothesis is that there is a difference between the algorithms performance so if the test results prove that it should be correct. We implemented the Friedman Rank Test on each dataset and then we determined the ranking for each paper. Regarding our data we are representing the AVg for error values so the last ranking value should be the best performer so we selected p10 as the highest one and used it as a control method to implement the Wilcoxon signed-rank test as a second phase so for that reason we implemented Wilcoxon, and we found that there was a difference between the control method (P10) and other papers in performance.
We implemeted Wilcoxon and Friedman in different Jyupter notebooks, separate one for each dimension from 1 to 14









* Adjusting P-Values 
Here we implemented the Wilcoxon test based on the control method, which is determined based on Friedman and then we got a P-Value for each separate paper according to different methods such as The Bonferroni, The Holm procedure, The Holland procedure, The Hochberg procedure, and The Hommel procedure.
We implemented the adjusting P-Values in a different Jyupter notebook which included all Dimension(10, 30, 50, 100) in all rows(1-14).
