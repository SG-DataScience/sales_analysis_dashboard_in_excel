
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

![create table data](https://user-images.githubusercontent.com/80168505/143173325-f81cc0aa-9fcb-49fb-9666-ee544d653776.png)
 
 ### Create pivot table for Line chart:

 - Name the table - LinePivot
 - Group Dates by Month & Year
 - Format Numbers
 - Insert Line Chart

 ![line charts](https://user-images.githubusercontent.com/80168505/143177092-6fbfb27e-2c8c-4ba0-86c1-fbfc78ed2275.png)

### Create pivot table for Bar chart by category:

- Copy Line Chart sheet
- Name the table - CategoryPivot
- Sort Grand Total in ascending order 
- Insert Bar chart

![category pivot](https://user-images.githubusercontent.com/80168505/143177633-e21db3cf-ff55-417a-a421-38c13d2ca0d5.png)

### Create pivot table for Bar chart by Manager:

- Name the table - ManagerPivot
- Sort Grand Total for state in ascending order 
- Insert Bar chart

![manager pivot](https://user-images.githubusercontent.com/80168505/143178085-411924cb-0c55-4a98-8ce8-be9241d4f1b1.png)

### Create a pivot table for Pie chart by chain field:

- Name the table -PiePivot
- Set to 'show items with no data'
- Insert Pie chart

![pie pivot](https://user-images.githubusercontent.com/80168505/143180877-02ebeb3a-5864-45ec-805f-c14953f93f3f.png)

### Create Sparkline pivot table:

- Name the table -SparklineTotalPivot
- Name the table -SparklinenextPivot
- Name the table -SparklineFashionsPivot
- Set to 'show items with no data'

![sparkline pivot](https://user-images.githubusercontent.com/80168505/143182514-61c7603a-906b-4c05-be73-e671017b8987.png)

### Create a pivot table for map chart:

- Name the table -MapPivot
- Country Field Settings Tabular & Repeat Labels

![map pivot 1](https://user-images.githubusercontent.com/80168505/143183426-1e1678c4-6b0b-4828-a629-28542573c74c.png)

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
    
    ![slicers](https://user-images.githubusercontent.com/80168505/143185563-ff9db683-3961-480c-9c97-82a4806a74de.png)

- Link the slicers with the charts

    ![link the slicers](https://user-images.githubusercontent.com/80168505/143187497-f2fbcb54-b9e2-4149-a89b-1ed965e4753f.png)

### Format and Align:

- Set Slicer Position and Layout to 'Disable Resizing'
- Set Theme - Organic

### Add dynamic label to the Pie chart:

- Add a dynamic label by using the below formula-

    ![dynamic label formula](https://user-images.githubusercontent.com/80168505/143188965-f3f8fdef-6d29-4a45-9fc4-a2b0b883dd40.png)

### The Final Dashboard looks like --

![final dashboard](https://user-images.githubusercontent.com/80168505/143191103-0dbee2c9-04aa-4fe4-9375-d9c84a4317bc.png)

    
