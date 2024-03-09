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


