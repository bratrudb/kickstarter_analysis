# Analysis of Kickstarter Campaigns
Performing analysis on Kickstarter campaigns to uncover trends

## Overview and Purpose of this Project
The purpose of this analysis is to gain insight into a variety of Kickstarter campaigns to find trends in previous campaigns to inform us what it takes to achieve a successful campaign.

## Analysis and Challenges

#### Analysis of Outcomes Based on Launch Date
The outcomes based on launch date analysis required the use of a pivot table to sort the count of successful, failed, and canceled outcomes for the theater category by month. One challenge this analysis could pose is working through how to sort the row labels by month. There are a couple different work arounds for this challenge. One is to create a new column on the Kickstarter tab and use the month() function applied to the date created conversion column to have a column with the months the Kickstarter was created. You could then use the month filed in the Rows section of the pivot table. The other option is to use the date created conversion field in the rows section of the pivot table and remove the Years2 and Quarters fields that automatically populate to return the months in the rows.

#### Analysis of Outcomes Based on Goals
The outcomes based on goals analysis required the use of the countifs() function to find the number of plays that were successful, failed, or cancelled across multiple goal levels. One challenge with this analysis was using the countifs() function. Depending on the different functions used, quotation marks are used differently. To develop the conutifs() function I referenced cells with the lower and upper bound of the goal level. This required using quotations only around the greater than or equals sign followed by an & and the cell as follows:  

=COUNTIFS(Criteria_Range_1,">="& cell_reference,Criteria_Range_2,"<"& cell_reference)  

This use of quotations is different than many other ways quotations are used in excel functions.

## Results

  * What are two conclusions you can draw about the Outcomes based on Launch Date?

There are two key conclusions  we can draw from the Theater outcomes by Launch Date. The first is that the months where Kickstarters are most likely to be successful are May and June. The second conclusion we have found in this analysis is that the proportion of Kickstarters that are successful are much lower in the final few months of a year with Kickstarters beginning in December less likely to succeed than not.

  * What can you conclude about the Outcomes based on Goals?

We can conclude that a Kickstarter is more likely to succeed when the fundraising goal is less than $15,000. If the fundraising goal is less than $15,000, a Kickstarter is more likely to be successful than not. It is difficult to draw any conclusions on the success of Kickstarters above $15,000 as less than 10 percent of the Kickstarters that are included in this data set started with goals above $15,000. 

  * What are some limitations of this dataset?

There are a few different limitations of this dataset. One limitation is the lack of campaigns that had goals above $15,000 in the play category. Another issue is the information provided about other campaigns lead one to believe that many of these campaigns are not professional productions. There are goals as low as $1 up to $100,000,000. Linda is attempting to work on a professional production. It is difficult to sort through and gain powerful insights if there are a significant number of campaigns in the dataset that do not represent professional productions.

  * What are some other possible tables and/or graphs that we could create?

I can think of many other graphs that would be helpful in this analysis. One analysis that could be helpful is a bar chart comparing the average donation across each of the different outcome categories. In this analysis, we would see that successful campaigns have an average donation over $20 higher than failed donations. 

Similarly, a bar chart showing the average number of backers of a campaign by outcome shows that the average donation is not the only indicator of success. Successful campaigns have 60 more backers on average than failed campaigns. This might be a more important indicator of success than the average donation or timing of the campaign. When filtered for a campaign created in December, the worst overall month for successful campaigns, we see that that successful campaigns have over 50 backers more on average than failed campaigns. 
