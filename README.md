# SQL-Sqoop-Data-ingestion

## Problem Statement :

Use Sqoop to read data from SQL database and import it into Hadoop.
You need to build the following requirement:
- Create SQL database at any cloud platform.
- Design an Ecommerce database and store 10 GB record in SQL Database.
- Use Sqoop to load data from SQL Database to Hadoop.
- Schedule pipeline such a way that new data from Database can be transferred to Hadoop automatically on daily basis.

## Create a AWS RDS Database :
1. Make sure to chnage the security rules.
2. Make sure inbound and outbound security rules are stated properly.
3. Make sure the Database is publically Accessible.

## Connect AWS RDS with MySQL Workbench :
1. 
1. Make sure to check the security group inbound and outbound rules otherwise it can create problem connecting with MySQL workbench.
2. If you are having any issue cconnecting with MySQL Workbench then refer this video ------> https://www.youtube.com/watch?v=N4tz-S65lVo&t=281s
