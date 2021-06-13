# Evaluate human balance with spark

Second project from Udacity's Data Streaming using spark streaming evaluate human balance.

Project sections:

- Problem understanding
- Project structure
- Project feature required 
- Data used
- Solution architeture
- Using the model
- output example

## Problem understanding

Complete the data flow from kafka streams to web app. The application development team was not able to complete the feature as the graph is currently not receiving any data. Because the graph is currently not receiving any data, you need to generate a new payload in a Kafka topic and make it available to the STEDI application to consume.


## Project structure

 - sparkpykafkajoin.py Python script
 - sparkpyeventskafkastreamtoconsole.py Python script
 - sparkpyrediskafkastreamtoconsole.py Python script
 - log file from running the sparkpykafkajoin.py Python script in Spark: /home/workspace/spark/logs/kafkajoin.log
 - log file from running the sparkpyeventskafkastreamtoconsole.py Python script in Spark: /home/workspace/spark/logs/eventstream.log
 - log file from running the sparkpyrediskafkastreamtoconsole.py Python script in Spark: /home/workspace/spark/logs/redisstream.log
 - stedi-application sub-folder In the Python script sparkpykafkajoin.py, including the /home/workspace/stedi-application/application.conf file
 - log files from the Spark master and Spark worker: /home/workspace/spark/logs

## Project feature required 

Your product manager has requested a graph that shows fall risk (will they fall and become injured?) for recent assessments. The development team has built a graph, which is ready to receive risk information from Kafka:

![image](https://user-images.githubusercontent.com/33405407/121740102-71ab3580-cab1-11eb-8ae0-e90065d139cb.png)

## Data 

The STEDI data science team has configured some real-time data sources using Kafka Connect. One of those data sources is Redis. When a customer is first assessed in the STEDI application, their record is added to a sorted set called Customer in Redis. Redis is configured as a Kafka source and whenever any data is saved to Redis (including Customer information), a payload is published to the Kafka topic called redis-server.

## output example

![image](https://user-images.githubusercontent.com/33405407/121740102-71ab3580-cab1-11eb-8ae0-e90065d139cb.png)

![image](https://user-images.githubusercontent.com/33405407/121740102-71ab3580-cab1-11eb-8ae0-e90065d139cb.png)
