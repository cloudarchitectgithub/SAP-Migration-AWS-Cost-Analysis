# Elaboration of Executive Presentation of Infrastructure costs for an SAP Migration project from On-Premises to AWS

<p align="center">
  <img src="https://i.imgur.com/EXgccrs.png" height="80%" width="80%" alt="SAP Migration Cost Analysis Banner"/>
</p>

## Project Description
This project focuses on estimating the costs associated with running a complex multi-environment setup on AWS. The environments involved include Production (Prod), Homologation (HML), and Development/Test (Dev/Test), each requiring its own configuration of services like EC2 instances, Elastic Block Storage (EBS), Load Balancers (LB), Network File System (NFS) storage, and Oracle Databases. By utilizing the AWS Pricing Calculator, the project aims to provide accurate cost estimations to inform business decisions, such as choosing the appropriate instance types and adopting AWS Compute Savings Plans. Additionally, the project includes an analysis of AWS support service costs and other optimizations to ensure cost efficiency.

## Project Objectives
1. **Cost Estimation:** Accurately estimate the costs of running multiple environments (Prod, HML, and Dev/Test) on AWS using the AWS Pricing Calculator.
2. **Service Configuration:** Determine the optimal configuration for key AWS services, including EC2, EBS, Load Balancer, NFS Storage, and Oracle Databases, to meet performance and business needs.
3. **Cost Optimization:** Identify opportunities for cost optimization, including evaluating Compute Savings Plans and specific instance types.
4. **Support Services:** Estimate the cost of AWS support services to ensure 24/7 availability and proactive management of the cloud infrastructure.
5. **Business Decision Making:** Provide a cost analysis that aids in making informed decisions about the architecture and budget allocation for the environments.

---

## Tools and Technologies
- **AWS Pricing Calculator:** Used to estimate the costs of various AWS services for each environment.
- **Amazon EC2:** Provisioned for computing capacity to run applications.
- **Amazon EBS (Elastic Block Storage):** Used for persistent block storage for the EC2 instances.
- **AWS Elastic Load Balancer (ELB):** Distributes incoming traffic across multiple instances for high availability.
- **Amazon NFS (Network File System):** Provides scalable storage for shared file systems.
- **Oracle Database on AWS:** Used for managing databases across the environments.
- **AWS Compute Savings Plan:** Evaluated for potential savings based on long-term usage of EC2 instances.
- **Visual Studio Code:** Used for coding and configuring the infrastructure.
- **AWS Support Plans:** Calculated for determining the additional costs for premium AWS support services.

---

## Project Solution

### Step 1: AWS Pricing Calculator Setup
- Open AWS Pricing Calculator to create estimates for each environment: Prod, HML, and Dev/Test.
- Enter details for EC2 instance types, EBS storage requirements, Load Balancer needs, NFS storage, and Oracle Database configurations.
- Use specific instance types that match performance and cost objectives, factoring in usage patterns for each environment.

### Step 2: Cost Estimation
- Generate estimates for the three environments, calculating the monthly and yearly costs for each AWS service.
- Include additional costs for reserved instances or Compute Savings Plans where applicable to reduce costs over time.

### Step 3: Cost Optimization Strategy
- Compare the estimated costs for on-demand pricing vs. Compute Savings Plans.
- Identify the most cost-efficient instance types that still meet performance requirements.
- Examine options to reduce EBS costs by selecting optimal storage types (e.g., gp3 over gp2 for lower cost and better performance).

### Step 4: Support Service Estimation
- Calculate the additional cost for AWS support services for each environment based on the projected usage and business needs.
- Compare different support tiers (Basic, Developer, Business, Enterprise) to ensure the best level of support for the architecture.

---

## Step-By-Step Directions

### Step 1: Navigate to AWS Pricing Calculator
- Start by visiting the AWS Pricing Calculator. This tool allows you to estimate the cost of AWS services for different environments.

<p align="center">
  <img src="https://i.imgur.com/OpBAgK9.png" height="80%" width="80%" alt="AWS Pricing Calculator Homepage"/>
</p>

- Select the option to Create a new estimate.
 
<p align="center">
  <img src="https://i.imgur.com/e8DFZy9.png" height="80%" width="80%" alt="Create New Estimate"/>
