# Executive Presentation of Infrastructure Costs for an SAP Migration Project from On-Premises to AWS

<p align="center">
  <img src="https://i.imgur.com/EXgccrs.png" height="80%" width="80%" alt="SAP Migration to AWS Banner"/>
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
1. **Open AWS Pricing Calculator:** Visit the [AWS Pricing Calculator](https://calculator.aws/) to create estimates for each environment: Prod, HML, and Dev/Test.
2. **Enter Details:** Configure EC2 instance types, EBS storage requirements, Load Balancer needs, NFS storage, and Oracle Database configurations.
3. **Select Instance Types:** Use specific instance types that match performance and cost objectives, factoring in usage patterns for each environment.
---

### Step 2: Cost Estimation
1. **Generate Estimates:** Calculate the monthly and yearly costs for each AWS service across the three environments.
2. **Include Savings Plans:** Factor in costs for reserved instances or Compute Savings Plans to reduce long-term expenses.
---

### Step 3: Cost Optimization Strategy
1. **Compare Pricing Models:** Evaluate on-demand pricing vs. Compute Savings Plans to identify cost-saving opportunities.
2. **Optimize Storage:** Select optimal storage types (e.g., gp3 over gp2) to reduce EBS costs while maintaining performance.
3. **Right-Size Instances:** Choose the most cost-efficient instance types that meet performance requirements.
---

### Step 4: Support Service Estimation
1. **Calculate Support Costs:** Estimate the additional cost for AWS support services based on projected usage and business needs.
2. **Compare Support Tiers:** Evaluate different support tiers (Basic, Developer, Business, Enterprise) to ensure the best level of support for the architecture.
---

## Step-by-Step Directions

### Step 1: Navigate to AWS Pricing Calculator
1. **Visit the AWS Pricing Calculator:** Start by visiting the [AWS Pricing Calculator](https://calculator.aws/).
2. **Create a New Estimate:** Select the option to create a new estimate.

<p align="center">
  <img src="https://i.imgur.com/OpBAgK9.png" height="80%" width="80%" alt="AWS Pricing Calculator Screenshot"/>
</p>

---

### Step 2: Configure the EC2 Instances
1. **Add Amazon EC2:** In the AWS Pricing Calculator, add Amazon EC2 to the estimate.
2. **Specify Instance Types:** For each environment (Prod, HML, Dev/Test), specify the required instance type based on performance needs (e.g., t3.medium for Development, m5.large for Production).
3. **Enter Usage Hours:** Input the anticipated usage hours and choose between On-Demand or Compute Savings Plan.

<p align="center">
  <img src="https://i.imgur.com/zcXaMqA.png" height="80%" width="80%" alt="EC2 Configuration Screenshot"/>
</p>

---

### Step 3: Configure Storage with Amazon EBS
1. **Add Amazon EBS:** Include Elastic Block Storage (EBS) in the estimate.
2. **Specify Storage Type:** Choose the type of EBS storage required (e.g., General Purpose SSD gp3 or Provisioned IOPS SSD io1) and the storage size for each environment.

<p align="center">
  <img src="https://i.imgur.com/icnemNC.png" height="80%" width="80%" alt="EBS Configuration Screenshot"/>
</p>

---

### Step 4: Set Up Load Balancers
1. **Add AWS Elastic Load Balancer (ELB):** Include ELB in the estimate for environments that need to distribute traffic across multiple EC2 instances.
2. **Choose Load Balancer Type:** Select between Application Load Balancer (ALB) or Network Load Balancer (NLB) based on application needs.
3. **Enter Traffic Estimates:** Input the estimated incoming traffic per month (in GB) and the number of load balancer hours required.

<p align="center">
  <img src="https://i.imgur.com/pG3qxny.png" height="80%" width="80%" alt="Load Balancer Configuration Screenshot"/>
</p>

---

### Step 5: Add NFS Storage and Oracle Database
1. **Include NFS Storage:** Add Amazon Elastic File System (EFS) or Amazon FSx for NFS to the estimate for shared storage requirements.
2. **Add Oracle Database:** Include Oracle Database on AWS, detailing the database instance type, storage, and availability requirements.

<p align="center">
  <img src="https://i.imgur.com/tentlQ2.png" height="80%" width="80%" alt="NFS and Oracle Configuration Screenshot"/>
</p>

---

### Step 6: Configure Database Instances for the Staging Environment
1. **Set Up Database Instances:** Configure two database instances with 16 vCPUs and 64 GB of memory for the staging environment.
2. **Allocate Storage:** Allocate 3 TB of storage for the staging environment.
3. **Choose Single-AZ:** Opt for Single-AZ deployment to reduce costs for non-critical environments.

<p align="center">
  <img src="https://i.imgur.com/22rhFUL.png" height="80%" width="80%" alt="Staging Database Configuration Screenshot"/>
</p>

---

### Step 7: Set Up Backup Storage for Staging
1. **Allocate Backup Storage:** Configure an additional 500 GB of storage for backups in the staging environment.
2. **Add to Estimate:** Include the backup storage estimate in the overall calculation.

<p align="center">
  <img src="https://i.imgur.com/2gYkfd4.png" height="80%" width="80%" alt="Backup Storage Configuration Screenshot"/>
</p>

---

### Step 8: Configure Database Instances for the Development Environment
1. **Set Up Smaller Instances:** Configure two database instances with 8 vCPUs and 32 GB of memory for the development environment.
2. **Allocate Storage:** Allocate 1 TB of storage for development.
3. **Choose Single-AZ:** Opt for Single-AZ deployment to lower costs for non-critical environments.

<p align="center">
  <img src="https://i.imgur.com/ZqfxVJo.png" height="80%" width="80%" alt="Development Database Configuration Screenshot"/>
</p>

---

### Step 9: Set Up Backup Storage for Development
1. **Allocate Backup Storage:** Configure 1.5 TB of storage for backups in the development environment.
2. **Add to Estimate:** Include the development backup estimate in the overall calculation.

<p align="center">
  <img src="https://i.imgur.com/8bkNCxf.png" height="80%" width="80%" alt="Development Backup Storage Screenshot"/>
</p>

---

### Step 10: Review the Complete Architecture
1. **Review Estimates:** Ensure that the estimates for all environments (Production, Staging, Development) include EC2 instances, Load Balancers, EBS, EFS, and RDS instances.
2. **Verify Configurations:** Double-check the configurations for accuracy and completeness.

<p align="center">
  <img src="https://i.imgur.com/ng6TT1I.png" height="80%" width="80%" alt="Complete Architecture Review Screenshot"/>
</p>

---

### Step 11: Add AWS Support Plan
1. **Select Enterprise Support:** Choose the AWS Enterprise Support Plan to ensure a response time of 15 minutes or less for high-severity issues.
2. **Confirm Selection:** Verify that the 24/7 support requirements are met.

<p align="center">
  <img src="https://i.imgur.com/lWL7Vne.png" height="80%" width="80%" alt="AWS Support Plan Screenshot"/>
</p>

---

### Step 12: Final Cost Summary
1. **Review Total Cost:** The total estimated cost for 12 months should be approximately $400,000.
2. **Monthly Cost:** The AWS Pricing Calculator will display the estimated monthly cost based on your selections.

<p align="center">
  <img src="https://i.imgur.com/znI1thm.png" height="80%" width="80%" alt="Final Cost Summary Screenshot"/>
</p>

---

### Step 13: Export the Estimate
1. **Export as CSV:** Export the estimate as a CSV file and review the details.
2. **Open in Excel:** Convert the CSV to columns and review the data in a structured format.

<p align="center">
  <img src="https://i.imgur.com/qlACnOp.png" height="80%" width="80%" alt="Export Estimate Screenshot"/>
</p>

---

### Step 14: Create a Presentation for Executive Review
1. **Import Data:** Import the data into a presentation template, adjusting the monthly and annual cost slides to reflect the estimates.
2. **Highlight Key Points:** Prepare a visually appealing presentation that highlights key cost drivers and savings opportunities compared to on-premises infrastructure.

<p align="center">
  <img src="https://i.imgur.com/V1U4sYm.png" height="80%" width="80%" alt="Executive Presentation Screenshot"/>
</p>

---

## Conclusion
This project provided a comprehensive cost analysis of the multi-environment architecture using AWS services. By leveraging the AWS Pricing Calculator, the project was able to generate accurate cost estimates and identify opportunities for cost savings. Implementing Compute Savings Plans significantly reduced the cost for long-term EC2 usage, while carefully selecting appropriate instance types and storage options further optimized the architecture. The project also accounted for AWS support services to ensure reliable 24/7 cloud operations.

---

## Challenges Encountered
1. **Complexity in Pricing:** The AWS Pricing Calculator can be complex when dealing with multiple services across several environments. It required detailed attention to ensure all variables (e.g., usage patterns, instance types) were accurately accounted for.
2. **Choosing the Right Instance Types:** Balancing performance and cost for different EC2 instances was challenging, especially for environments with varying usage intensities.
3. **Estimating Storage Needs:** Predicting future storage requirements (especially for Oracle Databases and NFS storage) proved difficult without detailed usage metrics from the application teams.

---

## Lessons Learned
1. **Detailed Cost Estimations Are Crucial:** It's important to go beyond simple cost estimates and evaluate the long-term benefits of Compute Savings Plans, reserved instances, and optimized storage configurations.
2. **Importance of Monitoring:** Accurate cost projections require constant monitoring of cloud usage patterns and the ability to adjust services dynamically.
3. **Understanding Support Requirements:** AWS support costs can add up quickly, and selecting the right support tier requires a deep understanding of the environment’s operational needs.

---

## Future Improvements
1. **Automate Cost Monitoring:** Implement automation for monitoring cloud cost metrics, using tools like AWS Cost Explorer, to detect and address cost overruns proactively.
2. **Explore Additional Savings Plans:** In future projects, explore more savings opportunities, such as spot instances, for environments like Dev/Test where uptime is less critical.
3. **Right-Sizing Instances:** Further analyze resource utilization in real-time to ensure that instances are not over-provisioned, helping to reduce costs.
