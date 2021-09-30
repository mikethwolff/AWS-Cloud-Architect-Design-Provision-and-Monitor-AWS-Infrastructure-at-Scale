
# AWS Cloud Architect Projects Udacity

*The listed projects were part of my AWS Cloud Architect Nanodegree and are displayed in derivated form due to possible copyright restrictions.*

*Form and requirements of my projects may differ from present projects. Udacity may vary projects and this repo is representing my findings at this point in time and may not be representative for future  AWS Cloud Architect projects. If you are currently enrolled into Udacity's AWS Cloud Architect Nanodegree please keep in mind that my findings can help you as a guide but copying these findings will go against Udacity's Honor Code.*


# Project 2: Design, Provision and Monito AWS Infrastructure at Scale

In this project, you will plan, design, provision, and monitor infrastructure in AWS using industry-standard and open source tools. You will practice the skills you have learned throughout the course to optimize infrastructure for cost and performance. You will also use Terraform to provision and configure AWS services in a global configuration.

**Task 1: Create AWS Architecture Schematics**

**Part 1**
You have been asked to plan and provision a cost-effective AWS infrastructure for a new social media application development project for 50,000 single-region users. The project requires the following AWS infrastructure and services. Please include your name and label all elements of the infrastructure on the diagram.

- Infrastructure in the following regions: us-east-1
- Users and Client machines
- One VPC
- Two Availability Zones
- Four Subnets (2 Public, 2 Private)
- A NAT Gateway
- A CloudFront distribution with an S3 bucket
- Web servers in the Public Subnets sized according to your usage estimates
- Application Servers in the Private Subnets sized according to your usage estimates
- DB Servers in the Private Subnets
- Web Servers Load Balanced and Autoscaled
- Application Servers Load Balanced and Autoscaled
- A Master DB in AZ1 with a read replica in AZ2
- Use LucidChart or a similar diagramming application to create your schematic. 
Export your schematic as a PDF and save as Udacity_Diagram_1.pdf.

**Solution:**

![alt text](https://github.com/mikethwolff/AWS-Cloud-Architect-Project-Design-Provision-and-Monitor-AWS-Infrastructure-at-Scale/blob/main/Design%2C%20Provision%20and%20Monito%20AWS%20Infrastructure%20at%20Scale/Udacity_Diagram_1.jpg)

**Task 2: Calculate Infrastructure Costs**
Use the AWS Pricing Calculator to estimate how much it will cost to run the services in your Part 1 diagram for one month.

- Target a monthly estimate between $8,000-$10,000.
- Be mindful of AWS regions when you are estimating costs.
- Export the estimate as a CSV file named Initial_Cost_Estimate.csv.

Return to the AWS Pricing Calculator and reconfigure your estimates for the following scenarios:

Your budget has been reduced from $8,000-$10,000 to a maximum of $6,500. What services will you modify to meet this new budget? Export the updated costs in a CSV file named Reduced_Cost_Estimate.csv and write up a brief narrative of the changes you made in the CSV file below the cost estimate.

Your budget has been increased to $20,000. What resources will you add and why?
Think about where to add redundancy and how to improve performance. Re-configure your estimate to a monthly invoice of $18K-20K. Export the updated costs to a CSV file named Increased_Cost Estimate.csv and write up a brief narrative of the changes you made in the CSV file below the cost estimate.

**Solution:**
Initial_Cost_Estimate.csv
```
Group hierarchy	Region	Service	Upfront	Monthly	First 12 months total	Currency	Configuration summary
My Estimate	US East (N. Virginia)	Amazon EC2	0	746.83	8961.96	USD	Operating system (Linux), Quantity (6), Pricing strategy (OnDemand), Storage amount (30 GB), Instance type (t3.xlarge)
My Estimate	US East (N. Virginia)	Amazon EC2	0	762.6	9151.2	USD	Operating system (Linux), Quantity (6), Pricing strategy (OnDemand), Storage amount (30 GB), Instance type (c5.xlarge)
My Estimate	US East (N. Virginia)	Application Load Balancer	0	191.63	2299.56	USD	Number of Application Load Balancers (1)
My Estimate	US East (N. Virginia)	S3 Standard	0	94.21	1130.52	USD	S3 Standard storage (4 TB per month)
My Estimate	US East (N. Virginia)	Data Transfer	0	0	0	USD	DT Inbound: All other regions (4 TB per month), DT Outbound: Amazon CloudFront (4 TB per month)
My Estimate	US East (N. Virginia)	Amazon Aurora PostgreSQL-Compatible DB	0	6,560.05	78,720.60	USD	Storage amount (4 TB), Quantity (2), Instance type (db.r6g.8xlarge), Pricing strategy (OnDemand), Additional backup storage (4 TB)
My Estimate	US East (N. Virginia)	Amazon Virtual Private Cloud (VPC)	0	434.34	5212.08	USD	Number of NAT Gateways (2)
My Estimate	US East (N. Virginia)	Amazon Route 53	0	938.5	11262	USD	Hosted Zones (2), Basic Checks Within AWS (100), Number of Elastic Network Interfaces (10)
							
			Total:	9728.16	116737.92	USD	
							
Acknowledgement							
* AWS Pricing Calculator provides only an estimate of your AWS fees and doesn't include any taxes that might apply. Your actual fees depend on a variety of factors, including your actual usage of AWS services.							
![image](https://user-images.githubusercontent.com/8941220/135459503-7b4cf8ef-1f05-461a-9997-38c70e495a9e.png)
...
