# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends
Analysis of Theater Play Kickstarters

Overview

-In this project we were given a set of data on kickstarter campaigns analyze. We first narrowed our lense by focusing on the theater parent category. We then compared the outcomes by the launch date and then by the initial goals set. 

Purpose

-The purpose of this analysis was to aid in determining whether the kickstarter for 'Fever' was successful or not.

Analysis of Outcomes Based on Launch Date

-Based off of the the 'Theater Outcomes Based on Launch Date' graph the best time Frame to launch a kickstarter is May. However, this is also one of the peak times for a kickstarter to fail. Further analysis should be done to see if the number of successful kickstarters in May is statistically significant compared to the other months in the year. 

Analysis of Outcomes Based on Goals

-The percentage of successful kickstarters that were successful was greatest when the goal was less than $1,000 dollars and was the least successful when the kickstarter had a goal from $45,000-$49,999. This could be because smaller goals are easier to achieve or it could be that the larger goals were for plays that the general population did not appreciate. 

![image](https://user-images.githubusercontent.com/78890771/111091456-fa412680-8500-11eb-81cf-283b56eced38.png)

Challenges and Difficulties Encountered

-One of the first challenges we ran in to was spilling the 'Category and Sub Category' column in to two sortable columns of 'Category' and 'Subcategory'. We overcame this by using 'Convert Text to Columns Wizard' which allowed us to split the text in to two columns where the '/' was. We then had to convert the launch date from Unix Timestamps to a readable form with the following code '=(((J2/60)/60)/24)+DATE(1970,1,1)'. We were then set to create the tables to get the graphs below of 'Theater Outcomes by Launch Date' and ' Outcomes Based on Goals'. The first graph was created off of a pivot table which was sorted by the theater category and results broken down by month. The second graph, ' Outcomes Based on Goals', was created by using the countifs function in excell (=COUNTIFS(Kickstarter!$D:$D, "<=19999", Kickstarter!$D:$D, ">=15000", Kickstarter!$F:$F, "Successful", Kickstarter!$R:$R, "plays"). This function only counts the cell if it meets certain criteria which in this case was a range of kickstarter goals. 

Results

-From the data above we can determine that the best time to launch a kickstarter is May whereas the worst time to launch a kickstarter is December. We can also conclude that most achievable goal, based on percentage of successfull kickstarters, to set is below $1,000 and that the least achievable is anything greater than $49,999.

-This analysis is limited in scope, and statistical weight. Further analysis will need to see if the values in these graphs are statistically significant from one another. In addition, a table with the blurb and ratings (1-5) would be helpful in determining whether this is a confounding factor in the 'Outcomes Based on Goals' data set. 
