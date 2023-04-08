# Spotify - data engineering project

## Introduction

In this project we will build a ETL pipeline using the Spotify API on AWS. We will retrieve data from the Spotify API, transform it to a desired format and load it into an AWS data store.

## ETL Architecture

![image](https://user-images.githubusercontent.com/129515504/230722400-4e05a610-7e01-4c31-a262-3b364eabd597.png)

## About Dataset/API

This API contains informations about music artists, albums and songs - [Spotify API](https://developer.spotify.com/documentation/web-api).

## Services used

1. **S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is a highly scalable object storage storage that can store and retrieve any amount of data from anywhere. It is commonly used to store and distribute large media files, data backups and static website files.

2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. You can use lambda to run code in response to events like changes in S3, DynamoDB or other AWS services.

3. **Cloud Watch:** Amazon Cloud Watch is a monitoring service for AWS resources and the applications you run on them. You can use Cloud Watch to collect and track metrics, collect and monitor log files and for setting alarms.

4. **Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawles your data sources, identifies data formats and infers schemas to create an AWS Glue Data Catalog.

5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. You can use the Glue Data Catalog with other AWS services such as Athena.

6. **Amazon Athena:** Amazon Athena is an interactive query services that makes it easy to analyze data in Amazon S3 using standard SQL. You can use Athena to analyze data in your Glue Data Catalog or in other S3 buckets.

## Used Python packages

pip install pandas<br />
pip install numpy<br />
pip install spotipy<br />

## Project Execution Flow

Extract Data from API -> Lambda Trigger (every 1 hour) -> run extract code -> store raw data -> trigger transformation function -> transform data and load it -> query data using Athena.


