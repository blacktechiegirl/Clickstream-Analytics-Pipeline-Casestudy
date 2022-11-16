# Clickstream-Analytics-Pipeline-Casestudy
Clickstream analytics is the process of collecting, analyzing and reporting aggregate data regarding pages a user visits on a website and the order in which they visit them. Clickstream data enables website owners to understand users behaviour, identify customer trends, discover new mediums and increase conversion.

You can detect user behavior in a website or application by analyzing the sequence of clicks a user makes, the amount of time the user spends, where they usually begin the navigation, and how it ends. By tracking this user behavior in real time, you can update recommendations, perform advanced A/B testing, push notifications based on session length, and much more.

# The-Clickstream-Analytics-Pipeline-Architecture
![alt text](https://github.com/blacktechiegirl/Clickstream-Analytics-Pipeline-Casestudy/blob/main/Cloud%20Architecture.png)

# The-Clickstream-Analytics-Data-Flow
### API Gateway
Data is sent from the source via the api gatewy endpoint.
### Kinesis Data Streams
Data is captured and strored by the Data streams in real time
### Kinesis Data Analytics
Data is process and analyzed with kinesis data analytics
### Kinesis Data Firehose
Data is loaded into kinesis fiehose to be distributed into storage channels in near real time
### S3 Bucket
Data is stored in an S3 bucket for further queries with Athena
### CloudWatch Alarms
Alarms are triggered based on predefined metrics
### Lambda Function
Lambda function performs actions based on real time insight

