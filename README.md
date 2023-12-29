# MedicAlert
This is an event-driven application which aggregates simulated medical data into a time-series within a SQL database.

## Overview
At a high level, the application contains several components 

* kafka-producer: the .NET core-based stream simulator which generates structured randomly-generated (read: fake) medical data and sends it to a Kafka stream
* kafka-consumer: the application which consumes the resulting stream data, performs various aggregations and ETL operations and sends the data to the SQL database
* web-api: the end web server application which serves the ingested data
