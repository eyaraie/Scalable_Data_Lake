# Scalable Data Lake
In contrast to most databases, a data lake is a distributed storage solution that runs on
commodity hardware and easily scales out horizontally. The data lake architecture, unlike that of databases, decouples the distributed storage
system from the distributed compute system. This allows each system to scale out as needed by the workload. Apache Spark is one of the best processing engines to use when building your own data lake, because it provides all the key features they require: 1) Support for diverse workloads 2)Support for diverse file formats 3)Support for diverse filesystems.
In this project we will build an ETL pipeline that extracts their data from the data lake hosted on S3, processes them using Spark which will be deployed on an EMR cluster using AWS, and load the data back into S3 as a set of dimensional tables in parquet format. 
Scenario: A music streaming startup, Sparkify, has grown their user base and song database even more and want to move their data warehouse to a data lake. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app. data credit is for udacity.

# ETL pipeline:
1) storage layer: Read data from S3
2) processing layer: Process data using spark (data transformsions is done to create five dimensions and fact tables)
3) serving layer: Load it back to S3 
