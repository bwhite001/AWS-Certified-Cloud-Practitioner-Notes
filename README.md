AWS Certified Cloud Practitioner
================================

The 5 Pillars of the AWS Well-Architected Framework
---------------------------------------------------

1.  Operational Excellence The Operational Excellence pillar includes the ability to support development and run workloads effectively, gain insight into their operation, and continuously improve supporting processes and procedures to delivery business value. You can find prescriptive guidance on implementation in the Operational Excellence Pillar whitepaper.
    
    Design Principles There are five design principles for operational excellence in the cloud:
    
    1.  Perform operations as code
    2.  Make frequent, small, reversible changes
    3.  Refine operations procedures frequently
    4.  Anticipate failure
    5.  Learn from all operational failures
    
    Best Practices Operations teams need to understand their business and customer needs so they can support business outcomes. Ops creates and uses procedures to respond to operational events, and validates their effectiveness to support business needs. Ops also collects metrics that are used to measure the achievement of desired business outcomes.
    
    Everything continues to change—your business context, business priorities, customer needs, etc. It’s important to design operations to support evolution over time in response to change and to incorporate lessons learned through their performance.
    
2.  Security The Security pillar includes the ability to protect data, systems, and assets to take advantage of cloud technologies to improve your security. You can find prescriptive guidance on implementation in the Security Pillar white-paper.
    
    Design Principles There are seven design principles for security in the cloud:
    
    1.  Implement a strong identity foundation
    2.  Enable traceability
    3.  Apply security at all layers
    4.  Automate security best practices
    5.  Protect data in transit and at rest
    6.  Keep people away from data
    7.  Prepare for security events
    
    Best Practices Before you architect any workload, you need to put in place practices that influence security. You’ll want to control who can do what. In addition, you want to be able to identify security incidents, protect your systems and services, and maintain the confidentiality and integrity of data through data protection.
    
    You should have a well-defined and practiced process for responding to security incidents. These tools and techniques are important because they support objectives such as preventing financial loss or complying with regulatory obligations.
    
    The AWS Shared Responsibility Model enables organisations that adopt the cloud to achieve their security and compliance goals. Because AWS physically secures the infrastructure that supports our cloud services, as an AWS customer you can focus on using services to accomplish your goals. The AWS Cloud also provides greater access to security data and an automated approach to responding to security events.
    
3.  Reliability The Reliability pillar encompasses the ability of a workload to perform its intended function correctly and consistently when it’s expected to. This includes the ability to operate and test the workload through its total lifecycle. You can find prescriptive guidance on implementation in the Reliability Pillar white-paper.
    
    Design Principles There are five design principles for reliability in the cloud:
    
    1.  Automatically recover from failure
    2.  Test recovery procedures
    3.  Scale horizontally to increase aggregate workload availability
    4.  Stop guessing capacity
    5.  Manage change in automation
    
    Best Practices To achieve reliability, you must start with the foundations—an environment where service quotas and network topology accommodate the workload. The workload architecture of the distributed system must be designed to prevent and mitigate failures. The workload must handle changes in demand or requirements, and it must be designed to detect failure and automatically heal itself.
    
    Before architecting any system, foundational requirements that influence reliability should be in place. For example, you must have sufficient network bandwidth to your data center. These requirements are sometimes neglected (because they are beyond a single project’s scope).
    
    This neglect can have a significant impact on the ability to deliver a reliable system. In an on-premises environment, these requirements can cause long lead times due to dependencies and therefore must be incorporated during initial planning.
    
    With AWS, most of these foundational requirements are already incorporated or may be addressed as needed. The cloud is designed to be essentially limitless, so it is the responsibility of AWS to satisfy the requirement for sufficient networking and compute capacity, while you are free to change resource size and allocation, such as the size of storage devices, on demand.
    
4.  Performance Efficiency The Performance Efficiency pillar includes the ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve. You can find prescriptive guidance on implementation in the Performance Efficiency Pillar whitepaper.
    
    Design Principles There are five design principles for performance efficiency in the cloud:
    
    1.  Democratize advanced technologies
    2.  Go global in minutes
    3.  Use serverless architectures
    4.  Experiment more often
    5.  Consider mechanical sympathy
    
    Best Practices Take a data-driven approach to building a high-performance architecture. Gather data on all aspects of the architecture, from the high-level design to the selection and configuration of resource types.
    
    Reviewing your choices on a regular basis ensures you are taking advantage of the continually evolving AWS Cloud. Monitoring ensures you are aware of any deviance from expected performance. Make trade-offs in your architecture to improve performance, such as using compression or caching, or relaxing consistency requirements
    
    The optimal solution for a particular workload varies, and solutions often combine multiple approaches. Well-Architected workloads use multiple solutions and enable different features to improve performance
    
5.  Cost Optimisation
    
    The Cost Optimisation pillar includes the ability to run systems to deliver business value at the lowest price point. You can find prescriptive guidance on implementation in the Cost Optimisation Pillar white-paper.
    
    Design Principles There are five design principles for cost optimisation in the cloud:
    
    1.  Implement cloud financial management
    2.  Adopt a consumption model
    3.  Measure overall efficiency
    4.  Stop spending money on undifferentiated heavy lifting
    5.  Analyse and attribute expenditure
    
    Best Practices As with the other pillars, there are trade-offs to consider. For example, do you want to optimize for speed to market or for cost? In some cases, it’s best to optimize for speed—going to market quickly, shipping new features, or simply meeting a deadline—rather than investing in up-front cost optimisation.
    
    Design decisions are sometimes directed by haste rather than data, and as the temptation always exists to overcompensate rather than spend time benchmarking for the most cost-optimal deployment. This might lead to over-provisioned and under-optimised deployments.
    
    Using the appropriate services, resources, and configurations for your workloads is key to cost savings
    

*   Billing (CloudWatch)
    
    *   CloudWatch - To setup Billing alarm (Use the Create Alarm underneath one)
*   Identity Access Management (IAM)
    

Summary:

1.  It is Global, you do not specify a region when dealing with IAM. When you create a user or group, this is created GLOBALLY.
    
2.  Your root account is the email address you used to set up your AWS account. The root account always has full administrator access. You should not give these account credentials away to anyone. Instead create a user for each individual within your organisation. You should always secure this root account using multi-factor authentication.
    
3.  A group is simply a place to store your users. Your users will inherit all permission that the group has. Examples of groups might be developers, sys admins, HR, finance...etc
    
4.  To set the permissions in a group you need to apply a policy to that group. Policies consist of Java Script Object Notation (or JSON). These are referred to as key value pairs. You have your key, such as name and then the value. Example: {"name" : "A Cloud Guru" }
    
    *   Allows to create users, groups and access
        *   Delete your root access keys / Rotate your access keys
        *   Activate MFA on your account
            *   Manage MFA (root user is the email that we used to sign-up) - Click on Activate MFA (Virtual MFA (Authenticator App), U2F security key (YubiKey) and other h/w MFA device)
        *   Create Individual IAM users
            *   Add a user (3 ways: Programmatic access, AWS Management Console access and Amazon SDK)
            *   Create a Group (3 ways: Add user to group, Copy Permission from existing user and Attach existing policies directly)
            *   AWS managed have AWS icon and we can view the policy in JSON
            *   Secret access key and password are shown only once when the user is created.
        *   Use groups to assign permissions
        *   Apply an IAM password policy

