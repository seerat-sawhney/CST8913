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


## description of how the target architecture addresses scalability, availability, and disaster recovery

Scalability
It was confirmed that the 3-tier E-Commerce application developed will reach its primary purpose and withstand different levels of loads.The strategies which we selected enable us to be able to grow and adapt to various changes in the traffic demand in the market. The initial things we did was to provide an Application Load Balancer (ALB) in the system configuration allowing for the distribution of the incoming traffic across several EC2 resources that host the front-end. This configuration has the advantage of not over-burdening any given instance and effectively dealing with this problem what so ever. When there is a sudden increase in user traffic, such as when users flood a particular server or the front end server within its limits, the mechanism proves the advanced backend design quite effective. Furthermore, the mechanism has rules to adapt to real time as the backend API load runs within an auto-scaling group. I.e., the number of EC2 instances in an auto-scaling group may increase or decrease without any manual intervention depending on the current demand escalation. This means that the number of servers can be increased during specific holidays especially promotion days and decreased when there are no promotions to optimize costs and also manage any performance killers. In terms of data management, we also make sure to include the database layer in Amazon RDS architecture and use read replicas which help us to handle read heavy loads of the system better by sending requests to multiple servers in order to share the load.

Availibilty
Every application in eCommerce is in a way directly related to online sales, customer satisfaction, among others. To mitigate this, some key components of our design are Congestion-free Services and the Storage Competent Database. Failure occurs in any of the zones then the active database service naturally switches to the disaster recovery system or secondary Endpoint in another zone. Similarly, the demand on EC2 components running balance in elastic HF is such that there is load balancing among different availability zones. When the valid instance’s host fails, traffic automatically starts targeting isolated working active instances instead of the inaccessible instance, and the product remains in use and available to the customer.

Disaster Recovery Strategy
Given that it is rather frequent that data is lost, there are many computer failures and are other causes for such. Therefore, we must minimize the risks faced once such happens and also we ensure that the enterprise can continue as planned. If such occurrence is with Amazon RDS with the pin-point recovery and automated backup feature, it will be easier to restore the database to any given time within the range of the definite period of storage. This implies that in the event of total destruction, we can quickly restore our data and continue running as expected. In order to further enhance our strategy’s readiness, we are currently applying the AWS Database Migration Services (DMS) to enable the real-time data transfer of from one SQL database that is stored on an on-site server in to the cloud. Such a method is useful for both preserving the changes of the original data as well as providing the new location as a back-up for the data so far being processed. In case there is a failure in an EC2 instance, Auto Scaling group automatically finds its replacement in a new instance thus does not require anyone to stop the operation of the application. Although, due to certain capabilities of database and encryption systems, it is less likely that such networks would be targeted by attackers without any consideration of the threat sources. Such measures therefore, ensure that the infrastructure built can effectively and in a timely manner handle any and all difficult situations that may arise.

## Step by Step Migration Process

1. Assessment and Planning:
It is important to account for the current state of an application before proceeding. This signifies the structure of each part and interface and the way forward or the transition of the set up—frontend, backend, database. After understanding the configuration, there is also a need to prepare a KPI activity chart for a migration which specifies all the relevant AWS resources, timeframes, and roles of each staff people. Such a preparation, before migration starts is paramount for every process because it helps to smoothen and avert unforeseen twists and turns.

2. Setting Up the AWS Environment:
The next thing we do is set up the infrastructure to AWS according to the plan. This involves creation of EC2 instances for the Frontend and Backend services. Additionally even an Application Load Balancer will be configured (ALB) which would help to distribute load effectively to the frontend servers. We use Amazon RDS with Multi-AZ Deployment for our DB and assure that this data is fully secure and available always. Do not forget to check Firewalls configurations as proper security is necessary for offices applications or systems.

3. Data Migration Strategy:
This is the part we all have been looking forward to – moving the data. We will take advantage of the Amazon AWS Database Migration Service (DMS) to copy data from the currently functioning on premises SQL database to the new Amazon RDS. One of the fortunes about the use of this particular tool is the guarantee of data consistency thereby minimizing inconveniences due to service outages. Also, we need to end a process by a back-up of the present data base to make sure that it is possible to recovery the data if something happens not right.


4. Application Deployment:
We have completed the data security requirements; the next step is to deploy the application. Let us install the frontend webserver as well as backend API server on EC2 instances created earlier. It is important to double-check the application code at this stage.

5. Testing:
Switching on the mechanism at all, we first need to make sure that everything has preliminary checks. This implies that the frontend and backend are on the right move, and the performance can be subjected to varying conditions among others while the RDS database is used. We should also check that load balancing and advanced security features are in place so that fluctuations in load that are within the scope of day-to-day operations do not result in inconsistencies in user information.


6. Cutover and Final Data Synchronization:
 The new Application Load Balancer shall be configured and the DNS records shall also be updated so that the traffic gets directed to the newly set up version of the system. On successful working of the entire new setup, another DMS is planned to be done to bridge the gap of all the changes that occurred on-premise after that.

7. Rollback Strategy:
It is important to have a rollback strategy in the event of a plan’s failure. If top priority issue is reported during the migration event we would want to revert the resolving IP back to the on-premises. We should build up a contingency plan once more since we will have the most recent backup copy of the database in case we need to return to the assessment made earlier. It is time well spent to conduct a dry run of this step before the actual event to establish how efficiently and painlessly it can be carried out.

8. Post-Migration Monitoring and Optimization:
Once the migration is through, closely follow the performance, resource utilization and availability of the application using AWS CloudWatch. This will help us find any bottlenecks for optimization. So it is important to design the appropriate review of the architecture as well as the performance metrics of the application to ensure that it runs well and effectively in its new environment.
