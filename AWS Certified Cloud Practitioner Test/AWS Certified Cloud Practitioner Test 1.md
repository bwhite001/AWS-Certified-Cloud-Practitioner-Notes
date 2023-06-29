AWS Certified Cloud Practitioner: Test 1 - Results
--------------------------------------------------



All knowledge areas

*   All knowledge areas
    
*   AWS Compute
    
*   AWS Networking & Content Delivery
    
*   AWS Cost Management
    
*   AWS Management & Governance
    
*   AWS Cloud Benefits
    
*   AWS Cloud Architecture & Design
    
*   AWS Database
    
*   AWS Security, Identity, & Compliance
    
*   AWS Storage
    
*   AWS Developer Tools
    
*   AWS Shared Responsibility Model
    
*   AWS Application Integration
    



Question 1:
A company is launching a new website which is expected to have highly variable levels of traffic. The website will run on Amazon EC2 and must be highly available.

What is the MOST cost-effective approach?

*   Create an Amazon EC2 Auto Scaling group and configure an Elastic Load Balancer.
    
    (Correct)
    
*   Determine the highest expected traffic and use an appropriate instance type.
    
*   Use the AWS CLI to launch and terminate Amazon EC2 instances to match demand.
    
*   Launch the website using an Amazon EC2 instance running on a dedicated host.
    

#### Explanation

The most cost-effective approach for ensuring the website is highly available on Amazon EC2 instances is to use an Amazon EC2 Auto Scaling group. This will ensure that the appropriate number of instances is always available to service the demand. An Elastic Load Balancer can be placed in front of the instances to distribute incoming connections.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_04-37-42-1b4fbc83fa93489d68635ff76bb4dc75.jpg)

**CORRECT:** "Create an Amazon EC2 Auto Scaling group and configure an Elastic Load Balancer" is the correct answer.

**INCORRECT:** "Use the AWS CLI to launch and terminate Amazon EC2 instances to match demand" is incorrect. This is a manual approach and would not be recommended.

**INCORRECT:** "Determine the highest expected traffic and use an appropriate instance type" is incorrect. This approach will result in the company overpaying when the demand is low.

**INCORRECT:** "Launch the website using an Amazon EC2 instance running on a dedicated host" is incorrect. This is an expensive solution as dedicated hosts are very costly and should only be used when physical isolation of resources or host visibility is required.

**References:**

[https://aws.amazon.com/ec2/autoscaling/](https://aws.amazon.com/ec2/autoscaling/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/auto-scaling-and-elastic-load-balancing/](https://digitalcloud.training/auto-scaling-and-elastic-load-balancing/)

Question 2:
A company is deploying an application on Amazon EC2 that requires low-latency access to application components in an on-premises data center. Which AWS service or resource can the company use to extend their existing VPC to the on-premises data center?

*   AWS Outposts
    
    (Correct)
    
*   AWS Direct Connect
    
*   Amazon Workspaces
    
*   Amazon Connect
    

#### Explanation

AWS Outposts is a fully managed service that offers the same AWS infrastructure, AWS services, APIs, and tools to virtually any datacenter, co-location space, or on-premises facility for a truly consistent hybrid experience. With AWS Outposts you can extend your VPC into the on-premises data center as in the following diagram:

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_04-55-42-9582226d568a8f18dc4cec68d73b71ba.jpg)

**CORRECT:** "AWS Outposts" is the correct answer.

**INCORRECT:** "Amazon Connect" is incorrect. Amazon Connect provides a seamless omnichannel experience through a single unified contact center for voice, chat, and task management.

**INCORRECT:** "AWS Direct Connect" is incorrect. Direct Connect is used for creating a low-latency private connection to an on-premises data center but it cannot be used to extend the VPC.

**INCORRECT:** "Amazon Workspaces" is incorrect. Amazon WorkSpaces is a managed, secure Desktop-as-a-Service (DaaS) solution.

**References:**

