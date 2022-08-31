# kickstarter-analysis
# Kickstarting with Excel

## Overview of Project

Louise, a Playwright is willing to start a crowdfunding campaign for her play and expecting a budget of over $10,000 for this play. She is little worried about starting her first campaign, so we will be assisting Loiuse with various Data Analysis skills such as filter/format the raw data which will result in creating the easy visualization of the data. Thus, helping her to generate the ideas and factors for a successful campaign.


### Purpose

The purpose of this project is to analyse the previous data to help Louise with her fundraising campaign. In this project we will be using data analysis skills and excel functions to filter the Kickstarter data and create the pivot tables, charts and graphs for the better visualization of the data. This will enhance the decision making skills for Louise for her play "fever".

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

For this analysis, we have to create pivot table and Line chart of the theater outcomes( "successful", "failed", "canceled") based on the Launch date.
Starting with the analysis, first we have to figure out that the Kickstarter data is in readable format. We can see that the data in columns deadline and launched_at is in Unix timestamps rather than in standard date format. Therefore, we will be using advanced formula for this conversion and convert the data into readable format (month, date, year). Then we will create new column "Years" and apply =YEAR() function to extract the year from the "Date" Column. 
Inorder to achieve more refined data we will break down the Column "Category and Subcategory" into "Parent Category" and "Sub category".
Next, we will create pivot table based on "Parent category" and "Years" with "date created conversion" as rows and "outcomes" as columns and values. Then we have to filer "successful", "failed", canceled" from the outcomes column and filter the "Parent Category" to display the data for "theater".
Finally we will generate the Line chart for the visualization of the data selected and filtered.

![Test Image](/Resources/Theater_Outcomes_vs_Launch.png)

From this Line Chart we can conclude that Month of May has the most successful theater events. 

### Analysis of Outcomes Based on Goals

jj

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
