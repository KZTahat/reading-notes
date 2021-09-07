# Raed 19

## AWS: Events

1. Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server

   - they both are written with node.js only AWS Gateway is on AWS.
   - provides consistent RESTful application programming interfaces (APIs) for mobile and web applications only AWS Gateway gives access to AWS cloud services.
   - For an app to call publicly available AWS services, you can use Lambda to interact with the required services and expose the Lambda functions through API methods in API Gateway.
   - Deploying Express Gateway is going to be very different from Amazon API Gateway because it is not a hosted solution.
   - both useing a CLI and admin API for managing users and credentials.

2. List the AWS Database offerings and talk about the pros and cons of each

   - RDS :
     Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching and backups. It frees you to focus on your applications so you can give them the fast performance, high availability, security and compatibility they need.
   - RedShift :
     No other data warehouse makes it as easy to gain new insights from all your data. With Redshift, you can query and combine exabytes of structured and semi-structured data across your data warehouse, operational database, and data lake using standard SQL. Redshift lets you easily save the results of your queries back to your S3 data lake using open formats, like Apache Parquet, so that you can do additional analytics from other analytics services like Amazon EMR, Amazon Athena, and Amazon SageMaker.
   - DynamoDB :
     Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-active, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second.

3. What’s the difference between a FIFO and a standard queue?
   Standard queues guarantee that a message is delivered at least once and duplicates can be introduced into the queue. FIFO queues ensure a message is delivered exactly once and remains available until a consumer processes and deletes it; duplicates are not introduced into the queue.

4. How can the server be assured a message was properly received?
   a server can never know if a message was properly received by the receiver unless there was some kind of feedback coming from the reciever side telling that the message was properly received like the work way of the TCP model.

## Terminologies

- `Serverless API` : Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers.
- `Triggers` : A trigger generally causes a program routine to be executed.

<br />
<br />
[Home](https://kztahat.github.io/reading-notes/)