</p>

### Step 2: Configure the EC2 Instances
- In the AWS Pricing Calculator, add Amazon EC2 to the estimate.

<p align="center">
  <img src="https://i.imgur.com/aARbtjb.png" height="80%" width="80%" alt="Adding EC2 to Estimate"/>
</p>
 
- For each environment (Prod, HML, Dev/Test), specify the required instance type based on the performance needs (e.g., t3.medium for Development, m5.large for Production).

<p align="center">
  <img src="https://i.imgur.com/8hzmCYY.png" height="80%" width="80%" alt="EC2 Instance Type Selection"/>
</p>

<p align="center">
  <img src="https://i.imgur.com/WqRNgql.png" height="80%" width="80%" alt="EC2 Instance Configuration"/>
</p>

- Enter the anticipated usage hours and choose between On-Demand or Compute Savings Plan based on your long-term strategy.

<p align="center">
  <img src="https://i.imgur.com/akKjvEl.png" height="80%" width="80%" alt="EC2 Usage Configuration"/>
</p>

### Step 3: Configure Storage with Amazon EBS
- Add Amazon EBS (Elastic Block Storage) to the estimate.
- Specify the type of EBS storage required (e.g., General Purpose SSD gp3 or Provisioned IOPS SSD io1) and the storage size for each environment.

<p align="center">
  <img src="https://i.imgur.com/zcXaMqA.png" height="80%" width="80%" alt="EBS Selection"/>
</p>

<p align="center">
  <img src="https://i.imgur.com/icnemNC.png" height="80%" width="80%" alt="EBS Configuration"/>
</p>

<p align="center">
  <img src="https://i.imgur.com/35EAx4Q.png" height="80%" width="80%" alt="EBS Settings"/>
</p>

### Step 4: Set Up Load Balancers
- Add AWS Elastic Load Balancer (ELB) to the estimate for environments that need to distribute traffic across multiple EC2 instances.

<p align="center">
  <img src="https://i.imgur.com/pG3qxny.png" height="80%" width="80%" alt="Adding Load Balancer"/>
</p>

- Choose between Application Load Balancer (ALB) or Network Load Balancer (NLB) based on the application needs.

<p align="center">
  <img src="https://i.imgur.com/L2ClxWT.png" height="80%" width="80%" alt="Load Balancer Type Selection"/>
</p>

<p align="center">
  <img src="https://i.imgur.com/PehEvnE.png" height="80%" width="80%" alt="Load Balancer Configuration"/>
</p>

- Enter the estimated incoming traffic per month (in GB) and the number of load balancer hours required.

<p align="center">
  <img src="https://i.imgur.com/nUcEgBX.png" height="80%" width="80%" alt="Load Balancer Traffic Configuration"/>
</p>
 
<p align="center">
  <img src="https://i.imgur.com/efNMnhf.png" height="80%" width="80%" alt="Load Balancer Hours Configuration"/>
</p>

### Step 5: Add NFS Storage and Oracle Database
- For environments that need shared storage, include Amazon Elastic File System (EFS) or Amazon FSx for NFS in the estimate. This will be used for Network File System (NFS) storage requirements.

<p align="center">
  <img src="https://i.imgur.com/tentlQ2.png" height="80%" width="80%" alt="Adding NFS Storage"/>
</p>
 
<p align="center">
  <img src="https://i.imgur.com/EPB9Anc.png" height="80%" width="80%" alt="NFS Storage Configuration"/>
</p>
 
<p align="center">
  <img src="https://i.imgur.com/v93xDfy.png" height="80%" width="80%" alt="NFS Storage Options"/>
</p>

- Add Oracle Database on AWS to the estimate, detailing the database instance type, storage, and availability requirements.

<p align="center">
  <img src="https://i.imgur.com/t9lARel.png" height="80%" width="80%" alt="Adding Oracle Database"/>
</p>
 
<p align="center">
  <img src="https://i.imgur.com/YRCKd7V.png" height="80%" width="80%" alt="Oracle Database Selection"/>
</p>

<p align="center">
  <img src="https://i.imgur.com/OVaMILR.png" height="80%" width="80%" alt="Oracle Database Configuration"/>
</p>
 
