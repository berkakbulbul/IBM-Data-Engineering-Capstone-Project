# IBM-Data-Engineering-Capstone-Project

![image](https://user-images.githubusercontent.com/108534539/218347565-ebebee5e-3de3-427a-8370-cef5e44c3591.png)


## Environment
This document introduces you to the data platform architecture of an ecommerce company named SoftCart.

SoftCart uses a hybrid architecture, with some of its databases on premises and some on cloud.

### Tools and Technologies:
- OLTP database - MySQL
- NoSql database - MongoDB
- Production Data warehouse – DB2 on Cloud
- Staging - Data warehouse – PostgreSQL
- Big data platform - Hadoop
- Big data analytics platform – Spark
- Business Intelligence Dashboard - IBM Cognos Analytics
- Data Pipelines - Apache Airflow

## Process
- SoftCart's online presence is primarily through its website, which customers access using a variety of devices like laptops, mobiles and tablets.

- All the catalog data of the products is stored in the MongoDB NoSQL server.

- All the transactional data like inventory and sales are stored in the MySQL database server.

- SoftCart's webserver is driven entirely by these two databases.

- Data is periodically extracted from these two databases and put into the staging data warehouse running on PostgreSQL.

- Production data warehouse is on the cloud instance of IBM DB2 server.

- BI teams connect to the IBM DB2 for operational dashboard creation. IBM Cognos Analytics is used to create dashboards.

- SoftCart uses Hadoop cluster as it big data platform where all the data collected for analytics purposes.

- Spark is used to analyse the data on the Hadoop cluster.

- To move data between OLTP, NoSQL and the dataware house ETL pipelines are used and these run on Apache Airflow.

## Scenario

You will assume the role of an Associate Data Engineer who has recently joined an e-commerce organization. You will be presented with a business challenge that requires building a data platform for retailer data analytics.


## Tasks

-	OLTP Task 2: Design a table named sales_data. (3pts)
-	OLTP Task 3: Import the data in the file oltpdata.csv. (1pt)
-	OLTP Task 8: Write a bash script to export data. (3pts)
-	NoSQL Task 1: Import 'Catalog.json' into mongodb server server into a database named 'catalog' and a collection named 'electronics'. (2pts)
-	NoSQL Task 4: Create an index on the field "type" (2pts)
-	NoSQL Task 7: Write a query to find out the average screen size of smart phones. (2pts)
-	Data Warehousing Task 1: Design the dimension table softcartDimDate. (2pts)
-	Data Warehousing Task 2: Design the dimension table softcartDimCategory, softcartDimItem, SoftcartDimCountry. (3pts)
-	Data Warehousing Task 3: Define the fact table softcartFactSales (2pts)
-	Data Warehouse Reporting Task 1: Create a grouping sets query using the columns country, category, totalsales. (2pts)
-	Data Warehouse Reporting Task 2: Create a cube query using the columns year, country, and average sales. (2pts)
-	Data Warehouse Reporting Task 3: Create an MQT named total_sales_per_country using the columns country and total sales. (4pts)
-	Dashboard Creation Task 4: Create a line chart. (2pts)
-	Dashboard Creation Task 6: Create a pie chart. (2pts)
-	Dashboard Creation Task 5: Create a bar chart. (2pts)
-	ETL Task 1: Implement the function get_last_rowid() (2pts)
-	ETL Task 2: Implement the function get_lastest_records() (2pts)
-	ETL Task 3: Implement the function insert_records() (2pts)
-	Pipelines Task 2: Define the DAG (2pts)
-	Pipelines Task 3: Create a task to extract data (2pts)
-	Pipelines Task 4: Create a task to transform the data in the txt file (2pts)
-	Big Data Task 5 - Print the top 5 most frequently used search terms. (2pts)
-	Big Data Task 6 - Load the sales forecast model. (1pt)
-	Big Data Task 7 - Using the sales forecast model, predict the sales for the year of 2023. (1pt)
