# Kickstarter-Analysis

## Overview

This an excel spreadsheet analyzing different kickstarter programs.  Analyzing and comparing trends with what was successful and what failed.
The purpose of this project was to focus on two areas of the data.  First, theater outcomes based on when the project was launched.  Data was extracted to visualize if the time of year the fundraising is started makes a difference in the success of meeting the goal needed to fund the project.  The second area of focus was the plays subcategory and the amount of money needed to fund it. Were certain ranges of goals more successful?

## Analysis
To analyze theater outcomes based on when the project was launched, a pivot table was created.  See below.

![image](https://user-images.githubusercontent.com/85581208/138557595-6b2c114c-e62c-4223-9cb2-d8b650d9cc96.png)
The pivot table separated the theater information by month.  Then plotting the information in a line plot made it easy to visualize the months that had the most success.  Noted next to the pivot table in above screenshot.  One of the challenges was the number of theater projects per month.  It varies each month.

To analyze the outcomes based on goals, a new sheet was started pulling information from the Kickstarter sheet.  Information pulled, included, twelve ranges of dollar values.  Starting with less than $1,000 all the way to greater than $50,000.  It looked like this.
<img width="1280" alt="Screen Shot 2021-10-24 at 8 56 59 PM" src="https://user-images.githubusercontent.com/85581208/138623547-963c6156-3a43-41cb-80ef-7df49d631bdd.png">
From there, the COUNTIFS command was used to pull out plays that had their fundraiser goal in each range within the columns of successful, failed, or canceled.  The coding used looked like this =COUNTIFS(Kickstarter!D:D,<1000, Kickstarter!F:F, "successful", Kickstarter!D:D, "plays") for example. This formula was applied to each column and row to determine in each range of goal how many play were successful, failed, or canceled.  Then a total was calculated using the SUM function.  After calculating the sum, the percentage of successful, failed, and canceled for each range could easily be calculated by dividing what was in each cell of successful, failed, and canceled by the total number of projects in each range.  Once those percentages were solidified a line graph was created titled Outcomes Based on Goals.
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/85581208/138624591-30dd35eb-55c0-4fcc-8a78-2749cc7a45c1.png)

## Challenges and Difficulties
Different challenges occurred during the analysis.  Looking at the data for the outcomes by launch date, there were a decent range of theater projects launched each month.  It ranged from 75-153.  Not a consistent number which could have skewed the data a little.  Another challenge in the data is it is only theater projects.  It is not assessing what types of projects.  A percentage of each category might have been a better representation.
In the outcomes based on goals sheet, it was challenging to use the COUNTIFS function at first.  It took some time to figure out how to place each component correctly and the first go round, the filtering of plays was forgotten.  After editing that, it was a little easier.  It was very tedious.  Another challenge within this data was again the amount of projects in each range.  There were very few as the range increased.

## Results
After creating the Theater Outcomes by Launch Date sheet and illustrating it in a line chart, it appears May is a very good month to launch for raising funds in theater projects.  When looking at the line graph, May, June, and July have the highest success rates.  May also has the highest number of successful projects out of all the other months but it also had one of the highest failed project numbers as well.  I think to further the analysis a percentage of successful, failed, and canceled for each month would be a better measure. Not doing this appears to limit the power of the data and making a conclusion for the future. With the data as of now, it appears February, May,June, July, and August appear to be a better time to launch with more chance of success in those months.

The outcomes based on goals appears to be pretty straightforward,  the most success occurred in the lowest range of less than 1000.  As you move up in the ranges the success rate keeps plummetting.  It is easier to raise a smaller amount so this is no surprise.