<p align="center">
  <img src="https://i.imgur.com/N3HOtCU.png" height="80%" width="80%" alt="Oracle Database Settings"/>
</p>

### Step 6: Configure Database Instances for the Staging Environment
- For the staging environment, you need to set up two database instances with 16 vCPUs and 64 GB of memory.

<p align="center">
  <img src="https://i.imgur.com/22rhFUL.png" height="80%" width="80%" alt="Staging Database Configuration"/>
</p>

- Go to the AWS Pricing Calculator and filter the database instance types based on the vCPU count (16) and memory requirements (64 GB).
- Select the suitable instance type for your staging environment.

<p align="center">
  <img src="https://i.imgur.com/nimCJno.png" height="80%" width="80%" alt="Instance Type Selection for Staging"/>
</p>

- Storage: You will also need 3 TB of storage for this environment.

<p align="center">
  <img src="https://i.imgur.com/50vxBZq.png" height="80%" width="80%" alt="Storage Configuration for Staging"/>
</p>

- Multi-AZ: For staging, you do not need a multi-AZ setup, as this is not a production environment.

<p align="center">
  <img src="https://i.imgur.com/oKNQlvH.png" height="80%" width="80%" alt="Multi-AZ Configuration for Staging"/>
</p>

- License: Choose the "Bring Your Own License" (BYOL) option to import the licenses from your on-premises setup.

<p align="center">
  <img src="https://i.imgur.com/wsQdEYk.png" height="80%" width="80%" alt="License Options for Staging"/>
</p>

### Step 7: Set Up Backup Storage for Staging
- For backup purposes, configure an additional 500 GB of storage.
- Add the backup storage estimate to your overall calculation for the staging environment.

<p align="center">
  <img src="https://i.imgur.com/2gYkfd4.png" height="80%" width="80%" alt="Backup Storage Configuration for Staging"/>
</p>

<p align="center">
  <img src="https://i.imgur.com/sd7qBEn.png" height="80%" width="80%" alt="Backup Storage Settings"/>
</p>

<p align="center">
  <img src="https://i.imgur.com/1FTbFFH.png" height="80%" width="80%" alt="Backup Storage Estimate"/>
</p>

### Step 8: Configure Database Instances for the Development Environment
- In the development environment, you need two smaller database instances with 8 vCPUs and 32 GB of memory.

<p align="center">
  <img src="https://i.imgur.com/22rhFUL.png" height="80%" width="80%" alt="Development Database Configuration"/>
</p>

- Use the AWS Pricing Calculator to filter instances with 8 vCPUs and select a suitable option.

<p align="center">
  <img src="https://i.imgur.com/ZqfxVJo.png" height="80%" width="80%" alt="Instance Type Selection for Development"/>
</p>
 
- Storage: Allocate 1 TB of storage for development.

<p align="center">
  <img src="https://i.imgur.com/IFIAmOf.png" height="80%" width="80%" alt="Storage Configuration for Development"/>
</p>
 
- Single-AZ: Since this is a non-critical environment, choose Single-AZ deployment to lower costs.

<p align="center">
  <img src="https://i.imgur.com/TkbrcGA.png" height="80%" width="80%" alt="Single-AZ Configuration for Development"/>
</p>
 
### Step 9: Set Up Backup Storage for Development
- Allocate 1.5 TB of storage for backups in the development environment as well.

<p align="center">
  <img src="https://i.imgur.com/8bkNCxf.png" height="80%" width="80%" alt="Backup Storage for Development"/>
</p>
 
- Add the development backup estimate to the overall calculation.

<p align="center">
  <img src="https://i.imgur.com/7b9S9mj.png" height="80%" width="80%" alt="Development Backup Estimate"/>
</p>
 
### Step 10: Review the Complete Architecture
- Review the estimates for all environments (Production, Staging, Development) and ensure that they include:
  - EC2 instances for application servers.
  - Load balancers.
  - Elastic Block Storage (EBS) for all environments.
  - Elastic File System (EFS) for file storage across environments.
  - RDS Instances for database layers in each environment.

<p align="center">
  <img src="https://i.imgur.com/ng6TT1I.png" height="80%" width="80%" alt="Complete Architecture Review"/>
</p>