*   S3 101 (Simple Storage Service)
    
    *   S3 is object based - i.e. allows you to upload files. Think of Objects just as files. Objects consists of the following OR The key fundamentals of S3 are: - Key (this is simply the name of the object)
        
        *   Value (this is simply the data and is made of a sequence of bytes)
        *   Version ID (important for versioning)
        *   Metadata (Data about data you are storing)
        *   Subresources:
            *   Access Control Lists
            *   Torrent
    *   Files can be from 0 Bytes to 5 TB
        
    *   There is unlimited storage
        
    *   Files are stored in Buckets (Bucket is like a folder in the cloud)
        
    *   S3 is a universal namespace. That is, names must be unique globally. Example: [https://s3-eu-west-1.amazonaws.com/acloudguru](https://s3-eu-west-1.amazonaws.com/acloudguru)
        
    *   When you upload a file to S3, you will receive a HTTP 200 code if the upload was successful.
        
    
    How does data consistency work for S3? - Read after Write consistency for PUTS of new objects (if you write a new file and read it immediately afterwards, you will be able to view the data) - Eventual Consistency for overwrite PUTS and DELETES (can take sometime to propagate) (If you update AN EXISTING file or delete a file and read it immediately, you may get the older version, or you may not. Basically changes to objects can take a little bit of time to propagate.)
    
    S3 - Guarantees S3 has the following guarantees from Amazon:
    
    *   Built for 99.99% availability for the S3 platform
    *   Amazon guarantees 99.9% availability
    *   Amazon guarantees 99.99999999999% durability for S3 information (Remember 11 9's)
    
    S3 - Features S3 has the following features
    
    *   Tiered Storage Available
    *   Lifecycle Management: Move objects around to two different storage tiers
    *   Versioning
    *   Encryption
    *   MFA Delete: use MFA when deleting the files
    *   Secure your data using Access Control Lists (File level) or Bucket Policies (Bucket level)
    
    S3 Storage Classes
    
    1.  S3 Standard: 99.99% availability, 99.99999999999% durability stored redundantly across multiple devices in multiple facilities and is designed to sustain the loss of 2 facilities concurrently.
    2.  S3 - IA (Infrequently Accessed): For the data that is accessed less frequently, but requires rapid access when needed. Lower fee than S3, but you are charged a retrieval fee.
    3.  S3 One Zone IA: For where you want a lower-cost option for infrequently accessed data, but do not require the multiple availability zone data resilience.
    4.  S3 - Intelligent Tiering: Designed to optimise costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead.
    5.  S3 Glacier: S3 Glacier is a secure, durable and low-cost storage class for data archiving. You can reliably store any amount of data at costs that are competitive with or cheaper than on-premises solutions. Retrieval times are configurable from minutes to hours.
    6.  S3 Glacier Deep Archive: S3 Glacier Deep Archive is Amazon's lowest-cost storage class where a retrieval time of 12 hours is acceptable.
    
    S3 Charges: You are charged for S3 in the following ways:
    
    1.  Storage
    2.  Requests
    3.  Storage Management Pricing
    4.  Data Transfer Pricing
    5.  Transfer Acceleration
    6.  Cross Region Replication Pricing
    
    S3 Transfer Acceleration
    
    1.  Amazon S3 Transfer Acceleration enables fast, easy and secure transfers of files over long distances between your end users and an S3 bucket.
    2.  Transfer Acceleration takes advantage of Amazon CloudFront's globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimised network path.
    
    S3 Exam Tips:
    
    1.  Remember that S3 is Object-based: i.e allows you to upload files.
    2.  Files can be 0 Bytes to 5 TB.
    3.  There is unlimited storage.
    4.  Files are stored in Buckets.
    5.  S3 is a universal namespace. That is, names must be unique globally. Example: [https://s3-eu-west-1.amazonaws.com/acloudguru](https://s3-eu-west-1.amazonaws.com/acloudguru)
    6.  Not suitable to install operating systems on S3 due to it being object based (not block storage - EBS), can only be used to store files
    7.  Successful upload will generate a HTTP 200 status code.
    8.  You can turn on MFA delete to avoid accidental delete.
    9.  The key fundamentals of S3 are:
        *   Key (This is simply the name of the object)
        *   Value (This is simply the data and is made up of a sequence of bytes).
    10.  S3 Model:
        *   Read after Write consistency for PUTS of new objects (if you write a new files and read it immediately afterwards, you will be able to view the data)
        *   Eventual Consistency for overwrite PUTS and DELETES (can take sometime to propagate) (If you update AN EXISTING file or delete a file and read it immediately, you may get the older version, or you may not. Basically changes to objects can take a little bit of time to propagate.)
    11.  S3 Storage Classes
        1.  S3 Standard: 99.99% availability, 99.99999999999% durability stored redundantly across multiple devices in multiple facilities and is designed to sustain the loss of 2 facilities concurrently.
        2.  S3 - IA (Infrequently Accessed): 99.9% availability, For the data that is accessed less frequently, but requires rapid access when needed. Lower fee than S3, but you are charged a retrieval fee.
        3.  S3 - Intelligent Tiering: 99.9% availability, Designed to optimise costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead.
        4.  S3 One Zone IA (also called S3 RRS): 99.5% availability, For where you want a lower-cost option for infrequently accessed data, but do not require the multiple availability zone data resilience.
        5.  S3 Glacier: S3 Glacier is a secure, durable and low-cost storage class for data archiving. You can reliably store any amount of data at costs that are competitive with or cheaper than on-premises solutions. Retrieval times are configurable from minutes to hours.
        6.  S3 Glacier Deep Archive: S3 Glacier Deep Archive is Amazon's lowest-cost storage class where a retrieval time of 12 hours is acceptable.
        7.  S3 Outposts for on-premises object storage to meet data residency needs
    
    S3 Bucket Exam Tips: 12. Bucket names share a common name space, you can't have the same bucket name as the others. 13. When you view Buckets you view them globally but you can have buckets in individual regions 14. We can use cross region replication to replicate buckets automatically to different regions. 15. We can change storage class and encryption on the fly. 16. Transfer acceleration 17. Restricting Bucket Access: 1. Bucket Policies - Applies across the bucket. 2. Object Policies - Applies to individual files. 3. IAM Policies to Users & Groups - Applies to Users & Groups. 18. By default Buckets are not public. 19. You can use bucket policies to make entire S3 buckets public. 20. You can use S3 bucket to host static websites but can't host dynamic websites or websites which require database, for ex: Wordpress...etc.
    
*   CloudFront CloudFront is a content delivery network (CDN) is a system of distributed servers (network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage and a content delivery server.
    
    CloudFront - Key Terminology:
    
    1.  Edge location: This is the location where content will be cached. This is separate to an AWS Region/AZ.
    2.  Origin - This is the origin of all the files that the CDN will distribute. This can be an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route 53.
    3.  Distribution - This is the name given the CDN which consists of a collection of Edge locations.
    
    When the first user queries for a file, it gets downloaded from the server. The second user gets a cached copy from the Edge Location instead of downloading it again from the server. The file has Time to live defined usually 48 hours.
    
    2 types of distribution: Web Distribution - Typically used for Websites RTMP - Used for Media Streaming
    
*   CloudFront Exam Tips
    
    1.  Edge location: This is the location where content will be cached. This is separate to an AWS Region/AZ.
    2.  Origin - This is the origin of all the files that the CDN will distribute. This can be an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route 53.
    3.  Distribution - This is the name given the CDN which consists of a collection of Edge locations.
    
    2 types of distribution: Web Distribution - Typically used for Websites RTMP - Used for Media Streaming
    
    Note:
    
    1.  Edge Locations are not just READ only - you can write them too. (ie Put an object on to them).
    2.  Objects are cached for the life of TTL (Time to live)
    3.  You can clear cached objects, but you will be charged.
*   EC2 101 Elastic Compute Cloud
    
    1.  Amazon Elastic Compute Cloud (Amazon EC2) is just a virtual server (or servers) in the cloud
    2.  Amazon EC2 reduces the time required to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requirements change.
    
    EC2 Pricing Models:
    
    1.  On Demand: Allows you to pay a fixed rate by the hour (or by the second) with no commitment.
    2.  Reserved: Provides you with a capacity reservation, and offer significant discount on the hourly charge for an instance. Contracts are 1 - 3 year terms. Higher discount with upfront payments and longer contracts.
    3.  Spot: Enables you to bid whatever price you want for instance capacity, providing for even greater savings if your applications have flexible start and end times.
    4.  Dedicated Hosts: Physical EC2 server dedicated for your use. Dedicated hosts can help reduce the costs by allowing you to use your existing server-bound software licenses.

\*EC2 Exam Tips: 1. EC2 is a compute based service. It is not server less. It's a Server! 2. Use a private key to connect to EC2. 3. Common Ports: Linux (port 22), Microsoft - RDP (port 3389), HTTP (80) and HTTPS (443) 4. Security groups are virtual firewalls. To let everything in 0.0.0.0/0. To let a single IP address in X.X.X.X/32 (32 means this ip address) 5. Always design for failure. Have one EC2 instance in each availability zone.

\*Using the command line: Exam Tips: 1. You can interact with AWS in 3 different ways a. Using the console b. Using the command line interface (CLI) c. Using the SDK's

\*Using Roles: Exam Tips 1. Roles are much more secure than using access key id's and secret access keys and are easier to manage. 2. Adding/Modifying policies to roles are instantaneous. You can apply roles to EC2 instances anytime. When you do this, the change takes place immediately. 3. Roles are universal. You do not need to specify what region they are in, similar to users.

*   Build a web server: Logon to AWS chmod 400 SriAWS.pem onnect to your instance using its Public DNS: c2-100-26-17-63.compute-1.amazonaws.com Example: ssh -i "SriAWS.pem" [ec2-user@ec2-100-26-17-63.compute-1.amazonaws.com](mailto:ec2-user@ec2-100-26-17-63.compute-1.amazonaws.com) sudo yum install http -y Setup index.html - Hello, this is web server 1
    
*   EC2 Load Balancer - Exam Tips:
    
    1.  Application Load Balancer (HTTP and HTTPS) - Layer 7 aware (make intelligent decisions).
    2.  Network Load Balancer (TCP, TLS and UDP) - Extreme Performance/Static IP Addresses.
    3.  Classic Load Balancer (PREVIOUS GENERATION for HTTP, HTTPS, and TCP) - Test & Dev to keep costs low.
*   Databases 101
    
    1.  Relational databases on AWS - RDS: 1.1 SQL Server 1.2 Oracle 1.3 Postgres 1.4 MySQL 1.5 Aurora 1.6 MariaDB
        
    2.  Exam Tips: RDS has two features 2.1 Multi-AZ - For DR 2.2 Read Replicas - For performance (Allows 5 copies of read replica)
        
    3.  Non Relational Databases (JSON/No SQL) called DynamoDB 3.1 Key Value pairs 3.2 The columns in the table can vary, this will not affect other rows in the DB)
        
    4.  OLTP (Online transaction processing) will differ from OLAP (Online analytics processing) in terms of the type of query you will run.
        
    5.  AWS data warehouse database called Redshift, uses a different type of architecture from a DB perspective and infrastructure layer.
        
    6.  ElastiCache is a web service that makes it easy to deploy, operate and scale as in-memory cache in the cloud. The service improves the performance of web applications by allowing you to retrieve the information fast, managed, in-memory cache instead of relying entirely on slower disk-based databases. 6.1 ElastiCache supports two open-source in-memory caching engines 6.1.1 Memcached 6.1.2 Redis
        
*   Auto Scaling
    
    1.  Create a Launch Configuration
    2.  Assign the launch configuration to an auto scaling group
*   Let's register a domain name (Route 53)
    
    1.  DNS Management
    2.  Traffic Management
    3.  Availability Monitoring
    4.  Domain Registration
    
    Route 53: Exam Tips:
    
    1.  Amazon DNS is called Route 53
    2.  It's global, similar to IAM and S3
    3.  You can use it to direct traffic all around the world and you can use it to register a domain name.
*   Elastic Beanstalk - Exam Tips
    
    1.  With Elastic Beanstalk, you can quickly deploy and manage application in the AWS cloud without worrying about the infrastructure that runs those applications. You simply upload the application, and Elastic Beanstalk handles the details of capacity provisioning, load balancing, scaling and application health monitoring.
*   Cloud Formation - Exam Tips
    
    1.  It's a service that helps you model and set up your AWS resources, so that you can spend less time managing those resources, and more time focusing on your applications that run in AWS. And you create a template that describes all the AWS resources that you want. So this can be things like EC2 instances, RDS instances ... etc. And AWS CloudFormation takes care of the provisioning and configuring of those resources for you. You don't need to individually go in and create and configure your AWS resources like we did with our WordPress site, and figure out what's dependent on what. AWS CloudFormation handles all of that for you. So, CloudFormation is fantastically powerful.
        
    2.  Elastic Beanstalk and CloudFormation are both free services. However, just remember that the resources that they provision, such as EC2 instances or RDS instances ... etc are not free. So the services itself is free, but not the actual resource that it provisions. And then, finally, just remember that Elastic Beanstalk is limited in what it can provision and is not programmable, whereas, CloudFormation can provision almost any AWS services and is completely programmable.
        
*   Architecting For The Cloud Best Practices - Part 1 AWS\_Cloud\_Best\_Practices.pdf
    
*   Architecting For The Cloud Best Practices - Part 2
    

Exam Tips: Which AWS Services are Global: 1. IAM 2. Route 53 3. CloudFront 4. SNS, is available in all regions 5. SES, is not available in all regions

    Some services give global views but are regional
    1. S3 buckets
    

*   What AWS Services Can Be Deployed On Premise
    
    1.  SnowCone - Disk that amazon send out to you, you load the data and then send it to amazon
    2.  Snowball Edge - Similar to Snowball plus CPU. Computer with storage, allows to deploy lambda functions on premise. Boeing uses this.
    3.  Storage Gateway - Caching your files inside your data centre and replicate files to S3
    4.  CodeDeploy - To deploy applications on premise
    5.  Opsworks - Opsworks uses chef to do automated deployments.
    6.  IoT Greengrass - AWS service, connect on premise devices to AWS cloud.
    7.  Systems Manager
*   CloudWatch 101
    
    1.  CloudWatch is to monitor performance
    2.  Monitors 2.1 EC2 Instances 2.2 Autoscaling Groups 2.3 Elastic Load Balancers 2.4 Route53 Health Checks
    3.  Storage and Content Delivery 3.1 EBS Volumes 3.2 Storage Gateways 3.3 CloudFront
    4.  Monitors host level metrics such as CPU, Network, Status check and Disk
*   CloudWatch 101 - Exam Tips:
    
    1.  CloudWatch is used for monitoring performance.
    2.  CloudWatch can monitor most of AWS as well as your applications that run on AWS
    3.  CloudWatch with EC2 will monitor events every 5 mins by default.
    4.  You can have 1 min interval by turning on detailed monitoring
    5.  You can create CloudWatch alarms which trigger on detailed monitoring.
    6.  CloudWatch is all about performance.
*   AWS Systems Manager - Exam Tips
    
    1.  Systems Manager is used to manage fleets of EC2 instances and virtual machines
    2.  A piece of software installed on each VM
    3.  Can be both inside AWS and on premise
    4.  Run command is used to install, patch and uninstall software.
    5.  Integrates with CloudWatch to give you a dashboard of your entire estate.
*   Summary of Cloud Concepts and Technology - Part I
    
    *   Know the 6 advantages of cloud
        
        1.  Trade Capital expense for variable expense
        2.  Benefit from massive economies of scale
        3.  Stop guessing about capacity.
        4.  Increase speed and agility.
        5.  Stop spending money running and maintaining data centres
        6.  Go global in minutes.
    *   Know the 3 different types of cloud computing
        
        1.  Infra as a service (IAAS) - EC2
        2.  Platform as a service (PAAS) - Elastic BeanStalk
        3.  Software as a service (SAAS) - Gmail
    *   Know the 3 different types of cloud computing deployments
        
        1.  Public Cloud - AWS, Azure, GCP
        2.  Hybrid - Mixture of private and public
        3.  Private Cloud (or on Premise) - You manage it in your datacenter. OpenStack or VMWare
    *   Understand the difference between a region, an availability zone (AZ) and an Edge location
        
        1.  A region is a physical location consists of 2 or more AZ's
        2.  An AZ is one or more datacenter's. Each with redundant power, networking and connectivity, housed in seperate facilities.
        3.  Edge locations are endpoints for AWS, which are used for caching content. Typically this consists of CloudFront, Amazon's Content Delivery Network (CDN).
    *   Choosing the right AWS region?
        
        1.  Data Sovereignty laws.
        2.  Latency to end users.
        3.  AWS Services.
    *   Understand the different support packages.
        
        1.  Basic - Free
        2.  Developer - $29 per month (scales based on usage)
        3.  Business - $100 per month (scales based on usage)
        4.  Enterprise - $15000 per month (scales based on usage) plus TAM (Technical Account Manager)
    *   Billing Alerts/Alarms will alert you automatically when a certain level of AWS spend has been reached.
        
    *   IAM (Identify Access Management). It is Global, you do not specify a region when dealing with IAM. When you create a user or group, this is created GLOBALLY.
        
    *   You can access the AWS platform in 3 ways
        
        1.  Via the console
        2.  Programatically (Using the command line)
        3.  Using the SDK
    *   Your root is the email address you used to set up your AWS account. The root account has full admin access. You should not give these account credentials away to anyone. Instead create a user for each individual within your org. You should always secure this root account using multi-factor authentication.
        
    *   A group is simply a place to store your users. Your users will inherit all permissions that the group has. Examples of groups: Developers, Sys admins, HR, finance...etc.
        
    *   To set the permission in the group you need to apply a policy to that group. Policies consists of JSON. These are referred to as key value pairs. You have your key such as name and then the value. For ex: {"name":"A cloud guru"}
        
    *   Remember that S3 is Object based: I.e allows you to upload files
        
    *   Files can be 0 Bytes to 5 TB
        
    *   There is unlimited storage
        
    *   Files are stored in Buckets
        
    *   S3 is universal namespace. That is, names must be unique globally. For Ex: [https://s3-eu-west-1.amazonaws.com/acloudguru](https://s3-eu-west-1.amazonaws.com/acloudguru)
        
    *   Not suitable to install an operating system on
        
    *   Successful uploads will generate HTTP 200 status code.
        
    *   The Key fundamentals of S3 are:
        
        1.  Key (this is simply the name of the object)
        2.  Value (this is simply the data and is made up of a sequence of bytes)
    *   Read after write consistency for PUTS of new objects
        
    *   Eventual consistency for overwrite PUTS and DELETS (can take some time to propagate)
        
    *   When you view your buckets, you view them globally but you can have buckets in individual regions.
        
    *   You can replicate the contents of one bucket to another bucket automatically by using cross region replication.
        
    *   S3 Transfer acceleration: Upload to an Edge location and then the files is transferred using Amazon network. Exam Tips:
        
    
    1.  S3 Standard: 99.99% availability, 99.99999999999% durability, stored redundantly across multiple devices, and is designed to sustain the loss of 2 facilities
    2.  S3 - IA (Infrequently accessed): For data that is accessed less frequently, but requires rapid access when needed. Lowe fee than S3, but you are charged a retrieval fee.
    3.  S3 One Zone IA: For where you want a lower cost option for infrequently accessed data, but do not require the multiple availability zone.
    4.  S3 Intelligent Tiering: Designed to optimise costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead.
    5.  S3 Glacier: S3 Glacier is a secure, durable and a low-cost storage class for data archiving. Retrieval times configurable from mins to hours.
    6.  S3 Glacier Deep Archive: S3 Glacier Deep Archive is Amazon S3's lowest-cost storage class where a retrieval time of 12 hours is acceptable.
    7.  You can use bucket policies to make entire S3 buckets public.
    8.  You can use S3 to host STATIC websites (such as .html). Websites that require database connections such as Wordpress etc cannot be hosted on S3.
    9.  S3 Scales automatically to meet your demand. Many enterprises will put static websites on S3 when they think there is going to be a large number of requests (such as for a movie preview for example)
    
    *   CloudFront - How it works with edge locations. Initial query at the edge location, if not available then it downloads from the sever. Otherwise from the edge location.
        
        1.  Edge Location: This is the location where content will be caches. This is seperate to an AWS Region/AZ.
        2.  Origin: This is the origin of all the files that CDN will distribute. This can be either a S3 Bucket, an EC2 instance, an Elastic Load Balancer or Route 53.
        3.  Distribution - This is the name given the CDN which consists of a collection of Edge locations.
        4.  Web Distribution - Typically used for Websites.
        5.  RTMP - Used for Media Streaming
        6.  Edge locations are not just READ only - you can write to them too. (i.e put an object on to them.)
        7.  Objects are cached for the life of the TTL (Time To Live)
        8.  You can clear cached objects, but you will be charged.
    *   EC2 Exam Tips: Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provided resizable compute capacity in the cloud. Amazon EC2 reduces the time required to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requirements change.
        
        1.  On Demand: Allows you to pay a fixed rate by the hour (or by the second) with no commitment.
        2.  Reserved: Provides you with a capacity reservation and offer a significant discount on the hourly charge for an instance. Contract Terms are 1 year or 3 year terms.
        3.  Spot: Enables you to bid whatever price you want for instance capacity, providing for even greater savings if your application have flexible start and end times. Note: If the spot instance is terminated by Amazon EC2, you will not be charged for a partial hour of usage. However, if you terminate the instance yourself, you will be charged for any hour in which the instance ran.
        4.  Dedicated Hosts: Physical EC2 server dedicated for your use. Dedicated Hosts can help reduce costs by allowing you to use your existing server-bound software licenses.
    *   EC2 instance classes FIGHTDRMCPXZ
        
        1.  F - For FPGA
        2.  I - For IOPS
        3.  G - Graphics
        4.  H - High Disk Throughput
        5.  T - Cheap general purpose (think T2 micro)
        6.  D - For Density
        7.  R - For RAM
        8.  M - Main choice for general purpose apps
        9.  C - For Compute
        10.  P - Graphics (think pics)
        11.  X - Extreme Memory
        12.  z - Extreme Memory and CPU
    *   What is EBS SSD:
        
        1.  General purpose SSD (GP2) - balances prices and performance for a wide variety of workloads
        2.  Provisioned IOPS SSD (IO1) - higher-performance SSD volume for mission-critical low-latency or high throughput workloads.
        
        Magnetic:
        
        1.  Throughput Optimised HDD (ST1) - Low cost HDD volume designed for frequently accessed, throughput-intensive workloads.
        2.  Cold HDD (SC1) - Lowest cost HDD volume designed for less frequently accessed workloads (File Servers)
        3.  Magnetic - Previous generation and some point will probably be phased out.
    *   EC2 is compute based service. It is not server-less. It's a server!
        
    *   Use a private key to connect to EC2
        
    *   Common Ports: Linux (22), MDP (RDP 3389), HTTP 80, HTTPS 443
        
    *   Firewall: TO let everything in 0.0.0.0/0. To let just one IP in X.X.X.X/32
        
    *   Security Groups are virtual firewalls in the cloud. You need to open ports in order to use them. Popular ports are SSH (22), RDP (3389), HTTP (80) and HTTPS (443)
        
    *   Always design for failure. Have one EC2 instance in each availability zone.
        
*   Summary of Cloud Concepts and Technology - Part II
    
    *   You can interact with AWS in 3 ways
        1.  Using the console
        2.  Using the command line (CLI)
        3.  Using SDK's
    *   Roles are much more secure than using access key id's and secret access keys and are easier to manage
    *   You can apply a roles to EC2 instances at any time. When you do this the change takes place immediately.
    *   Roles are universal. You do not need to specify the region they are in, similar to users.
    *   Load Balancers come in 3 different flavours.
        1.  Application load balancers: Layer 7 (make intelligent decisions)
        2.  Network load balancers: Extreme performance/Static IP Addresses.
        3.  Classic load balancers: Test & Dev, keep costs low
    *   RDS (SQL/OLTP)
        1.  SQL
        2.  MySQL
        3.  PostgresSQL
        4.  Oracle
        5.  Aurora
        6.  MariaDB
    *   DynamoDB (No SQL)
    *   Red Shift OLAP
    *   Elasticache
        1.  Memcached
        2.  Redis
    *   Red Shift is for BI or Data warehousing
    *   Elasticache is to speed up performance of existing databases (frequent identical queries)
    *   Graph Databases - Aurora Neptune
        1.  Scalability
        2.  High Availability
    *   RDS has 2 key features
        1.  Mutli-AZ - For DR
        2.  Read Replicas - For Performance
    *   Autoscaling: Autoscaling allows you to provision multiple EC2 instances behind a load balancer automatically depending on your demand.
    *   Amazon DNS service is called Route 53
    *   It's global, similar to IAM and S3
    *   You can use it to direct traffic all around the world and you can use it to register a domain name.
    *   With Elastic Beanstalk, you can quickly deploy and manage applications in the AWS cloud without worrying about the infrastructure that run those applications. You simply upload your application, and Elastic Beanstalk automatically handles the details of capacity provisioning, load balancing, scaling and application health monitoring.
    *   AWS CloudFormation is a service that helps you model and set up your Amazon Web Services resources so that you can spend less time managing those resources and more time focussing on you applications that run in AWS. You can create template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and AWS CloudFormation takes care of provisioning and configuring those resources for you. You don't need to individually create and configure AWS resources and figure out what's dependent on what; AWS CloudFormation handles all of that.
    *   Elastic Beanstalk and CloudFormation are both free services, however the resources they provision (such as EC2 instances) are not free.
    *   Elastic Beanstalk is limited in what it can provision and is not programmable and CloudFormation can provision almost any AWS service and is completely programmable.
    *   Remember the important Global Services
        1.  IAM
        2.  Route 53
        3.  CloudFront
        4.  SNS
        5.  SES
    *   Which AWS services can be used on premise
        1.  Snowball
        2.  Snowball Edge
        3.  Storage Gateway
        4.  CodeDeploy
        5.  OpsWorks
        6.  IoT Greengrass
    *   CloudWatch
        1.  CloudWatch is used to monitor performance
        2.  CloudWatch can monitor most of AWS as well as your applications that run on AWS
        3.  CloudWatch with EC2 will monitor events every 5 mins by default.
        4.  You can have 1 min intervals by turning on detailed monitoring.
        5.  You can create CloudWatch alarms which trigger notifications.
        6.  CloudWatch is all about performance.
    *   AWS Systems Manager
        1.  AWS Systems Manager can be used to manage fleets of EC2 instances & virtual machines.
        2.  A piece of software is installed on each VM.
        3.  Can be both inside AWS and on premise.
        4.  Run command is used to install, patch. Uninstall software.
        5.  Integrated with CloudWatch to give you a dashboard of your entire estate.
    *   Server-based services include: Amazon EC2, Amazon RDS, Amazon Redshift and Amazon EMR.
    *   Serverless platform includes: AWS lambda, AWS Fargate, Amazon S3, DynamoDB, API gateway, Amazon SNS, AWS step functions, Amazon Kinesis and developing tools and services.

\================================= AWS Pricing (12% in exam)
============================================================

*   Different Pricing Models: (Exam Tips)
    
    *   Capex (Capital expenditure) vs Opex (Operational Costs)
        
    *   The basic pricing policies are as follows:
        
        1.  Pay as you go
        2.  Pay less when you reserve
        3.  Pay even less per unit by using more
        4.  Pay even less as AWS grows
        5.  Custom pricing
    *   While pricing models vary across services, it's worthwhile to review key principles and best practices that are broadly applicable
        
        1.  Understand the fundamentals of pricing.
        2.  Start early with cost optimisation
        3.  Maximise the power of flexibility
        4.  Use the right pricing model for the job.
    *   There are three fundamental drivers of cost with AWS: (Exam Tips)
        
        1.  Compute
        2.  Storage
        3.  And Data Outbound
    *   AWS offers several pricing models depending on the product
        
        1.  On Demand
        2.  Dedicated Instances
        3.  Spot Instances
        4.  Reservations
    *   The following services are free: (Exam Tips)
        
        1.  Amazon VPC
        2.  Elastic BeanStalk
        3.  CloudFormation
        4.  IAM
        5.  Auto Scaling
        6.  Opsworks
        7.  Consolidated Billing
    *   What determines Price?
        
        1.  Clock hours of server time.
        2.  Instance Type
        3.  Pricing Model
        4.  Number of Instances
        5.  Load Balancing
        6.  Detailed Monitoring
        7.  Auto Scaling
        8.  Elastic IP Addresses (one is free)
        9.  Operating Systems and Software Packages
    *   EC2 Pricing Models
        
        1.  On Demand: Allows you to pay by the hour (or by the second) with no commitment
        2.  Reserved: Provides you with capacity reservation, and offer a significant discount on the hourly charge for an instance. Contact terms are 1 year or 3 year terms.
        3.  Spot: Enables you to bud whatever price you want for instance capacity, providing for even greater savings if your application have flexible start and end times
        4.  Dedicated hosts: Physical EC2 server dedicated for your use. Dedicated hosts can help you reduct costs by allowing you to use your existing server-bound software licenses
    *   You can use Amazon EC2 reserved instances to reserve capacity and receive a discount on your instance usage compared to running On-Demand instances.
        
    *   What determines price for Lambda?
        
        1.  Request Pricing
            *   Free Tier: 1 million requests per month
            *   $0.20 per 1 million requests thereafter
        2.  Duration Pricing
            *   400,000 GB-seconds per month free, up to 3.2 million seconds of compute time\*
            *   $0.00001667 for every GB-second used thereafter
        3.  Additional Charges
            *   You may incur additional charges if your lambda functions uses other AWS services or transfers data. For example, If your lambda function reads and writes data to or from Amazon S3, you will be billed for the read/write requests and the data stored in Amazon S3
    *   What determines price for Lambda?
        
        1.  Number of requests
        2.  Compute time.
    *   What determines price for EBS?
        
        1.  Volumes (per GB)
        2.  Snapshots (per GB)
        3.  Data Transfer
    *   What determines price for S3?
        
        1.  Storage Class Type (Standard or IA or 1 AZ IA etc)
        2.  Storage
        3.  Requests (GET, PUT, COPY)
        4.  Data Transfer
    *   What determines price for Glacier?
        
        1.  Storage
        2.  Data Retrieval Times: In general, longer the retrieval times, we receive more savings.
    *   What is Snowball?
        
        1.  AWS Snowball is a PB-Scale data transport solution that uses secure appliances to transfer large amounts of data in and out of the AWS cloud. Think of it as a gigantic disk to move your data into AWS
    *   What determines price for Snowball?
        
        1.  Service fee per job
            *   Snowball 50 TB: $200
            *   Snowball 80 TB: $250
        2.  Daily Charge
            *   First 10 days are free, after that it's $15 a day.
        3.  Data transfer
            *   Data transfer in to S3 is free. Data transfer out is not.
    *   What determines price for RDS?
        
        1.  Clock hours of server time.
        2.  Database characteristics (Type of DB)
        3.  Database Purchase Type (Different instance type)
        4.  Number of Database Instances
        5.  Provisioned Storage
        6.  Additional Storage
        7.  Requests
        8.  Deployment Type
        9.  Data Transfer
    *   What determines price for Dynamo DB
        
        1.  Provisioned throughput (write)
        2.  Provisioned throughput (read)
        3.  Index data storage
    *   What determines price for CloudFront
        
        1.  Traffic Distribution
        2.  Requests
        3.  Data transfer out
*   AWS Budgets vs Cost Explorer: (Exam Tips)
    
    *   AWS Budgets gives you the ability to set custom budgets that alert you when your costs of your usage exceed (or are forecasted to exceed) your budget amount.
    *   Used to budget costs BEFORE they have been incurred
    *   AWS Cost Explorer has an easy-to-use interface that lets you visualise, understand, and manage your AWS costs and usage over time.
    *   Used to explore costs AFTER they have been incurred.
*   AWS Support Plans (Exam Tips)
    
    *   Basic: Free, No Tech support, no TAM and no one can open cases
    *   Developer: $29 a month, Business hour access via email, no TAM and 1 person/unlimited cases
    *   Business $100 a month, 24 X 7 email, chat & phone, no TAM and Unlimited contacts/unlimited cases
    *   Enterprise $15000 a month, 24 X 7 email, chat & phone, Plus TAM and Unlimited contacts/unlimited cases
    
    Case Severity/Response times:
    
    *   Basic: None
    *   Developer: General guidance: < 24 business hours, System impaired: < 12 business hours
    *   Business: General guidance: < 24 business hours, System impaired: < 12 business hours, Prod System impaired: < 4hours, Prod Sys down: < 1 hour
    *   Enterprise: General guidance: < 24 business hours, System impaired: < 12 business hours, Prod System impaired: < 4hours, Prod Sys down: < 1 hour, Business-Critical system down: < 15 mins
    
*   Tagging & Resource Groups (Exam Tips) What are Tags?
    
    *   Key value pairs attached to AWS resources
    *   Metadata (data about data)
    *   Tags can sometimes be inherited
    
    What are Resource Groups?
    
    *   Resource groups make it easy to group your resources using the tags that are assigned to them. You can group resources that share one or more tags.
    *   Resource groups contain information such as:
        *   Region
        *   Name
        *   Employee ID
        *   Department
    *   Tags can have specific information
        *   For EC2 - Public and Private IP Addresses
        *   For ELB - Port Configurations
        *   For RDS - Database Engine etc
    *   Using Resource Groups you can apply automation to resources tagged with specific tags. For Example, we stopped all EC2 instances in the Stockholm region.
    *   Resource Groups in combination with AWS Systems manager allow you to control and execute automation against entire fleets of EC2 instances, all at a push of a button.
    *   Tag Editor is a global service that allows us to discover resources and to add additional tags to them as well. Newer regions may take some time to be compatible with tag editor.
*   AWS Organisations & Consolidated Billing (Exam Tips)
    
    *   AWS Organisations is an account management service that enables you to consolidate multiple AWS accounts into an organisation that you create and centrally manage For Example: OU group with AWS accounts, policies can be applied to OU's or accounts directly.
    *   Available in two feature sets
        1.  Consolidated billing
        2.  All features
    *   Consolidated Billing
        1.  Paying Account is independent, cannot access the resources of the other accounts, all linked accounts are independent. Currently a limit of 20 linked accounts for consolidated billing,
    *   Advantages of consolidated billing account include:
        1.  One bill per AWS account
        2.  Very easy to track charges and allocate costs
        3.  Volume pricing discount
    *   Some best practices with AWS organisations:
        1.  Always enable multi-fact auth on root account.
        2.  Always use a strong and complex password on root account.
        3.  Paying account should be used for billing purposes only. Do not deploy resources into the paying account.
*   CloudTrail vs CloudWatch
    
    *   CloudWatch monitors performance.
    *   CloudTrail monitors API calls in the AWS platform.
    
    CloudTrail (Exam Tips) 1. Per AWS account and is enabled per region. 2. Can consolidate logs using S3 bucket: 2.1 Turn on CloudTrail in paying account. 2.2 Create a bucket policy that allows cross-account access. 2.3 Turn on CloudTrail in the other accounts and use the bucket in the paying account.
    
    Billing Alerts: 1. When monitoring is enabled on the paying account, the billing data for all linked accounts is included. 2. You can still create billing alters per individual account. 3. Consolidated billing allows you to get volume discounts on all your accounts. 4. Unused reserved instances for EC2 are applied across the group. 5. CloudTails is on a per account and per region basis, but can be aggregated into a single bucket belonging to the paying account.
    
*   AWS Organisations - Lab
    
*   AWS Quick Start & AWS Landing Zone - Lab (Exam Tips)
    
    *   AWS Quick Start is a way of deploying environments quickly, using CloudFormation templates built by AWS Solutions Architects who are experts in that particular technology.
    *   AWS Landing Zone is a solution that helps customers more quickly set up secure, multi-account AWS environment based on AWS best practices.
*   AWS Calculators (Important for practitioner exam)
    
    *   Helps to calculate costs using a couple of different calculators
    *   Available in two feature sets:
        1.  AWS Simple Monthly Calculator: Monthly cost of AWS
        2.  AWS Total Cost of Ownership Calculator: Comparison of doing it ourselves or using AWS.
*   Billing & Pricing Summary:
    
    *   As above

\=============================== Security in the cloud
======================================================

*   AWS Compliance & AWS Artifact
    
    *   Services > Security, Identity, & Compliance > Artifact Exam Tip: AWS Artifact is used to retrieve compliance reports.
    *   A PCI DSS Level 1 certification attests to the security of the AWS platform regarding credit card transactions.
    *   A HIPAA certification attests to the fact that the AWS Platform has met the standard required for the secure storage of medical records in the US
    *   All AWS Services GDPR (European Union’s General Data Protection Regulation) ready
*   Shared Responsibility Model (Important for the exam)
    
    *   While AWS manages the security of the cloud, security in the cloud is responsibility of the customer. Customers retains control of what security they choose to implement to protect their own content, platform, applications, systems and networks, no differently than they would in an on-site datacenter.
    *   AWS responsible (Security of the cloud) for REGIONS, AZ's, Edge Locations. H/W/AWS Global infrastructure. Compute. Storage, Database, networking and software
    *   Customer is responsible (Security in the cloud) for client side data encryption & data integrity authentication, server side encryption (FS or data), networking traffic protection (encryption, integrity, identity), OS, N/W & F/W configuration, Platform, applications, IAM and customer data
    *   Encryption is a shared responsibility.
*   AWS WAF & AWS Shield (Exam Tips)
    
    *   What is AWS WAF? To prevent Cross scripting or SQL injection
        1.  AWS WAF is a web application firewall that helps protect your web application from common web exploits that could affect application availability, compromise security, or consume excessive resources
    *   What is AWS Shield - to prevent DDOS
        1.  AWS Shield is a managed DDOS protection service that safeguards web applications running on AWS. AWS Shield provided always-on detection and automatic inline mitigations that minimise application downtime and latency, so there is no need to engage AWS support to benefit from DDOS protection.
    *   There are two tiers of AWS shield - Standard and Advanced.
    *   Advanced costs $3K per month.
    *   Only Advanced offers automated application layer monitoring.
*   AWS Inspector vs AWS Trusted Advisor vs CloudTrail (Exam Tips)
    
    *   AWS Inspector assesses the security and compliance of your EC2 instances.
        
    *   Amazon Inspector is for EC2 instances only, it's an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. Amazon Inspector automatically assesses application for vulnerabilities or deviations from best practices. After performing as assessment, Amazon inspector produces a detailed list of security findings prioritised by level of severity. These findings can be reviewed directly or as part of detailed assessment reports which are available via the Amazon Inspector Console or API.
        
    *   AWS Trusted Advisor (Global Service) and it's for your AWS account. It is an online resource to help you reduce cost, increase performance and improve security by optimising your AWS environment, Trusted Advisor provides real-time guidance to help you provision your resources following AWS best practices. Advisor will advise you on Cost Optimisation, Performance, Security, Fault Tolerance and service limits.
        
    *   Comes in two flavours
        
        1.  Core checks and recommendations
        2.  Full Trusted Advisor - Business and Enterprise Companies Only
    *   Trusted Advisor helps you optimise your entire AWS environment in real time following AWS best practices. It helps you optimise cost, fault-tolerance, and more.
        
    *   AWS Trusted Advisor can help you assess the fault-tolerance of your AWS environment.
        
    *   AWS CloudTrail increases visibility into your user and resource activity by recording AWS management console actions and API calls. You can identify which users and accounts called AWS, the source IP address from which the calls were made, and when the calls occurred
        
*   CloudWatch vs AWS Config
    
    *   What is CloudWatch?
        *   CloudWatch is used to monitor performance.
        *   CloudWatch is used with EC2
        *   Host Level metrics such as CPU, N/W, Disk and Status Check.
        *   Custom level metrics such as disk can be done using a script
    *   AWS Config provides a detailed view of the configuration of AWS resources in your AWS account. This included how the resources are related to one another and how they were configured in the past so that you can see how the configurations and relationships change over time.
*   Athena Vs Macie (Exam Tips)
    
    *   What is Athena?
        
        *   Interactive query service which enables you to analyse and query data located in S3 using standard SQL
        *   Serverless, nothing to provision, pay per query / per TB scanned
        *   No need to set up complex Extract/Transform/Load (ETL) process
        *   Works directly with data stored in S3
    *   Athena can be used for
        
        1.  Can be used to query log files stores in S3. Ex: ELB Logs, S3 access logs ... etc
        2.  Generate business reports on data stored in S3.
        3.  Analyse AWS cost and usage reports
        4.  Run queries on click-stream data.
    *   What is Macie?
        
        *   Security service which uses machine learning and NLP (natural language processing) to discover, classify and protect sensitive data stored in S3
        *   Uses AI to recognise if your S3 objects contain sensitive data such as personal identification information.
        *   Dashboards, reporting and alerts
        *   Works directly with data stored in S3
        *   Can also analyse CloudTrail logs
        *   Great for PCI-DSS and preventing ID theft.

· S3 capacity can’t be reserved

· S3 One Zone IA is of lower availability of 99.5 compared to S3 Intelligent-Tiering\* and S3 Standard-IA 99.9 and others at 99.99

· One EBS to one EC2 only

· EFS can be attached to many EC2’s

· High availability – initial with multi AZ’s, otherwise multi regions

· Inherited controls – Physical and environmental controls

· Shared Controls: Patch Management

· Business and enterprise have access to full set of trusted advisor recommendations and checks And the rest get partial ...and enterprise only has access to well architected framework

· Security and Compliance is a shared responsibility between AWS and the customer. This customer/AWS shared responsibility model also extends to IT controls

· Dedicated Instances, EBS Snapshots, and products in AWS Marketplace are still billed on an hourly basis

Like your customised cloud expert, AWS Trusted Advisor analyses your AWS environment and provides best practice recommendations in five categories: cost optimisation, performance, security, fault tolerance and service limits.

Server platforms are EC2, RDS, Red Shift and EMR (Hadoop)

Serverless platform includes: AWS lambda, Fargate, Athena, Amazon S3, DynamoDB, API gateway, Amazon SNS, SQS, AWS step functions, Amazon kinesis and developing tools and services

Amazon QuickSight (BI)

Amazon Redshift (DW / OLAP)

AWS Data Pipeline is a web service that helps you reliably process and move data between different AWS compute and storage services, as well as on-premises data sources, at specified intervals.

AWS Glue (ETL)

AWS Lake Formation (Data Lakes)

Amazon Managed Streaming for Kafka (MSK) to build and run applications that use Apache Kafka to process streaming data

AWS Step Functions lets you coordinate multiple AWS services into serverless workflows so you can build and update apps quickly. Using Step Functions, you can design and run workflows that stitch together services such as AWS Lambda and Amazon ECS into feature-rich applications.

Amazon Simple Workflow (Amazon SWF) helps developers build, run, and scale background jobs that have parallel or sequential steps. You can think of Amazon SWF as a fully-managed state tracker and task coordinator in the cloud.

AR and VR: Amazon Sumerian lets you create and run virtual reality (VR), augmented reality (AR), and 3D applications quickly and easily without requiring any specialized programming or 3D graphics expertise.

AWS Cost Explorer has an easy-to-use interface that lets you visualize, understand, and manage your AWS costs and usage over time.

AWS Budgets gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amount.

Reserved Instance (RI) Reporting: AWS provides a number of RI-specific cost management solutions out-of-the-box to help you better understand and manage your RIs.

Amazon Elastic Container Registry (Amazon ECR) is a fully-managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images.

Amazon Elastic Container Service (Amazon ECS) is a highly scalable, high-performance container orchestration service that supports Docker containers and allows you to easily run and scale containerised applications on AWS. Amazon ECS eliminates the need for you to install and operate your own container orchestration software, manage and scale a cluster of virtual machines, or schedule containers on those virtual machines.

Amazon Elastic Container Service for Kubernetes (Amazon EKS) makes it easy to deploy, manage, and scale containerised applications using Kubernetes on AWS.

Amazon Lightsail is designed to be the easiest way to launch and manage a virtual private server with AWS.

AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and Internet Information Services (IIS).

AWS Fargate is a compute engine for Amazon ECS that allows you to run containers without having to manage servers or clusters.

The AWS Serverless Application Repository enables you to quickly deploy code samples, components, and complete applications for common use cases such as web and mobile back-ends, event and data processing, logging, monitoring, IoT, and more. Each application is packaged with an AWS Serverless Application Model (SAM) template that defines the AWS resources used.

AWS Outposts bring native AWS services, infrastructure, and operating models to virtually any data center, co-location space, or on-premises facility.

Amazon ElastiCache is a web service that makes it easy to deploy, operate, and scale an in-memory cache in the cloud.

Amazon Corretto is a no-cost, multiplatform, production-ready distribution of the Open Java Development Kit (OpenJDK).

AWS Cloud9 is a cloud-based integrated development environment (IDE) that lets you write, run, and debug your code with just a browser. It includes a code editor, debugger, and terminal.

AWS X-Ray helps developers analyse and debug distributed applications in production or under development, such as those built using a microservices architecture.

Amazon GameLift is a managed service for deploying, operating, and scaling dedicated game servers for session-based multiplayer games.

Amazon Lumberyard is a free, cross-platform, 3D game engine for you to create the highest-quality games, connect your games to the vast compute and storage of the AWS Cloud, and engage fans on Twitch.

AWS IoT Core is a managed cloud service that lets connected devices easily and securely interact with cloud applications and other devices. AWS IoT Core can support billions of devices and trillions of messages, and can process and route those messages to AWS endpoints and to other devices reliably and securely.

AWS IoT Greengrass seamlessly extends AWS to devices so they can act locally on the data they generate, while still using the cloud for management, analytics, and durable storage.

Machine Learning: Amazon SageMaker is a fully-managed platform that enables developers and data scientists to quickly and easily build, train, and deploy machine learning models at any scale.

    Amazon SageMaker Ground Truth helps you build highly accurate training datasets for machine learning quickly.
    
    Amazon Lex is a service for building conversational interfaces into any application using voice and text.
    
    Amazon Polly is a service that turns text into lifelike speech. Polly lets you create applications that talk, enabling you to build entirely new categories of speech-enabled products.
    

AWS Control Tower automates the set-up of a baseline environment, or landing zone, that is a secure, well-architected multi-account AWS environment.

AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet.

AWS Service Catalog allows organisations to create and manage catalogs of IT services that are approved for use on AWS.

AWS Application Discovery Service helps enterprise customers plan migration projects by gathering information about their on-premises data centers.

AWS DataSync is a data transfer service that makes it easy for you to automate moving data between on-premises storage and Amazon S3 or Amazon Elastic File System (Amazon EFS).

AWS Amplify makes it easy to create, configure, and implement scalable mobile applications powered by AWS.

Amazon Cognito lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily. (Social Media SSO)

Amazon Pinpoint makes it easy to send targeted messages to your customers through multiple engagement channels.

AWS Device Farm is an app testing service that lets you test and interact with your Android, iOS, and web apps on many devices at once, or reproduce issues on a device in real time.

AWS AppSync is a serverless back-end for mobile, web, and enterprise applications.

AWS PrivateLink simplifies the security of data shared with cloud-based applications by eliminating the exposure of data to the public Internet.

AWS Direct Connect makes it easy to establish a dedicated network connection from your premises to AWS.

AWS Global Accelerator is a networking service that improves the availability and performance of the applications that you offer to your global users.

Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale.

AWS Transit Gateway is a service that enables customers to connect their Amazon Virtual Private Clouds (VPCs) and their on-premises networks to a single gateway.

AWS App Mesh makes it easy to monitor and control microservices running on AWS.

AWS Cloud Map is a cloud resource discovery service. With Cloud Map, you can define custom names for your application resources, and it maintains the updated location of these dynamically changing resources. This increases your application availability because your web service always discovers the most up-to-date locations of its resources.

AWS Security Hub gives you a comprehensive view of your high-priority security alerts and compliance status across AWS accounts.

Amazon Cloud Directory enables you to build flexible, cloud-native directories for organising hierarchies of data along multiple dimensions. With Cloud Directory, you can create directories for a variety of use cases, such as organisational charts, course catalogs, and device registries.

Amazon GuardDuty is a threat detection service that continuously monitors for malicious or unauthorised behavior to help you protect your AWS accounts and workloads.

AWS CloudHSM is a cloud-based hardware security module (HSM) that enables you to easily generate and use your own encryption keys on the AWS Cloud. With CloudHSM, you can manage your own encryption keys using FIPS 140-2 Level 3 validated HSMs.

AWS Firewall Manager is a security management service that makes it easier to centrally configure and manage AWS WAF rules across your accounts and applications.

AWS Key Management Service (KMS) makes it easy for you to create and manage keys and control the use of encryption across a wide range of AWS services and in your applications.

AWS Secrets Manager helps you protect secrets needed to access your applications, services, and IT resources.

Amazon FSx for Lustre is a fully managed file system that is optimised for compute-intensive workloads, such as high performance computing, machine learning, and media data processing workflows.

The AWS Cost & Usage Report is a single location for accessing comprehensive information about your AWS costs and usage.

AWS Directory Service is for Single Sign On. Single sign-on only works when used on a computer that is joined to the AWS Directory Service directory. It cannot be used on computers that are not joined to the directory.

What feature of Amazon RDS helps to create globally redundant databases? Snapshots (not read replicas)

A director has been tasked with investigating hybrid cloud architecture. The company currently accesses AWS over the public internet. Which service will facilitate private hybrid connectivity? AWS Direct Connect (not Amazon Virtual Private Cloud (Amazon VPC) NAT Gateway)

Which AWS service provides a secure, fast, and cost-effective way to migrate or transport exabyte-scale datasets into AWS? AWS Snowmobile (not AWS Snowball)

Which of the following services have Distributed Denial of Service (DDoS) mitigation features? (Choose two.)

1.  WAF
2.  CloudFront

Which services manage and automate application deployments on AWS? AWS CodeDeploy

Mega Quiz
---------

*   A region is a geographical area divided into Availability Zones. Each region contains at least two Availability Zones.
    
*   Aurora is AWS's managed database service that is up to 5X faster than a traditional MySQL database.
    
*   Under the Shared Responsibility model, for which of the following does AWS not assume responsibility? A: Customer data The customer is responsible for their own customer data.
    
*   True or false: With AWS Organizations, there are two available feature sets — so you may choose to use the consolidated billing features, or use all the offered features. A: True With AWS Organizations, you can use either the consolidated billing features or all the offered features. If you create an organisation with consolidated billing features only, you can later enable all features.
    
*   An online resource to help you reduce cost, increase performance, and improve security by optimising your AWS environment, Trusted Advisor provides real time guidance to help you provision your resources following AWS best practices.
    
*   The AWS Database Migrations Service is the best choice for conventional data migrations.
    
*   Which AWS service is specifically designed to assist you in processing large data sets? A: EMR (not AWS big data processing) Amazon EMR is a web service that makes it easy to process large amounts of data efficiently.
    
*   Which of the following is correct? A: # of Edge Locations > # of Availability Zones > # of Regions The number of Edge Locations is greater than the number of Availability Zones, which is greater than the number of Regions.
    
*   Which of the following is not a feature of AWS Organizations? A: Granular configuration of Security Groups within a VPC AWS Organizations is an account management service which allows you manage multiple accounts centrally.
    
*   In both AWS-Budget & CloudWatch alarms can be set to monitor spending on your AWS Account.
    
*   All accounts receive billing support.
    
*   Trusted Advisor can assist you with the cost optimisation of your AWS environment.
    
*   You have a mission-critical application which must be globally available at all times. Which deployment strategy should you follow? A Multi-Region deployment will best ensure global availability. A: Multi-Region
    
*   You have a project that will require 90 hours of computing time. There is no deadline, and the work can be stopped and restarted without adverse effect. Which of the following computing options offers the most cost-effective solution? - A: Spot Instances
    
*   Which of the following are principles of sound cloud design? A: Infrastructure as code, Disposable resources, Assume everything will fail, and Scalability Build your systems to be scalable, use disposable resources, reduce infrastructure to code, and, please, assume EVERYTHING will fail sooner or later.
    
*   You need to host a file in a location that's publicly accessible from anywhere in the world. Which AWS service would best meet that need? A: S3 With S3, objects can be accessed from anywhere in the world via a dedicated URL.
    
*   Both Enterprise and business support plans feature unlimited (customer-side) contacts and unlimited support cases.
    
*   Which AWS service allows you to run code without having to worry about provisioning any underlying resources (such as virtual machines, databases etc.) A: Lambda is the AWS Function-as-a-Service (FaaS) offering that lets you run code without provisioning or managing servers.
    
*   Redshift is AWS's data warehousing service.
    
*   Which native AWS service will act as a file system mounted on an S3 bucket? A: AWS Storage Gateway The Storage Gateway service is primarily used for attaching infrastructure located in a Data centre to the AWS Storage infrastructure. The AWS documentation states that; "You can think of a file gateway as a file system mount on S3." Amazon Elastic File System (EFS) is a mountable file storage service for EC2, but has no connection to S3 which is an object storage service. Amazon Elastic Block Store (EBS) is a block level storage service for use with Amazon EC2 and again has no connection to S3.
    
*   Your Development team uses four on-demand EC2 instances and your QA team has 5 reserved instances, only three of which are being used. Assuming all AWS accounts are under a single AWS Organization, how will the Development team's instances be billed?
    

If using AWS Organization, Development Team will only be billed for 2 On-Demand Instances. Because QA Team has 5 Reserved instances and only 3 are being used so remaining 2 instances will be used for Development's Team Billing. In this case we are saving money because Reserved instances are cheaper than On-Demand because of commitment and upfront cost

*   Which of the following are AWS compute services? A: EC2 and Lambda are AWS Compute Services.
    
*   Important to remember Security Groups default Limits Security groups (SG) control inbound and outbound traffic for your instances (SG = Firewall for EC2 Instances) NACLs control inbound and outbound traffic for your subnets (NACL = Firewall for Subnets)
    

Yes, You can have any number of EC2 Instances in a Security Group, but, bear in mind this Limits: - Security groups per Region : 2500 (default limit)  
\- Security Groups per Network Interface (EC2 Instance) : 5 (default limit), 16 (the maximum per request)  
\- Inbound or Outbound rules per Security Group : 60 (default limit). You can have 60 inbound and 60 outbound rules per security group (making a total of 120 rules)

You can Increase your Security Group Limit by a request, To request a limit increase:  
\- Open the Amazon EC2 console at [https://console.aws.amazon.com/ec2/](https://console.aws.amazon.com/ec2/).  
\- From the navigation bar, select a Region.  
\- From the navigation pane, choose **Limits**.  
\- Select the resource in the list, and choose Request limit increase.  
\- Complete the required fields on the limit increase form.