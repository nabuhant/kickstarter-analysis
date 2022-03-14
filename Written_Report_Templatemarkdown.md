# Kickstarting with Excel

## Overview of Project
### Background of the Project
### Purpose of this analysis

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Describe the steps you followed and explain the code with snippets
![image1](https://raw.githubusercontent.com/nabuhant/kickstarter-analysis/main/Resources/Theater_Outcomes_vs_Launch.png?token=GHSAT0AAAAAABSKACJ2B45BO5BISPWMSR52YROQ3SQ)

### Analysis of Outcomes Based on Goals
Describe the steps you followed and explain the code with snippets
![image2](https://raw.githubusercontent.com/nabuhant/kickstarter-analysis/main/Resources/Outcomes_vs_Goals.png?token=GHSAT0AAAAAABSKACJ2Y35M25GI3JMPQ3RYYROQ2KQ)
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

