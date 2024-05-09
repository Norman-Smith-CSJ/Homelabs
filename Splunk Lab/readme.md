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

signature_id
signature
user
status
severity



![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/Splunk%20Lab/images/image1.png)


## With the server logs ingested I then begin to see the amount of high and informational severity 

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/Splunk%20Lab/images/image2.png)

