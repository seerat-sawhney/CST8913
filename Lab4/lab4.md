## LAB 4 - CLOUD MIGRATION

### High-Level Design (HLD) Document

### Introduction

In work with equipment in face of two physical machines - **WebServerVM**, application server and **SQLVM**, MySQL server. In this migration, however, the design is altered to come out with a version that is more reliable and can be scaled up, using serverless strategies and managed database facilities. 

In the very beginning, there are following virtual machines (VMs):

1-WebServerVM 

2-SQLVM 

When it comes to Migration (Target Architecture):

The WebServerVM has been changed to  AWS Lambda

And the SQLVM is replaced to Amazon RDS (Relational Database Service) 

## Diagram



## Overview of the Target Architecture

 The WebServerVM has been changed to  AWS Lambda, a serverless computing service which implies that API web application would from that moment operate using Lambda constructs and hence not as a virtual machine, making it a serverless architecture that expands or shrinks automatically, keeping in mind the key aspect of it i.e **scalability** . This obviates the need for provisioning and managing servers or downtime, thereby lessening operational expenses as well as possible **downtime**. The system automatically adjusts to the changing workloads making the interaction with the system very flexible. 

And the SQLVM is replaced to Amazon RDS (Relational Database Service) with Multi-AZ setup for more availability, which means that the RDS will be used in managing the MySQL database. Such a configuration duplicates the database in two different AZs, preventing data loss in case of the failure of one between the twin instances. Automated backups to **Amazon S3** help in improving data recoveries. 

## Migration Steps

### Refactoring the application to use serverless functions.
Change the Design of the Application to Work in a Serverless Environment A major part of the changes will be turning the API-oriented applications of Web Server VM to AWS Lambda to create a serverless design. In this sector, stateless services are manufactured which are long absolved from direct burden and they converse and engage effectively. This is an application that can adjust its physical or computational resources on the fly, depending on the incoming traffic, thus curbing idle resource consumption and the wastage of operations' costs greatly. In this case, cloud itself makes the underlying infrastructure more efficient, reduces latency, and improves the experience of the final users. 

### Migrating the database to Amazon RDS with multi-AZ replication.
Migrating the Database onto Amazon RDS with Multi-AZ Coverage As far as the database migration was concerned, it was decided that the migration would start by deploying Amazon RDS with a Multi-AZ configuration. In this configuration, two or more zones are used to facilitate high availability and redundancy by provisioning primary and read-only instances in different zones. During the migration, the emphasis would be on the use of AWS Database Migration Service not only the services but also to bridge the gap in the data in the San Francisco event. 

### Configuring failover and redundancy for minimal downtime
Planning for Failure in Order to Minimize Downtime Configured for Failover and Redundancy High availability will be minimized by taking advantage of automatic failover for the Amazon RDS instances during the migration. Failover means that a system can be automatically switched to a standby one without any manual intervention, thus ensuring that the database remains available during periods of hindrances. Automated Backups stored on Amazon S6 also play a more significant role in bolstering our approach to disaster recovery. 