[https://aws.amazon.com/outposts/](https://aws.amazon.com/outposts/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 3:
What can a Cloud Practitioner use to categorize and track AWS costs by project?

*   Cost Allocation Tags
    
    (Correct)
    
*   Multiple accounts
    
*   AWS Trusted Advisor
    
*   Consolidated billing
    

#### Explanation

Cost allocation tags can be used to tag and categorize your resources and then run view the billing in Cost Explorer and the cost allocation report. For example you can tag your resources by department or project and then view costs attributed to the resources used by those groups.

**CORRECT:** "Cost Allocation Tags" is the correct answer.

**INCORRECT:** "AWS Trusted Advisor" is incorrect. This service advises you on best practices for provisioning resources.

**INCORRECT:** "Consolidated billing" is incorrect. Consolidated billing will give you usage per account but not per project.

**INCORRECT:** "Multiple accounts" is incorrect. You do not need to split your usage across multiple accounts, you can instead use cost allocation tags.

**References:**

[https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 4:
Which AWS services can a company use to gather information about activity in their AWS account? (Select TWO.)

*   AWS Trusted Advisor
    
*   AWS CloudTrail
    
    (Correct)
    
*   Amazon Connect
    
*   Amazon CloudWatch
    
    (Correct)
    
*   Amazon CloudFront
    

#### Explanation

Amazon CloudWatch is a performance monitoring service. AWS services send metrics about their utilization to CloudWatch which collects the metrics. Additionally, CloudWatch collects metrics about account activity such as billing information which can also be viewed.

AWS CloudTrail is an auditing service that monitors API activity in your account. Whenever you perform any operation in the account this results in an API action and this information is recorded to create an audit trail.

**CORRECT:** "AWS CloudTrail" is a correct answer.

**CORRECT:** "Amazon CloudWatch" is also a correct answer.

**INCORRECT:** "Amazon CloudFront" is incorrect. CloudFront is a content delivery network (CDN).

**INCORRECT:** "AWS Trusted Advisor" is incorrect. This service is used to assist with guidance on provisioning resources according to best practice.

**INCORRECT:** "Amazon Connect" is incorrect. This is a contact center service.

**References:**

[https://aws.amazon.com/cloudwatch/](https://aws.amazon.com/cloudwatch/)

[https://aws.amazon.com/cloudtrail/](https://aws.amazon.com/cloudtrail/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-monitoring-and-logging-services/](https://digitalcloud.training/aws-monitoring-and-logging-services/)

Question 5:
A user needs to identify underutilized Amazon EC2 instances to reduce costs.

Which AWS service or feature will meet this requirement?

*   AWS Trusted Advisor
    
    (Correct)
    
*   AWS CodeBuild
    
*   AWS Cost Explorer
    
*   AWS Health Dashboard
    

#### Explanation

AWS Trusted Advisor offers a rich set of best practice checks and recommendations across five categories: cost optimization, security, fault tolerance, performance, and service limits.

The Trusted Advisor “low utilization Amazon EC2 instances” check, checks the Amazon Elastic Compute Cloud (Amazon EC2) instances that were running at any time during the last 14 days and alerts you if the daily CPU utilization was 10% or less and network I/O was 5 MB or less on 4 or more days.

**CORRECT:** "AWS Trusted Advisor" is the correct answer.

**INCORRECT:** "AWS CodeBuild" is incorrect. CodeBuild is used for compiling and testing code ahead of deployment.

**INCORRECT:** "AWS Cost Explorer" is incorrect. Cost Explorer can be used to view itemized costs but you cannot check resource utilization.

**INCORRECT:** "AWS Health Dashboard" is incorrect. This dashboard will not warn you about underutilization of resources.

**References:**

[https://aws.amazon.com/premiumsupport/technology/trusted-advisor/best-practice-checklist/](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/best-practice-checklist/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-management-services/](https://digitalcloud.training/aws-cloud-management-services/)

Question 6:
Which of the following represents a value proposition for using the AWS Cloud?

*   AWS is responsible for securing your applications.
    
*   AWS provides full access to their data centers.
    
*   It is not necessary to enter into long term contracts.
    
    (Correct)
    
*   Customers can request specialized hardware.
    

#### Explanation

With AWS you can pay for what you use and there is no requirement to enter into long term contracts. However, there are opportunities to gain large discounts by committing to 1 or 3 years contracts for reserved instances and savings plans.

**CORRECT:** "It is not necessary to enter into long term contracts" is the correct answer.

**INCORRECT:** "AWS is responsible for securing your applications" is incorrect. AWS does not secure your applications.

**INCORRECT:** "Customers can request specialized hardware" is incorrect. This is not true; you have no say in what hardware AWS utilize.

**INCORRECT:** "AWS provides full access to their data centers" is incorrect. This is never the case; you cannot access the AWS data centers.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 7:
Which tasks can a user complete using the AWS Cost Management tools? (Select TWO.)

*   Launch either EC2 Spot instances or On-Demand instances based on the current pricing.
    
*   Move data stored in Amazon S3 Standard to an archiving storage class to reduce cost.
    
*   Delete all of your AWS resources with a single click.
    
*   Automatically terminate AWS resources if budget thresholds are exceeded.
    
    (Correct)
    
*   Create budgets and receive notifications if current or forecasted usage exceeds the budgets.
    
    (Correct)
    

#### Explanation

The AWS Cost Management tools includes services, tools, and resources to organize and track cost and usage data, enhance control through consolidated billing and access permissions, enable better planning through budgeting and forecasts, and further lower costs with resources and pricing optimizations.

**CORRECT**: "Automatically terminate AWS resources if budget thresholds are exceeded.” Is a correct answer. Within the AWS Budgets service you can use AWS Budgets Actions to automatically terminate certain resources.

**CORRECT:** "Create budgets and receive notifications if current or forecasted usage exceeds the budgets" is also a correct answer.

**INCORRECT:** "Delete all of your AWS resources with a single click” is incorrect. This can be done using third party tools, but not natively through the console.

**INCORRECT:** "Launch either EC2 Spot instances or On-Demand instances based on the current pricing" is incorrect. The cost management tools do not integrate with the tools used to launch EC2 instances and cannot choose the best pricing plan.

**INCORRECT:** "Move data stored in Amazon S3 Standard to an archiving storage class to reduce cost" is incorrect. This is performed using lifecycle management in Amazon S3, it is not a task performed by cost management tools.

**References:**

https://aws.amazon.com/aws-cost-management/

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

  

Question 8:
A company has multiple AWS accounts and is using AWS Organizations with consolidated billing. Which advantages will they benefit from? (Select TWO.)

*   They will receive one bill for the accounts in the Organization.
    
    (Correct)
    
*   They may benefit from lower unit pricing for aggregated usage.
    
    (Correct)
    
*   The default service limits in all accounts will be increased.
    
*   They will receive a fixed discount for all usage across accounts.
    
*   They will be automatically enrolled in a business support plan.
    

#### Explanation

You can use the consolidated billing feature in AWS Organizations to consolidate billing and payment for multiple AWS accounts. With consolidated billing you get:

\- One bill for multiple accounts.

\- Easy tracking or charges across accounts.

\- Combined usage across accounts and sharing of volume pricing discounts, reserved instance discounts and savings plans.

\- No extra fee.

**CORRECT:** "They will receive one bill for the accounts in the Organization" is a correct answer.

**CORRECT:** "They may benefit from lower unit pricing for aggregated usage" is also a correct answer.

**INCORRECT:** "The default service limits in all accounts will be increased" is incorrect. This is not true; service limit defaults are unaffected.

**INCORRECT:** "They will receive a fixed discount for all usage across accounts" is incorrect. There is no fixed usage discount applied for consolidated billing.

**INCORRECT:** "They will be automatically enrolled in a business support plan" is incorrect. This is not true; you must always pay for the business support plan.

**References:**

[https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 9:
Which resource should a new user on AWS use to get help with deploying popular technologies based on AWS best practices, including architecture and deployment instructions?

*   AWS CloudFormation
    
*   AWS Partner Solutions
    
    (Correct)
    
*   AWS Artifact
    
*   AWS Config
    

#### Explanation

Partner Solutions are built by Amazon Web Services (AWS) solutions architects and partners to help you deploy popular technologies on AWS, based on AWS best practices for security and high availability. These accelerators reduce hundreds of manual procedures into just a few steps, so you can build your production environment quickly and start using it immediately.

Each Quick Start includes AWS CloudFormation templates that automate the deployment and a guide that discusses the architecture and provides step-by-step deployment instructions.

**CORRECT:** "AWS Partner Solutions" is the correct answer.

**INCORRECT:** "AWS CloudFormation" is incorrect. CloudFormation is used to deploy infrastructure from templates, the Partner Solutions use CloudFormation.

**INCORRECT:** "AWS Artifact" is incorrect. Artifact provides on-demand access to AWS security and compliance reports.

**INCORRECT:** "AWS Config" is incorrect. Config is a service used for compliance relating the configuration of AWS resources.

**References:**

[https://aws.amazon.com/quickstart/](https://aws.amazon.com/quickstart/)

Question 10:
An application uses a PostgreSQL database running on a single Amazon EC2 instance. A Cloud Practitioner has been asked to increase the availability of the database so there is automatic recovery in the case of a failure.

Which tasks can the Cloud Practitioner take to meet this requirement?

*   Migrate the database to Amazon RDS and enable the Multi-AZ feature.
    
    (Correct)
    
*   Set the DeleteOnTermination value to false for the EBS root volume.
    
*   Configure an Elastic Load Balancer in front of the EC2 instance.
    
*   Configure EC2 Auto Recovery to move the instance to another Region.
    

#### Explanation

Moving the database to Amazon RDS means that the database can take advantage of the built-in Multi-AZ feature. This feature creates a standby instance in another Availability Zone and synchronously replicates to it. In the event of a failure that affects the primary database an automatic failover can occur and the database will become functional on the standby instance.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_04-33-05-264eb29a3b4cab75f611361ca72e6e71.jpg)

**CORRECT:** "Migrate the database to Amazon RDS and enable the Multi-AZ feature" is the correct answer.

**INCORRECT:** "Configure an Elastic Load Balancer in front of the EC2 instance" is incorrect. You cannot use an ELB to distribute traffic to a database and with a single instance there’s no benefit here at all.

**INCORRECT:** "Configure EC2 Auto Recovery to move the instance to another Region" is incorrect. The auto recovery feature of EC2 automatically moves the instance to another host, not to another Region.

**INCORRECT:** "Set the DeleteOnTermination value to false for the EBS root volume" is incorrect. This will simply preserve the root volume; it will not perform automatic recovery

**References:**

[https://aws.amazon.com/rds/features/multi-az/](https://aws.amazon.com/rds/features/multi-az/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 11:
A user is planning to launch three EC2 instances behind a single Elastic Load Balancer. The deployment should be highly available. How should the user achieve this?

*   Launch the instances across multiple Availability Zones in a single AWS Region.
    
    (Correct)
    
*   Launch the instances as EC2 Spot Instances in the same AWS Region and the same Availability Zone.
    
*   Launch the instances in multiple AWS Regions, and use Elastic IP addresses.
    
*   Launch the instances as EC2 Reserved Instances in the same AWS Region, but in different Availability Zones.
    

#### Explanation

To make the deployment highly available the user should launch the instances across multiple Availability Zones in a single AWS Region. Elastic Load Balancers can only serve targets in a single Region so it is not possible to deploy across Regions.

**CORRECT:** "Launch the instances across multiple Availability Zones in a single AWS Region" is the correct answer.

**INCORRECT:** "Launch the instances as EC2 Spot Instances in the same AWS Region and the same Availability Zone" is incorrect. The pricing model is not relevant to high availability and deploying in a single AZ does not result in a highly available deployment.

**INCORRECT:** "Launch the instances in multiple AWS Regions, and use Elastic IP addresses" is incorrect. You cannot use an ELB with instances in multiple Regions and using an EIP does not help.

**INCORRECT:** "Launch the instances as EC2 Reserved Instances in the same AWS Region, but in different Availability Zones" is incorrect. Using reserved instances may not be appropriate as we do not know whether this is going to be a long-term workload or not.

**References:**

[https://aws.amazon.com/about-aws/global-infrastructure/regions\_az/](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-global-infrastructure/](https://digitalcloud.training/aws-global-infrastructure/)

Question 12:
What is the best practice for managing AWS IAM access keys?

*   Never use access keys, always use IAM roles.
    
*   AWS rotate access keys on a schedule.
    
*   There is no need to manage access keys.
    
*   Customers should rotate access keys regularly.
    
    (Correct)
    

#### Explanation

It is a security best practice to rotate access keys regularly. This practice ensures that if access keys are compromised the security exposure is mitigated.

**CORRECT:** "Customers should rotate access keys regularly" is the correct answer.

**INCORRECT:** "There is no need to manage access keys" is incorrect. This is not true; you must rotate access keys.

**INCORRECT:** "AWS rotate access keys on a schedule" is incorrect. AWS do not rotate your access keys.

**INCORRECT:** "Never use access keys, always use IAM roles" is incorrect. It is often better and more secure to use IAM roles for some uses but it is certainly not the case that you should never use access keys.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 13:
Customers using AWS services must patch operating systems on which of the following services?

*   Amazon DynamoDB
    
*   AWS Fargate
    
*   AWS Lambda
    
*   Amazon EC2
    
    (Correct)
    

#### Explanation

Amazon EC2 is an infrastructure as a service (IaaS) solution. This means the underlying hardware and software layer for running a virtual server are managed for you. As a customer you must then manage the operating system and any software you install. This includes installing patches on the operating system as part of regular maintenance activities.

**CORRECT:** "Amazon EC2" is the correct answer.

**INCORRECT:** "AWS Lambda" is incorrect. This is a serverless service and you do not need to manage patches.

**INCORRECT:** "AWS Fargate" is incorrect. This is a serverless service and you do not need to manage patches.

**INCORRECT:** "Amazon DynamoDB" is incorrect. This is a serverless service and you do not need to manage patches.

**References:**

[https://aws.amazon.com/ec2/](https://aws.amazon.com/ec2/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 14:
How much data can a company store in the Amazon S3 service?

*   Virtually unlimited
    
    (Correct)
    
*   100 PB
    
*   100 TB
    
*   1 PB
    

#### Explanation

The Amazon Simple Storage Service (S3) offers virtually unlimited storage. The total volume of data and number of objects you can store are unlimited. Individual Amazon S3 objects can range in size from a minimum of 0 bytes to a maximum of 5 terabytes. The largest object that can be uploaded in a single PUT is 5 gigabytes.

**CORRECT:** "Virtually unlimited" is the correct answer.

**INCORRECT:** "1 PB" is incorrect. There is no such limit.

**INCORRECT:** "100 TB" is incorrect. There is no such limit.

**INCORRECT:** "100 PB" is incorrect. There is no such limit.

**References:**

[https://aws.amazon.com/s3/faqs/](https://aws.amazon.com/s3/faqs/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 15:
Which AWS service provides a managed software version control system?

*   AWS CodeCommit
    
    (Correct)
    
*   AWS CodePipeline
    
*   AWS DataSync
    
*   Amazon CodeDeploy
    

#### Explanation

AWS CodeCommit is a fully-managed source control service that hosts secure Git-based repositories. It makes it easy for teams to collaborate on code in a secure and highly scalable ecosystem.

CodeCommit eliminates the need to operate your own source control system or worry about scaling its infrastructure. You can use CodeCommit to securely store anything from source code to binaries, and it works seamlessly with your existing Git tools.

**CORRECT:** "AWS CodeCommit" is the correct answer.

**INCORRECT:** "Amazon CodeDeploy" is incorrect. CodeDeploy is a deployment service that deploys your application onto infrastructure.

**INCORRECT:** "AWS CodePipeline" is incorrect. CodePipeline is a continuous delivery service that automates release pipelines for code. CodeCommit can be used in a pipeline.

**INCORRECT:** "AWS DataSync" is incorrect. DataSync is used for replication and migrating data between storage systems and AWS.

**References:**

[https://aws.amazon.com/codecommit/](https://aws.amazon.com/codecommit/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 16:
What is one method of protecting against distributed denial of service (DDoS) attacks in the AWS Cloud?

*   Use Amazon CloudWatch monitoring.
    
*   Configure a firewall in front of resources.
    
    (Correct)
    
*   Monitor the AWS Health Dashboard.
    
*   Enable AWS CloudTrail logging.
    

#### Explanation

Some forms of DDoS mitigation are included automatically with AWS services. You can further improve your DDoS resilience by using an AWS architecture with specific services and by implementing additional best practices. Using a firewall with AWS resources is recommended to reduce the attack surface of your services which can mitigate some DDoS attacks.

**CORRECT:** "Configure a firewall in front of resources" is the correct answer.

**INCORRECT:** "Use Amazon CloudWatch monitoring" is incorrect. Performance monitoring will not protect against DDoS.

**INCORRECT:** "Enable AWS CloudTrail logging" is incorrect. Logging API calls will not protect against DDoS.

**INCORRECT:** "Monitor the AWS Health Dashboard" is incorrect. The AWS Health dashboard is not useful for monitoring and will not protect against DDoS.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-best-practices-ddos-resiliency/mitigation-techniques.html](https://docs.aws.amazon.com/whitepapers/latest/aws-best-practices-ddos-resiliency/mitigation-techniques.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 17:
What advantages does a database administrator obtain by using the Amazon Relational Database Service (RDS)?

*   RDS simplifies relational database administration tasks.
    
    (Correct)
    
*   RDS databases automatically scale based on load.
    
*   RDS enables users to dynamically adjust CPU and RAM resources.
    
*   RDS provides 99.99999999999% reliability and durability.
    

#### Explanation

Amazon RDS is a managed relational database service on which you can run several types of database software. The service is managed so this reduces the database administration tasks an administrator would normally undertake. The managed service includes hardware provisioning, database setup, patching and backups.

**CORRECT:** "RDS simplifies relational database administration tasks" is the correct answer.

**INCORRECT:** "RDS databases automatically scale based on load" is incorrect. This is not true, storage auto scaling is possible but for compute it scales by changing instance type (manual).

**INCORRECT:** "RDS provides 99.99999999999% reliability and durability" is incorrect. This is not true of Amazon RDS.

**INCORRECT:** "RDS enables users to dynamically adjust CPU and RAM resources" is incorrect. You cannot adjust CPU and RAM dynamically, you must change the instance type and reboot the database instance.

**References:**

[https://aws.amazon.com/rds/](https://aws.amazon.com/rds/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 18:
Which AWS service can a company use to discover and protect sensitive data that is stored in Amazon S3 buckets.

*   Amazon GuardDuty
    
*   Amazon Detective
    
*   Amazon Macie
    
    (Correct)
    
*   AWS Policy Generator
    

#### Explanation

Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data in AWS. Amazon Macie automates the discovery of sensitive data at scale and lowers the cost of protecting your data.

Macie automatically provides an inventory of Amazon S3 buckets including a list of unencrypted buckets, publicly accessible buckets, and buckets shared with AWS accounts outside those you have defined in AWS Organizations.

Then, Macie applies machine learning and pattern matching techniques to the buckets you select to identify and alert you to sensitive data, such as personally identifiable information (PII).

**CORRECT:** "Amazon Macie" is the correct answer.

**INCORRECT:** "Amazon GuardDuty" is incorrect. Amazon GuardDuty is a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts, workloads, and data stored in Amazon S3.

**INCORRECT:** "AWS Policy Generator" is incorrect. The AWS Policy Generator is a tool that enables you to create policies that control access to Amazon Web Services (AWS) products and resources.

**INCORRECT:** "Amazon Detective" is incorrect. Amazon Detective automatically processes terabytes of event data records about IP traffic, AWS management operations, and malicious or unauthorized activity.

**References:**

[https://aws.amazon.com/macie/](https://aws.amazon.com/macie/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 19:
A Cloud Practitioner requires point-in-time recovery (PITR) for an Amazon DynamoDB table. Who is responsible for configuring and performing backups?

*   AWS is responsible for both tasks.
    
*   AWS is responsible for configuring and the user is responsible for performing backups.
    
*   The customer is responsible for configuring and AWS is responsible for performing backups.
    
    (Correct)
    
*   The customer is responsible for both tasks.
    

#### Explanation

Point-in-time recovery (PITR) provides continuous backups of your DynamoDB table data. When enabled, DynamoDB maintains incremental backups of your table for the last 35 days until you explicitly turn it off. It is a customer responsibility to enable PITR on and AWS is responsible for actually performing the backups.

**CORRECT:** "The customer is responsible for configuring and AWS is responsible for performing backups" is the correct answer.

**INCORRECT:** "AWS is responsible for configuring and the user is responsible for performing backups" is incorrect. This is backwards, users are responsible for configuring and AWS is responsible for performing backups.

**INCORRECT:** "AWS is responsible for both tasks" is incorrect. This is not true as users must configure PITR.

**INCORRECT:** "The customer is responsible for both tasks" is incorrect. This is not true, AWS perform the backups.

**References:**

[https://aws.amazon.com/blogs/aws/new-amazon-dynamodb-continuous-backups-and-point-in-time-recovery-pitr/](https://aws.amazon.com/blogs/aws/new-amazon-dynamodb-continuous-backups-and-point-in-time-recovery-pitr/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 20:
Which of the following AWS services are compute services? (Select TWO.)

*   Amazon Inspector
    
*   AWS Elastic Beanstalk
    
    (Correct)
    
*   AWS Batch
    
    (Correct)
    
*   AWS CloudTrail
    
*   Amazon EFS
    

#### Explanation

AWS Batch enables developers, scientists, and engineers to easily and efficiently run hundreds of thousands of batch computing jobs on AWS.

AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

**CORRECT:** "AWS Batch" is a correct answer.

**CORRECT:** "AWS Elastic Beanstalk" is also a correct answer.

**INCORRECT:** "AWS CloudTrail" is incorrect. CloudTrail is used for auditing.

**INCORRECT:** "Amazon EFS" is incorrect. The Elastic File System (EFS) is used for storing data and is mounted by EC2 instances.

**INCORRECT:** "Amazon Inspector" is incorrect. Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS.

**References:**

[https://aws.amazon.com/batch/](https://aws.amazon.com/batch/)

[https://aws.amazon.com/elasticbeanstalk/](https://aws.amazon.com/elasticbeanstalk/)

Question 21:
Which of the following AWS features or services can be used to provide root storage volumes for Amazon EC2 instances?

*   Amazon Machine Image
    
*   Amazon Simple Storage Service (S3)
    
*   Amazon Elastic File System (EFS)
    
*   Amazon Elastic Block Store (EBS)
    
    (Correct)
    

#### Explanation

The Amazon Elastic Block Store (EBS) provides block-based storage volumes for Amazon EC2 instances. Root volumes are where the operating system is installed and can be either EBS volumes or instance store volumes.

**CORRECT:** "Amazon Elastic Block Store (EBS)" is the correct answer.

**INCORRECT:** "Amazon Machine Image" is incorrect. An AMI provides the information required to launch an instance including the mapping of EBS volumes.

**INCORRECT:** "Amazon Elastic File System (EFS)" is incorrect. EFS volumes cannot be used for the root storage volume but can be mounted to store data.

**INCORRECT:** "Amazon Simple Storage Service (S3)" is incorrect. Amazon S3 buckets cannot be attached to EC2 instances in any way, it is a service that is accessed via a REST API.

**References:**

[https://docs.aws.amazon.com/opsworks/latest/userguide/best-practices-storage.html](https://docs.aws.amazon.com/opsworks/latest/userguide/best-practices-storage.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 22:
A company plans to use reserved instances to get discounted pricing for Amazon EC2 instances. The company may need to change the EC2 instance type during the one year period.

Which instance purchasing option is the MOST cost-effective for this use case?

*   Standard Reserved Instances
    
*   Zonal Reserved Instances
    
*   Regional Reserved Instances
    
*   Convertible Reserved Instances
    
    (Correct)
    

#### Explanation

A convertible reserved instance enables you to _exchange_ one or more Convertible Reserved Instances for another Convertible Reserved Instance with a different configuration, including instance family, operating system, and tenancy.

**CORRECT:** "Convertible Reserved Instances" is the correct answer.

**INCORRECT:** "Standard Reserved Instances" is incorrect. With standard RIs you cannot change the instance type but you can change the instance size.

**INCORRECT:** "Regional Reserved Instances" is incorrect. Regional RIs apply to instance usage within any AZ in a specified Region.

**INCORRECT:** "Zonal Reserved Instances" is incorrect. Zonal RIs apply to instance usage within a specific AZ within an AWS Region.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/cost-optimization-reservation-models/standard-vs.-convertible-offering-classes.html](https://docs.aws.amazon.com/whitepapers/latest/cost-optimization-reservation-models/standard-vs.-convertible-offering-classes.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 23:
A company is designing a new a service that must align with the operational excellence pillar of the AWS Well-Architected Framework.

Which design principles should the company follow? (Select TWO.)

*   Perform manual operations.
    
*   Anticipate failure.
    
    (Correct)
    
*   Create static operational procedures.
    
*   Perform operations as code.
    
    (Correct)
    
*   Make large-scale changes.
    

#### Explanation

AWS Well-Architected helps cloud architects build secure, high-performing, resilient, and efficient infrastructure for their applications and workloads. There are 5 pillars and under the operational excellence pillar the following best practices are recommended:

• Perform operations as code

• Make frequent, small, reversible changes

• Refine operations procedures frequently

• Anticipate failure

• Learn from all operational failures

**CORRECT:** "Anticipate failure" is a correct answer.

**CORRECT:** "Perform operations as code" is also a correct answer.

**INCORRECT:** "Make large-scale changes" is incorrect. This is not an operational best practice.

**INCORRECT:** "Perform manual operations" is incorrect. This is not an operational best practice.

**INCORRECT:** "Create static operational procedures" is incorrect. This is not an operational best practice.

**References:**

[https://aws.amazon.com/architecture/well-architected/](https://aws.amazon.com/architecture/well-architected/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 24:
When running applications in the AWS Cloud, which common tasks can AWS manage on behalf of their customers? (Select TWO.)

*   Creating a database schema
    
*   Patching database software
    
    (Correct)
    
*   Taking a backup of a database
    
    (Correct)
    
*   Application source code auditing
    
*   Application security testing
    

#### Explanation

With AWS managed services you can reduce your time spent performing common IT tasks. With services such as Amazon RDS, AWS will patch the database host operating system and database software and perform patch management activities.

**CORRECT:** "Patching database software" is a correct answer.

**CORRECT:** "Taking a backup of a database" is also a correct answer.

**INCORRECT:** "Application source code auditing" is incorrect. AWS does not audit your source code. You can use Amazon CodeGuru for recommendations for improvement though.

**INCORRECT:** "Creating a database schema" is incorrect. AWS does not create your schema; this is something that’s in the customer’s control.

**INCORRECT:** "Application security testing" is incorrect. AWS does not perform any security testing of your applications.

**References:**

[https://aws.amazon.com/rds/](https://aws.amazon.com/rds/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 25:
Which of the following can an AWS customer use to launch a new ElastiCache cluster? (Select TWO.)

*   AWS CloudFormation
    
    (Correct)
    
*   AWS Data Pipeline
    
*   AWS Management Console
    
    (Correct)
    
*   AWS Systems Manager
    
*   AWS Concierge
    

#### Explanation

There are several ways to launch resources in AWS. You can use the AWS Management Console or Command Line Interface (CLI) or you can automate the process by using tools such as AWS CloudFormation.

With AWS CloudFormation you can deploy infrastructure such as Amazon ElastiCache clusters by defining your desired configuration state in code using a template file written in JSON or YAML. CloudFormation will then deploy the resources by creating a Stack according to the template file.

**CORRECT:** "AWS CloudFormation" is a correct answer.

**CORRECT:** "AWS Management Console" is also a correct answer.

**INCORRECT:** "AWS Concierge" is incorrect. The Concierge Support Team is available for customer who have an Enterprise level support plan. This team does not launch resources for you.

**INCORRECT:** "AWS Systems Manager" is incorrect. Systems Manager will not launch an ElastiCache cluster for you.

**INCORRECT:** "AWS Data Pipeline" is incorrect. AWS Data Pipeline is a web service that helps you reliably process and move data between different AWS compute and storage services.

**References:**

[https://aws.amazon.com/cloudformation/](https://aws.amazon.com/cloudformation/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 26:
Which AWS service or feature can assist with protecting a website that is hosted outside of AWS?

*   Amazon VPC route tables
    
*   Amazon EC2 security groups
    
*   AWS Web Application Firewall (WAF)
    
    (Correct)
    
*   Amazon VPC network ACLs
    

#### Explanation

AWS WAF can be used to protect on-premises resources if they are deployed behind an Application Load Balancer (ALB). In this scenario the on-premises website servers are added to a target group by IP address. The ALB has a WAF WebACL attached to it and distributes connections to the on-premises website.

**CORRECT:** "AWS Web Application Firewall (WAF)" is the correct answer.

**INCORRECT:** "Amazon VPC route tables" is incorrect. A route table cannot be used for protecting resources running outside AWS.

**INCORRECT:** "Amazon EC2 security groups" is incorrect. Security groups can only be attached to EC2 instances.

**INCORRECT:** "Amazon VPC network ACLs" is incorrect. Network ACLs only filter traffic entering and leaving a VPC subnet.

**References:**

[https://aws.amazon.com/waf/features/](https://aws.amazon.com/waf/features/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 27:
A company uses Amazon EC2 instances to run applications that are dedicated to different departments. The company needs to break out the costs of these applications and allocate them to the relevant department. The EC2 instances run in a single VPC.

How can the company achieve these requirements?

*   Add additional Amazon VPCs and launch each application in a separate VPC.
    
*   Create tags by department on the instances and then run a cost allocation report.
    
    (Correct)
    
*   Enable billing alerts through Amazon CloudWatch and Amazon SNS.
    
*   Enable billing access for IAM users and view the costs in Cost Explorer.
    

#### Explanation

The company should create cost allocation tags that specify the department and assign them to resources. These tags must be activated so they are visible in the cost allocation report. Once this is done and a monthly cost allocation report has been configured it will be easy to monitor the costs for each department.

**CORRECT:** "Create tags by department on the instances and then run a cost allocation report" is the correct answer.

**INCORRECT:** "Enable billing access for IAM users and view the costs in Cost Explorer" is incorrect. Cost explorer will not show a breakdown of the costs by department.

**INCORRECT:** "Enable billing alerts through Amazon CloudWatch and Amazon SNS" is incorrect. A billing alert simply lets you know you have reached a cost threshold.

**INCORRECT:** "Add additional Amazon VPCs and launch each application in a separate VPC" is incorrect. This will not help as billing is not broken out by VPC so they will not be able to determine the costs per department using this method.

**References:**

[https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/configurecostallocreport.html](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/configurecostallocreport.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 28:
A company is deploying an application in the AWS Cloud. How can they secure the application? (Select TWO.)

*   Limit access privileges according to the principal of least privilege.
    
    (Correct)
    
*   Configure public access for the AWS services used by the application.
    
*   Enable encryption for the application data at rest.
    
    (Correct)
    
*   Enable monitoring by turning off encryption for data in transit.
    
*   Provide full admin access to developer and operations staff.
    

#### Explanation

In this scenario the company must apply best practice principals for securing their application. Enabling encryption for data at rest is definitely a good practice and data in transit should also be encrypted where possible as well. It is also a good practice to limit access privileges according to the principal of least privilege. This means limiting privileges to those required to perform a specific role.

**CORRECT:** "Enable encryption for the application data at rest" is a correct answer.

**CORRECT:** "Limit access privileges according to the principal of least privilege" is also a correct answer.

**INCORRECT:** "Configure public access for the AWS services used by the application" is incorrect. In some cases public access may be required and in that case only the front end service(s) should be configured for public access. Otherwise it would be best to not enable public access.

**INCORRECT:** "Enable monitoring by turning off encryption for data in transit" is incorrect. There is no need to turn off encryption in transit to enable monitoring and this would reduce security.

**INCORRECT:** "Provide full admin access to developer and operations staff" is incorrect. This is not a security best practice; it is better to assign permissions according to the principal of least privilege

**References:**

[https://aws.amazon.com/security/](https://aws.amazon.com/security/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 29:
How does the AWS cloud increase the speed and agility of execution for customers? (Select TWO.)

*   Fast provisioning of resources
    
    (Correct)
    
*   Scalable compute capacity
    
    (Correct)
    
*   Lower cost of deployment
    
*   Secured data centers
    
*   Private connections to data centers
    

#### Explanation

The ability to quickly provision resources on AWS is a good example of speed and agility. On AWS the resources are readily available and can be deployed extremely quickly. Scalable compute capacity is another example as it gives you the agility to easily reconfigure your resources with more or less capacity as is required.

**CORRECT:** "Fast provisioning of resources" is a correct answer.

**CORRECT:** "Scalable compute capacity" is also a correct answer.

**INCORRECT:** "Private connections to data centers" is incorrect. A private connection to a data center is not an example of speed and agility.

**INCORRECT:** "Secured data centers" is incorrect. Secured data centers are not an example of speed and agility.

**INCORRECT:** "Lower cost of deployment" is incorrect. This is not an example of speed and agility.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 30:
A company runs a batch job on an Amazon EC2 instance and it takes 6 hours to complete. The workload is expected to double in volume each month with a proportional increase in processing time.

What is the most efficient cloud architecture to address the growing workload?

*   Run the batch workload in parallel across multiple Amazon EC2 instances.
    
    (Correct)
    
*   Run the application on a bare metal Amazon EC2 instance.
    
*   Change the Amazon EC2 volume type to a Provisioned IOPS SSD volume.
    
*   Run the batch job on a larger Amazon EC2 instance type with more CPU.
    

#### Explanation

The most efficient option is to use multiple EC2 instances and distribute the workload across them. This is an example of horizontal scaling and will allow the workload to keep growing in size without any issue and without increasing the overall processing timeframe.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_04-42-38-1f497a6b021e0dd85228f78b7b47f63e.jpg)

**CORRECT:** "Run the batch workload in parallel across multiple Amazon EC2 instances" is the correct answer.

**INCORRECT:** "Run the batch job on a larger Amazon EC2 instance type with more CPU" is incorrect. This may help initially but over time this will not scale well and the workload will take many days to complete.

**INCORRECT:** "Change the Amazon EC2 volume type to a Provisioned IOPS SSD volume" is incorrect. This will improve the underlying performance of the EBS volume but does not assist with processing (more CPU is needed, i.e. by spreading across instances).

**INCORRECT:** "Run the application on a bare metal Amazon EC2 instance" is incorrect. Bare metal instances are used for workloads that require access to the hardware feature set (such as Intel VT-x), for applications that need to run in non-virtualized environments for licensing or support requirements, or for customers who wish to use their own hypervisor.

**References:**

[https://wa.aws.amazon.com/wellarchitected/2020-07-02T19-33-23/wat.concept.horizontal-scaling.en.html](https://wa.aws.amazon.com/wellarchitected/2020-07-02T19-33-23/wat.concept.horizontal-scaling.en.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 31:
Which of the following deployments involves the reliability pillar of the AWS Well-Architected Framework?

*   Amazon EBS provisioned IOPS volume
    
*   Attach a WebACL to a CloudFront distribution
    
*   Use CloudFormation to deploy infrastructure
    
*   Amazon RDS Multi-AZ deployment
    
    (Correct)
    

#### Explanation

An Amazon Relational Database Service (RDS) deployment across multiple availability zones is a good example of using the reliability pillar of the AWS Well-Architected Framework. The specific design principle being followed here is “Automatically recover from failure”.

**CORRECT:** "Amazon RDS Multi-AZ deployment" is the correct answer.

**INCORRECT:** "Amazon EBS provisioned IOPS volume" is incorrect. This would be an example of performance efficiency.

**INCORRECT:** "Attach a WebACL to a CloudFront distribution" is incorrect. This would be an example of using the security pillar.

**INCORRECT:** "Use CloudFormation to deploy infrastructure" is incorrect. This would be an example of using the operational excellence pillar.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 32:
A Cloud Practitioner anticipates an increase in application traffic at a future date and time when a sales event will take place. How can the Cloud Practitioner configure Amazon EC2 Auto Scaling to ensure the right number of Amazon EC2 instances are available ahead of the event?

*   Configure a scheduled scaling policy.
    
    (Correct)
    
*   Configure predictive scaling.
    
*   Configure a step scaling policy.
    
*   Configure a target tracking scaling policy.
    

#### Explanation

Scheduled scaling helps you to set up your own scaling schedule according to predictable load changes. For example, let's say that every week the traffic to your web application starts to increase on Wednesday, remains high on Thursday, and starts to decrease on Friday. You can configure a schedule for Amazon EC2 Auto Scaling to increase capacity on Wednesday and decrease capacity on Friday.

**CORRECT:** "Configure a scheduled scaling policy" is the correct answer.

**INCORRECT:** "Configure predictive scaling" is incorrect. Predictive scaling uses daily and weekly trends to determine when to scale. In this case the Cloud Practitioner knows about the event that will require more resources.

**INCORRECT:** "Configure a target tracking scaling policy" is incorrect. This policy will cause the ASG to attempt to keep resource utilization at the target value.

**INCORRECT:** "Configure a step scaling policy" is incorrect. Step scaling will launch resources in response to demand, this will not ensure the resource are ready at the right time as there will be a delay.

**References:**

[https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule\_time.html](https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/auto-scaling-and-elastic-load-balancing/](https://digitalcloud.training/auto-scaling-and-elastic-load-balancing/)

Question 33:
A Cloud Practitioner needs a tool that can assist with viewing and managing AWS costs and usage over time. Which tool should the Cloud Practitioner use?

*   AWS Organizations
    
*   Amazon Inspector
    
*   AWS Cost Explorer
    
    (Correct)
    
*   AWS Budgets
    

#### Explanation

AWS Cost Explorer has an easy-to-use interface that lets you visualize, understand, and manage your AWS costs and usage over time. AWS Cost Explorer provides you with a set of default reports that you can use as the starting place for your analysis. From there, use the filtering and grouping capabilities to dive deeper into your cost and usage data and generate custom insights.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_04-45-54-cb987c08235919fe7daa713ac8870bd8.jpg)

**CORRECT:** "AWS Cost Explorer" is the correct answer.

**INCORRECT:** "AWS Budgets" is incorrect. AWS Budgets allows you to set custom budgets to track your cost and usage from the simplest to the most complex use cases.

**INCORRECT:** "Amazon Inspector" is incorrect. Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS

**INCORRECT:** "AWS Organizations" is incorrect. AWS Organizations allows you to organize accounts, create accounts programmatically, and leverage consolidated billing.

**References:**

[https://aws.amazon.com/aws-cost-management/aws-cost-explorer/](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 34:
Which type of credential should a Cloud Practitioner use for programmatic access to AWS resources from the AWS CLI/API?

*   User name and password
    
*   SSL/TLS certificate
    
*   SSH public keys
    
*   Access keys
    
    (Correct)
    

#### Explanation

Access keys are long-term credentials for an IAM user or the AWS account root user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API (directly or using the AWS SDK).

Access keys consist of two parts: an access key ID (for example, AKIAIOSFODNN7EXAMPLE) and a secret access key (for example, wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY).

Like a user name and password, you must use both the access key ID and secret access key together to authenticate your requests. Manage your access keys as securely as you do your user name and password.

**CORRECT:** "Access keys" is the correct answer.

**INCORRECT:** "SSL/TLS certificate" is incorrect. Certificates are not used by users for authenticating to AWS services.

**INCORRECT:** "SSH public keys" is incorrect. These are used for connections using the SSH protocol.

**INCORRECT:** "User name and password" is incorrect. An IAM user name and password can be used for console access but cannot be used with the CLI or API.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 35:
A customer needs to determine Total Cost of Ownership (TCO) for a workload that requires physical isolation. Which hosting model should be accounted for?

*   On-Demand Instances
    
*   Dedicated Hosts
    
    (Correct)
    
*   Reserved Instances
    
*   Spot Instances
    

#### Explanation

An Amazon EC2 Dedicated Host is a physical server with EC2 instance capacity fully dedicated to your use. Dedicated Hosts allow you to use your existing per-socket, per-core, or per-VM software licenses, including Windows Server, Microsoft SQL Server, SUSE, and Linux Enterprise Server.

Note that dedicated hosts can be considered “hosting model” as it determines that actual underlying infrastructure that is used for running your workload. All of the other answers are simply pricing plans for shared hosting models.

**CORRECT:** "Dedicated Hosts" is the correct answer.

**INCORRECT:** "Reserved Instances" is incorrect as this pricing model does not support physical isolation.

**INCORRECT:** "On-Demand Instances" is incorrect as this pricing model does not support physical isolation.

**INCORRECT:** "Spot Instances" is incorrect as this hosting pricing does not support physical isolation.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 36:
A Cloud Practitioner needs to monitor a new Amazon EC2 instances CPU and network utilization. Which AWS service should be used?

*   AWS Systems Manager
    
*   AWS CloudTrail
    
*   Amazon CloudWatch
    
    (Correct)
    
*   Amazon Inspector
    

#### Explanation

Amazon CloudWatch is a performance monitoring service. AWS services send metrics about their utilization to CloudWatch which collects the metrics. You can then view the results in CloudWatch and configure alarms.

**CORRECT:** "Amazon CloudWatch" is the correct answer.

**INCORRECT:** "AWS CloudTrail" is incorrect. CloudTrail is used for auditing, not performance monitoring.

**INCORRECT:** "Amazon Inspector" is incorrect. Inspector is an automated security service.

**INCORRECT:** "AWS Systems Manager" is incorrect. Systems Manager is used for managing EC2 instances such as installing patches and software.

**References:**

[https://aws.amazon.com/cloudwatch/features/](https://aws.amazon.com/cloudwatch/features/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-monitoring-and-logging-services/](https://digitalcloud.training/aws-monitoring-and-logging-services/)

Question 37:
A large company is interested in avoiding long-term contracts and moving from fixed costs to variable costs.

What is the value proposition of AWS for this company?

*   Automated cost optimization
    
*   Volume pricing discounts
    
*   Pay-as-you-go pricing
    
    (Correct)
    
*   Economies of scale
    

#### Explanation

Pay-as-you-go pricing helps companies move away from fixed costs to variable costs in a model in which they only pay for what they actually use. There are no fixed term contracts with AWS so that requirement is also met.

**CORRECT:** "Pay-as-you-go pricing" is the correct answer.

**INCORRECT:** "Economies of scale" is incorrect. You do get good pricing because of the economies of scale leveraged by AWS. However, the value proposition for companies wishing to avoid fixed costs is pay-as-you-go pricing. This flexibility can be more important in some cases than the actual cost per unit.

**INCORRECT:** "Volume pricing discounts" is incorrect. This is not the value proposition for this company as they are seeking to avoid long-term contracts and fixed costs, not to achieve a discount.

**INCORRECT:** "Automated cost optimization" is incorrect. This is a not a feature that relates to the value proposition for this customer.

**References:**

[https://aws.amazon.com/pricing/](https://aws.amazon.com/pricing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 38:
An Amazon Virtual Private Cloud (VPC) can include multiple:

*   Edge locations.
    
*   Availability Zones.
    
    (Correct)
    
*   AWS Regions.
    
*   Internet gateways.
    

#### Explanation

An Amazon VPC includes multiple Availability Zones. Within a VPC you can create subnets in each AZ that is available in the Region and distribute your resources across these subnets for high availability.

**CORRECT:** "Availability Zones" is the correct answer.

**INCORRECT:** "AWS Regions" is incorrect. A VPC cannot include multiple Regions.

**INCORRECT:** "Edge locations" is incorrect. A VPC cannot include multiple Edge locations as these are independent of the Regions in which a VPC is created.

**INCORRECT:** "Internet gateways" is incorrect. You can only attach one Internet gateway to each VPC.

**References:**

[https://aws.amazon.com/vpc](https://aws.amazon.com/vpc)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 39:
A company is planning to deploy an application with a relational database on AWS. The application layer requires access to the database instance’s operating system in order to run scripts.

The company prefer to keep management overhead to a minimum. Which deployment should be used for the database?

*   Amazon EC2
    
    (Correct)
    
*   Amazon S3
    
*   Amazon RDS
    
*   Amazon DynamoDB
    

#### Explanation

The company would like to keep management overhead to a minimum so RDS would be good to meet that requirement. However, with RDS you cannot access the operating system so the requirement for running scripts on the OS rules RDS out. Therefore, the next best solution is to deploy on an Amazon EC2 instances as the other options presented are unsuitable for a relational database.

**CORRECT:** "Amazon EC2" is the correct answer.

**INCORRECT:** "Amazon RDS" is incorrect as the application would not be able to access the OS of the RDS instance to run scripts.

**INCORRECT:** "Amazon DynamoDB" is incorrect. This is a non-relational database.

**INCORRECT:** "Amazon S3" is incorrect. This is an object-storage system and is not suitable for running a relational database.

**References:**

[https://aws.amazon.com/rds/](https://aws.amazon.com/rds/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 40:
A company is deploying a MySQL database on AWS. The database must easily scale and have automatic backup enabled.

Which AWS service should the company use?

*   Amazon DocumentDB
    
*   Amazon Athena
    
*   Amazon Aurora
    
    (Correct)
    
*   Amazon DynamoDB
    

#### Explanation

Amazon Aurora is a relational database that is compatible with MySQL and PostgreSQL database engines. Aurora is extremely fast and scales up to 128 TB. You can also deploy replicas for read scaling within and across Regions. Aurora also offers automated backups.

**CORRECT:** "Amazon Aurora" is the correct answer.

**INCORRECT:** "Amazon DynamoDB" is incorrect. DynamoDB is a NoSQL (non-relational) database and you cannot deploy a MySQL database as it is a relational database type.

**INCORRECT:** "Amazon Athena" is incorrect. Athena is used for querying data in Amazon S3 using SQL.

**INCORRECT:** "Amazon DocumentDB" is incorrect. DocumentDB is a NoSQL database that supports document data structures.

**References:**

[https://aws.amazon.com/rds/aurora/mysql-features/](https://aws.amazon.com/rds/aurora/mysql-features/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 41:
Which design principles are enabled by the AWS Cloud to improve the operation of workloads? (Select TWO.)

*   Loose coupling
    
    (Correct)
    
*   Remove single points of failure
    
    (Correct)
    
*   Minimum viable product
    
*   Minimize platform design
    
*   Customized hardware
    

#### Explanation

Loose coupling is when you break systems down into smaller components that are loosely coupled together. This reduces interdependencies between systems components. This is achieved in the cloud using messages buses, notification and messaging services.

Removing single points of failure ensures fault tolerance and high availability. This is easily achieved in the cloud as the architecture and features of the cloud support the implementation of highly available and fault tolerant systems.

**CORRECT:** "Loose coupling" is a correct answer.

**CORRECT:** "Remove single points of failure" is also a correct answer.

**INCORRECT:** "Customized hardware" is incorrect. You cannot customize hardware in the cloud.

**INCORRECT:** "Minimize platform design" is incorrect. This is not an operational advantage for workloads in the cloud.

**INCORRECT:** "Minimum viable product" is incorrect. This is not an operational advantage for workloads in the cloud.

**References:**

[https://d1.awsstatic.com/whitepapers/AWS\_Cloud\_Best\_Practices.pdf](https://d1.awsstatic.com/whitepapers/AWS_Cloud_Best_Practices.pdf)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 42:
According to the AWS shared responsibility model, which of the following is a responsibility of AWS?

*   Updating security group rules to enable connectivity.
    
*   Configuring network ACLs to block malicious attacks.
    
*   Updating the firmware on the underlying EC2 hosts.
    
    (Correct)
    
*   Patching software running on Amazon EC2 instances.
    

#### Explanation

AWS are responsible for updating firmware on the physical Amazon EC2 host servers. Customers are then responsible for any patching of the EC2 operating system and any installed software.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_05-59-59-1cb2fa80dbe89196d7184e7edb8177cd.jpg)

**CORRECT:** "Updating the firmware on the underlying EC2 hosts" is the correct answer.

**INCORRECT:** "Configuring network ACLs to block malicious attacks" is incorrect. This is a customer responsibility.

**INCORRECT:** "Patching software running on Amazon EC2 instances" is incorrect. This is a customer responsibility.

**INCORRECT:** "Updating security group rules to enable connectivity" is incorrect. This is a customer responsibility.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 43:
A company is deploying a new workload and software licensing requirements dictate that the workload must be run on a specific, physical server.

Which Amazon EC2 instance deployment option should be used?

*   Spot Instances
    
*   Reserved Instances
    
*   Dedicated Instances
    
*   Dedicated Hosts
    
    (Correct)
    

#### Explanation

An Amazon EC2 Dedicated Host is a physical server fully dedicated for your use, so you can help address corporate compliance requirements. Amazon EC2 Dedicated Hosts allow you to use your eligible software licenses from vendors such as Microsoft and Oracle on Amazon EC2, so that you get the flexibility and cost effectiveness of using your own licenses, but with the resiliency, simplicity and elasticity of AWS

**CORRECT:** "Dedicated Hosts" is the correct answer.

**INCORRECT:** "Dedicated Instances" is incorrect. With dedicated instances you are not given a specific physical server to run your instances on.

**INCORRECT:** "Spot Instances" is incorrect. This deployment option does not provide a specific physical server.

**INCORRECT:** "Reserved Instances" is incorrect. This deployment option does not provide a specific physical server.

**References:**

[https://aws.amazon.com/ec2/dedicated-hosts/](https://aws.amazon.com/ec2/dedicated-hosts/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 44:
Which of the following statements best describes the concept of agility in relation to cloud computing on AWS? (Select TWO.)

*   The ability to experiment quickly.
    
    (Correct)
    
*   The ability to automatically scale capacity.
    
*   The elimination of wasted capacity.
    
*   The speed at which AWS resources can be created.
    
    (Correct)
    
*   The speed at which AWS rolls out new features.
    

#### Explanation

In a cloud computing environment, new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes. This results in a dramatic increase in agility for the organization, since the cost and time it takes to experiment and develop is significantly lower.

**CORRECT:** "The ability to experiment quickly" is a correct answer.

**CORRECT:** "The speed at which AWS resources can be created" is also a correct answer.

**INCORRECT:** "The speed at which AWS rolls out new features" is incorrect. This is not a statement that describes agility.

**INCORRECT:** "The elimination of wasted capacity" is incorrect. This is also known as right-sizing and it is a cost benefit of running in the cloud. It is not a statement that describes agility.

**INCORRECT:** "The ability to automatically scale capacity" is incorrect. Auto scaling ensures you have the right amount of capacity available.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 45:
A company has many underutilized compute resources on-premises. Which AWS Cloud feature will help resolve this issue?

*   Global deployment
    
*   Elasticity
    
    (Correct)
    
*   Fault tolerance
    
*   High availability
    

#### Explanation

Elasticity can resolve the issue of underutilization as you can easily and automatically adjust the resource allocations for your compute resources based on actual utilization. This ensures that you have the right amount of resources and do not pay for more than you need.

**CORRECT:** "Elasticity" is the correct answer.

**INCORRECT:** "High availability" is incorrect. This does not help with resolving underutilization.

**INCORRECT:** "Fault tolerance" is incorrect. This does not help with resolving underutilization.

**INCORRECT:** "Global deployment" is incorrect. This does not help with resolving underutilization.

**References:**

[https://aws.amazon.com/aws-cost-management/aws-cost-optimization/right-sizing/](https://aws.amazon.com/aws-cost-management/aws-cost-optimization/right-sizing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 46:
A company plans to deploy a relational database on AWS. The IT department will perform database administration. Which service should the company use?

*   Amazon ElastiCache
    
*   Amazon RedShift
    
*   Amazon EC2
    
    (Correct)
    
*   Amazon DynamoDB
    

#### Explanation

A self-managed relational database can be installed on Amazon EC2. When using this deployment you can choose the operating system and instance type that suits your needs and then install and manage any database software you require.

The table below helps you to understand when to use different types of database deployment:

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_04-48-25-d6c35be2d73ed63c18930dc943cdd3f1.jpg)

**CORRECT:** "Amazon EC2" is the correct answer.

**INCORRECT:** "Amazon RedShift" is incorrect. RedShift is managed data warehouse solution and is better suited to use cases where analytics of data is required.

**INCORRECT:** "Amazon ElastiCache" is incorrect. ElastiCache is a managed service for in-memory, high-performance caching of database content.

**INCORRECT:** "Amazon DynamoDB" is incorrect. DynamoDB is a non-relational (NoSQL) type of database.

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 47:
AWS are able to continually reduce their pricing due to:

*   Economies of scale.
    
    (Correct)
    
*   Pay-as-you go pricing.
    
*   Compute savings plans.
    
*   Elastic compute services.
    

#### Explanation

By using cloud computing, you can achieve a lower variable cost than you can get on your own. Because usage from hundreds of thousands of customers is aggregated in the cloud, providers such as AWS can achieve higher economies of scale, which translates into lower pay as-you-go prices.

**CORRECT:** "economies of scale" is the correct answer.

**INCORRECT:** "pay-as-you go pricing" is incorrect. This is a benefit to the customer but is not the reason the actual unit prices are continually being reduce.

**INCORRECT:** "elastic compute services" is incorrect. Elasticity is useful for scaling your resources and aligning costs with demand but is not why AWS prices are being lowered.

**INCORRECT:** "compute savings plans" is incorrect. This is another feature you can take advantage of for bigger discounts but is not the reason for prices being lowered.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 48:
Which of the following are valid benefits of using the AWS Cloud? (Select TWO.)

*   Ability to go global quickly.
    
    (Correct)
    
*   Outsource all operational risk.
    
*   Fast provisioning of IT resources.
    
    (Correct)
    
*   Total control over data center infrastructure.
    
*   Outsource all application development to AWS.
    

#### Explanation

The ability to provision IT resources quickly and easily and also globally are valid benefits of using the AWS cloud. These are covered in AWS’ 6 advantages of cloud which include “Increase speed and agility” and “Go global in minutes”.

**CORRECT:** "Fast provisioning of IT resources" is a correct answer.

**CORRECT:** "Ability to go global quickly" is also a correct answer.

**INCORRECT:** "Outsource all operational risk" is incorrect. You do not outsource all operational risk; you still have to manage risk for the applications you run on AWS.

**INCORRECT:** "Total control over data center infrastructure" is incorrect. You don’t have any control over data center infrastructure in the AWS Cloud.

**INCORRECT:** "Outsource all application development to AWS" is incorrect. You must still develop your own applications on the AWS Cloud.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 49:
Which of the following will help a user determine if they need to request an Amazon EC2 service limit increase?

*   AWS Trusted Advisor
    
    (Correct)
    
*   Amazon RDS
    
*   AWS Health Dashboard
    
*   AWS Cost Explorer
    

#### Explanation

AWS Trusted Advisor is an online tool that provides you real time guidance to help you provision your resources following AWS best practices. Trusted Advisor checks help optimize your AWS infrastructure, improve security and performance, reduce your overall costs, and monitor service limits.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_05-23-49-b38f895f8cce38ef89055f6a44ad1106.jpg)

**CORRECT:** "AWS Trusted Advisor" is the correct answer.

**INCORRECT:** "AWS Health Dashboard" is incorrect. The  health dashboard shows issues or upcoming events that may impact your resources. It does not notify of service limit breaches.

**INCORRECT:** "Amazon RDS" is incorrect. This is a managed SQL database and has nothing to do with service limits generally.

**INCORRECT:** "AWS Cost Explorer" is incorrect. Cost Explorer is used for viewing costs and will not assist with service limits.

**References:**

[https://aws.amazon.com/premiumsupport/technology/trusted-advisor/](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-management-services/](https://digitalcloud.training/aws-cloud-management-services/)

Question 50:
A website has a global customer base and users have reported poor performance when connecting to the site.

Which AWS service will improve the customer experience by reducing latency?

*   Amazon ElastiCache
    
*   Amazon CloudFront
    
    (Correct)
    
*   Amazon EC2 Auto Scaling
    
*   AWS Direct Connect
    

#### Explanation

Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment.

**CORRECT:** "Amazon CloudFront" is the correct answer.

**INCORRECT:** "AWS Direct Connect" is incorrect. Direct Connect is a private network connection between an on-premises data center and AWS.

**INCORRECT:** "Amazon EC2 Auto Scaling" is incorrect. Auto Scaling launches and terminates instances, this does not reduce latency for global users.

**INCORRECT:** "Amazon ElastiCache" is incorrect. ElastiCache is a database caching service, it is not used to cache websites.

**References:**

[https://aws.amazon.com/cloudfront/](https://aws.amazon.com/cloudfront/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-content-delivery-and-dns-services/](https://digitalcloud.training/aws-content-delivery-and-dns-services/)

Question 51:
For what purpose would a Cloud Practitioner access AWS Artifact?

*   Access training materials for AWS services.
    
*   Create a security assessment report for AWS services.
    
*   Download configuration details for all AWS resources.
    
*   Gain access to AWS security and compliance documents.
    
    (Correct)
    

#### Explanation

AWS Artifact is your go-to, central resource for compliance-related information that matters to you. It provides on-demand access to AWS’ security and compliance reports and select online agreements.

Reports available in AWS Artifact include our Service Organization Control (SOC) reports, Payment Card Industry (PCI) reports, and certifications from accreditation bodies across geographies and compliance verticals that validate the implementation and operating effectiveness of AWS security controls.

**CORRECT:** "Gain access to AWS security and compliance documents" is the correct answer.

**INCORRECT:** "Download configuration details for all AWS resources" is incorrect. Artifact does not provide this capability.

**INCORRECT:** "Access training materials for AWS services" is incorrect. Artifact does not provide training materials.

**INCORRECT:** "Create a security assessment report for AWS services" is incorrect. Artifact cannot be used for this purpose.

**References:**

[https://aws.amazon.com/artifact/](https://aws.amazon.com/artifact/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 52:
Which of the following is a sole responsibility of AWS?

*   Customer data access controls
    
*   Patch management
    
*   Application deployment
    
*   Availability Zone management
    
    (Correct)
    

#### Explanation

According to the shared responsibility model, AWS is responsible to the management of all AWS global infrastructure components including Regions, Availability Zones, Edge locations, Regional Edge Caches, and Local Zones.

**CORRECT:** "Availability Zone management" is the correct answer.

**INCORRECT:** "Application deployment" is incorrect. Applications are deployed by customers, not AWS.

**INCORRECT:** "Patch management" is incorrect. Patch management is a shared responsibility. Customers must patch instances databases running on EC2 and AWS will patch the underlying infrastructure and some managed services.

**INCORRECT:** "Customer data access controls" is incorrect. Customers are responsible for implementing access controls for their data.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 53:
An individual IAM user must be granted access to an Amazon S3 bucket using a bucket policy. Which element in the S3 bucket policy should be updated to define the user account for which access will be granted?

*   Resource
    
*   Condition
    
*   Principal
    
    (Correct)
    
*   Action
    

#### Explanation

The Principal element specifies the user, account, service, or other entity that is allowed or denied access to a resource. The bucket policy below has a Principal element set to \* which is a wildcard meaning any user. To grant access to a specific IAM user the following format can be used:

"Principal":{"AWS":"arn:aws:iam::AWSACCOUNTNUMBER:user/username"}

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_04-44-38-5579acec3c1d72e383f4017ddaa9461a.jpg)

**CORRECT:** "Principal" is the correct answer.

**INCORRECT:** "Action" is incorrect. Actions are the permissions that you can specify in a policy.

**INCORRECT:** "Resource" is incorrect. Resources are the ARNs of resources you wish to specify permissions for.

**INCORRECT:** "Condition" is incorrect. Conditions define certain conditions to apply when granting permissions such as the source IP address of the caller.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-bucket-user-policy-specifying-principal-intro.html](https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-bucket-user-policy-specifying-principal-intro.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 54:
Which tasks require the use of the AWS account root user? (Select TWO.)

*   Enabling encryption for S3.
    
*   Viewing AWS CloudTrail logs.
    
*   Changing payment currency.
    
*   Changing the account name.
    
    (Correct)
    
*   Changing AWS Support plans.
    
    (Correct)
    

#### Explanation

Some tasks can only be performed by the root user of an AWS account. This includes changing the account name and changing AWS support plans. For more information view the AWS article referenced below.

**CORRECT:** "Changing the account name" is a correct answer.

**CORRECT:** "Changing AWS Support plans" is also a correct answer.

**INCORRECT:** "Enabling encryption for S3" is incorrect. This does not require root.

**INCORRECT:** "Viewing AWS CloudTrail logs" is incorrect. This does not require root.

**INCORRECT:** "Changing payment currency" is incorrect. This does not require root.

**References:**

[https://docs.aws.amazon.com/general/latest/gr/root-vs-iam.html](https://docs.aws.amazon.com/general/latest/gr/root-vs-iam.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 55:
Which AWS feature can be used to launch a pre-configured Amazon Elastic Compute Cloud (EC2) instance?

*   Amazon Machine Image (AMI)
    
    (Correct)
    
*   Amazon Elastic Block Store (EBS)
    
*   Amazon AppStream 2.0
    
*   Amazon EC2 Systems Manager
    

#### Explanation

An Amazon Machine Image (AMI) provides the information required to launch an instance. You must specify an AMI when you launch an instance. You can launch multiple instances from a single AMI when you need multiple instances with the same configuration. You can use different AMIs to launch instances when you need instances with different configurations.

**CORRECT:** "Amazon Machine Image (AMI)" is the correct answer.

**INCORRECT:** "Amazon Elastic Block Store (EBS)" is incorrect. EBS is block-based storage for EC2.

**INCORRECT:** "Amazon EC2 Systems Manager" is incorrect . AWS Systems Manager gives you visibility and control of your infrastructure on AWS.

**INCORRECT:** "Amazon AppStream 2.0" is incorrect. Amazon AppStream 2.0 is a fully managed non-persistent application and desktop streaming service.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 56:
A company is planning to move a number of legacy applications to the AWS Cloud. The solution must be cost-effective. Which approach should the company take?

*   Use AWS Lambda to host the legacy applications in the cloud.
    
*   Rehost the applications on Amazon EC2 instances that are right-sized.
    
    (Correct)
    
*   Migrate the applications to dedicated hosts on Amazon EC2.
    
*   Use an Amazon S3 static website to host the legacy application code.
    

#### Explanation

The most cost-effective solution that works is to use Amazon EC2 instances that are right-sized with the most optimum instance types. Right-sizing is the process of ensuring that the instance type selected for each application provides the right amount of resources for the application.

**CORRECT:** "Rehost the applications on Amazon EC2 instances that are right-sized" is the correct answer.

**INCORRECT:** "Migrate the applications to dedicated hosts on Amazon EC2" is incorrect. Dedicated hosts are expensive and there is no need to use them with this solution.

**INCORRECT:** "Use AWS Lambda to host the legacy applications in the cloud" is incorrect. It is unlikely that you can simply host legacy applications using AWS Lambda.

**INCORRECT:** "Use an Amazon S3 static website to host the legacy application code" is incorrect. You cannot host legacy application code in an S3 static website, only static content is possible.

**References:**

[https://d1.awsstatic.com/whitepapers/cost-optimization-right-sizing.pdf](https://d1.awsstatic.com/whitepapers/cost-optimization-right-sizing.pdf)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 57:
A company is deploying a new web application in a single AWS Region that will be used by users globally.

Which AWS services will assist with lowering latency and improving transfer speeds for the global users? (Select TWO.)

*   AWS Direct Connect
    
*   AWS Snowcone
    
*   Amazon CloudFront
    
    (Correct)
    
*   AWS Global Accelerator
    
    (Correct)
    
*   AWS Transit Gateway
    

#### Explanation

Amazon CloudFront is a content delivery network (CDN) that caches content around the world for lower latency access. AWS Global Accelerator enables access to your application by leveraging the same Edge Locations as CloudFront and routing connections across the AWS global network.

Both of these services assist with lowering latency and improving transfer speeds for users who are distributed around the world.

**CORRECT:** "AWS Global Accelerator" is a correct answer.

**CORRECT:** "Amazon CloudFront" is also a correct answer.

**INCORRECT:** "AWS Direct Connect" is incorrect. This service provides private connections from data centers to AWS. It is not useful for distributed users as they will not be able to take advantage of it.

**INCORRECT:** "AWS Transit Gateway" is incorrect. This service is used for optimizing the network topology of interconnected VPCs and on-premises networks.

**INCORRECT:** "AWS Snowcone" is incorrect. Snowcone is used as an edge device for transferring data.

**References:**

[https://aws.amazon.com/global-accelerator/](https://aws.amazon.com/global-accelerator/)

[https://aws.amazon.com/cloudfront/](https://aws.amazon.com/cloudfront/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-content-delivery-and-dns-services/](https://digitalcloud.training/aws-content-delivery-and-dns-services/)

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 58:
A Cloud Practitioner is developing a new application and wishes to integrate features of AWS services directly into the application.

Which of the following is the BEST tool for this purpose?

*   AWS CodePipeline
    
*   AWS CodeDeploy
    
*   AWS Command Line Interface (CLI)
    
*   AWS Software Development Kit
    
    (Correct)
    

#### Explanation

A software development kit (SDK) is a collection of software development tools in one installable package. AWS provide SDKs for various programming languages and these can be used for integrating the features of AWS services directly into an application.

**CORRECT:** "AWS Software Development Kit" is the correct answer.

**INCORRECT:** "AWS Command Line Interface (CLI)" is incorrect. The AWS CLI is used for running commands but is not the best tool for integrating features of AWS services directly into an application.

**INCORRECT:** "AWS CodeDeploy" is incorrect. CodeDeploy is used for deploying code from a code repository and actually installing the application.

**INCORRECT:** "AWS CodePipeline" is incorrect. CodePipeline is used for automating the code release lifecycle.

**References:**

[https://aws.amazon.com/tools/](https://aws.amazon.com/tools/)

Question 59:
A company is migrating a monolithic application that does not scale well into the cloud and refactoring it into a microservices architecture.

Which best practice of the AWS Well-Architected Framework does this plan relate to?

*   Stop spending money on undifferentiated heavy lifting.
    
*   Manage change in automation.
    
*   Implement loosely coupled services.
    
    (Correct)
    
*   Use multiple solutions to improve performance.
    

#### Explanation

A microservices architecture will help ensure that each component of the application can scale independently and be updated independently. Loose coupling further assists as it places reduces the dependencies between systems and ensures that messages and data being passed between application components can be reliably and durably stored.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-04-25_05-56-00-a5aeabde11392dab27b2d3eb48c19013.jpg)

**CORRECT:** "Implement loosely coupled services" is the correct answer.

**INCORRECT:** "Stop spending money on undifferentiated heavy lifting" is incorrect. This is not the best practice being implemented by the company.

**INCORRECT:** "Manage change in automation" is incorrect. This is not the best practice being implemented by the company.

**INCORRECT:** "Use multiple solutions to improve performance" is incorrect. This is not the best practice being implemented by the company.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 60:
Which benefits can a company gain by deploying a relational database on Amazon RDS instead of Amazon EC2? (Select TWO.)

*   Schema management
    
*   Software patching
    
    (Correct)
    
*   Root access to OS
    
*   Indexing of tables
    
*   Automated backups
    
    (Correct)
    

#### Explanation

Two of the benefits of using a managed Amazon RDS service instead of a self-managed database on EC2 are that you get automated backups and automatic software patching.

**CORRECT:** "Automated backups" is a correct answer.

**CORRECT:** "Software patching" is also a correct answer.

**INCORRECT:** "Schema management" is incorrect. This is not a feature of the managed service.

**INCORRECT:** "Indexing of tables" is incorrect. This is not a feature of the managed service.

**INCORRECT:** "Root access to OS" is incorrect. You do not get root access to an RDS instance’s operating system.

**References:**

[https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 61:
A company must provide access to AWS resources for their employees. Which security practices should they follow? (Select TWO.)

*   Create IAM policies based on least privilege principles.
    
    (Correct)
    
*   Create IAM Roles and apply them to IAM groups.
    
*   Create IAM users in different AWS Regions.
    
*   Enable multi-factor authentication for users.
    
    (Correct)
    
*   Disable password policies and management console access.
    

#### Explanation

There are a several security best practices for AWS IAM that are listed in the document shared below. Enabling multi-factor authentication is a best practice to require a second factor of authentication when logging in. Another best practice is to grant least privilege access when configuring users and password policies.

**CORRECT:** "Enable multi-factor authentication for users" is a correct answer.

**CORRECT:** "Create IAM policies based on least privilege principles" is also a correct answer.

**INCORRECT:** "Disable password policies and management console access" is incorrect. This is not a security best practice. There is no need to disable management console access and password policies should be used.

**INCORRECT:** "Create IAM users in different AWS Regions" is incorrect. You cannot create IAM users in different Regions as the IAM service is a global service.

**INCORRECT:** "Create IAM Roles and apply them to IAM groups" is incorrect. You cannot apply roles to groups, you apply policies to groups.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 62:
Which AWS Cloud service provides recommendations on how to optimize performance for AWS services?

*   Amazon CloudWatch
    
*   AWS CloudTrail
    
*   AWS Trusted Advisor
    
    (Correct)
    
*   Amazon Inspector
    

#### Explanation

AWS Trusted Advisor can improve the performance of your service by checking your service limits, ensuring you take advantage of provisioned throughput, and monitoring for overutilized instances.

**CORRECT:** "AWS Trusted Advisor" is the correct answer.

**INCORRECT:** "Amazon Inspector" is incorrect. Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS.

**INCORRECT:** "Amazon CloudWatch" is incorrect. CloudWatch monitors performance but does not provide recommendations for optimization.

**INCORRECT:** "AWS CloudTrail" is incorrect. CloudTrail is an auditing service.

**References:**

[https://aws.amazon.com/premiumsupport/technology/trusted-advisor/](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 63:
What are AWS Identity and Access Management (IAM) access keys used for?

*   Logging in to the AWS Management Console.
    
*   Enabling encryption in transit for web servers.
    
*   Ensuring the integrity of log files.
    
*   Making programmatic calls to AWS from AWS APIs.
    
    (Correct)
    

#### Explanation

Access keys are long-term credentials for an IAM user or the AWS account root user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API (directly or using the AWS SDK).

Access keys consist of two parts: an access key ID (for example, AKIAIOSFODNN7EXAMPLE) and a secret access key (for example, wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY).

Like a user name and password, you must use both the access key ID and secret access key together to authenticate your requests. Manage your access keys as securely as you do your user name and password.

**CORRECT:** "Making programmatic calls to AWS from AWS APIs" is the correct answer.

**INCORRECT:** "Logging in to the AWS Management Console" is incorrect. You use a user name and password for the management console.

**INCORRECT:** "Ensuring the integrity of log files" is incorrect. This is not what access keys are used for.

**INCORRECT:** "Enabling encryption in transit for web servers" is incorrect. SSL/TLS certificates are used for creating encrypted channels using HTTPS.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 64:
A company needs to publish messages to a thousands of subscribers simultaneously using a push mechanism.

Which AWS service should the company use?

*   Amazon Simple Queue Service (Amazon SQS)
    
*   AWS Step Functions
    
*   Amazon Simple Notification Service (Amazon SNS)
    
    (Correct)
    
*   Amazon Simple Workflow Service (SWF)
    

#### Explanation

Amazon SNS is a publisher/subscriber notification service that uses a push mechanism to publish messages to multiple subscribers. Amazon SNS enables you to send messages or notifications directly to users with SMS text messages to over 200 countries, mobile push on Apple, Android, and other platforms or email (SMTP).

**CORRECT:** "Amazon Simple Notification Service (Amazon SNS)" is the correct answer.

**INCORRECT:** "Amazon Simple Queue Service (Amazon SQS)" is incorrect. SQS is a message queue service used for decoupling applications.

**INCORRECT:** "Amazon Simple Workflow Service (SWF)" is incorrect. SWF is a workflow orchestration service, not a messaging service.

**INCORRECT:** "AWS Step Functions" is incorrect. AWS Step Functions is a serverless workflow orchestration service for modern applications.

**References:**

[https://aws.amazon.com/sns/](https://aws.amazon.com/sns/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-application-integration/](https://digitalcloud.training/aws-application-integration/)

Question 65:
Which AWS service can a team use to deploy infrastructure on AWS using familiar programming languages?

*   AWS CodeCommit
    
*   AWS Cloud Development Kit (AWS CDK)
    
    (Correct)
    
*   AWS Config
    
*   Amazon CodeGuru
    

#### Explanation

The AWS Cloud Development Kit (AWS CDK) is an open source software development framework to define cloud application resources using familiar programming languages. With AWS CDK you can stick to using programming languages that are familiar to you and have infrastructure deployed using AWS CloudFormation.

**CORRECT:** "AWS Cloud Development Kit (AWS CDK)" is the correct answer.

**INCORRECT:** "Amazon CodeGuru" is incorrect. CodeGuru is used to review code and provide intelligent recommendations for improvement.

**INCORRECT:** "AWS Config" is incorrect. AWS Config is used for configuration compliance management.

**INCORRECT:** "AWS CodeCommit" is incorrect. CodeCommit is a fully-managed source control service.

**References:**

[https://aws.amazon.com/cdk/](https://aws.amazon.com/cdk/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)