### Step 11: Add AWS Support Plan
- Given the critical nature of the SAP application, you will need AWS Enterprise Support to ensure a response time of 15 minutes or less for any high-severity issues.

<p align="center">
  <img src="https://i.imgur.com/0G5vsC2.png" height="80%" width="80%" alt="AWS Support Requirements"/>
</p>
 
- In the AWS Pricing Calculator, click on Add Support and select the Enterprise Support Plan.

<p align="center">
  <img src="https://i.imgur.com/lWL7Vne.png" height="80%" width="80%" alt="Adding Support Plan"/>
</p>
 
- Confirm the selection and ensure that the 24/7 support requirements are met.

<p align="center">
  <img src="https://i.imgur.com/nHOkIeA.png" height="80%" width="80%" alt="Support Plan Confirmation"/>
</p>
 
### Step 12: Final Cost Summary
- After adding all the services (compute, storage, networking, databases, and support), review the total cost for the architecture.
- The total estimated cost for 12 months should be approximately $400,000.
- Monthly cost: The AWS Pricing Calculator will display the estimated monthly cost based on your selections.

<p align="center">
  <img src="https://i.imgur.com/znI1thm.png" height="80%" width="80%" alt="Final Cost Summary"/>
</p>
 
### Step 13: Export the Estimate
- Export the estimate as a CSV file and review the details.
- Open the CSV in Excel, convert it to columns, and review the data in a structured format.
- Ensure that all fields (services, configurations, costs) are correctly populated.

<p align="center">
  <img src="https://i.imgur.com/qlACnOp.png" height="80%" width="80%" alt="Exporting Estimate"/>
</p>
 
### Step 14: Create a Presentation for Executive Review
- Import the data into a presentation template, adjusting the monthly and annual cost slides to reflect the estimates.
- Prepare to present this information in a visually appealing format that highlights key cost drivers and savings opportunities compared to on-premises infrastructure.

<p align="center">
  <img src="https://i.imgur.com/V1U4sYm.png" height="80%" width="80%" alt="Executive Presentation"/>
</p>
 
<p align="center">
  <img src="https://i.imgur.com/7rM5EzA.png" height="80%" width="80%" alt="Cost Comparison Slides"/>
</p>

By presenting the estimate in a structured and visual format, you'll make it easier for executives to understand the financial implications and approve the next steps for the project.

---

## Conclusion
This project provided a comprehensive cost analysis of the multi-environment architecture using AWS services. By leveraging the AWS Pricing Calculator, the project was able to generate accurate cost estimates and identify opportunities for cost savings. Implementing Compute Savings Plans significantly reduced the cost for long-term EC2 usage, while carefully selecting appropriate instance types and storage options further optimized the architecture. The project also accounted for AWS support services to ensure reliable 24/7 cloud operations.

## Challenges Encountered
- **Complexity in Pricing:** The AWS Pricing Calculator can be complex when dealing with multiple services across several environments. It required detailed attention to ensure all variables (e.g., usage patterns, instance types) were accurately accounted for.
- **Choosing the Right Instance Types:** Balancing performance and cost for different EC2 instances was challenging, especially for environments with varying usage intensities.
- **Estimating Storage Needs:** Predicting future storage requirements (especially for Oracle Databases and NFS storage) proved difficult without detailed usage metrics from the application teams.

## Lessons Learned
- **Detailed Cost Estimations Are Crucial:** It's important to go beyond simple cost estimates and evaluate the long-term benefits of Compute Savings Plans, reserved instances, and optimized storage configurations.
- **Importance of Monitoring:** Accurate cost projections require constant monitoring of cloud usage patterns and the ability to adjust services dynamically.
- **Understanding Support Requirements:** AWS support costs can add up quickly, and selecting the right support tier requires a deep understanding of the environment's operational needs.

## Future Improvements
- **Automate Cost Monitoring:** Implement automation for monitoring cloud cost metrics, using tools like AWS Cost Explorer, to detect and address cost overruns proactively.
- **Explore Additional Savings Plans:** In future projects, explore more savings opportunities, such as spot instances, for environments like Dev/Test where uptime is less critical.
- **Right-Sizing Instances:** Further analyze resource utilization in real-time to ensure that instances are not over-provisioned, helping to reduce costs.
