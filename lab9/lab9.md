# Lab 9: Cloud Cost Estimation for Enterprise Application Migration
## Submitted by- Seerat Sawhney
## Student Id- 041107886


## Scenario Overview
ShopPro International, a global eCommerce company, is planning to migrate its on-premises infrastructure to the cloud. The migration aims to be cost-effective while ensuring performance, reliability, and scalability to support business growth.


# Migration Cost Estimation Report for ShopPro International on Azure

**Prepared by:** [Your Name]  
**Date:** [Current Date]

## Executive Summary

ShopPro International is planning to migrate its on-premises infrastructure to Azure to enhance scalability, performance, and reliability across its global operations. This report outlines a comprehensive cost estimation for the migration, ongoing operational expenses, and management costs on Azure. We will also explore potential optimization strategies to ensure a cost-effective transition to the cloud.

## 1. Migration Cost Estimation

The migration cost includes one-time expenses for moving databases, applications, and data to Azure. Accurately estimating these costs is crucial for effective budgeting and resource allocation.

### Database Migration Costs

| **Component**                       | **Details**                             | **Cost (USD)**  |
|-------------------------------------|-----------------------------------------|------------------|
| **Primary SQL Database (5 TB)**    | Data Transfer (5,000 GB × $0.087)      | $435             |
|                                     | Azure Database Migration Service        | $200             |
|                                     | **Total for SQL Database**              | **$635**         |
| **NoSQL Database (10 TB)**         | Data Transfer (10,000 GB × $0.087)     | $870             |
|                                     | Azure Database Migration Service        | $300             |
|                                     | **Total for NoSQL Database**            | **$1,170**       |
| **Data Warehouse (15 TB)**         | Data Transfer (15,000 GB × $0.087)     | $1,305           |
|                                     | Azure Data Factory for replication      | $500             |
|                                     | **Total for Data Warehouse**            | **$1,805**       |
| **Total Database Migration Cost**   |                                         | **$3,610**       |
| **Application Migration**           |                                         |                  |
| **Virtual Machines (30 VMs)**      | Migration Cost (30 × $100)             | $3,000           |
| **Total Application Migration Cost**|                                         | **$3,000**       |
| **Overall Migration Cost**          |                                         | **$6,610**       |

### Summary of Migration Costs

The overall migration cost to Azure is estimated at **$6,610**. This encompasses both database and application migrations, providing a solid foundation for the budgeting process as ShopPro prepares for its cloud transition.

---

## 2. Operational Cost Estimation

After the migration, we need to consider ongoing operational costs for running the cloud infrastructure on Azure. These costs are essential to maintain services and ensure that ShopPro International can effectively meet user demands.

### Monthly Operational Costs

| **Component**                       | **Details**                          | **Monthly Cost (USD)** |
|-------------------------------------|--------------------------------------|-------------------------|
| **Web Front-End Cluster**           | 30 Standard D4s VMs (10 per region × 3 regions) | $4,500                 |
| **API Back-End Services**           | 20 Standard D4s VMs for microservices | $3,000                 |
| **Payment Processing VMs**          | 5 High-Performance VMs for PCI compliance | $1,500                 |
| **Database Layer**                  |                                      |                         |
| **Primary SQL Database**            | Azure SQL Database                    | $400                   |
| **NoSQL Database**                  | Azure Cosmos DB                      | $600                   |
| **Data Warehouse**                  | Azure Synapse Analytics              | $800                   |
| **Total Database Layer**            |                                      | **$1,800**             |
| **Data Analytics and ML Processing**|                                      |                         |
| **GPU-Enabled VMs for ML**         | 5 NV-series VMs                      | $2,000                 |
| **Scheduled Batch Jobs**            | Azure Batch Service                  | $500                   |
| **Total Data Analytics**            |                                      | **$2,500**             |
| **Backup and Disaster Recovery**    | Geo-Redundant Storage (RA-GRS)      | $1,000                 |
| **Total Monthly Operational Cost**  |                                      | **$12,300**            |

