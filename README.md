# Challenge-1
Kickstarter Excel Challenge
--------------------------------------------------------------------------------------------------------------------------------------------------------
An Analysis of Kickstarter Data to Identify Successful Launches by Observing Monotary and Chronological Trends 

Project Overview and Purpose:
This project was conducted to identify elements of successful Kickstarter campaigns. Kickstarter data from 4114 campaigns was compiled and analysed based on the time of month the campaign was launched, as well as the funding goals of each campaign. The purpose of identifying this data was to optimize time of launch and funding goals for the upcoming theater Kickstarter funding campaign.

Analysis and Challenges:

Theater Outcome by Launch Date
The data used for this this analysis contained over 4000 entries with mutliple categories of information.  Manual code entry and data compiling would have been a tediously monotonous task.  Using the tools and skills introduced for excel, the data was easily condensed and visualized to determine the time of year and campaign goals of successful Kickstarters funding campaigns. Pivot tables were used to condense the information and sort the data by month in order to determine the most successful start date (Figure 1). 
![Figure 1](https://user-images.githubusercontent.com/108313294/177065558-52a0e279-4134-4657-8d04-656f59ada265.png).
The raw data contained dates in a difficult to understand UNIX format, and was converted into plain long date format using the excel equation =(((I8/60)/60)/24)+DATE(1970,1,1).  Once the long date format was obtained and added to the pivot table, it was sorted by default in years.  Right clicking and using the grouping tool allowed the data to quickly be converted into months (Figure 2). 
![Figure 2](https://user-images.githubusercontent.com/108313294/177065958-d6ff21c6-d225-49a8-a6b3-09962aca794f.png). 
Filtering by theater to consolidate data relevent to the type of campaign being launched, a count of all successful, failed and cancelled campaigns was added to the pivot table and charted.

Theater Outcome by Goals

Kickstarter campaigns deemed successful are funded with greater than or equal to the goal amount.  The raw data already contained a column summarizing the successful funding of any given Kickstarter campaign in the dataset.  Campaigns were grouped, sorted and placed in brackets according to the monotary goal of the funding campaign (Figure 3). 
![Figure 3](https://user-images.githubusercontent.com/108313294/177066580-84c1f3cf-7c0a-499c-ba7a-362e7c7025e4.png). 
Conditional filtering was done using the COUNTIFS function to obtain a count of campaigns within the definied goal boundaries as well as campaigns with successful, failed, or cancelled statuse (Figure 4). 
![Figure 4](https://user-images.githubusercontent.com/108313294/177066622-e89a6aa9-7953-4c5b-8a72-bf5f7e7d7e0f.png). 
The percentage of successful, failed, or cancelled campaigns was determined by dividing the count of each category of campaign success by the sum of all campaigns within the given goal bracket (using the SUM function). While the data was initially expressed in decimal format, it was quickly converted into a percentage format by changing the number format of the cells in the table (Figure 5). 
![Figure 5](https://user-images.githubusercontent.com/108313294/177066859-15ad24fc-e189-42ed-b22b-c3418d752e68.png).

Results and Conclusion:

Based on the analysis, successful theater campaigns are most likely to be launched in May, and most successful when funding goals are less than $1000. However, the analysis is likely to contain some bias.  For time of year, while May contained the most number of successful campaigns, it also contained the most number of failures.  This could suggest that more campaigns are successful in the month of May because more campaigns are launched in May.  The data could be normalized by plotting the ratio of successful campaigns and number of campaigns launched in a given month. The analysis of successful campaigns by target goal is also likely biased as it does not take into account factors such as campaign advertising, the length of the campaign, and scale of production.  Possible additional analysis could be conducted by plotting campaign success against the length of time the campaign was lauched as well as revenue spent in advertising and goal funding normalized against expected scale and cost of production.
