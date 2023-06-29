AWS Certified Cloud Practitioner: Test 5 - Results
--------------------------------------------------



All knowledge areas

*   All knowledge areas
    
*   AWS Networking & Content Delivery
    
*   AWS Security, Identity, & Compliance
    
*   AWS Storage
    
*   AWS Management & Governance
    
*   AWS Compute
    
*   AWS Machine Learning
    
*   AWS Cost Management
    
*   AWS Cloud Architecture & Design
    
*   AWS Cloud Benefits
    
*   AWS Analytics
    
*   AWS Database
    
*   AWS Support
    
*   AWS Internet of Things
    
*   AWS Application Integration
    
*   AWS Shared Responsibility Model
    



Question 1:
What are the primary benefits of using AWS Elastic Load Balancing? (Select TWO.)

*   Regional resilience   
*   Automation   
*   Caching   
*   High availability   
    
    (Correct)
    
*   Elasticity   
    
    (Correct)
    

#### Explanation

**High availability –** ELB automatically distributes traffic across multiple EC2 instances in different AZs within a region.

**Elasticity –** ELB is capable of handling rapid changes in network traffic patterns.

**CORRECT:** "High availability" is a correct answer.

**CORRECT:** "Elasticity" is also a correct answer.

**INCORRECT:** "Automation" is incorrect. Automation is not a primary benefit of ELB.

**INCORRECT:** "Caching" is incorrect. Caching is not a benefit of ELB

**INCORRECT:** "Regional resilience" is incorrect. An ELB can distribute incoming traffic across your Amazon EC2 instances in a single Availability Zone or multiple Availability Zones, but not across regions (for regional resilience).

**References:**

