# Kickstarting with Excel

## Overview of Project
### Background of the Project
The project's focus is to aid Louise in confidently planning a Kickstarter campaign to successfully obtain funding for her play based on trends determnied by studying previous campaigns. The trends are determined by analysing the data of previous Kickstarter crowdfunding campaigns (over 4,000 campaigns). 
### Purpose of this analysis
The analysis carried out here focus specifically on the data regrding crowdfunding campaigns for the parent category theater and its subcategory plays. 

The first part of the analysis examine the campaigns' outcomes for theater campaigns in respect to the campaign's launch date. This dataset of the Kickstarter data is displayed in a PivotTable and visualised through a line graph. This is done to demonstrate the correlation between launch dates and campaign success, aiding Louise in deciding what time is best to successfully carry out her campaign.

The second part of the analysis examine the campaigns' funding goal in the plays subcategory, and weather the campaign was successful. failed, or got cancelled. The data is visualised in a line graph as well. This is done to aid Louise in setting her campaign's goal.


## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date Describe the steps you followed and explain the code with snippets
Beyond viewing the sum of successful, failed, and cancelled campaigns for each month of the launch year in a PivotTable, the table's data is also visualised by the line graph below (Theater Outcomes vs Launch).

![image1](/Resources/Theater_Outcomes_vs_Launch.png)

#### To create this line graph the following steps were followed:  
**1.** Using the code below, and applying it to the "launched_at" column of the Kickstarter data, the Unix timestamp was converted to a readable date in the short date format (yyyy-mm-dd). The new column was named "Created Date".
>Unix Timestamp to readable date code: =(((cell_of_launched_at/60)/60)/24)+DATE(1970,1,1)  

**2.** The **YEAR()** function was then applied to the "Created Date" column to extract the year value of the campaign's created date. This value was stored in the "Years" column.  
**3.** The entirety of the data was used to create a PivotTable. The table's column data is the outcomes (filtered to exclude live campaigns), rows is the Created Date (by months after the year value is ungrouped), the values is the count of outcomes, and it is filtered by the years and Parent Category (theater).  
**4.** The PivotTable was finally used to create the line graph.
### Analysis of Outcomes Based on Goals Describe the steps you followed and explain the code with snippets
Below is the Outcomes vs. Goals line graph visualising the percentage of successful, cancelled, and failed campaigns in relation the their goals.
![image2](/Resources/Outcomes_vs_Goals.png)

#### To create this line graph the following steps were followed:  
**1.** The table were the data of counting the number of successful, failed, cancelled, their percentages and totals was set up.  
**2.** The **COUNTIFS()** function was applied to each cell, modifying the code based on the goal's range and outcome status. The subcategory remained constant as plays.  
For example, the conditions set in the code below will only increase the count by 1 in the cell if: the value of the goal is less than $1,000, the outcome value is "succussful", and when the subcategory is "plays".
> = COUNTIFS(Kickstarter!$D:$D, "<1000", Kickstarter!$G:$G, "successful", Kickstarter!$T:$T, "plays")  

In the case of the code below, the conditions set will only increase the count by 1 in the cell if: the value of the goal is greater than or equal to $25,0000 and less than or equal to $29,9999 the outcome value is "failed", and when the subcategory is "plays".
> =COUNTIFS(Kickstarter!$D:$D, ">=25000", Kickstarter!$D:$D, "<=29999", Kickstarter!$G:$G, "failed", Kickstarter!$T:$T, "plays")  

**3.** The total projects of all outcomes in a goal range was calculated using the **SUM()** function.  
**4.** Dividing the total of number of each outcome by the total project, and setting the data style to "Percent" was used to calculate the percentage values. The calculated percentage values for each outcome were graphed against the goal ranges as a line graph.     
### Challenges and Difficulties Encountered
#### YEAR() Function
YEAR() function did not provide the correct output since column where the function was being applied had short date type. I tested the function YEAR(TODAY()) on a new sheet an it worked. The difference was that the data type there was general. This issue was resolved by setting the Year column's data type to general
#### PivotTables Features
* PivotTables fields were missing when a new column is added. This issue was resolved by refreshing the pivot table (right-click on table and click referesh. refreshes table cache)
https://answers.microsoft.com/en-us/msoffice/forum/all/missing-column-from-table-in-pivot-table-field/4f85a8b5-50c9-45b7-8b5e-b8481984995a
Learned
* Grouping/Ungrouping of pivot table fields, especially dates
https://support.microsoft.com/en-us/office/group-or-ungroup-data-in-a-pivottable-c9d1ddd0-6580-47d1-82bc-c84a5a340725?ui=en-us&rs=en-us&ad=us

## Results (in complete and coherent sentences)

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?

## Challenges
* YEAR() function did not provide the correct output since column where the function was being applied had short date type. I tested the function YEAR(TODAY()) on a new sheet an it worked. The difference was that the data type there was general. This issue was resolved by setting the Year column's data type to general. 
* PivotTables fields were missing when a new column is added. This issue was resolved by refreshing the pivot table (right-click on table and click referesh. refreshes table cache)
https://answers.microsoft.com/en-us/msoffice/forum/all/missing-column-from-table-in-pivot-table-field/4f85a8b5-50c9-45b7-8b5e-b8481984995a

## Learned
* Grouping/Ungrouping of pivot table fields, especially dates
https://support.microsoft.com/en-us/office/group-or-ungroup-data-in-a-pivottable-c9d1ddd0-6580-47d1-82bc-c84a5a340725?ui=en-us&rs=en-us&ad=us

## To ASK
* From deliverable 1: The row labels are changed to display the months of the year, and ???the campaign outcomes are sorted in descending order??? (5 pt).

