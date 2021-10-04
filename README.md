# Uber Case Analysis
## Description
In this project we grab the real time data from Kaggle and perform various operation on this data, and we separate it  into 3 different types of data so it will more effectively show the details. This contains all records of real time Uber rides.
After thinking 360 degrees we partitioned this data into 3 DataSets(Admin, Passesnger, Rider).
We were done this project over the integration with PySpark with Jupyter Notebook and using databricks cloud resources and perform all queries by using PySpark and SparkSQL also.
So we have 2 different types of syntaxes here.

## Tools and Technologies

Kaggle ( Real time data)

Jupyter Notebook ( used cases )

PySpark ( for Quries )

GitHub ( Deploy Project )

MS ( Excel --> File formats )

MS ( Power Point --> Presentation )

MS ( Word --> Project flow )

NotePad ( JSON )


## Features

Effective Discount on Uber Wallet & Trusted Contact

Display Vaccination Status for hygiene and safety

Average rating for Driver 

Free and Acquire data

Estimate Cost According to the ride Category

## list of Concepts

SparkSQL

SparkSession

DataFrames

File Formats

## Keynotes

Integrate with WebApp and Deploy this on AWS.

Providing earnings for passengers.

Secure admin DB Admin.

Grab the all data in real time Scenario.

Make more flexible & we will integrate with UI.

## Roles and Responsibilities 

DataBase Management

Quality & Deployment Manager

Data Analytics 

Data Collection & pre-Processing

## Getting Started

1. Grab the data from Kaggle and Pre-processed the data in CSV file format.
2. import findspark using command

            import findspark

            findspark.init()

            findspark.find()
    
3. create SparkSession and make a Data Frame.


            from pyspark.sql import SparkSession

            spark = SparkSession.builder.getOrCreate()

            df = spark.sql("select 'spark' as hello ")

            df.show()
4. Import SparkSQL functions and load the data


            from pyspark.sql.functions import *

            p = spark.read.csv(r"E:\Jupyter Noteii\Python Basics\Revature\P2\DS\Main_DS\Admin_data.csv",header=True)
            p.show(3)
            
5. For showing the view of Spark.SQL

            p.printSchema()

6. a single used cases 
            p.show(2)
            
            p.withColumn("Status", when(p.Status == "Arrived","cancelled").otherwise(p.Status)).show(2)
7. used tempview and change the name

            p.createOrReplaceTempView("pa")

8. for performance tunning ( partitioning and bucketing)

            rest=s.read.csv("C:/Users/USER/Desktop/Revature/cleanedData_final.csv",inferSchema=True,header=True)
            rest.write.partitionBy('Discount').saveAsTable("restaurant_partition1")

            rest.write.bucketBy(20, "rest_type").saveAsTable("restaurant_bucket1")

            

## Contributors

Piyush Goyal

Aysha Muktesar

Surya Dev Gedela

Bhawana Priya
