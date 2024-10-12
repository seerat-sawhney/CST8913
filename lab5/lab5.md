## LAB 5 - CLOUD MIGRATION

High-Level Design (HLD) Document Outline

Title: High-Level Design for eCommerce Application Migration to AWS

Date: 11.10.2024

Prepared By: Seerat Sawhney 

## Visual Representation of Rehosting  a 3-tier eCommerce application from an on-premises environment to AWS.
The application consists of:

![Alt text](lab5.png)

# Major AWS Services Used for Migration and Their Specific Roles

1. **Amazon EC2 (Elastic Compute Cloud):**  
   Amazon EC2 provides cloud computing services, where we deploy instances that host our frontend web server running Apache or Nginx to serve static content. Additionally, the backend EC2 instances will host the REST API developed in Node.js, Java, or .NET.

2. **Application Load Balancer (ALB):**  
   The ALB distributes incoming traffic across multiple EC2 instances, ensuring no single instance becomes overloaded. This setup improves both availability and performance.

3. **Amazon RDS (Relational Database Service):**  
   RDS manages our SQL database, ensuring high availability with Multi-AZ deployment. It eliminates the need for manual database management while providing automated backups and failover capabilities.

4. **Auto Scaling:**  
   Auto Scaling dynamically adjusts the number of EC2 instances based on traffic demand. This ensures sufficient resources are available during peak loads and helps optimize costs during low-traffic periods.

# Description of How the Target Architecture Addresses Scalability, Availability, and Disaster Recovery

### Scalability  
The architecture uses an Application Load Balancer to distribute traffic across multiple EC2 instances, preventing any instance from being overburdened. Auto Scaling ensures that the system can scale up during peak demand and scale down when demand is low, optimizing both performance and cost. For database scalability, Amazon RDS employs read replicas to handle read-heavy workloads, distributing the load across multiple servers.

### Availability  
To ensure high availability, the architecture leverages Multi-AZ deployment for Amazon RDS, which automatically fails over to a secondary instance if the primary instance fails. Additionally, the EC2 instances are spread across multiple Availability Zones, ensuring that if one zone becomes unavailable, traffic is redirected to healthy instances in other zones.

### Disaster Recovery Strategy  
Amazon RDS offers automated backups and point-in-time recovery, enabling quick restoration of the database if needed. In case of EC2 instance failure, the Auto Scaling group automatically replaces the failed instance, ensuring continuous operation without manual intervention. AWS Database Migration Service (DMS) facilitates real-time data replication from on-premises SQL databases to Amazon RDS, providing an additional layer of disaster recovery.

# Minimal Downtime During Migration

To ensure there’s minimal disruption during the move of a 3-tier commerce application to AWS, all actions and steps must be mapped out. Primarily, before taking any other step, we’ll run a detailed analysis on the current infrastructure. Moreover, it will enable us to understand the relations among the frontend, backend and database since viewing their architectural plan only explains the course of actions. Planning is more granular when it comes to the technical mechanism of the migration and it is more focused on identifying risks and the ways to overcome them. Another thing that would prevent all steps is the fact that the AWS DMS comes in as a significant variable of the migration process, as it seamless allows the capacity to keep copying data on a cloud-based Amazon RDS from the On-premise db. This only means we won’t lose our data as most of the databases are hindered from being losing with use of this proven data replication technology in real time.

In addition, another operational environment called staging will be set up in AWS to also cover all preparations activity before application finally flips over. Such step enables the incorporation of all changes without any interruption of the operating system. On the designated downtime date, the cutover of the ELEVATE ICE will be implemented by changing the DNS to the new Application Load Balancer. Users will be also informed in good time if any difficulties in the transition are expected. It is very important to have a plan to move back; we will be able to restore the previous tier if problems occur advancing the changes. Finally, AWS Cloud Watch will be used post-migration for the renewal of ITIL processes for monitoring and remediation of any post-migration issues. This should ensure that the end users have a smooth handoff experience from start to finish.


# Step-by-Step Migration Process

1. **Assessment and Planning:**  
   Perform a detailed assessment of the current application, identify relevant AWS resources, and create a migration KPI chart to guide the process.

2. **Setting Up the AWS Environment:**  
   Create EC2 instances for the frontend and backend services, configure an Application Load Balancer, and set up Amazon RDS with Multi-AZ deployment.

3. **Data Migration Strategy:**  
   Use AWS DMS to migrate data from the on-premises SQL database to Amazon RDS while ensuring data consistency and minimizing service outages.

4. **Application Deployment:**  
   Deploy the application on the newly created EC2 instances and ensure that all code and configurations are correct.

5. **Testing:**  
   Conduct thorough tests to ensure that the frontend, backend, and database are functioning correctly, and that load balancing and security features are in place.

6. **Cutover and Final Data Synchronization:**  
   Configure the Application Load Balancer and update DNS records to direct traffic to the new setup. Perform final data synchronization using AWS DMS.

7. **Rollback Strategy:**  
   If any critical issues arise during the migration, revert to the on-premises setup and restore the database from a backup.

8. **Post-Migration Monitoring and Optimization:**  
   Use AWS CloudWatch to monitor performance and resource utilization, and optimize the application as needed.

# Data Consistency Strategy for the SQL Database During the Migration

To ensure data consistency during the migration, we will use AWS DMS for continuous data replication from the on-premises database to Amazon RDS. DMS ensures that updates made to the on-premises database are reflected in real-time on the RDS instance. Additionally, we will place the on-premises database in ‘Read-only’ mode during the final stages of the migration to prevent new write operations.

Before the final cutover, we will validate the data transfer by checking critical datasets. Post-migration, further validation will be done to confirm the accuracy and availability of the data in the RDS instance.

A rollback plan will be in place to revert to the pre-migration state if necessary. Regular backups and real-time data replication ensure that data consistency is maintained throughout the migration process.




 




