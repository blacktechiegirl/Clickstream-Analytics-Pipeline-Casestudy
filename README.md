# Clickstream-Analytics-Pipeline-Casestudy
Clickstream analytics is the process of collecting, analyzing and reporting aggregate data regarding pages a user visits on a website and the order in which they visit them. Clickstream data enables website owners to understand users behaviour, identify customer trends, discover new mediums and increase conversion.

You can detect user behavior in a website or application by analyzing the sequence of clicks a user makes, the amount of time the user spends, where they usually begin the navigation, and how it ends. By tracking this user behavior in real time, you can update recommendations, perform advanced A/B testing, push notifications based on session length, and much more.

# The-Clickstream-Analytics-Pipeline-Architecture
![alt text](https://github.com/blacktechiegirl/Clickstream-Analytics-Pipeline-Casestudy/blob/main/Cloud%20Architecture%20(1).png)

# The-Clickstream-Analytics-Data-Flow
### Data Source Layer
The data source layer receives data from various sources via the API gateway endpoint.
### Kinesis Data Streams
Data is captured and strored by the Data streams in real time.
### Kinesis Data Analytics
Data is processed and analyzed with kinesis data analytics. Kinesis data analytics trigger lambda functions based on preefined metrics.
### Kinesis Data Firehose
This is the persistence layer. Kinesis Firehose is a streaming service that is used when you want to load your data into storage channels like S3, Redshift, Elastic Search e.t.c In this architecture data is loaded into kinesis firehose to be distributed into s3 Bucket in near real time.
### S3 Bucket
Data is stored in an S3 bucket for further queries with Athena
### CloudWatch Alarms
Alarms are triggered based on predefined metrics
### Lambda Function
Lambda function performs actions based on real time insight