[https://aws.amazon.com/elasticloadbalancing/](https://aws.amazon.com/elasticloadbalancing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/2018/10/19/cloud-computing-basics-compute/](https://digitalcloud.training/2018/10/19/cloud-computing-basics-compute/)

Question 2:
What are the benefits of using IAM roles for applications that run on EC2 instances? (Select TWO.)

*   Role credentials are permanent   
*   Easier to configure than using storing access keys within the EC2 instance   
*   It is easier to manage IAM roles   
    
    (Correct)
    
*   More secure than storing access keys within applications   
    
    (Correct)
    
*   Can apply multiple roles to a single instance   

#### Explanation

Using IAM roles instead of storing credentials within EC2 instances is more secure It is also easier to manage roles.

**CORRECT:** "More secure than storing access keys within applications" is the correct answer.

**CORRECT:** "It is easier to manage IAM roles" is the correct answer.

**INCORRECT:** "Easier to configure than using storing access keys within the EC2 instance" is incorrect. It is not easier to configure as there are extra steps that need to be completed.

**INCORRECT:** "Can apply multiple roles to a single instance" is incorrect. You cannot apply multiple roles to a single instance.

**INCORRECT:** "Role credentials are permanent" is incorrect. Role credentials are temporary, not permanent, and are rotated automatically.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_roles\_use\_switch-role-ec2.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 3:
How can a company protect their Amazon S3 data from a regional disaster?

*   Archive to Amazon Glacier   
*   Use Cross-Region Replication (CRR) to copy to another region   
    
    (Correct)
    
*   Use lifecycle actions to move to another S3 storage class   
*   Enable Multi-Factor Authentication (MFA) delete   

#### Explanation

Cross-Region replication (CRR) is used to copy objects across Amazon S3 buckets in different AWS Regions. The only option here that will help is to use CRR to copy the data to another region. This will provide disaster recovery.

**CORRECT:** "Use Cross-Region Replication (CRR) to copy to another region" is the correct answer.

**INCORRECT:** "Archive to Amazon Glacier" is incorrect. Moving to Glacier does not copy the data out of the region.

**INCORRECT:** "Use lifecycle actions to move to another S3 storage class" is incorrect as this will not move the data to another region.

**INCORRECT:** "Enable Multi-Factor Authentication (MFA) delete" is incorrect. Enabling MFA delete will not protect the data from a regional disaster.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 4:
What is an Edge location?

*   A content delivery network (CDN) endpoint for CloudFront   
    
    (Correct)
    
*   A virtual private gateway for VPN   
*   A VPC peering connection endpoint   
*   A public endpoint for Amazon S3   

#### Explanation

Edge locations are Content Delivery Network (CDN) endpoints for CloudFront. There are many more edge locations than regions.

**CORRECT:** "A content delivery network (CDN) endpoint for CloudFront" is the correct answer.

**INCORRECT:** "A public endpoint for Amazon S3" is incorrect as it is not related to S3.

**INCORRECT:** "A virtual private gateway for VPN" is incorrect as it is not related to VPN.

**INCORRECT:** "A VPC peering connection endpoint" is incorrect as it is not related to VPC.

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-global-infrastructure/](https://digitalcloud.training/aws-global-infrastructure/)

Question 5:
Which service provides alerts and remediation guidance when AWS is experiencing events that may impact you?

*   AWS Health Dashboard   
    
    (Correct)
    
*   AWS Inspector   
*   AWS Shield   
*   AWS Trusted Advisor   

#### Explanation

AWS Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you.

**CORRECT:** "AWS Health Dashboard" is the correct answer.

**INCORRECT:** "AWS Trusted Advisor" is incorrect. Trusted Advisor is an online resource that helps to reduce cost, increase performance and improve security by optimizing your AWS environment.

**INCORRECT:** "AWS Inspector" is incorrect. Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS.

**INCORRECT:** "AWS Shield" is incorrect. AWS Shield is a managed Distributed Denial of Service (DDoS) protection service.

**References:**

[https://aws.amazon.com/premiumsupport/technology/aws-health-dashboard/](https://aws.amazon.com/premiumsupport/technology/aws-health-dashboard/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 6:
When designing a VPC, what is the purpose of an Internet Gateway?

*   Provides Internet access for EC2 instances in private subnets   
*   It's a bastion host for inbound management connections   
*   It's used for making VPN connections to a VPC   
*   Enables Internet communications for instances in public subnets   
    
    (Correct)
    

#### Explanation

An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. It therefore imposes no availability risks or bandwidth constraints on your network traffic.

An internet gateway serves two purposes: to provide a target in your VPC route tables for internet-routable traffic, and to perform network address translation (NAT) for instances that have been assigned public IPv4 addresses.

**CORRECT:** "Enables Internet communications for instances in public subnets" is the correct answer.

**INCORRECT:** "Provides Internet access for EC2 instances in private subnets" is incorrect. You cannot connect instances in a private subnet to the Internet using an Internet Gateway, you need a NAT Gateway or NAT Instance for this purpose.

**INCORRECT:** "It's a bastion host for inbound management connections" is incorrect. You cannot use an Internet Gateway as a bastion host, deploy an EC2 instance in a public subnet for this purpose.

**INCORRECT:** "It's used for making VPN connections to a VPC" is incorrect. You cannot use the Internet Gateway for making VPN connections to a VPC, you need a Virtual Private Gateway for this purpose.

**References:**

[https://docs.aws.amazon.com/vpc/latest/userguide/VPC\_Internet\_Gateway.html](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 7:
Which of the following statements is correct about Amazon S3 cross-region replication?

*   The source S3 bucket owner must have the source and destination AWS Regions disabled for their account
    
*   The source and destination S3 buckets cannot be in different AWS Regions
    
*   Both source and destination S3 buckets must have versioning disabled
    
*   S3 buckets conﬁgured for cross-region replication can be owned by a single AWS account or by different accounts
    
    (Correct)
    

#### Explanation

Replication enables automatic, asynchronous copying of objects across Amazon S3 buckets. Buckets that are configured for object replication can be owned by the same AWS account or by different accounts. You can copy objects between different AWS Regions or within the same Region.

Both source and destination buckets must have versioning enabled. The source bucket owner must have the source and destination AWS Regions enabled for their account. The destination bucket owner must have the destination Region-enabled for their account.

**CORRECT:** "S3 buckets conﬁgured for cross-region replication can be owned by a single AWS account or by different accounts" is the correct answer.

**INCORRECT:** "Both source and destination S3 buckets must have versioning disabled" is incorrect as explained above.

**INCORRECT:** "The source and destination S3 buckets cannot be in different AWS Regions" is incorrect as explained above.

**INCORRECT:** "The source S3 bucket owner must have the source and destination AWS Regions disabled for their account" is incorrect as explained above.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 8:
What are two benefits of using AWS Lambda? (Select TWO.)

*   Continuous scaling (scale out)   
    
    (Correct)
    
*   Open source software   
*   Flexible operating system choices   
*   Integrated snapshots   
*   No servers to manage   
    
    (Correct)
    

#### Explanation

With AWS Lambda you don’t have any servers to manage (serverless). Lambda functions scale out rather than up running multiple invocations of the function in parallel.

**CORRECT:** "No servers to manage" is a correct answer.

**CORRECT:** "Continuous scaling (scale out)" is also a correct answer.

**INCORRECT:** "Integrated snapshots" is incorrect. You do not have integrated snapshots (or any persistent storage) with Lambda.

**INCORRECT:** "Flexible operating system choices" is incorrect. You do not manage the operating system on which the functions run so have no choice of software.

**INCORRECT:** "Open source software" is incorrect. Lambda is AWS proprietary not open source.

**References:**

[https://aws.amazon.com/lambda/](https://aws.amazon.com/lambda/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 9:
How can a company connect from their on-premises network to VPCs in multiple regions using private connections?

*   Inter-Region VPC Peering   
*   AWS Managed VPN   
*   Amazon CloudFront   
*   AWS Direct Connect Gateway   
    
    (Correct)
    

#### Explanation

You can use an AWS Direct Connect gateway to connect your AWS Direct Connect connection over a private virtual interface to one or more VPCs in your account that are located in the same or different Regions

**CORRECT:** "AWS Direct Connect Gateway" is the correct answer.

**INCORRECT:** "AWS Managed VPN" is incorrect. AWS Managed VPN uses the public Internet and is therefore not a private connection.

**INCORRECT:** "Amazon CloudFront" is incorrect. Amazon CloudFront is a content delivery network used for caching data.

**INCORRECT:** "Inter-Region VPC Peering" is incorrect. Inter-Region VPC peering does not help you to connect from an on-premise network.

**References:**

[https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways.html](https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 10:
Which AWS service enables developers and data scientists to build, train, and deploy machine learning models?

*   Amazon SageMaker   
    
    (Correct)
    
*   Amazon Comprehend   
*   Amazon Rekognition   
*   Amazon MQ   

#### Explanation

Amazon SageMaker is a fully-managed platform that enables developers and data scientists to quickly and easily build, train, and deploy machine learning models at any scale. Amazon SageMaker removes all the barriers that typically slow down developers who want to use machine learning.

**CORRECT:** "Amazon SageMaker" is the correct answer.

**INCORRECT:** "Amazon Rekognition" is incorrect. Amazon Rekognition makes it easy to add image and video analysis to your applications.

**INCORRECT:** "Amazon Comprehend" is incorrect. Amazon Comprehend is a natural language processing (NLP) service that uses machine learning to find insights and relationships in text

**INCORRECT:** "Amazon MQ" is incorrect. Amazon MQ is a managed message broker service for Apache ActiveMQ that makes it easy to set up and operate message brokers in the cloud.

**References:**

[https://aws.amazon.com/sagemaker/](https://aws.amazon.com/sagemaker/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 11:
An Elastic IP Address can be remapped between EC2 instances across which boundaries?

*   Regions
    
*   DB Subnets
    
*   Edge Locations
    
*   Availability Zones
    
    (Correct)
    

#### Explanation

Elastic IP addresses are for use in a specific region only and can therefore only be remapped between instances within that region. You can use Elastic IP addresses to mask the failure of an instance in one Availability Zone by rapidly remapping the address to an instance in another Availability Zone.

**CORRECT:** "Availability Zones" is the correct answer.

**INCORRECT:** "Regions" is incorrect as you cannot remap across regions.

**INCORRECT:** "Edge Locations" is incorrect. Edge Locations are used by CloudFront and are not places where you can run EC2 instances.

**INCORRECT:** "DB Subnets" is incorrect. DB subnets (groups) are used by the RDS relational database service and are not used for running EC2 instances.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-global-infrastructure/](https://digitalcloud.training/aws-global-infrastructure/)

Question 12:
To reward customers for using their services, what are two ways AWS reduce prices? (Select TWO.)   

*   Reduction in inbound data transfer charges     
*   Reduced cost for reserved capacity   
    
    (Correct)
    
*   Volume based discounts when you use more services   
    
    (Correct)
    
*   Removal of termination fees for customers who spend more   
*   Discounts for using a wider variety of services   

#### Explanation

AWS provide volume based discount so that when you use more services you reduce the cost per service. You can also reserve capacity by locking in to fixed 1 or 3 year contracts to get significant discounts

You never pay for inbound data transfer

You don’t get discounts for using a variety of services, only when you use more services

There are never termination fees with AWS

**CORRECT:** "Volume based discounts when you use more services" is the correct answer.

**CORRECT:** "Reduced cost for reserved capacity" is the correct answer.

**INCORRECT:** "Reduction in inbound data transfer charges" is incorrect $

**INCORRECT:** "Discounts for using a wider variety of services" is incorrect $

**INCORRECT:** "Removal of termination fees for customers who spend more" is incorrect $

**References:**

[https://aws.amazon.com/pricing/](https://aws.amazon.com/pricing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 13:
Which of the following descriptions is incorrect in relation to the design of Availability Zones?

*   Each subnet in a VPC is mapped to all AZs in the region
    
    (Correct)
    
*   Each AZ is designed as an independent failure zone   
*   AZ’s have direct, low-latency, high throughput and redundant network connections between each other   
*   AZs are physically separated within a typical metropolitan region and are located in lower risk flood plains   

#### Explanation

Subnets are created within a single AZ and do not get mapped to multiple AZs.

**CORRECT:** "Each subnet in a VPC is mapped to all AZs in the region" is the correct answer.

**INCORRECT:** "AZ’s have direct, low-latency, high throughput and redundant network connections between each other" is incorrect as this is true.

**INCORRECT:** "Each AZ is designed as an independent failure zone" is incorrect as this is true.

**INCORRECT:** "AZs are physically separated within a typical metropolitan region and are located in lower risk flood plains" is incorrect as this is true.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-global-infrastructure/](https://digitalcloud.training/aws-global-infrastructure/)

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 14:
Which AWS IAM best practice recommends applying the minimum permissions necessary to perform a task when creating IAM policies?

*   Use roles to delegate permissions   
*   Grant least privilege   
    
    (Correct)
    
*   Create individual IAM users   
*   Enable MFA for privileged users   

#### Explanation

When you create IAM policies, follow the standard security advice of granting least privilege—that is, granting only the permissions required to perform a task. Determine what users need to do and then craft policies for them that let the users perform only those tasks.

The other answer are all valid best practices but are not related to applying minimum permissions to IAM policies.

**CORRECT:** "Grant least privilege" is the correct answer.

**INCORRECT:** "Create individual IAM users" is incorrect as explained above.

**INCORRECT:** "Use roles to delegate permissions" is incorrect as explained above.

**INCORRECT:** "Enable MFA for privileged users" is incorrect as explained above.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 15:
An application that is deployed across multiple Availability Zones could be described as:

*   Having elasticity
    
*   Being secure
    
*   Being highly available
    
    (Correct)
    
*   Having global reach
    

#### Explanation

When you deploy an application across multiple Availability Zones the application can be considered to be highly available. You must also have a way of directing traffic to the application in each AZ such as an Elastic Load Balancer.

The diagram below depicts an example of a highly available application deployed on EC2 instances in multiple AZs and using an ELB to direct traffic:

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-56-43-18c74cdb76bdf22d27960f04e73c465c.png)

**CORRECT:** "Being highly available" is the correct answer.

**INCORRECT:** "Having global reach" is incorrect as this refers to deploying applications that can be connected to from around the world and also deploying applications into different regions.

**INCORRECT:** "Being secure" is incorrect as this is not an example of the implementation of security.

**INCORRECT:** "Having elasticity" is incorrect. Auto Scaling is an example of elasticity and it is not mentioned in this question.

**References:**

[https://aws.amazon.com/about-aws/global-infrastructure/regions\_az/](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 16:
Which service can you use to monitor, store and access log files generated by EC2 instances and on-premises servers?

*   Amazon Kinesis   
*   AWS CloudTrail   
*   AWS OpsWorks   
*   Amazon CloudWatch Logs   
    
    (Correct)
    

#### Explanation

You can use Amazon CloudWatch Logs to monitor, store, and access your log files from Amazon Elastic Compute Cloud (Amazon EC2) instances, AWS CloudTrail, Route 53, and other sources. You can then retrieve the associated log data from CloudWatch Logs.

**CORRECT:** "Amazon CloudWatch Logs" is the correct answer.

**INCORRECT:** "AWS CloudTrail" is incorrect. AWS CloudTrail is used for recording a history of API actions taken on your account.

**INCORRECT:** "AWS OpsWorks" is incorrect. OpsWorks is a configuration management service.

**INCORRECT:** "Amazon Kinesis" is incorrect. Amazon Kinesis is a set of services used for collecting, processing and analyzing streaming data.

**References:**

[https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html)

**Save time with our AWS cheat sheets:**

[https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html)

Question 17:
Which service is used introduce fault tolerance into an application architecture?

*   Amazon CloudFront
    
*   Amazon DynamoDB
    
*   Amazon ElastiCache
    
*   Amazon Elastic Load Balancing
    
    (Correct)
    

#### Explanation

Amazon Elastic Load Balancing is used to spread load and introduce fault tolerance by distributing connections across multiple identically configured back-end EC2 instances.

**CORRECT:** "Amazon Elastic Load Balancing" is the correct answer.

**INCORRECT:** "Amazon CloudFront" is incorrect. Amazon CloudFront is a content delivery network that is used for caching content and serving it to web-based users quickly.

**INCORRECT:** "Amazon ElastiCache" is incorrect. Amazon ElastiCache is an in-memory database cache and is used to introduce improved performance rather than fault tolerance.

**INCORRECT:** "Amazon DynamoDB" is incorrect. Amazon DynamoDB is fault tolerant; however, it is not something you add to an architecture to introduce fault tolerance to the application stack.

**References:**

[https://aws.amazon.com/elasticloadbalancing/](https://aws.amazon.com/elasticloadbalancing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 18:
Which AWS security service provides a firewall at the subnet level within a VPC?

*   Network Access Control List
    
    (Correct)
    
*   Security Group
    
*   IAM Policy
    
*   Bucket Policy
    

#### Explanation

A Network ACL is a firewall that is associated with a subnet within your VPC. It is used to filter the network traffic that enters and exits the subnet.

**CORRECT:** "Network Access Control List" is the correct answer.

**INCORRECT:** "Security Group" is incorrect. A Security Group is a firewall that is associated with an EC2 instances (not the subnet). Security Groups control the traffic the inbound and outbound network traffic from/to the instance.

**INCORRECT:** "IAM Policy" is incorrect. An IAM Policy is used to assign permissions to users and roles.

**INCORRECT:** "Bucket Policy" is incorrect. A Bucket Policy is used with Amazon S3 buckets to control access.

**References:**

[https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 19:
What offerings are included in the Amazon LightSail product set? (Select TWO.)

*   File storage   
*   Virtual Private Server
    
    (Correct)
    
*   Serverless functions   
*   Managed MySQL database   
    
    (Correct)
    
*   NoSQL database   

#### Explanation

Amazon LightSail provides an easy, low cost way to consume cloud services without needing the skill set for using VPC resources. The product set includes virtual private servers (instances), managed MySQL databases, block and object storage, simplified load balancers, and CDN distributions.

**CORRECT:** "Virtual Private Server" is a correct answer.

**CORRECT:** "Managed MySQL database" is also a correct answer.

**INCORRECT:** "NoSQL database" is incorrect as explained above.

**INCORRECT:** "File storage" is incorrect as explained above.

**INCORRECT:** "Serverless functions" is incorrect as explained above.

**References:**

[https://aws.amazon.com/lightsail/features/](https://aws.amazon.com/lightsail/features/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 20:
Which AWS service is part of the suite of "serverless" services and runs code as functions?

*   AWS CodeCommit   
*   Amazon EKS
    
*   AWS Lambda   
    
    (Correct)
    
*   Amazon ECS   

#### Explanation

AWS Lambda is a serverless compute service that runs your code in response to events and automatically manages the underlying compute resources for you. The code you run on AWS Lambda is called a “Lambda function”.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_02-42-33-61c62583f577363cffcbce5c09b1d4a8.jpg)

**CORRECT:** "AWS Lambda" is the correct answer.

**INCORRECT:** "Amazon ECS" is incorrect. Amazon ECS is used for running software containers such as Docker containers.

**INCORRECT:** "Amazon EKS" is incorrect. Amazon EKS is used for managing software containers such as Docker containers.

**INCORRECT:** "AWS CodeCommit" is incorrect. AWS CodeCommit is a fully-managed source control service that hosts secure Git-based repositories.

**References:**

[https://aws.amazon.com/lambda/](https://aws.amazon.com/lambda/)

[https://aws.amazon.com/lambda/features/](https://aws.amazon.com/lambda/features/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 21:
Which type of storage stores objects comprised of key, value pairs?

*   Amazon DynamoDB   
*   Amazon S3   
    
    (Correct)
    
*   Amazon EBS   
*   Amazon EFS   

#### Explanation

Amazon Simple Storage Service is storage for the Internet. It is designed to make web-scale computing easier for developers. Amazon S3 is an object-based storage system that stores objects that are comprised of key, value pairs.

**CORRECT:** "Amazon S3" is the correct answer.

**INCORRECT:** "Amazon DynamoDB" is incorrect. Amazon DynamoDB stores items, not objects, based on key, value pairs.

**INCORRECT:** "Amazon EBS" is incorrect. Amazon EBS is a block-based storage system.

**INCORRECT:** "Amazon EFS" is incorrect. Amazon EFS is a file-based storage system.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/Welcome.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/Welcome.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 22:
Assuming you have configured them correctly, which AWS services can scale automatically without intervention? (Select TWO.)

*   Amazon EBS
    
*   Amazon RDS
    
*   Amazon EC2
    
*   Amazon DynamoDB
    
    (Correct)
    
*   Amazon S3
    
    (Correct)
    

#### Explanation

Both S3 and DynamoDB automatically scale as demand dictates. In the case of DynamoDB you can either configure the on-demand or provisioned capacity mode. With on-demand capacity mode DynamoDB automatically adjusts the read and write throughput for you.

EBS and RDS do not scale automatically. You must intervene to adjust volume sizes and database instance types to scale these resources

**CORRECT:** "Amazon S3" is a correct answer.

**CORRECT:** "Amazon DynamoDB" is also a correct answer.

**INCORRECT:** "Amazon RDS" is incorrect as explained above.

**INCORRECT:** "Amazon EC2" is incorrect. EC2 cannot scale automatically. You need to use Auto Scaling to scale the number of EC2 instances deployed.

**INCORRECT:** "Amazon EBS" is incorrect as explained above.

**References:**

[https://aws.amazon.com/blogs/architecture/tag/scalability/](https://aws.amazon.com/blogs/architecture/tag/scalability/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 23:
A company wants to utilize a pay as you go cloud model for all of their applications without CAPEX costs and which is highly elastic. Which cloud delivery model will suit them best?   

*   Private   
*   Hybrid
    
*   On-premise   
*   Public
    
    (Correct)
    

#### Explanation

The public cloud is offered under a purely pay as you go model (unless you choose to reserve), and allows companies to completely avoid CAPEX costs. The public cloud is also highly elastic so companies can grow and shrink the applications as demand changes.

Private and on-premise clouds are essentially the same, though both could be managed by a third party and even could be delivered under an OPEX model by some vendors. However, they are typically more CAPEX heavy and the elasticity is limited.

A hybrid model combines public and private and this company wants to go all in on a single model.

**CORRECT:** "Public" is the correct answer.

**INCORRECT:** "Private" is incorrect as explained above.

**INCORRECT:** "Hybrid" is incorrect as explained above.

**INCORRECT:** "On-premise" is incorrect as explained above.

**References:**

[https://aws.amazon.com/types-of-cloud-computing/](https://aws.amazon.com/types-of-cloud-computing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 24:
Which AWS service can be used to prepare and load data for analytics using an extract, transform and load (ETL) process?

*   Amazon Athena   
*   Amazon EMR   
*   AWS Lambda
    
*   AWS Glue   
    
    (Correct)
    

#### Explanation

AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics.

You can point AWS Glue to data stored on AWS, and AWS Glue discovers the data and stores the associated metadata (e.g. table definition and schema) in the AWS Glue Data Catalog. Once cataloged, the data is immediately searchable, queryable, and available for ETL.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_02-36-58-e4d7e1c54611e9c71f0a268c38de6fd1.jpg)

**CORRECT:** "AWS Glue" is the correct answer.

**INCORRECT:** "AWS Lambda" is incorrect. AWS Lambda is a serverless application that runs code as functions in response to events

**INCORRECT:** "Amazon EMR" is incorrect. Amazon Elastic Map Reduce (EMR) provides a managed Hadoop framework that makes it easy, fast, and cost-effective to process vast amounts of data across dynamically scalable Amazon EC2 instances

**INCORRECT:** "Amazon Athena" is incorrect. Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL.

**References:**

[https://aws.amazon.com/glue/](https://aws.amazon.com/glue/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 25:
A Cloud Practitioner needs to rapidly deploy a popular IT solution and start using it immediately.

What should the Cloud Practitioner use?

*   AWS Quick Start reference deployments
    
    (Correct)
    
*   Amazon CloudFront
    
*   AWS Well-Architected Framework documentation
    
*   AWS Elastic Beanstalk
    

#### Explanation

Quick Starts are built by AWS solutions architects and partners to help you deploy popular technologies on AWS, based on AWS best practices for security and high availability. These accelerators reduce hundreds of manual procedures into just a few steps, so you can build your production environment quickly and start using it immediately.

Each Quick Start includes AWS CloudFormation templates that automate the deployment and a guide that discusses the architecture and provides step-by-step deployment instructions.

**CORRECT:** "AWS Quick Start reference deployments" is the correct answer.

**INCORRECT:** "AWS Well-Architected Framework documentation" is incorrect. The well architected framework is documentation that provides guidance on design best practices. It is not used to actually deploy anything.

**INCORRECT:** "Amazon CloudFront" is incorrect. CloudFront is a content delivery network (CDN) that caches content for better performance.

**INCORRECT:** "AWS Elastic Beanstalk" is incorrect. Elastic Beanstalk can be used to easily deploy certain web applications. However, you still need to supply the code and it is limited to EC2 instances.

**References:**

[https://aws.amazon.com/quickstart/](https://aws.amazon.com/quickstart/)

Question 26:
Which AWS components aid in the construction of fault-tolerant applications? (Select TWO.)

*   Tags
    
*   Block device mappings
    
*   AMIs
    
    (Correct)
    
*   ARNs
    
*   Elastic IP addresses   
    
    (Correct)
    

#### Explanation

Elastic IP addresses can be easily remapped between EC2 instances in the event of a failure. Amazon Machine Images (AMIs) can be used to quickly launch replacement instances when there is a failure

Amazon Resource Names (ARNs), tags and block device mappings don’t really help with fault tolerance

**CORRECT:** "Elastic IP addresses" is a correct answer.

**CORRECT:** "AMIs" is also a correct answer.

**INCORRECT:** "ARNs" is incorrect as explained above.

**INCORRECT:** "Tags" is incorrect as explained above.

**INCORRECT:** "Block device mappings" is incorrect as explained above.

**References:**

[https://d1.awsstatic.com/whitepapers/aws-building-fault-tolerant-applications.pdf](https://d1.awsstatic.com/whitepapers/aws-building-fault-tolerant-applications.pdf)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 27:
What charges are applicable to Amazon S3 Standard storage class? (Select TWO.)

*   Retrieval fee   
*   Data ingress   
*   Minimum capacity charge per object   
*   Per GB/month storage fee   
    
    (Correct)
    
*   Data egress   
    
    (Correct)
    

#### Explanation

With the standard storage class you pay a per GB/month storage fee, and data transfer out of S3. Standard-IA and One Zone-IA have a minimum capacity charge per object. Standard-IA, One Zone-IA, and Glacier also have a retrieval fee. You don’t pay for data into S3 under any storage class.

**CORRECT:** "Per GB/month storage fee" is the correct answer.

**CORRECT:** "Data egress" is the correct answer.

**INCORRECT:** "Retrieval fee" is incorrect as explained above.

**INCORRECT:** "Minimum capacity charge per object" is incorrect as explained above.

**INCORRECT:** "Data ingress" is incorrect as explained above.

**References:**

[https://aws.amazon.com/s3/pricing/](https://aws.amazon.com/s3/pricing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 28:
What information must be entered into the AWS TCO Calculator?

*   The number of end users in your company
    
*   The number of applications in your company
    
*   The number of storage systems in your company
    
*   The number of servers in your company
    
    (Correct)
    

#### Explanation

The TCO calculator asks for the number of servers (Physical or VMs) you are running on-premises. You also need to supply the resource information (CPU, RAM) and specify whether the server is a DB or non-DB.

Use this new calculator to compare the cost of your applications in an on-premises or traditional hosting environment to AWS. Describe your on-premises or hosting environment configuration to produce a detailed cost comparison with AWS.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_03-29-27-48506cecbb9c3b1ef77a4a90476983e8.jpg)

**CORRECT:** "The number of servers in your company" is the correct answer.

**INCORRECT:** "The number of end users in your company" is incorrect. You do not need to supply the number of end users.

**INCORRECT:** "The number of applications in your company" is incorrect. You do not need to supply the number of applications.

**INCORRECT:** "The number of storage systems in your company" is incorrect. You don’t need to specify the number of storage systems, you just need to specify the raw capacity.

**References:**

[https://aws.amazon.com/tco-calculator/](https://aws.amazon.com/tco-calculator/)

[https://awstcocalculator.com/](https://awstcocalculator.com/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 29:
A company needs protection from distributed denial of service (DDoS) attacks on its website and assistance from AWS experts during such events.

Which AWS managed service will meet these requirements?

*   Amazon GuardDuty
    
*   AWS Shield Advanced
    
    (Correct)
    
*   AWS Firewall Manager
    
*   AWS Web Application Firewall
    

#### Explanation

AWS Shield Advanced provides enhanced detection and includes a specialized support team for customers on Enterprise or Business support plans. The AWS DDoS Response Team (DRT) are available 24/7 and can be engaged before, during, or after a DDoS attack.

**CORRECT:** "AWS Shield Advanced" is the correct answer.

**INCORRECT:** "AWS Firewall Manager" is incorrect. This service is used to simplify management of AWS WAF, AWS Shield Advanced, and Amazon VPC security groups.

**INCORRECT:** "AWS Web Application Firewall" is incorrect. AWS WAF is used for protecting web applications and APIs against malicious attacks. This is not a DDoS prevention service.

**INCORRECT:** "Amazon GuardDuty" is incorrect. This service is used for continuously monitoring AWS resources for threats. It is not a DDoS prevention service, it uses machine learning and anomaly detection to identify security vulnerabilities in resources.

**References:**

[https://aws.amazon.com/shield/getting-started/](https://aws.amazon.com/shield/getting-started/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 30:
What is the relationship between subnets and availability zones?

*   You can create one or more subnets within each availability zone   
    
    (Correct)
    
*   You can create one subnet per availability zone   
*   Subnets contain one or more availability zones   
*   Subnets span across multiple availability zones   

#### Explanation

You can create one or more subnets within each availability zone but subnets cannot span across availability zones.

**CORRECT:** "You can create one or more subnets within each availability zone" is the correct answer.

**INCORRECT:** "Subnets span across multiple availability zones" is incorrect as they are contained within a single AZ.

**INCORRECT:** "You can create one subnet per availability zone" is incorrect as you can create many subnets per AZ.

**INCORRECT:** "Subnets contain one or more availability zones" is incorrect as they are created within a single AZ.

**References:**

[https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 31:
Which of the following constitute the six pillars for the AWS Well-Architected Framework? (Select TWO.)

*   Data consistency, and cost optimization   
*   Operational excellence, elasticity and scalability   
*   Cost prioritization, and cost optimization   
*   Performance efficiency, sustainability, and cost optimization
    
    (Correct)
    
*   Operational excellence, security, and reliability   
    
    (Correct)
    

#### Explanation

The six pillars of the AWS Well-Architected Framework are operational excellence, security, reliability, performance efficiency, cost optimization, and sustainability.

**CORRECT:** "Operational excellence, security, and reliability" is the correct answer.

**CORRECT:** "Performance efficiency, sustainability, and cost optimization" is the correct answer.

**INCORRECT:** "Operational excellence, elasticity and scalability" is incorrect as elasticity and scalability are not included.

**INCORRECT:** "Cost prioritization, and cost optimization" is incorrect as cost prioritization is not included.

**INCORRECT:** "Data consistency, and cost optimization" is incorrect as data consistency is not included.

**References:**

[https://aws.amazon.com/blogs/apn/the-6-pillars-of-the-aws-well-architected-framework](https://aws.amazon.com/blogs/apn/the-6-pillars-of-the-aws-well-architected-framework)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 32:
Which AWS feature of Amazon EC2 allows an administrator to create a standardized image that can be used for launching new instances?

*   Amazon Block Template
    
*   Amazon Machine Image
    
    (Correct)
    
*   Amazon EBS Mount Point
    
*   Amazon Golden Image
    

#### Explanation

An Amazon Machine Image (AMI) provides the information required to launch an instance. You can use an AMI to launch identical instances from a standard template. This is also known as a Golden Image (though no such feature exists in AWS with this name). An AMI is created from an EBS snapshot and also includes launch permissions and a block device mapping.

**CORRECT:** "Amazon Machine Image" is the correct answer.

**INCORRECT:** "Amazon Golden Image" is incorrect as this is not an AWS feature.

**INCORRECT:** "Amazon Block Template" is incorrect. Amazon Block Templates do not exist.

**INCORRECT:** "Amazon EBS Mount Point" is incorrect. An Amazon EBS Mount Point is not an AWS feature. You do mount EBS volumes however this is within the operating system. Block device mappings are used in AMIs to specify how to mount the EBS volume.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)

**Save time with our AWS cheat sheets:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)

Question 33:
Which tools can you use to manage identities in IAM? (Select TWO.)

*   Amazon Workspaces
    
*   EC2 Management Console
    
*   AWS Command Line Tools
    
    (Correct)
    
*   AWS Management Console
    
    (Correct)
    
*   Amazon CloudWatch API
    

#### Explanation

You can manage AWS Identity and Access Management identities through the AWS Management Console, AWS Command Line Tools, AWS SDKs, and IAM HTTPS API.

**CORRECT:** "AWS Management Console" is a correct answer.

**CORRECT:** "AWS Command Line Tools" is also a correct answer.

**INCORRECT:** "Amazon CloudWatch API" is incorrect. CloudWatch is not used for managing identities in IAM. It is a service used for monitoring the state of your AWS resources.

**INCORRECT:** "EC2 Management Console" is incorrect. The EC2 management console cannot be used for managing identities in IAM.

**INCORRECT:** "Amazon Workspaces" is incorrect. Amazon WorkSpaces is a managed desktop computing service running on the AWS cloud.

**References:**

[https://aws.amazon.com/iam/](https://aws.amazon.com/iam/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 34:
What feature of Amazon S3 enables you to set rules to automatically transfer objects between different storage classes at defined time intervals?

*   Elastic Data Management
    
*   S3 Archiving   
*   Object Lifecycle Management   
    
    (Correct)
    
*   Auto Lifecycle Scaling   

#### Explanation

Object lifecycle management can be used with objects so that they are stored cost effectively throughout their lifecycle. Objects can be transitioned to another storage class or expired.

All other options are incorrect as they are not services that can automatically transfer objects between S3 storage classes.

**CORRECT:** "Object Lifecycle Management" is the correct answer.

**INCORRECT:** "Elastic Data Management" is incorrect as explained above.

**INCORRECT:** "Auto Lifecycle Scaling" is incorrect as explained above.

**INCORRECT:** "S3 Archiving" is incorrect as explained above.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 35:
Which type of Amazon RDS automated backup allows you to restore the database with a granularity of as little as 5 minutes?

*   Full backup   
*   Point-in-time recovery   
    
    (Correct)
    
*   Incremental backup   
*   Snapshot backup   

#### Explanation

You can restore an Amazon RDS database instance to a specific point in time with a granularity of 5 minutes. Amazon RDS uses transaction logs which it uploads to Amazon S3 to do this.

**CORRECT:** "Point-in-time recovery" is the correct answer.

**INCORRECT:** "Snapshot backup" is incorrect. This is not a point-in-time backup with 5 minute granularity.

**INCORRECT:** "Full backup" is incorrect. This just describes taking a fully backup of the database, typically with backup software.

**INCORRECT:** "Incremental backup" is incorrect. This describes taking a backup of items that have changed since the last backup.

**References:**

[https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER\_PIT.html](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PIT.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 36:
Which DynamoDB feature provides in-memory acceleration to tables that result in significant performance improvements?

*   Amazon CloudFront   
*   Amazon DynamoDB Accelerator (DAX)   
    
    (Correct)
    
*   Amazon EFS   
*   Amazon ElastiCache   

#### Explanation

Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement – from milliseconds to microseconds – even at millions of requests per second.

DAX does all the heavy lifting required to add in-memory acceleration to your DynamoDB tables, without requiring developers to manage cache invalidation, data population, or cluster management.

**CORRECT:** "Amazon DynamoDB Accelerator (DAX)" is the correct answer.

**INCORRECT:** "Amazon ElastiCache" is incorrect. This service is also an in-memory cache but it is not a feature of DynamoDB.

**INCORRECT:** "Amazon EFS" is incorrect. This is an elastic filesystem based on the NFS protocol.

**INCORRECT:** "Amazon CloudFront" is incorrect. This is a content delivery network for caching content.

**References:**

[https://aws.amazon.com/dynamodb/dax/](https://aws.amazon.com/dynamodb/dax/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 37:
With which service can a developer upload code using a ZIP or WAR file and have the service handle the end-to-end deployment of the resources?

*   AWS CodeCommit   
*   Amazon ECS   
*   AWS CodeDeploy   
*   AWS Elastic Beanstalk   
    
    (Correct)
    

#### Explanation

AWS Elastic Beanstalk can be used to quickly deploy and manage applications in the AWS Cloud. Developers upload applications and Elastic Beanstalk handles the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring.

You can upload code directly using a ZIP or WAR file. You can also use a Git archive.

**CORRECT:** "AWS Elastic Beanstalk" is the correct answer.

**INCORRECT:** "AWS CodeDeploy" is incorrect. AWS CodeDeploy is a fully managed deployment service that automates software deployments to a variety of compute services such as Amazon EC2, AWS Lambda, and on-premises servers.

**INCORRECT:** "Amazon ECS" is incorrect. Amazon Elastic Container Service is a managed service for running Docker containers.

**INCORRECT:** "AWS CodeCommit" is incorrect. AWS CodeCommit is a fully-managed source control service that hosts secure Git-based repositories. It does not actually automate the build of the code or infrastructure on which it runs.

**References:**

[https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/applications-sourcebundle.html](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/applications-sourcebundle.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 38:
Which of the following Amazon EC2 pricing models allows customers to use existing server-bound software licenses?

*   Reserved Instances
    
*   Dedicated Hosts
    
    (Correct)
    
*   On-Demand Instances
    
*   Spot Instances
    

#### Explanation

Amazon EC2 Dedicated Hosts allow you to use your eligible software licenses from vendors such as Microsoft and Oracle on Amazon EC2, so that you get the flexibility and cost effectiveness of using your own licenses, but with the resiliency, simplicity and elasticity of AWS. An Amazon EC2 Dedicated Host is a physical server fully dedicated for your use, so you can help address corporate compliance requirements.

**CORRECT:** "Dedicated Hosts" is the correct answer.

**INCORRECT:** "On-Demand Instances" is incorrect. This is a standard pricing model and does not offer the advantages requested.

**INCORRECT:** "Spot Instances" is incorrect. This is used to obtain discounted pricing for short-term requirements that can be interrupted.

**INCORRECT:** "Reserved Instances" is incorrect. This is used to lower cost by reserving usage of an instance for a term of 1 or 3 years.

**References:**

[https://aws.amazon.com/ec2/dedicated-hosts/](https://aws.amazon.com/ec2/dedicated-hosts/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 39:
Which AWS program can help an organization to design, build, and manage their workloads on AWS?

*   AWS Business Development Manager
    
*   APN Technology Consultants
    
*   AWS Technical Account Manager
    
*   APN Consulting Partners
    
    (Correct)
    

#### Explanation

APN Consulting Partners are professional services firms that help customers of all sizes design, architect, build, migrate, and manage their workloads and applications on AWS. Consulting Partners include System Integrators (SIs), Strategic Consultancies, Agencies, Managed Service Providers (MSPs), and Value-Added Resellers (VARs).

None of the other options are AWS Programs that can assist a customer with the design, build and management of their workloads.

**CORRECT:** "APN Consulting Partners" is the correct answer.

**INCORRECT:** "APN Technology Consultants" is incorrect as explained above.

**INCORRECT:** "AWS Business Development Manager" is incorrect as explained above.

**INCORRECT:** "AWS Technical Account Manager" is incorrect as explained above.

**References:**

[https://aws.amazon.com/partners/consulting/](https://aws.amazon.com/partners/consulting/)

Question 40:
Which service allows an organization to bring their own licensing on host hardware that is physically isolated from other AWS accounts?

*   EC2 Dedicated Instances
    
*   EC2 Spot Instances
    
*   EC2 Reserved Instances
    
*   EC2 Dedicated Hosts
    
    (Correct)
    

#### Explanation

An Amazon EC2 Dedicated Host is a physical server with EC2 instance capacity fully dedicated to your use. Dedicated Hosts allow you to use your existing per-socket, per-core, or per-VM software licenses, including Windows Server, Microsoft SQL Server, SUSE, Linux Enterprise Server, and so on.

**CORRECT:** "EC2 Dedicated Hosts" is the correct answer.

**INCORRECT:** "EC2 Dedicated Instances" is incorrect. Dedicated Instances are Amazon EC2 instances that run in a VPC on hardware that’s dedicated to a single customer. Bring your own licensing (BYOL) is not supported for dedicated instances.

**INCORRECT:** "EC2 Spot Instances" is incorrect. Spot instances allow you to bid in the marketplace for EC2 instances to reduce cost, they do not allow BYOL.

**INCORRECT:** "EC2 Reserved Instances" is incorrect. Reserved instances allow you to reduce on-demand price by up to 70% by committing to a 1- or 3-year term.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 41:
Which of the following are advantages of using the AWS cloud computing over legacy IT? (Select TWO.)   

*   You can bring new applications to market faster     
    
    (Correct)
    
*   You don't need to patch your operating systems   
*   You don't need to worry about over provisioning as you can elastically scale   
    
    (Correct)
    
*   You are able to pass responsibility for the availability of your application to AWS   
*   You can bring services closer to your end users   

#### Explanation

With cloud computing you no longer need to guess about capacity as you can elastically scale. This means you don’t end up overprovisioning but instead react to the load on your servers. You can also be faster and more agile with development and release of applications.

**CORRECT:** "You don't need to worry about over provisioning as you can elastically scale" is a correct answer.

**CORRECT:** "You can bring new applications to market faster" is also a correct answer.

**INCORRECT:** "You are able to pass responsibility for the availability of your application to AWS" is incorrect. You do not pass responsibility for your application to AWS. AWS runs the infrastructure but you still manage the application

**INCORRECT:** "You don't need to patch your operating systems" is incorrect. You still need to patch your own operating systems.

**INCORRECT:** "You can bring services closer to your end users" is incorrect. The cloud is centralized so you won’t necessarily bring services closer to your end users.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 42:
Which AWS support plan provides email only support by Cloud Support Associates?

*   Enterprise   
*   Developer   
    
    (Correct)
    
*   Basic
    
*   Business   

#### Explanation

Developer provides email support by the Cloud Support Associates team whereas Business and Enterprise provide email, 24×7 phone and chat access to Cloud Support Engineers. Basic does not provide email support at all.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_02-35-55-3f24edd0339b7631fb5b7a5ea7c6c70f.jpg)

**CORRECT:** "Developer" is the correct answer.

**INCORRECT:** "Basic" is incorrect as explained above.

**INCORRECT:** "Business" is incorrect as explained above.

**INCORRECT:** "Enterprise" is incorrect as explained above.

**References:**

[https://aws.amazon.com/premiumsupport/plans/](https://aws.amazon.com/premiumsupport/plans/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 43:
Which services allow you to store files on AWS? (Select TWO.)

*   AWS Lambda
    
*   Amazon LightSail
    
*   Amazon EBS
    
    (Correct)
    
*   Amazon SQS
    
*   Amazon EFS
    
    (Correct)
    

#### Explanation

You can store files on the Elastic Block Store (EBS), and Elastic File System (EFS). EBS volumes are mounted as block devices to EC2 instances and EFS volumes are mounted to the instance using the NFS protocol.

**CORRECT:** "Amazon EBS" is a correct answer.

**CORRECT:** "Amazon EFS" is also a correct answer.

**INCORRECT:** "AWS Lambda" is incorrect. AWS Lambda is a compute service for running code as functions.

**INCORRECT:** "Amazon LightSail" is incorrect. Amazon LightSail is a compute service for running instances.

**INCORRECT:** "Amazon SQS" is incorrect. Amazon Simple Queue Service (SQS) is a message bus for temporarily storing data that is being passed between application components.

**References:**

[https://aws.amazon.com/ebs/](https://aws.amazon.com/ebs/)

[https://aws.amazon.com/efs/](https://aws.amazon.com/efs/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 44:
A user deploys an Amazon Aurora database instance in multiple Availability Zones.

This strategy involves which pillar of the AWS Well-Architected Framework?

*   Performance efﬁciency
    
*   Cost optimization
    
*   Security
    
*   Reliability
    
    (Correct)
    

#### Explanation

The reliability pillar includes the ability of a system to recover from infrastructure or service disruptions, dynamically acquire computing resources to meet demand, and mitigate disruptions such as misconfigurations or transient network issues.

There are five design principles for reliability in the cloud:

• Test recovery procedures

• Automatically recover from failure

• Scale horizontally to increase aggregate system availability

• Stop guessing capacity

• Manage change in automation

The example given in the question is related to “Automatically recover from failure”.

**CORRECT:** "Reliability" is the correct answer.

**INCORRECT:** "Performance efﬁciency" is incorrect as this is an example of reliability.

**INCORRECT:** "Cost optimization" is incorrect as this is an example of reliability.

**INCORRECT:** "Security" is incorrect as this is an example of reliability.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 45:
Which support plan is the lowest cost option that allows unlimited cases to be open?

*   Basic
    
*   Enterprise
    
*   Developer
    
    (Correct)
    
*   Business
    

#### Explanation

With the Developer plan you can open unlimited cases. You can also open unlimited cases with the Business and Enterprise plans but these are more expensive. You cannot open any support cases with the basic support plan.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_03-02-52-581528b22e36a56928e874a36b0bceaa.jpg)

**CORRECT:** "Developer" is the correct answer.

**INCORRECT:** "Basic" is incorrect as explained above.

**INCORRECT:** "Business" is incorrect as explained above.

**INCORRECT:** "Enterprise" is incorrect as explained above.

**References:**

[https://aws.amazon.com/premiumsupport/plans/](https://aws.amazon.com/premiumsupport/plans/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 46:
What is the name of the online, self-service portal that AWS provides to enable customers to view reports and, such as PCI reports, and accept agreements?

*   AWS Compliance Portal   
*   AWS Artifact   
    
    (Correct)
    
*   AWS Documentation Portal   
*   AWS DocuFact   

#### Explanation

AWS Artifact is your go-to, central resource for compliance-related information that matters to you. It provides on-demand access to AWS’ security and compliance reports and select online agreements.

Reports available in AWS Artifact include our Service Organization Control (SOC) reports, Payment Card Industry (PCI) reports, and certifications from accreditation bodies across geographies and compliance verticals that validate the implementation and operating effectiveness of AWS security controls.

Agreements available in AWS Artifact include the Business Associate Addendum (BAA) and the Nondisclosure Agreement (NDA).

**CORRECT:** "AWS Artifact" is the correct answer.

**INCORRECT:** "AWS Compliance Portal" is incorrect as this is not a real service.

**INCORRECT:** "AWS Documentation Portal" is incorrect as this is not a real service.

**INCORRECT:** AWS DocuFact"" is incorrect as this is not a real service.

**References:**

[https://aws.amazon.com/artifact/](https://aws.amazon.com/artifact/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 47:
A developer needs a way to automatically provision a collection of AWS resources. Which AWS service is primarily used for deploying infrastructure as code?

*   AWS CodeDeploy   
*   AWS Elastic Beanstalk   
*   Jenkins   
*   AWS CloudFormation   
    
    (Correct)
    

#### Explanation

AWS CloudFormation is a service that gives developers and businesses an easy way to create a collection of related AWS resources and provision them in an orderly and predictable fashion. AWS CloudFormation provides a common language for you to describe and provision all the infrastructure resources in your cloud environment. Think of CloudFormation as deploying infrastructure as code.

**CORRECT:** "AWS CloudFormation" is the correct answer.

**INCORRECT:** "AWS Elastic Beanstalk" is incorrect. Elastic Beanstalk is more focused on deploying applications on EC2 (PaaS).

**INCORRECT:** "AWS CodeDeploy" is incorrect. AWS CodeDeploy is a fully managed deployment service that automates software deployments to a variety of compute services such as Amazon EC2, AWS Lambda, and your on-premises servers.

**INCORRECT:** "Jenkins" is incorrect. Jenkins is a Continuous Integration tool but is not an AWS service.

**References:**

[https://aws.amazon.com/cloudformation/](https://aws.amazon.com/cloudformation/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 48:
Which AWS service lets connected devices easily and securely interact with cloud applications and other devices?

*   AWS Server Migration Service (SMS)
    
*   Amazon Workspaces
    
*   AWS Directory Service   
*   AWS IoT Core   
    
    (Correct)
    

#### Explanation

AWS IoT Core is a managed cloud service that lets connected devices easily and securely interact with cloud applications and other devices. AWS IoT Core can support billions of devices and trillions of messages, and can process and route those messages to AWS endpoints and to other devices reliably and securely.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_03-22-15-e655703432d1a4d1da1880440a781b8f.jpg)

**CORRECT:** "AWS IoT Core" is the correct answer.

**INCORRECT:** "AWS Directory Service" is incorrect. AWS Directory Service for Microsoft Active Directory, also known as AWS Managed Microsoft AD, enables your directory-aware workloads and AWS resources to use managed Active Directory in the AWS Cloud

**INCORRECT:** "Amazon Workspaces" is incorrect. Amazon WorkSpaces is a managed, secure cloud desktop service

**INCORRECT:** "AWS Server Migration Service (SMS)" is incorrect. AWS Server Migration Service (SMS) is an agentless service which makes it easier and faster for you to migrate thousands of on-premises workloads to AWS.

**References:**

[https://aws.amazon.com/iot-core/](https://aws.amazon.com/iot-core/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 49:
Which service runs your application code only when needed without needing to run servers?

*   AWS LightSail
    
*   AWS Lambda
    
    (Correct)
    
*   Amazon ECS
    
*   Amazon EC2
    

#### Explanation

AWS Lambda is a serverless service that runs code as “functions”. That means that your code is run when needed but there are no servers running (at least not servers that you see or manage). This reduces cost and operational overhead.

**CORRECT:** "AWS Lambda" is the correct answer.

**INCORRECT:** "Amazon EC2" is incorrect. Amazon EC2 is used for running server instances so this is an incorrect answer.

**INCORRECT:** "Amazon ECS" is incorrect. Amazon ECS is used for running Docker containers which do need to run waiting for requests.

**INCORRECT:** "AWS LightSail" is incorrect. AWS LightSail is a service that is used for running virtual instances and databases using a simplified user interface for users who are less experienced with AWS (also at a much lower cost than EC2).

**References:**

[https://aws.amazon.com/lambda/](https://aws.amazon.com/lambda/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 50:
Which of the following must be used together to gain programmatic access to an AWS account? (Select TWO.)

*   A secondary key
    
*   A primary key
    
*   A user ID
    
*   A secret access key
    
    (Correct)
    
*   An access key ID
    
    (Correct)
    

#### Explanation

Access keys are long-term credentials for an IAM user or the AWS account root user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API (directly or using the AWS SDK).

Access keys consist of two parts: an access key ID (for example, AKIAIOSFODNN7EXAMPLE) and a secret access key (for example, wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY).

Like a user name and password, you must use both the access key ID and secret access key together to authenticate your requests. Manage your access keys as securely as you do your user name and password.

**CORRECT:** "An access key ID" is the correct answer.

**CORRECT:** "A secret access key" is the correct answer.

**INCORRECT:** "A primary key" is incorrect. Primary keys are not associated with authentication.

**INCORRECT:** "A user ID" is incorrect. A user ID is used to logon using the AWS Management Console, not programmatically.

**INCORRECT:** "A secondary key" is incorrect. Secondary keys are not associated with authentication.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 51:
A company has deployed several relational databases on Amazon RDS. Every month, the database software vendor releases new security patches that need to be applied to the database.

What is the MOST efficient way to apply the security patches?

*   Connect to each database instance on a monthly basis, and download and apply the necessary security patches from the vendor
    
*   Use AWS Systems Manager to automate database patching according to a schedule
    
*   Enable automatic patching for the instances using the Amazon RDS console
    
    (Correct)
    
*   In AWS Config, conﬁgure a rule for the instances and the required patch level
    

#### Explanation

Periodically, Amazon RDS performs maintenance on Amazon RDS resources. Maintenance most often involves updates to the DB instance's underlying hardware, underlying operating system (OS), or database engine version. Updates to the operating system most often occur for security issues and should be done as soon as possible.

Required patching is automatically scheduled only for patches that are related to security and instance reliability. Such patching occurs infrequently (typically once every few months) and seldom requires more than a fraction of your maintenance window.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-07_22-12-48-085343f971a3813c0c8b32d30fdad40f.JPG)

All you need to do to get enable patching is specify the maintenance window in which the patching will take place. This can be done at instance creation time or at any time afterwards.

**CORRECT:** "Enable automatic patching for the instances using the Amazon RDS console" is the correct answer.

**INCORRECT:** "Connect to each database instance on a monthly basis, and download and apply the necessary security patches from the vendor" is incorrect. Amazon RDS is a managed service and you do not need to do this manually.

**INCORRECT:** "In AWS Config, conﬁgure a rule for the instances and the required patch level" is incorrect. This service is used for auditing and evaluating resource configurations.

**INCORRECT:** "Use AWS Systems Manager to automate database patching according to a schedule" is incorrect. Systems Manager can be used to manage EC2 instances but it cannot be used to patch RDS instances.

**References:**

[https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER\_UpgradeDBInstance.Maintenance.html](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_UpgradeDBInstance.Maintenance.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 52:
Which AWS service can be used to send automated notifications to HTTP endpoints?

*   Amazon SWF   
*   Amazon SNS   
    
    (Correct)
    
*   Amazon SQS   
*   Amazon SES   

#### Explanation

Amazon Simple Notification Service (Amazon SNS) is a web service that makes it easy to set up, operate, and send notifications from the cloud. SNS can be used to send automated or manual notifications to email, mobile (SMS), SQS, and HTTP endpoints.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_03-04-16-c61257a0368e763e4a2e5a07189b973f.jpg)

**CORRECT:** "Amazon SNS" is the correct answer.

**INCORRECT:** "Amazon SQS" is incorrect. Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. This is a message bus, not a notification service.

**INCORRECT:** "Amazon SWF" is incorrect. Amazon SWF helps developers build, run, and scale background jobs that have parallel or sequential step. It is not a notification service.

**INCORRECT:** "Amazon SES" is incorrect. Amazon Simple Email Service (Amazon SES) is a cloud-based email sending service designed to help digital marketers and application developers send marketing, notification, and transactional emails. It is limited to sending email.

**References:**

[https://aws.amazon.com/sns/](https://aws.amazon.com/sns/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-application-integration/](https://digitalcloud.training/aws-application-integration/)

Question 53:
Which type of EBS volumes can be encrypted?

*   Only non-root volumes created from snapshots   
*   Only root volumes can have encryption applied at launch time   
*   Both non-root and root volumes
    
    (Correct)
    
*   Non-root volumes only   

#### Explanation

Amazon EBS encryption offers a straight-forward encryption solution for your EBS resources that doesn't require you to build, maintain, and secure your own key management infrastructure. It uses AWS Key Management Service (AWS KMS) customer master keys (CMK) when creating encrypted volumes and snapshots.

Encryption operations occur on the servers that host EC2 instances, ensuring the security of both data-at-rest and data-in-transit between an instance and its attached EBS storage.

All volumes can now be encrypted at launch time and it’s possible to set this as the default setting.

**CORRECT:** "Both non-root and root volumes" is the correct answer.

**INCORRECT:** "Non-root volumes only" is incorrect as this is not true.

**INCORRECT:** "Only non-root volumes created from snapshots" is incorrect as you can encrypt all EBS volumes whether created from snapshots or not.

**INCORRECT:** "Only root volumes can have encryption applied at launch time" is incorrect as all volumes can have encryption applied at launch time.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 54:
Under the AWS Shared Responsibility Model, which of the following is the customer NOT responsible for?

*   Applying encryption to data stored on an EBS volume   
*   Applying bucket policies to share Amazon S3 data   
*   Installing firmware updates on host servers   
    
    (Correct)
    
*   Adding firewall rules to security groups and network ACLs   

#### Explanation

AWS customers are not responsible for installing firmware updates on the underlying infrastructure. AWS customers must protect their AWS services through policies, encryption, and firewall rules.

**CORRECT:** "Installing firmware updates on host servers" is the correct answer.

**INCORRECT:** "Adding firewall rules to security groups and network ACLs" is incorrect as this is a customer responsibility.

**INCORRECT:** "Applying encryption to data stored on an EBS volume" is incorrect as this is a customer responsibility.

**INCORRECT:** "Applying bucket policies to share Amazon S3 data" is incorrect as this is a customer responsibility.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 55:
Which of the following would be good reasons to move from on-premises to the AWS Cloud? (Select TWO.)

*   Gain end-to-end operational management of the entire infrastructure stack
    
*   Reduce costs through easier right-sizing of workloads
    
    (Correct)
    
*   Outsource all security responsibility
    
*   Improve agility and elasticity
    
    (Correct)
    
*   Gain access to free technical support services
    

#### Explanation

There are many benefits to moving to the AWS Cloud and these include reducing costs through right-sizing workloads. This is easier with elastic computing and the ability to easily adjust workloads, monitor utilization and programmatically make changes. You can improve agility and elasticity through services such as Auto Scaling, Elastic Load Balancing and highly scalable services such as S3 and Lambda.

**CORRECT:** "Reduce costs through easier right-sizing of workloads" is a correct answer.

**CORRECT:** "Improve agility and elasticity" is also a correct answer.

**INCORRECT:** "Gain access to free technical support services" is incorrect. You do not get free technical support services with AWS.

**INCORRECT:** "Gain end-to-end operational management of the entire infrastructure stack" is incorrect. You do not gain end-to-end operational management of your entire infrastructure stack. AWS manage the infrastructure and, for some services, the application too.

**INCORRECT:** "Outsource all security responsibility" is incorrect. You do not outsource all security responsibility with AWS – you are still responsible for ensuring the security of your applications, users, and data.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 56:
A Cloud Practitioner is developing a disaster recovery plan and intends to replicate data between multiple geographic areas.

Which of the following meets these requirements?

*   Edge locations
    
*   Availability Zones
    
*   AWS Accounts
    
*   AWS Regions
    
    (Correct)
    

#### Explanation

AWS has the concept of a Region, which is a physical location around the world where we cluster data centers. We call each group of logical data centers an Availability Zone. Each AWS Region consists of multiple, isolated, and physically separate AZ's within a geographic area.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-54-55-d3535bc0bf76aee9cfc0d80cc1c91af6.png)

Therefore, the Cloud Practitioner should replicate data between multiple Regions as these are separate geographical areas.

**CORRECT:** "AWS Regions" is the correct answer.

**INCORRECT:** "AWS Accounts" is incorrect. An account is not a geographic area.

**INCORRECT:** "Availability Zones" is incorrect. AZs are within a Region, not across geographical areas.

**INCORRECT:** "Edge locations" is incorrect. These are not locations to which you can replicate your data. They are used primarily by Amazon CloudFront for caching content, not for disaster recovery.

**References:**

[https://aws.amazon.com/about-aws/global-infrastructure/regions\_az/](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-global-infrastructure/](https://digitalcloud.training/aws-global-infrastructure/)

Question 57:
What is the name of the AWS managed Docker registry service used by the Amazon Elastic Container Service (ECS)?   

*   ECS Container Registry   
*   Docker Image Repository   
*   Elastic Container Registry   
    
    (Correct)
    
*   Docker Container Registry   

#### Explanation

Amazon Elastic Container Registry (ECR) is a fully-managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images.

Amazon ECR is integrated with Amazon Elastic Container Service (ECS). Amazon ECR eliminates the need to operate your own container repositories or worry about scaling the underlying infrastructure.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_03-01-49-a6bffbd73d607a63067aedde8e716ca8.jpg)

**CORRECT:** "Elastic Container Registry" is the correct answer.

**INCORRECT:** "ECS Container Registry" is incorrect as this is the wrong name.

**INCORRECT:** "Docker Container Registry" is incorrect as this is not an AWS registry.

**INCORRECT:** "Docker Image Repository" is incorrect as this is not an AWS registry.

**References:**

[https://aws.amazon.com/ecr/](https://aws.amazon.com/ecr/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 58:
A cloud practitioner needs to decrease application latency and increase performance for globally distributed users.

Which services can assist? (Select TWO.)

*   Amazon S3
    
    (Correct)
    
*   Amazon ECS
    
*   Amazon CloudFront
    
    (Correct)
    
*   Amazon AppStream 2.0
    
*   Amazon ElastiCache
    

#### Explanation

Amazon S3 is an object-based storage system. It can be used to store data such as files and images that need to be served. Optionally, an S3 bucket can be configured as a static website. Amazon CloudFront is a content delivery network (CDN) that caches content at Edge Locations around the world.

These two services can work together with an S3 bucket configured as an origin for the CloudFront distribution. Users around the world will then be able to pull the content from the local Edge Location with lower latency and better performance.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-55-54-ee622fd30b47649e15d2344baffd6e36.png)

**CORRECT:** "Amazon S3" is a correct answer.

**CORRECT:** "Amazon CloudFront" is also a correct answer.

**INCORRECT:** "Amazon ECS" is incorrect. The Elastic Container Service (ECS) is used for running Docker containers on AWS. This is not going to help with reducing latency or increasing performance for global users.

**INCORRECT:** "Amazon AppStream 2.0" is incorrect. This is an application streaming service for streaming applications to computers. It is unsuitable for these requirements.

**INCORRECT:** "Amazon ElastiCache" is incorrect. ElastiCache caches data from a database in-memory. It is unsuitable for these requirements.

**References:**

[https://aws.amazon.com/cloudfront/](https://aws.amazon.com/cloudfront/)

[https://aws.amazon.com/s3/](https://aws.amazon.com/s3/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-content-delivery-and-dns-services/](https://digitalcloud.training/aws-content-delivery-and-dns-services/)

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 59:
What are two correct statements about AWS Organizations with consolidated billing? (Select TWO.)

*   One bill provided for multiple accounts   
    
    (Correct)
    
*   Multiple bills are provided per organization   
*   CloudTrail can be configured per organization   
*   Linked accounts lose their management independence   
*   Volume pricing discounts applied across multiple accounts   
    
    (Correct)
    

#### Explanation

With AWS organizations you create a paying account and linked accounts. One bill is provided for multiple accounts within an organization. Volume pricing discounts can be applied across resources in multiple accounts.

**CORRECT:** "One bill provided for multiple accounts" is a correct answer.

**CORRECT:** "Volume pricing discounts applied across multiple accounts" is also a correct answer.

**INCORRECT:** "Multiple bills are provided per organization" is incorrect as one bill is provided for multiple accounts within an organization.

**INCORRECT:** "Linked accounts lose their management independence" is incorrect. Linked accounts can still be managed independently.

**INCORRECT:** "CloudTrail can be configured per organization" is incorrect. CloudTrail is on a per account basis and per region basis but can be aggregated into a single bucket in the paying account.

**References:**

[https://aws.amazon.com/organizations/](https://aws.amazon.com/organizations/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 60:
Which of the below is an example of optimizing for cost?

*   Choosing the fastest EC2 instance to ensure performance
    
*   Provision extra capacity to allow for growth
    
*   Replace an EC2 compute instance with AWS Lambda
    
    (Correct)
    
*   Deploy resources with AWS CloudFormation
    

#### Explanation

Where possible, you should replace EC2 workloads with AWS managed services that don’t require you to take any capacity decisions. AWS Lambda is a serverless services and you only pay for actual processing time. Other examples of services that you don’t need to make capacity decisions with include: ELB, CloudFront, SQS, Kinesis Firehose, SES, and CloudSearch.

**CORRECT:** "Replace an EC2 compute instance with AWS Lambda" is the correct answer.

**INCORRECT:** "Choosing the fastest EC2 instance to ensure performance" is incorrect. You should not choose the fastest EC2 instance if you’re trying to optimize for cost as this will be expensive, you should right-size your EC2 instances, so you use the cheapest EC2 instance to suit your workload’s requirements.

**INCORRECT:** "Provision extra capacity to allow for growth" is incorrect. Provisioning extra capacity for growth is not an example of cost optimization. With cloud computing you no longer need to do this as you can configure applications, databases and storage systems to grow on demand.

**INCORRECT:** "Deploy resources with AWS CloudFormation" is incorrect. Deploying resources with CloudFormation is great for consistently deploying application configurations from a template. However, this is not an example of cost optimization, it is more an example of operational optimization.

**References:**

[https://aws.amazon.com/aws-cost-management/](https://aws.amazon.com/aws-cost-management/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 61:
How can you configure Amazon Route 53 to monitor the health and performance of your application?

*   Using the Route 53 API   
*   Using CloudWatch   
*   Using Route 53 health checks   
    
    (Correct)
    
*   Using DNS lookups   

#### Explanation

Amazon Route 53 health checks monitor the health and performance of your web applications, web servers, and other resources.

None of the other options provide a solution that can check the health and performance of an application.

**CORRECT:** "Using Route 53 health checks" is the correct answer.

**INCORRECT:** "Using DNS lookups" is incorrect as explained above.

**INCORRECT:** "Using the Route 53 API" is incorrect as explained above.

**INCORRECT:** "Using CloudWatch" is incorrect as explained above.

**References:**

[https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover.html](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-content-delivery-and-dns-services/](https://digitalcloud.training/aws-content-delivery-and-dns-services/)

Question 62:
How can an online education company ensure their video courses play with minimal latency for their users around the world?

*   Use Amazon CloudFront to get the content closer to users
    
    (Correct)
    
*   Use Amazon EBS Cross Region Replication to get the content close to the users
    
*   Use Amazon Aurora Global Database
    
*   Use Amazon S3 Transfer Acceleration to speed up downloads
    

#### Explanation

Amazon CloudFront is a content delivery network (CDN) that enables you to cache content in Edge Locations that are located around the world. This brings your media closer to your end users which reduces latency and improves the user experience.

**CORRECT:** "Use Amazon CloudFront to get the content closer to users" is the correct answer.

**INCORRECT:** "Use Amazon S3 Transfer Acceleration to speed up downloads" is incorrect. Amazon S3 Transfer Acceleration is a feature that is used for accelerating uploads to Amazon S3, not for downloads.

**INCORRECT:** "Use Amazon EBS Cross Region Replication to get the content close to the users" is incorrect. Amazon EBS Cross Region Replication does not exist (S3 Cross Region Replication does). You can copy EBS volumes across regions manually (or programmatically), however EBS is not a good way to get your content closer to your users as you would need to mount the volume to an EC2 instance (additional cost) and would also need to find a way to keep your files in sync.

**INCORRECT:** "Use Amazon Aurora Global Database" is incorrect. Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS regions. This is a way to have an SQL database across regions, which is not a good use case for hosting media files.

**References:**

[https://aws.amazon.com/cloudfront/](https://aws.amazon.com/cloudfront/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-content-delivery-and-dns-services/](https://digitalcloud.training/aws-content-delivery-and-dns-services/)

Question 63:
Which service is used for caching data?

*   Amazon DynamoDB DAX
    
    (Correct)
    
*   Amazon Simple Queue Service (SQS)
    
*   AWS Key Management Service (KMS)
    
*   Amazon Elastic File System (EFS)
    

#### Explanation

Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement – from milliseconds to microseconds – even at millions of requests per second.

**CORRECT:** "Amazon DynamoDB DAX" is the correct answer.

**INCORRECT:** "Amazon Simple Queue Service (SQS)" is incorrect. Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

**INCORRECT:** "Amazon Key Management Service (KMS)" is incorrect. AWS Key Management Service (KMS) makes it easy for you to create and manage keys and control the use of encryption across a wide range of AWS services and in your applications.

**INCORRECT:** "Amazon Elastic File System (EFS)" is incorrect. Amazon Elastic File System (Amazon EFS) provides a simple, scalable, elastic file system for Linux-based workloads for use with AWS Cloud services and on-premises resources.

**References:**

[https://aws.amazon.com/dynamodb/dax/](https://aws.amazon.com/dynamodb/dax/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 64:
Which AWS service can assist with providing recommended actions on cost optimization?

*   Amazon CloudWatch Events
    
*   AWS Artifact
    
*   AWS Inspector
    
*   AWS Trusted Advisor
    
    (Correct)
    

#### Explanation

Trusted Advisor is an online resource that helps to reduce cost, increase performance and improve security by optimizing your AWS environment.

**CORRECT:** "AWS Trusted Advisor" is the correct answer.

**INCORRECT:** "AWS Inspector" is incorrect. Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS.

**INCORRECT:** "AWS Artifact" is incorrect. AWS Artifact is a resource for obtaining compliance-related information.

**INCORRECT:** "Amazon CloudWatch Events" is incorrect. Amazon CloudWatch Events delivers a near real-time stream of system events that describe changes in Amazon Web Services (AWS) resources.

**References:**

[https://aws.amazon.com/premiumsupport/technology/trusted-advisor/](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 65:
Which AWS services form the app-facing services of the AWS serverless infrastructure? (Select TWO.)

*   AWS Lambda   
    
    (Correct)
    
*   Amazon DynamoDB   
*   Amazon API Gateway   
    
    (Correct)
    
*   AWS Step Functions     
*   Amazon EFS   

#### Explanation

AWS Lambda and Amazon API Gateway are both app-facing components of the AWS Serverless infrastructure

AWS Step Functions is an orchestration service

**CORRECT:** "AWS Lambda" is a correct answer.

**CORRECT:** "Amazon API Gateway" is also a correct answer.

**INCORRECT:** "AWS Step Functions" is incorrect. This is a serverless orchestration service.

**INCORRECT:** "Amazon DynamoDB" is incorrect. Amazon DynamoDB is a serverless database service. Databases are backend, not app-facing.

**INCORRECT:** "Amazon EFS" is incorrect. EFS is a filesystem. Typically, EFS is mounted by Amazon EC2 instances.

**References:**

[https://aws.amazon.com/serverless/](https://aws.amazon.com/serverless/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Continue

Retake test

Settings

*   Report abuse
    

Fullscreen