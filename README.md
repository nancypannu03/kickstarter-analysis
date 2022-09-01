
# Kickstarting with Excel

## Overview of Project

Louise, a Playwright is willing to start a crowdfunding campaign for her play and expecting a budget of over $10,000 for this play. She is little worried about starting her first campaign, so we will be assisting Louise with various Data Analysis skills such as filter/format the raw data which will result in creating the easy visualization of the data. Thus, helping her to generate the ideas and factors for a successful campaign.


### Purpose

The purpose of this project is to analyse the previous data to help Louise with her fundraising campaign. In this project we will be using data analysis skills and excel functions to filter the Kickstarter data and create the pivot tables, charts and graphs for the better visualization of the data. This will enhance the decision making skills for Louise for her play "fever".

## Analysis and Challenges

[Kickstarter Challenge](/Kickstarter_Challenge.xlsx) <br/>

[Kickstarter Challenge ZIP FILE](/Kickstarter_Challenge.zip)

### Analysis of Outcomes Based on Launch Date

For this analysis, we have to create pivot table and Line chart of the theater outcomes( "successful", "failed", "canceled") based on the Launch date.
Starting with the analysis, first we have to figure out that the Kickstarter data is in readable format. We can see that the data in columns deadline and launched_at is in <b>Unix timestamps</b> rather than in <b>standard date format</b>. Therefore, we will be using advanced formula for this conversion and convert the data into readable format (month, date, year). Then we will create new column "Years" and apply <b>=YEAR() </b> function to extract the year from the "Date" Column. 
Inorder to achieve more refined data we will break down the Column "Category and Subcategory" into <b>"Parent Category"</b> and <b>"Sub category"</b>.
Next, we will create pivot table based on "Parent category" and "Years" with "date created conversion" as rows and "outcomes" as columns and values. Then we have to filer "successful", "failed", canceled" from the outcomes column and filter the "Parent Category" to display the data for "theater".
Finally we will generate the Line chart for the visualization on the basis of filtered and selected data.

![Test Image](/Resources/PivotChart_Outcomes_vs_Launch.png) <br/>

![Test Image](/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

In this Analysis, we have to figure out the percentage of the total successful, failed and canceled plays based on dollar amount goal ranges.
For this, we created a new sheet named as "Outcomes Based On Goals" with the following Columns: <br />

-Goal <br />
-Number Successful <br />
-Number Failed <br />
-Number Canceled <br />
-Total Projects <br />
-Percentage Successful <br />
-Percentage Failed <br />
-Percentage Canceled <br />

Created following rows in "Goal" Column as dollar amount ranges: <br />
-Less Than 1000 <br />
-1000 to 4999 <br />
-5000 to 9999 <br />
-10000 to 14999 <br />
-15000 to 19999 <br />
-20000 to 24999 <br />
-25000 to 29999 <br />
-30000 to 34999 <br />
-35000 to 39999 <br />
-40000 to 44999 <br />
-45000 to 49999 <br />
-50000 or more <br />

Inorder to get the values for the columns "Number Successful", "Number Failed", "Number Canceled", we will use <b>=COUNTIFS()</b> function, by using the criteria for subcategory as "plays". <br />
<b>example: =COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<1000",Kickstarter!$T:$T,"plays") </b>
<br />
Total projects values will be equivalent to the total of all three Columns: ("Number Succesfful"+ "Number Failed" + "Number Canceled"). we will use <b>=SUM()</b> function inorder to retrieve these values. <br />
Percentage Successful/ Failed/ Canceled will be calculated by <b>(Successful events/total Projects) * 100 %</b> <br />
Finally we will generate a Line Chart illustrating the relations between the outcomes based on "plays" percentage and the Goal Range.

![Test Image](/Resources/PivotChart_Outcomes_vs_Goals.png)</br>
  
![Test Image](/Resources/Outcomes_vs_Goals.png)


### Challenges and Difficulties Encountered
The main Challenges I expereinced in this Analysis project : <br />
- The data was not in the readable format. For example, the date was in Unix Timestamp which was later converted to the readable format (month, date, year) by using the the appropriate formula. <br />
- Another Challenge I encountered was with the Pivot Chart, to determine what Columns need to dragged to the Rows, Columns and Values specified spacing inorder to make data more representable and easy for the visualization. <br />
- Thirdly, with the usage of the COUNTIFS() formula, had to try it for few times inorder to achieve the desired results.



## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  -Firstly, we can conclude that we achieved highest success rate of "Theater" outcomes in the month of May followed by June, July.In the month of November, December and January we experience the lowest success rate of the theater outcomes. <br />
  -Failure rate of the theater outcomes is the lowest in January, march, September, November and none of the event has been canceled in October.<br />


- What can you conclude about the Outcomes based on Goals?

  -On the basis of "Outcomes Based On Goal" Line chart I can conclude that the percentage of the successful Outcomes is relatively high when the funding goal is less than 4999 and the rate of success decreases with the increase of the funding goals.<br />
  -Even The failure rate of the theater outcomes is the lowest when the funding goal is less than 4999. The trend of the failure keeps on increasing with the higher funding goals. <br />
-The canceled percentage remains constant with the funding goals.<br />



- What are some limitations of this dataset? <br />
   -The main limitation is these results are just based on the theater outcomes whereas, results will vary if we use the other categories such as games, publishing, music. Therefore, the outcomes must be limited on the the basis of theater category. <br />
   -Same with the second line chart: "Outcomes Based on Goals is just limited to "plays" subcategory, we should expand and explore the analysing platform so that we can interpret the data in a better way. <br />

- What are some other possible tables and/or graphs that we could create? <br />
  -We can add an extra filter on the subcategory, for example "theater" has further sub categories -"plays","musical" and "spaces" and create a line chart to figure out the trend of all the subcategories as well.
  - We can create boxplots and identify outliers for easier and effective decision making.
