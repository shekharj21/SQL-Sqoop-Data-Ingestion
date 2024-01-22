# SQL-Sqoop-Data-ingestion

## Problem Statement :

Use Sqoop to read data from SQL database and import it into Hadoop.
You need to build the following requirement:
- Create SQL database at any cloud platform.
- Design an Ecommerce database and store 10 GB record in SQL Database.
- Use Sqoop to load data from SQL Database to Hadoop.
- Schedule pipeline such a way that new data from Database can be transferred to Hadoop automatically on daily basis.

## Create EC2 Instance :
![Screenshot (513)](https://github.com/shekharj21/shekharj21/assets/54074505/613e72eb-a6b5-4e6c-9cec-31e9fa7cbaaf)
1. Create a EC2 Instance.
2. Please choose OS as ubuntu.
3. Make sure we create a new security group or use a previous one where Setting is selected as SSH and assigned to user's IP.
4. Download a key-pair in .ppk format so we can use it to connect it to the putty.
5. If there is error message saying "connection timed out" then please refer this video -------> https://www.youtube.com/watch?v=YWwJuO9299s

## EC2 Connection to Putty :
![Screenshot (514)](https://github.com/shekharj21/shekharj21/assets/54074505/0ebc14a7-f3c0-46a7-be1d-0f8476ab5f69)
1. Download and install Putty.
2. make use of PuttyGen if private key is in .ppm file and not in .ppk
3. Open PuttyGen and Load the .ppm keypair file downloaded from instance.
4. Save as private key and give the same name as .ppm key_pair filea and save it.
6. Copy the Public IPv4 DNS from EC2 instance and Paste inside Host Name of putty.
7. Go to SSH----> Auth ------> Credential
8. Select the .ppk file in Private key Authentication file section and open it.
![Screenshot (516)](https://github.com/shekharj21/shekharj21/assets/54074505/183b5a8b-0f6e-47e6-9044-cff54dd304dc)


## Create a AWS RDS Database :
![Screenshot (512)](https://github.com/shekharj21/shekharj21/assets/54074505/d335a599-e733-41ec-a12a-6fdf7ba7f1fa)

1. Make sure to chnage the security rules.
2. Make sure inbound and outbound security rules are stated properly.
3. Make sure the Database is publically Accessible.

## Connect AWS RDS with MySQL Workbench :
![Screenshot (511)](https://github.com/shekharj21/shekharj21/assets/54074505/bf65698c-15d9-4d8f-89c3-78a14baafdf5)
1. Select the Connection name.
2. Copy the endpoint from RDS and paste it in the Hostname of MySQL Workbench.
3. Add the Username used while creating RDS account and add the password too.
4. Click on test connection and if its successful then create the connection.
1. if you are facing the error while making connection, then Make sure to check the security group inbound and outbound rules otherwise it can create problem connecting with MySQL workbench.
2. If you are having any issue cconnecting with MySQL Workbench then refer this video ------> https://www.youtube.com/watch?v=N4tz-S65lVo&t=281s

## Create Table Schema and Add Records :
1. At this point, i am assuming that we are successfully connected the RDS with MySQL Workbench.
2. We will create a schema of the table, by creating the different tables. (Schema.sql)
3. we will add records in the table. (Records.sql)

## Install Airflow on EC2 instance using Putty.
- Please refer following video for airflow installation ------->   https://www.youtube.com/watch?v=6HQiiUk-a_o
