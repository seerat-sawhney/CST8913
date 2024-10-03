## CLOUD MIGRATION 

## Cloud Resource Comparison Across AWS, Azure, and Google Cloud

| #  | Description                                                                                 | AWS (Service Name)                  | Azure (Service Name)           | Google Cloud (Service Name)   |
|----|---------------------------------------------------------------------------------------------|-------------------------------------|--------------------------------|-------------------------------|
| 1  | A compute service that provides scalable virtual machines for running applications.          | EC2                                 | Virtual Machines               | Compute Engine                |
| 2  | An object storage service used to store and retrieve data, commonly used for backups and static website content. | S3                                  | Blob Storage                   | Cloud Storage                 |
| 3  | A managed relational database service that supports multiple database engines like MySQL, PostgreSQL, and SQL. | RDS                                 | Azure SQL Database             | Cloud SQL                     |
| 4  | A serverless compute service that allows you to run code in response to events without provisioning servers. | Lambda                              | Azure Functions                | Cloud Functions               |
| 5  | A virtual private network service that allows you to create isolated networks within the cloud provider’s infrastructure. | VPC                                 | Virtual Network                | VPC                           |
| 6  | A content delivery network (CDN) service that delivers data, videos, applications, and APIs globally. | CloudFront                          | Azure CDN                      | Cloud CDN                     |
| 7  | A managed NoSQL database service designed for low-latency, high-scale applications.          | DynamoDB                            | Cosmos DB                      | Firestore / Bigtable          |
| 8  | A block storage service for use with virtual machines, offering persistent storage for data. | EBS                                 | Azure Managed Disks            | Persistent Disk               |
| 9  | A managed container orchestration service based on Kubernetes.                              | EKS                                 | Azure Kubernetes Service (AKS) | GKE                           |
| 10 | A service for managing user access and encryption keys to secure cloud resources.            | IAM                                 | Azure Active Directory (AD)    | Cloud IAM                     |
| 11 | A platform that automates application deployment and scaling without needing to manage infrastructure. | Elastic Beanstalk                   | App Service                    | App Engine                    |
| 12 | A service that provides monitoring and logging of applications and infrastructure, offering insights into resource usage and performance. | CloudWatch                          | Azure Monitor                  | Stackdriver                   |
| 13 | A domain name system (DNS) service that routes traffic globally and translates domain names to IP addresses. | Route 53                            | Azure DNS                      | Cloud DNS                     |
| 14 | A load balancing service that distributes incoming network traffic across multiple targets, improving application availability. | Elastic Load Balancing (ELB)         | Azure Load Balancer            | Cloud Load Balancing          |
| 15 | A service that automatically scales your cloud infrastructure based on demand, ensuring resources are available as needed. | Auto Scaling                        | Virtual Machine Scale Sets     | Autoscaler                    |
| 16 | A message queuing service that enables applications to send and receive messages between different components. | SQS                                 | Azure Queue Storage            | Pub/Sub                       |
| 17 | A managed real-time data streaming service that collects and processes large amounts of data from various sources. | Kinesis                             | Azure Event Hubs               | Dataflow                      |
| 18 | A fully managed, highly scalable data warehouse service optimized for analytics and large-scale queries. | Redshift                            | Azure Synapse Analytics         | BigQuery                      |
| 19 | A service that automates the execution of workflows and allows the integration of different cloud services in a sequence of steps. | Step Functions                      | Logic Apps                     | Cloud Composer                |
| 20 | A service that integrates multiple data sources and enables data migration, transformation, and movement across platforms. | AWS Glue                            | Data Factory                   | Dataflow                      |
| 21 | A data catalog and governance service that helps manage metadata across your data estate, supporting compliance and security. | AWS Glue Data Catalog               | Azure Purview                  | Data Catalog                  |
| 22 | A set of machine learning and AI services that provide pre-built models, APIs, and tools for developers to easily implement AI in their apps. | SageMaker                           | Azure Machine Learning         | AI Platform                   |
| 23 | A service that allows you to define and deploy infrastructure using code, automating the management of cloud resources. | CloudFormation                      | Azure Resource Manager (ARM)   | Cloud Deployment Manager      |
| 24 | A fully managed CI/CD service that automates the building, testing, and deployment of applications to production environments. | CodePipeline                        | Azure DevOps                   | Cloud Build                   |
| 25 | A desktop as a service (DaaS) offering that allows you to deploy virtual desktops in the cloud and access them remotely. | WorkSpaces                          | Windows Virtual Desktop        | Cloud Virtual Desktops        |
| 26 | A backup and disaster recovery service that helps to protect your data by creating backups and replicas of your cloud resources. | AWS Backup                          | Azure Backup                   | Backup and DR Services        |
| 27 | A service designed for big data analytics, allowing organizations to store, process, and analyze large datasets in real time. | EMR                                 | HDInsight                      | Dataproc                      |
| 28 | A file storage service for storing and sharing files with users, typically used in shared file systems across applications. | EFS                                 | Azure Files                    | Filestore                     |
| 29 | A service that helps you transcode, process, and stream media content such as video and audio. | Elastic Transcoder                  | Azure Media Services           | Transcoder API                |
| 30 | A real-time communication service used for sending notifications, emails, and text messages to users and devices. | SNS                                 | Azure Notification Hubs        | Firebase Cloud Messaging (FCM)|


## Summary Report
## Key Similarities and Differences

When observing AWS, Azure, and Google Cloud, we can see that they each provide a range of comparable cloud services, but there are notable discrepancies in their platforms and operational strategies. Examples include AWS's EC2, Azure's Virtual Machines, and Google Cloud's Compute Engine offering scalable computing services. However, how you manage these services, their prices, and customization options may vary greatly.

All three platforms provide a diverse selection of networking, storage, and database services. An important factor to consider when choosing a provider is that AWS's RDS has a wider range of databases compared to Google Cloud's Cloud SQL.

Azure's smooth incorporation with Microsoft tools like Active Directory and Office 365 positions it as a leading choice for businesses that have strong ties to the Microsoft network. In contrast, Google Cloud stands out in areas such as machine learning and data analysis, offering strong features like BigQuery, whereas AWS provides options such as SageMaker for AI and machine learning.

AWS is often praised for its wide range of services and tools, along with its position as a leader in cloud technology and disruptive innovations like Lambda for serverless computing.

## Exclusive Features or Abilities

AWS offers a wide range of cloud services that are perfect for businesses with intricate needs. DynamoDB and similar services provide businesses with a versatile, securely managed NoSQL database that can easily scale, making it a popular option for many companies.

Azure stands out in its seamless integration with on-premise solutions and Microsoft services. An example of this is how Azure Active Directory easily integrates with enterprise apps and Microsoft 365, offering a unified experience for companies that heavily depend on these platforms.

Google Cloud is renowned for its focus on data, offering strong tools such as BigQuery and advanced AI/ML services. It also highlights the use of open-source technologies and DevOps tools, with a focus on Kubernetes, which makes it a competitive option for developers and data scientists.

## Rules for Naming Things

When it comes to naming conventions, AWS usually chooses acronyms or descriptive names for its services, such as EC2, S3, and VPC. On the other hand, Azure typically adds "Azure" at the beginning of its service titles, frequently opting for simple names like Azure Blob Storage and Azure Virtual Network. Typically, Google Cloud includes names like "Google" or "Cloud" in its services, but often streamlines them, such as Cloud Storage and Compute Engine.

The naming conventions of AWS, Azure, and Google Cloud mirror their respective branding strategies: AWS highlights functionality, Azure focuses on the Microsoft brand, and Google Cloud prioritizes simplicity and clarity

