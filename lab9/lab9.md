# Lab 9: Cloud Cost Estimation for Enterprise Application Migration
## Submitted by- Seerat Sawhney
## Student Id- 041107886


## Scenario Overview
ShopPro International, a global eCommerce company, is planning to migrate its on-premises infrastructure to the cloud. The migration aims to be cost-effective while ensuring performance, reliability, and scalability to support business growth.

# Cost Estimate Report


# Migration Cost Estimation Report for ShopPro International


## 1. Migration Cost Estimation

The migration cost includes one-time expenses for moving databases, applications, and data to the cloud. Accurately estimating these costs is crucial for effective budgeting and resource allocation.

### Database Migration Costs

| **Component**                       | **Details**                             | **Cost**  |
|-------------------------------------|-----------------------------------------|-----------|
| **Primary SQL Database (5 TB)**    | Data Transfer (5,000 GB × $0.15)       | $750      |
|                                     | Replication Services                    | $200      |
|                                     | **Total for SQL Database**              | **$950**  |
| **NoSQL Database (10 TB)**         | Data Transfer (10,000 GB × $0.15)      | $1,500    |
|                                     | Replication Services                    | $300      |
|                                     | **Total for NoSQL Database**            | **$1,800**|
| **Data Warehouse (15 TB)**         | Data Transfer (15,000 GB × $0.15)      | $2,250    |
|                                     | Replication Services                    | $500      |
|                                     | **Total for Data Warehouse**            | **$2,750**|
| **Total Database Migration Cost**   |                                         | **$5,500**|
| **Application Migration**           |                                         |           |
| **Virtual Machines (30 VMs)**      | Migration Cost (30 × $100)             | $3,000    |
| **Total Application Migration Cost**|                                         | **$3,000**|
| **Overall Migration Cost**          |                                         | **$8,500**|

### Summary of Migration Costs

The overall migration cost is estimated at **$8,500**. This encompasses both database and application migrations, providing a solid foundation for the budgeting process as ShopPro prepares for its cloud transition.

---

## 2. Operational Cost Estimation

Once the migration is complete, we need to consider ongoing operational costs for running the cloud infrastructure. These costs are essential to maintain services and ensure that ShopPro International can effectively meet user demands.

### Monthly Operational Costs

| **Component**                       | **Details**                          | **Monthly Cost** |
|-------------------------------------|--------------------------------------|-------------------|
| **Web Front-End Cluster**           | 30 VMs (10 per region × 3 regions)  | $6,000            |
| **API Back-End Services**           | 20 VMs hosting 50 microservices      | $3,000            |
| **Payment Processing VMs**          | 5 high-security VMs                  | $1,500            |
| **Database Layer**                  |                                      |                   |
| **Primary SQL Database**            |                                      | $400              |
| **NoSQL Database**                  |                                      | $600              |
| **Data Warehouse**                  |                                      | $800              |
| **Total Database Layer**            |                                      | **$1,800**        |
| **Data Analytics and ML Processing**|                                      |                   |
| **GPU-Enabled VMs**                 | 5 VMs for ML workloads               | $2,000            |
| **Scheduled Batch Jobs**            |                                      | $500              |
| **Total Data Analytics**            |                                      | **$2,500**        |
| **Backup and Disaster Recovery**    | Geo-Redundant Storage                | $1,000            |
| **Total Monthly Operational Cost**  |                                      | **$15,800**       |

### Summary of Operational Costs

The total estimated monthly operational cost is **$15,800**, which covers all major components of the cloud infrastructure. This figure is vital for ShopPro to assess its budget for cloud services moving forward.

---

## 3. Management Cost Estimation

To ensure effective oversight and control over the cloud environment, we must also factor in management costs, which include expenses for monitoring and cost management tools.

### Monthly Management Costs

| **Component**                       | **Details**                          | **Monthly Cost** |
|-------------------------------------|--------------------------------------|-------------------|
| **Monitoring and Management Tools** | Monitoring System                    | $600              |
|                                     | Cost Management Tools                | $400              |
| **Total Monthly Management Cost**   |                                      | **$1,000**        |

### Summary of Management Costs

The total estimated monthly management cost is **$1,000**. This investment in management tools is essential for preventing cost overruns and ensuring operational efficiency in the cloud environment.

---

## 4. Cost Optimization Choices

Identifying cost-saving strategies is crucial for maximizing the efficiency of ShopPro’s cloud infrastructure. Below are several optimization options that can lead to substantial savings.

### Optimization Strategies

| **Strategy**                        | **Details**                          | **Savings**      |
|-------------------------------------|--------------------------------------|-------------------|
| **Reserved Instances**              | Savings from reserved instances       | $3,000            |
| **Auto-Scaling and Right-Sizing**   | Estimated savings during off-peak    | $1,500            |
| **Total Cost Optimization Savings** |                                      | **$4,500**        |

### Summary of Optimization Strategies

Implementing reserved instances can lead to significant savings, especially for long-term workloads. Additionally, auto-scaling allows ShopPro to dynamically adjust resources, optimizing costs during periods of fluctuating traffic.

---

## 5. Discounts and Hybrid Benefits

ShopPro can leverage various discounts and benefits to further reduce cloud costs. This section outlines available options that could enhance savings.

### Discounts and Benefits

| **Discount Type**                  | **Details**                          | **Savings**      |
|------------------------------------|--------------------------------------|-------------------|
| **Hybrid Benefits**                | Estimated savings                    | $1,200            |
| **Reserved Instances**             | Additional savings                   | $2,000            |
| **Total Discounts and Savings**    |                                      | **$3,200**        |

### Summary of Discounts

Utilizing hybrid benefits and reserved instances can significantly lower operational costs, enabling ShopPro to allocate resources more effectively while still maintaining service quality.

---

## 6. Future Projections

Planning for future costs is essential for maintaining budgetary control and ensuring that ShopPro can support its growth over time. Below are projections for the next three years.

### Cost Projections

| **Projection Type**                | **Details**                          | **Cost**         |
|------------------------------------|--------------------------------------|-------------------|
| **Year 1 Total Cost**             | Initial operational cost              | $189,600          |
| **Year 2 Total Cost**             | 5% increase                          | $199,080          |
| **Year 3 Total Cost**             | 5% increase                          | $208,534          |
| **Total Three-Year Projection**    |                                      | **$597,214**      |

### Summary of Projections

The total projected cost over three years amounts to **$597,214**, accounting for a 5% annual increase. This projection will help ShopPro align its budget with anticipated business growth.

---

## Conclusion

This report provides a comprehensive estimate of the costs associated with migrating ShopPro International's infrastructure to the cloud. By leveraging optimization strategies and applying discounts, the company can achieve significant savings while effectively managing operational costs. The recommendations for future projections will further assist in ensuring that the cloud budget aligns with business growth.

## Next Steps

1. Validate estimates with real data from the cloud provider's pricing calculator.
2. Review this report with stakeholders to gather insights and necessary adjustments.
3. Develop a detailed migration plan and timeline based on this cost analysis.




