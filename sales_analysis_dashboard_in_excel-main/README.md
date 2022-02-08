
# Sales Dashboard in Excel

## Project Description:
The purpose of this project is to build a dashboard regrading sales report of two big fashion stores "New Look" and "Fashion Direct" in Australia.We are building this dashboard so that in later stages we can make some insightful business decisions based on this sales dashboard.
## Project Requirements:
- We should build this dahboard in such a way that it can be updated in an instance whenever we add new data to our raw data file.
- we need to use interctive tools like slicers in this dashboard so that we can selectively analyze our sales data whether areawise or timewise or managerwise.
- We have to add dynamic label in our chart.
## Project Walkthrough:
### Format data in table:
 
 First we formatted the raw data and give a name to the table-"Data".

![a](https://user-images.githubusercontent.com/80168511/153016176-65f54eb9-706c-42b2-bb47-9c30dd1f7ccc.PNG)

 ### Create pivot table for Line chart:

 - Name the table - LinePivot
 - Group Dates by Month & Year
 - Format Numbers
 - Insert Line Chart

 ![b](https://user-images.githubusercontent.com/80168511/153016230-b6f0388b-fbaf-43fd-800f-14281cb46a05.PNG)

### Create pivot table for Bar chart by category:

- Copy Line Chart sheet
- Name the table - CategoryPivot
- Sort Grand Total in ascending order 
- Insert Bar chart

![c](https://user-images.githubusercontent.com/80168511/153016250-452be3ce-40c9-4bac-ba10-984b09527f1b.PNG)
### Create pivot table for Bar chart by Manager:

- Name the table - ManagerPivot
- Sort Grand Total for state in ascending order 
- Insert Bar chart

![d](https://user-images.githubusercontent.com/80168511/153016319-4d4602a1-4881-4856-bd59-c322d569d073.PNG)
### Create a pivot table for Pie chart by chain field:

- Name the table -PiePivot
- Set to 'show items with no data'
- Insert Pie chart

![e](https://user-images.githubusercontent.com/80168511/153016346-5137c125-366f-4afd-8929-d53004b7c848.PNG)

### Create Sparkline pivot table:

- Name the table -SparklineTotalPivot
- Name the table -SparklinenextPivot
- Name the table -SparklineFashionsPivot
- Set to 'show items with no data'

![f](https://user-images.githubusercontent.com/80168511/153016424-ddb8e8d2-e098-468d-b16f-eed17ca6a583.PNG)

### Create a pivot table for map chart:

- Name the table -MapPivot
- Country Field Settings Tabular & Repeat Labels

![g](https://user-images.githubusercontent.com/80168511/153016455-8c1bed88-1098-45bc-a2b4-5c1a8cd0aba9.PNG)
- Remove Grand Totals
- Copy PivotTable and paste beside as values
- Insert Map Chart
- Edit the chart range so it points to the PivotTable again
- Delete the copied table

### Create a Dashboard sheet and move charts:

- Create a separate sheet for building the final Dashboard
- Move all the charts to this Dashboard sheet
- Set up Sparklines (use IF to handle states)
    
    =IF('Sparkline Pivots'!A6="","",'Sparkline Pivots'!A6)
- Add Conditional Formatting bars (show bar only)

     ![sparkline pivot2](https://user-images.githubusercontent.com/80168505/143184966-4c6c8fa2-4ee1-4d32-94d0-5728b7aa7123.png)

- Use GETPIVOTDATA to MapPivot & IFERROR  

    =IFERROR(GETPIVOTDATA("Sales",'Map Pivot'!$A$3,"State",D28,"Country","Australia"),"")

### Add Slicers:

- Add 3 slicers to the Dashboard
    1. Financial Year
    2. State
    3. Category
    
    ![h](https://user-images.githubusercontent.com/80168511/153016487-d0eb8847-cc4f-4d51-af26-3eaf488468e1.PNG)

- Link the slicers with the charts

    ![link the slicers](https://user-images.githubusercontent.com/80168505/143187497-f2fbcb54-b9e2-4149-a89b-1ed965e4753f.png)

### Format and Align:

- Set Slicer Position and Layout to 'Disable Resizing'
- Set Theme - Organic

### Add dynamic label to the Pie chart:

- Add a dynamic label by using the below formula-

    ![dynamic label formula](https://user-images.githubusercontent.com/80168505/143188965-f3f8fdef-6d29-4a45-9fc4-a2b0b883dd40.png)

### The Final Dashboard looks like --

![i](https://user-images.githubusercontent.com/80168511/153016504-8df3f736-5756-42fd-96a5-d469f7fa842b.PNG)

    
