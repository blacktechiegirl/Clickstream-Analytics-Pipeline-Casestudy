# Clickstream-Analytics-Pipeline-Casestudy
Clickstream analytics is the process of collecting, analyzing and reporting aggregate data regarding pages a user visits on a website and the order in which they visit them. Clickstream data enables website owners to understand users behaviour, identify customer trends, discover new mediums and increase conversion.

You can detect user behavior in a website or application by analyzing the sequence of clicks a user makes, the amount of time the user spends, where they usually begin the navigation, and how it ends. By tracking this user behavior in real time, you can update recommendations, perform advanced A/B testing, push notifications based on session length, and much more.

# The-Clickstream-Analytics-Pipeline-Architecture
![alt text](https://github.com/blacktechiegirl/Clickstream-Analytics-Pipeline-Casestudy/blob/main/Cloud%20Architecture%20(2).png)

# The-Clickstream-Analytics-Data-Flow
### Data Source Layer
The data source layer receives data from various sources via the API gateway endpoint.
### Data Ingestion Layer
In the data ingestion layer data is captured and stored by the Data streams in real-time. The kinesis data streams capture and process data from various sources.
### Data Processing Layer
In the data processing layer, data is processed and analyzed using kinesis data analytics. Kinesis data analytics trigger lambda functions based on predefined metrics.
### Data Reaction Layer
In the data reaction layer, Lambda function is used to react to events.
### Data Persistence Layer
In the data persistence layer,  Kinesis Firehose is used to persist data into storage channels. kinesis Firehose is a streaming service that is used when you want to load your data into storage channels like S3, Redshift, Elastic Search e.t.c In this architecture data is loaded into kinesis firehose to be distributed into s3 Bucket in near real-time.
### Data Visualization Layer
In the data visualization layer, Amazon Athena is used to fetch data from s3 buckets to perform SQL queries on it. Amazon QuickSight is a visualization tool that is natively used to build dashboards over Amazon Athena data.
