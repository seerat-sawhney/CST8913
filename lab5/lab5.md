## LAB 5 - CLOUD MIGRATION

High-Level Design (HLD) Document Outline

Title: High-Level Design for eCommerce Application Migration to AWS
Date: 11.10.2024
Prepared By: Seerat Sawhney 

## Visual Representation of Rehosting  a 3-tier eCommerce application from an on-premises environment to AWS.
The application consists of:

![Alt text](lab5.png)


## Major AWS services used for this migration and their specific roles 
In the migration to AWS, i utilized a lot of key services:-

1. Amazon EC2 (Elastic Compute Cloud):
Amazon Elastic Compute Cloud (Amazon EC2) is the cloud computing web service hosted on the Amazon EC2 instances. Like we will grade load in these instances with a frontend web server that will execute apache or nginx and render static content. As the backend are EC2 instances, for the API server, we are going to deploy an instance which is going to host the rest API which we have created in either Node.js, Java or.NET.

2. Application Load Balancer (ALB):
Particularly in handling traffic, the role of the ALB is of great importance. Appropriate ec2-s will be fronted by it and made to respond to the pending requests so that no single ec2 instance will be bogged down. This picture framework improves the availability of the system and the performance of the application as a whole. 

3. Amazon RDS (Relational Database Service):
Instead of creating and managing a SQL database in a VM, we shall use Amazon's RDS service. It takes care of everything that concerns database management for us. We will set it up for Multi-AZ deployment which ensures high availability and failover so that our database does not collapse.

4. Auto Scaling:
Auto Scaling is used to address the imbalance in available supply to demand. Once you have virtual machines with APIs and traffic increases, resources become insufficient, as the application is not reusing the previously released VMs.

## Mminimal downtime during the migration process

## description of how the target architecture addresses scalability, availability, and disaster recovery

Scalability
It was confirmed that the 3-tier E-Commerce application developed will reach its primary purpose and withstand different levels of loads.The strategies which we selected enable us to be able to grow and adapt to various changes in the traffic demand in the market. The initial things we did was to provide an Application Load Balancer (ALB) in the system configuration allowing for the distribution of the incoming traffic across several EC2 resources that host the front-end. This configuration has the advantage of not over-burdening any given instance and effectively dealing with this problem what so ever. When there is a sudden increase in user traffic, such as when users flood a particular server or the front end server within its limits, the mechanism proves the advanced backend design quite effective. Furthermore, the mechanism has rules to adapt to real time as the backend API load runs within an auto-scaling group. I.e., the number of EC2 instances in an auto-scaling group may increase or decrease without any manual intervention depending on the current demand escalation. This means that the number of servers can be increased during specific holidays especially promotion days and decreased when there are no promotions to optimize costs and also manage any performance killers. In terms of data management, we also make sure to include the database layer in Amazon RDS architecture and use read replicas which help us to handle read heavy loads of the system better by sending requests to multiple servers in order to share the load.

Availibilty
Every application in eCommerce is in a way directly related to online sales, customer satisfaction, among others. To mitigate this, some key components of our design are Congestion-free Services and the Storage Competent Database. Failure occurs in any of the zones then the active database service naturally switches to the disaster recovery system or secondary Endpoint in another zone. Similarly, the demand on EC2 components running balance in elastic HF is such that there is load balancing among different availability zones. When the valid instance’s host fails, traffic automatically starts targeting isolated working active instances instead of the inaccessible instance, and the product remains in use and available to the customer.

Disaster Recovery Strategy
Given that it is rather frequent that data is lost, there are many computer failures and are other causes for such. Therefore, we must minimize the risks faced once such happens and also we ensure that the enterprise can continue as planned. If such occurrence is with Amazon RDS with the pin-point recovery and automated backup feature, it will be easier to restore the database to any given time within the range of the definite period of storage. This implies that in the event of total destruction, we can quickly restore our data and continue running as expected. In order to further enhance our strategy’s readiness, we are currently applying the AWS Database Migration Services (DMS) to enable the real-time data transfer of from one SQL database that is stored on an on-site server in to the cloud. Such a method is useful for both preserving the changes of the original data as well as providing the new location as a back-up for the data so far being processed. In case there is a failure in an EC2 instance, Auto Scaling group automatically finds its replacement in a new instance thus does not require anyone to stop the operation of the application. Although, due to certain capabilities of database and encryption systems, it is less likely that such networks would be targeted by attackers without any consideration of the threat sources. Such measures therefore, ensure that the infrastructure built can effectively and in a timely manner handle any and all difficult situations that may arise.
