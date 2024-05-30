In this project we were presented with a scenario in which a company experienced an attack on their network and logs were captured for both their window servers and apache servers. Listed below are the objectives of this project


1. Load and Analyze Windows Logs

Students will soon be provided a document that will guide them through all of the steps required to complete the Day 1 activities.

Explain that students will first be provided with a set of logs from the Windows servers that run VSI's back-end systems. The logs are representative of normal business operations. Students will load these logs and analyze the data that they contain in order to determine baselines of normal activity.

2. Create Reports, Alerts, and Dashboards for the Windows Logs

Students will then create reports, alerts, and dashboards based on their research in the previous step. They will use these reports, alerts, and dashboards to determine if a future attack occurs.

Important - Point out that students must grab screenshots where indicated in their daily guide, as they will add those to their presentation on Day 3.

3. Load and Analyze Apache Logs

Next, students will be provided with a set of logs from the Apache web servers that host VSI's web application. The logs are representative of normal business operations. Students will load these logs and analyze the data that they contain in order to determine baselines of normal activity.

4. Create Reports, Alerts, and Dashboards for the Apache Logs

Students will again create reports, alerts, and dashboards based on their research in the previous step. They will use these reports, alerts, and dashboards to determine if a future attack occurs against their web server.

5. Install an Add-On Splunk Application for Additional Monitoring

Students will choose one of several Splunk add-on apps to assist with monitoring. Students will install the app and configure it to protect VSI's systems.

## Our goal was to analyze both logs and determine baselines and create reports to generate alerts. Here I began to briefly analyze the logs and the available fields, specifically examining the following important fields:

- signature_id
- signature
- user
- status
- severity



![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image1.png)


## With the server logs ingested I then searched for high and informational severity levels

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image2.png)



## Here I wanted to see the comparison of failure / success logs


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image3.png)


## From here I crafted an alert to trigger when more than 6 failures occurred 


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image4.png)


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image4.1.png)


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image4.2.png)



## Creating an alert that triggers when there are more than 15 successful logons in an hour.

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image5.png)


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image5.1.png)


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image5.2.png)


## Creating an alert that triggers when there are 12 accounts deleted in an hour



![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image6.png)

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image6.1.png)


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image6.2.png)

## From here I converted search into a dashboard observing signature by hour 



![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image7.png)


## User by hour

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image8.png)


## Signature visualization



![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image9.png)


## User visualization

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image10.png)


## All put together for a dashboard

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image11.png)


## We were then allowed to pick an addon to supplement our dashboard - my group decided on a website monitoring app. Here you can see we are monitoring the uptime
of Target.com

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image12.png)


## We then pivoted to analyzing the apache logs.

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image13.png)

## Here we can see the top 10 domains being visited.

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image14.png)

## Digging into HTTP status codes and seeing what the counts are on the far right column


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image15.png)

## Creating an alert that tracks activity outside of the United States

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image16.png)


## Creating an HTTP post response alert tracking anything greater than 3 

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image17.png)


![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image18.png)

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BCompleted%5D%20Splunk%20Lab/images/image19.png)