### Summary of Operational Costs

The total estimated monthly operational cost on Azure is **$12,300**, which covers all major components of the cloud infrastructure. This figure is vital for ShopPro to assess its budget for cloud services moving forward.

---

## 3. Management Cost Estimation

To ensure effective oversight and control over the Azure environment, we must factor in management costs, which include expenses for monitoring and cost management tools.

### Monthly Management Costs

| **Component**                       | **Details**                          | **Monthly Cost (USD)** |
|-------------------------------------|--------------------------------------|-------------------------|
| **Monitoring and Management Tools** | Azure Monitor                        | $600                   |
|                                     | Azure Cost Management                | $400                   |
| **Total Monthly Management Cost**   |                                      | **$1,000**             |

### Summary of Management Costs

The total estimated monthly management cost is **$1,000**. This investment in management tools is essential for preventing cost overruns and ensuring operational efficiency in the Azure environment.

---

## 4. Cost Optimization Choices

Identifying cost-saving strategies is crucial for maximizing the efficiency of ShopPro’s cloud infrastructure. Below are several optimization options that can lead to substantial savings.

### Optimization Strategies

| **Strategy**                        | **Details**                          | **Savings (USD)**     |
|-------------------------------------|--------------------------------------|------------------------|
| **Reserved Instances**              | Savings from reserved instances       | $3,000                 |
| **Auto-Scaling and Right-Sizing**   | Estimated savings during off-peak    | $1,500                 |
| **Total Cost Optimization Savings** |                                      | **$4,500**             |

### Summary of Optimization Strategies

Implementing reserved instances can lead to significant savings, especially for long-term workloads. Additionally, auto-scaling allows ShopPro to dynamically adjust resources, optimizing costs during periods of fluctuating traffic.

---

## 5. Discounts and Hybrid Benefits

ShopPro can leverage various discounts and benefits to further reduce cloud costs. This section outlines available options that could enhance savings.

### Discounts and Benefits

| **Discount Type**                  | **Details**                          | **Savings (USD)**     |
|------------------------------------|--------------------------------------|------------------------|
| **Hybrid Benefits**                | Estimated savings for existing licenses | $1,200                 |
| **Reserved Instances**             | Additional savings                   | $2,000                 |
| **Total Discounts and Savings**    |                                      | **$3,200**             |

### Summary of Discounts

Utilizing hybrid benefits and reserved instances can significantly lower operational costs, enabling ShopPro to allocate resources more effectively while still maintaining service quality.

---

## 6. Future Projections

Planning for future costs is essential for maintaining budgetary control and ensuring that ShopPro can support its growth over time. Below are projections for the next three years.

### Cost Projections

| **Projection Type**                | **Details**                          | **Cost (USD)**        |
|------------------------------------|--------------------------------------|------------------------|
| **Year 1 Total Cost**             | Initial operational cost              | $147,600               |
| **Year 2 Total Cost**             | 5% increase                          | $155,980               |
| **Year 3 Total Cost**             | 5% increase                          | $164,779               |
| **Total Three-Year Projection**    |                                      | **$468,359**           |

### Summary of Projections

The total projected cost over three years amounts to **$468,359**, accounting for a 5% annual increase. This projection will help ShopPro align its budget with anticipated business growth.

---

## Conclusion

This report provides a comprehensive estimate of the costs associated with migrating ShopPro International's infrastructure to Azure. By leveraging optimization strategies and applying discounts, the company can achieve significant savings while effectively managing operational costs. The recommendations for future projections will further assist in ensuring that the cloud budget aligns with business growth.

## Next Steps

1. Validate estimates with real data from the Azure Pricing Calculator.
2. Review this report with stakeholders to gather insights and necessary adjustments.
3. Develop a detailed migration plan and timeline based on this cost analysis.



