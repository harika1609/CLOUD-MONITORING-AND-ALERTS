# CLOUD-MONITORING-AND-ALERTS

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : MOGALAPALLI HARIKA

*INTERN ID* : CT08NSB

*DOMAIN NAME* : CLOUD COMPUTING

*DURATION* : 4 WEEKS

*MENTOR* : NEELA SANTOSH

##DESCRIPTION
Task 2: Setting Up Cloud Monitoring and Alerts with AWS CloudWatch
As part of my internship task, I was required to configure monitoring and alerting for a cloud-based application using AWS CloudWatch, ensuring that critical performance metrics are continuously tracked and notifications are sent when certain thresholds are breached. This task aimed to ensure that any potential issues within the application are quickly identified and addressed.

Step 1: Accessing AWS CloudWatch
The first step in the process was to log into the AWS Management Console and navigate to CloudWatch under the Services tab. CloudWatch is a powerful monitoring service provided by AWS that allows users to collect, visualize, and set up alarms for various cloud resource metrics. Upon entering the CloudWatch dashboard, I gained access to a range of tools for monitoring AWS resources such as EC2, RDS, Lambda, and others.

Step 2: Selecting Metrics for Monitoring
CloudWatch allows users to track performance metrics across different services. I selected EC2 (Elastic Compute Cloud) for my task, as I was tasked with monitoring the performance of virtual machines running cloud-based applications. Under the Metrics section in CloudWatch, I selected EC2 and then proceeded to select Per-Instance Metrics to monitor the individual performance of an EC2 instance.

Some of the key metrics available for monitoring EC2 instances include CPU Utilization, Network In/Out, Disk Read/Write, and Status Checks. For my task, I chose CPU Utilization as the primary metric to monitor. Monitoring CPU utilization is crucial because high CPU usage can lead to degraded application performance or even downtime.

Step 3: Configuring CloudWatch Alarms
Once the metric was selected, I moved on to configuring an alarm. AWS CloudWatch allows users to define thresholds for metrics, which trigger alarms when breached. In my case, I set up an alarm for CPU Utilization to notify me if the usage exceeds 80% for more than 5 consecutive minutes. This threshold is critical because sustained high CPU usage can indicate an application performance issue, which needs to be addressed promptly.

To configure the alarm, I clicked on Create Alarm, selected the CPU Utilization metric, and specified the threshold (80%). I also defined the period (5 minutes) and the statistical calculation (average) to monitor the performance over time. This configuration ensured that if the CPU utilization was too high for a prolonged period, the alarm would trigger.

Step 4: Setting Up Notifications with SNS
Next, I configured Simple Notification Service (SNS) to send notifications when the alarm is triggered. SNS allows you to send alerts to various endpoints like email or SMS. I created an SNS topic, named it EC2Alerts, and added an email subscription. I provided my email address to receive notifications.

The benefit of using SNS is that you can notify stakeholders in real-time, ensuring that corrective actions can be taken immediately to resolve any performance issues.

Step 5: Creating a CloudWatch Dashboard
To enhance monitoring and visualize the metrics in a more structured way, I created a CloudWatch Dashboard. Dashboards in CloudWatch allow users to visualize multiple metrics from different AWS services in a single view. I created a new dashboard and added a Graph Widget to display the CPU Utilization metric for the selected EC2 instance.

The dashboard also included Number Widgets, which display key metrics such as total requests and average response time. This was crucial for having an at-a-glance overview of the system’s health.

Step 6: Testing the Setup
To verify that the monitoring and alerts were set up correctly, I simulated a heavy load on the EC2 instance by running a CPU-intensive task. After a few minutes, the CPU Utilization metric exceeded 80%, triggering the alarm. As expected, I received an email notification through SNS, indicating that the threshold was breached.

Step 7: Review and Documentation
Once everything was working as expected, I documented the entire process, detailing the steps taken, the metrics monitored, and the thresholds set. The CloudWatch dashboard was included in the report, showcasing the real-time metrics and visualizations I had created.

This task helped me gain practical experience in cloud monitoring, alarm configuration, and alerting within the AWS ecosystem. It also provided valuable insights into the importance of proactive monitoring to ensure that applications remain healthy and performant in the cloud.

##OUTPUT
![Image](https://github.com/user-attachments/assets/b5a88afc-8e72-4c73-a463-01a1b9ba1472)

https://cloudwatch.amazonaws.com/dashboard.html?dashboard=mydashboard&context=eyJSIjoidXMtZWFzdC0xIiwiRCI6ImN3LWRiLTg0NDAzMDEyNDYzOSIsIlUiOiJ1cy1lYXN0LTFfNWJjbkZ4WVNJIiwiQyI6InVocDN2anM1Mm9zY2RqOHV0bG5wdWNvYzMiLCJJIjoidXMtZWFzdC0xOjIzMTQ1NTc5LTVjNDUtNDFhNi1hNDgyLTAyMTdiMzA4NGRiYyIsIk8iOiJhcm46YXdzOmlhbTo6ODQ0MDMwMTI0NjM5OnJvbGUvc2VydmljZS1yb2xlL0NXREJTaGFyaW5nLVB1YmxpY1JlYWRPbmx5QWNjZXNzLVBJSk9JQlk5IiwiTSI6IlB1YmxpYyJ9
