# AdventureWorks-Analysis-with-Microsoft-Fabric-and-SQL-Server
The objective of this project is to create an interactive dashboard that enable a SQL view in SQL Server On-Premises and Integrate the data into Microsoft Fabric

## About the Dataset
The dataset used for this project is a backup database file (.bak) that has been imported into the MySQL database. The backup database file was downloaded from [Microsoft Learn](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms).

## Project Architectuer

This project maximizes the capabilities of Microsoft Fabric by seamlessly extracting data from a VIEW in my SQL Server and loading it into Microsoft Fabric to create a dynamic and interactive dashboard. The first step involved establishing an On-Premises gateway connection to facilitate seamless communication between Microsoft Fabric and SQL Server and Creating a Workspace in Power BI.

*SQL View*
![SQL View](https://github.com/Ainaganiu/AdventureWorks-Analysis-with-Microsoft-Fabric-and-SQL-Server/blob/main/Pictures/sql_view.png)

*GateWay Connect*
![GateWay Connection](https://github.com/Ainaganiu/AdventureWorks-Analysis-with-Microsoft-Fabric-and-SQL-Server/blob/main/Pictures/gateway_connect.png)

Following the successful creation of the gateway connection, the dataset underwent loading into a Lakehouse using dataflow Gen2. Subsequently, the semantic link in Microsoft Fabric Lakehouse was employed to connect the data to Power BI Desktop for visualization purposes.

*DataFlow Gen2 Connection*
![DataFlow Gen2](https://github.com/Ainaganiu/AdventureWorks-Analysis-with-Microsoft-Fabric-and-SQL-Server/blob/main/Pictures/DataFlow_Gen2.png)

Initially, the plan was to utilize DirectQuery Mode; however, considering that the database is not live, Import Mode was chosen for enhanced performance. Additionally, various data transformations were applied, including altering column names, creating a Date table using DAX, profit calculation, adjusting column data types, and generating measure tables. These steps were crucial to optimize the data for effective visualization and analysis.

*Data Model Power BI*
![Data Model](https://github.com/Ainaganiu/AdventureWorks-Analysis-with-Microsoft-Fabric-and-SQL-Server/blob/main/Pictures/DataModel_PowerBI.png)

## Findings from the Analysis

*Main Page*

![Dashboard Pic1](https://github.com/Ainaganiu/AdventureWorks-Analysis-with-Microsoft-Fabric-and-SQL-Server/blob/main/Pictures/dashboard.png)

Based on the findings results, the company made a total sale of 18.9 million in relation to the KPI of 10 million dollars. This shows the commitment and drive of the entire company staff for keeping work with the company goals.

The total quantity ordered from 2011 to 2014 for Adventure Works is 438 thousand items, while the company receive their highest order in a year in 2013 (2022 million Dollars). This implied that within the last 3 financial year for Adventures Works, 46% of total ordered quantity comes from 2013 financial year.

Among the 4-product category, Bikes 81% of the share revenue. Also, Road Bikes is the most ordered product by subcategory followed by Helmets, Jerseys, Mountain Bikes and Road Frames. The insights further indicate that the company also makes most profit in 2013. Also, March in Year 2014 made up 6.23% of Total Revenue. 2013 had the highest average Total Revenue (Sales) at 8,704,834.61, followed by 2012, 2014, and 2011.

*Profit Margin DrillThrough Page**
![DrillThrough](https://github.com/Ainaganiu/AdventureWorks-Analysis-with-Microsoft-Fabric-and-SQL-Server/blob/main/Pictures/DrillThrough_1st.png)
![DrillThrough](https://github.com/Ainaganiu/AdventureWorks-Analysis-with-Microsoft-Fabric-and-SQL-Server/blob/main/Pictures/DrillThrough_Page.png)

Among the five countries that were analysed the united has the (62.70%) of contribution towards the total revenue with profit of 57 million dollars profit. Canada has the highest profit margin 38%, which implied that the company retain 38% of their revenue (sales) has profit. This can be attributed operating cost of doing business in Canada compared to other region the company is operating.

## Recommendation

The study recommends that more Bikes inventories should be made available in-stock around March and May because this two are subjected to experience high sales. 
Furthermore, more goods should be purchased or produced in due to high profit margin and revenue generated in this region.
Improvement in advertising and promotion about company products in Australia and Germany. Furthermore, the company should conduct further analysis on the reason for low profit margin in Australia evaluating factors such as Operating Cost, Tax and government policies.

## Dashboard
[Click here to view the dashboard](https://app.fabric.microsoft.com/view?r=eyJrIjoiN2E1OTE4ZDEtY2I5MS00ODM1LTgyZTctNjkyYjIzZjUxMzAyIiwidCI6IjUzNjJiMjkyLTI2ZGEtNGE2Yi05OWQ3LWM5ZjJiZWRiOWE2YyIsImMiOjh9) 



