# kickstarter-analysis
analysis of kickstarter campaigns
# Kickstarting with Excel
## Overview
- In this spreadsheet, I took the data from a list of kickstarter campaigns provided by Louise and applied statistics in Excel to find the desired information for Louise to see how other campaigns did compared to hers. The specific information Louise is looking for is the Outcomes Based on Launch Date and Outcomes Based on Goals, these a provided with the final excel spreadsheets of the complete data anaylsis. 
## Analysis and Challenges
### Data Analysis
-The start of this analysis was to create additional data from the data provided. This additional data included the percentage of the goal funded, the average donation of each campaign, converting the campaign start and end dates from Unix Timestamps to the day-month-year format, and lastly extracting the year each campaign was ran. Afters this additional data was extracted from the provided data, pivot tables were created sorting out the specific data that was being sought after and charts were created in order to make this data easier to visualize. 
#### Performed Analysis
- To find any of the percentages needed for this anayalsis the following equation was used with the corresponding cells =ROUND(E2/D2*100,0)
- The convert the Unix Timestamps to day-month-year the following equation was used: =(((J2/60)/60)/24)+DATE(1970,1,1). 
- To sort the successful, failed, and canceled campaigns based on goal range the following CountIfs statement was used: =COUNTIFS(Kickstarter!D:D,"<1000",Kickstarter!F:F,"successful",Kickstarter!R:R,"plays"), with appropriate conditional range substituted in.
#### Challenges
- The challenges and difficulties I encountered with this data set was determining the CountIFs statement. This is one equation I have not personally used in excel in the past, so getting it formatted correctly was difficult. The difficulty I had with this statement was getting the correct number of campaigns to populate for each range, I was able to overcome this difficulty by looking in the help tab of excel as well as utilizing my classmates in Slack. One other challenge that can be seen with this dataset is the shear size of the data itself, this is one of the largest sets of data I have worked with in my educational career, by freezing the intial column and header row I was able to overcome this difficulty. 
### Analysis of Outcomes Based on Launch Date
- The Outcomes Based on Launch Date chart shows the data for the each theater campaign sorted by month and whether is was successful, failed, or was canceled. According to this, 839 of the 1369 theaters campaigns were success with 493 that failed, and 37 canceled for one reason or another. The highest number of successful campaigns were started åin May and June, with the lowest amount of successful campains launch in December. The month December looks to be split between the amount of succsessful campaigns and those that failed. The highest prevalence of failed campains occurs in the month of October, which is also the same month that no one campaign was canceled. The month of December has equal numbers of successful campagins as it does failed campaigns. 
- ![Theater_Outcomes_vs_Lauch ](https://user-images.githubusercontent.com/111200771/187825422-7a81f058-b4ab-45c4-b7d5-be334b2ced97.png)
### Analysis of Outcomes Based on Goals
- The Outcomes Based on Goals chart shows the percentage of failed, successful, and canceled campaigns based on campaign goals in increments of 1000 up to 50000 for the funding goals for the subcategory, plays. For plays specifically, there were no canceled campaigns, meaning they were all completed. This chart is not as straight forward between successful and failed campaigns, there are a couple of goals increments were there were more failed campaigns than successful and vise versa, it is not as cut and dry. According to the chart, the campaigns with a lower goal had a higher percentage of successes than failed, but in the 15000 to 35000 there was a greater percentage of failures than success. For campaigns with goals 35000 to 45000 the successes were higher than the failures, with the remaining campaigns with goals greater than 45000 having the least amount of successes compared to failures. 
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/111200771/187825247-ebee7050-9023-4a13-a477-a87dbbed26a4.png)
## Results
### What are two conclusions you can draw about the Outcomes based on Launch Date?
 - Two conclusions that can be made about the Outcomes based on Launch Date are that there is a better chance of having a successful campaign if it is launched within the late spring and early summer months, so May or June, and it is least likely to succeed in the winter months, or November, December, or January. 
 ### What can you conclude about the Outcomes based on Goals?
 - One can conclude form the Outcomes based on Goals chart, that the smaller the goal the more likely you are to be successful in your campaign.
 ### What are some limitations of this dataset?
 - The biggest limitation of the this dataset is the shear amount of provided data, there was some data that was not neccessary in order to evaluate for what the client, Lousie, needed in order to see how other campaigns in her category fared. The amount of excess data made it a little difficult to extrapolate the necessary data points. 
### What are some other possible tables and/or graphs that we could create?
