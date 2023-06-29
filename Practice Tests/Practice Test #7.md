Practice Test 1 - Results
-------------------------



All knowledge areas

*   All knowledge areas
    
*   AWS Management & Governance
    
*   AWS Compute
    
*   AWS Cost Management
    
*   AWS Support
    
*   AWS Shared Responsibility Model
    
*   AWS Security, Identity, & Compliance
    
*   AWS Storage
    
*   AWS Cloud Benefits
    
*   AWS Cloud Architecture & Design
    
*   AWS Networking & Content Delivery
    
*   AWS Media Services
    
*   AWS Analytics
    
*   AWS Migration & Transfer
    
*   AWS Database
    
*   AWS Global Infrastructure
    
*   AWS Machine Learning
    



Question 1: Correct

Which AWS services can be used as infrastructure automation tools? (Select TWO.)

*   AWS CloudFormation
    
    (Correct)
    
*   Amazon CloudFront
    
*   AWS Batch
    
*   AWS OpsWorks
    
    (Correct)
    
*   Amazon QuickSight
    

#### Explanation

AWS CloudFormation provides a common language for you to model and provision AWS and third party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts.

AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet. Chef and Puppet are automation platforms that allow you to use code to automate the configurations of your servers. OpsWorks lets you use Chef and Puppet to automate how servers are configured, deployed, and managed across your [Amazon EC2](https://aws.amazon.com/ec2/) instances or on-premises compute environments.

**CORRECT:** "AWS CloudFormation" is a correct answer.

**CORRECT:** "AWS OpsWorks" is also a correct answer.

**INCORRECT:** "Amazon CloudFront" is incorrect. Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds.

**INCORRECT:** "AWS Batch" is incorrect. AWS Batch enables developers, scientists, and engineers to easily and efficiently run hundreds of thousands of batch computing jobs on AWS.

**INCORRECT:** "Amazon QuickSight" is incorrect. Amazon QuickSight is a fast, cloud-powered business intelligence service that makes it easy to deliver insights to everyone in your organization.

**References:**

[https://aws.amazon.com/cloudformation/](https://aws.amazon.com/cloudformation/)

[https://aws.amazon.com/opsworks/](https://aws.amazon.com/opsworks/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 2: Correct

What technology enables compute capacity to adjust as loads change?

*   Load balancing
    
*   Automatic failover
    
*   Round robin
    
*   Auto Scaling
    
    (Correct)
    

#### Explanation

Auto Scaling allows the dynamic adjustment of provisioned resources based on demand. For instance, you can use Amazon EC2 Auto Scaling to launch additional EC2 instances when CloudWatch metrics report the CPU utilization has reached a certain threshold.

**CORRECT:** "Auto Scaling" is the correct answer.

**INCORRECT:** "Load balancing" is incorrect. This technology is more focused on high availability by distributing connections to multiple instances.

**INCORRECT:** "Automatic failover" is incorrect. This is a technology that enables high availability by failing over to standby resources in the event of a service disruption.

**INCORRECT:** "Round robin" is incorrect. This is typically associated with the Domain Name Service (DNS) where responses are provided from a pool of addresses in a sequential and circular fashion.

**References:**

[https://aws.amazon.com/autoscaling/](https://aws.amazon.com/autoscaling/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/elastic-load-balancing-and-auto-scaling/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/elastic-load-balancing-and-auto-scaling/)

Question 3: Incorrect

How can a company separate costs for storage, Amazon EC2, Amazon S3, and other AWS services by department?

*   Add department-speciﬁc tags to each resource
    
    (Correct)
    
*   Create a separate VPC for each department
    
*   Create a separate AWS account for each department
    
*   Use AWS Organizations
    
    (Incorrect)
    

#### Explanation

A tag is a label that you or AWS assigns to an AWS resource. Each tag consists of a _key_ and a _value_. For each resource, each tag key must be unique, and each tag key can have only one value.

You can use tags to organize your resources, and cost allocation tags to track your AWS costs on a detailed level. After you activate cost allocation tags, AWS uses the cost allocation tags to organize your resource costs on your cost allocation report, to make it easier for you to categorize and track your AWS costs.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-30_02-34-45-78142437fad11bafcc5420fb8cf68327.jpg)

AWS provides two types of cost allocation tags, an _AWS generated tags_ and _user-defined tags_. AWS defines, creates, and applies the AWS generated tags for you, and you define, create, and apply user-defined tags. You must activate both types of tags separately before they can appear in Cost Explorer or on a cost allocation report.

**CORRECT:** "Add department-speciﬁc tags to each resource" is the correct answer.

**INCORRECT:** "Create a separate VPC for each department" is incorrect. This is unnecessary and would not help with separating costs.

**INCORRECT:** "Create a separate AWS account for each department" is incorrect. This is overly complex and unnecessary.

**INCORRECT:** "Use AWS Organizations" is incorrect. Consolidated billing can separate bills by account but for department based cost separation cost allocation tags should be used.

**References:**

[https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 4: Correct

Which AWS Support plan provides access to architectural and operational reviews, as well as 24/7 access to Cloud Support Engineers through email, online chat, and phone?

*   Basic
    
*   Business
    
*   Developer
    
*   Enterprise
    
    (Correct)
    

#### Explanation

Only the AWS enterprise support plan provides Well-Architected Reviews and Operational Reviews. 24/7 access to Cloud Support Engineers through email, online chat, and phone is offered on the business and enterprise plans.

**CORRECT:** "Enterprise" is the correct answer.

**INCORRECT:** "Basic" is incorrect. Basic only includes: 24x7 access to customer service, documentation, whitepapers, and support forums.

**INCORRECT:** "Business" is incorrect as it does not provide access to architectural and operational reviews.

**INCORRECT:** "Developer" is incorrect as you get support from Cloud Support Associates, not Engineers and also do not get access to architectural and operational reviews.

**References:**

[https://aws.amazon.com/premiumsupport/plans/](https://aws.amazon.com/premiumsupport/plans/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 5: Correct

Under the AWS shared responsibility model, which of the following is an example of security in the AWS Cloud?

*   Managing edge locations
    
*   Physical security
    
*   Firewall conﬁguration
    
    (Correct)
    
*   Global infrastructure
    

#### Explanation

Firewall configuration is an example of “security in the cloud”. This is the customer’s responsibility, not an AWS responsibility.

**CORRECT:** "Firewall conﬁguration" is the correct answer.

**INCORRECT:** "Managing edge locations" is incorrect. This is an example of “security of the cloud” and is an AWS responsibility.

**INCORRECT:** "Physical security" is incorrect. This is an example of “security of the cloud” and is an AWS responsibility.

**INCORRECT:** "Global infrastructure" is incorrect. This is an example of “security of the cloud” and is an AWS responsibility.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-shared-responsibility-model/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-shared-responsibility-model/)

Question 6: Correct

Which AWS service provides on-demand downloads of AWS security and compliance reports?

*   AWS Directory Service
    
*   AWS Artifact
    
    (Correct)
    
*   AWS Trusted Advisor
    
*   Amazon Inspector
    

#### Explanation

AWS Artifact is the go-to, central resource for compliance-related information that matters to you. It provides on-demand access to AWS’ security and compliance reports and select online agreements.

Reports available in AWS Artifact include Service Organization Control (SOC) reports, Payment Card Industry (PCI) reports, and certifications from accreditation bodies across geographies and compliance verticals that validate the implementation and operating effectiveness of AWS security controls.

**CORRECT:** "AWS Artifact" is the correct answer.

**INCORRECT:** "AWS Directory Service" is incorrect. AWS Directory Service for Microsoft Active Directory, also known as AWS Managed Microsoft AD, is an AWS-managed directory service built on actual Microsoft Active Directory and powered by Windows Server 2012 R2.

**INCORRECT:** "AWS Trusted Advisor" is incorrect. AWS Trusted Advisor is an online tool that provides you real time guidance to help you provision your resources following AWS best practices.

**INCORRECT:** "Amazon Inspector" is incorrect. Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS.

**References:**

[https://aws.amazon.com/artifact/](https://aws.amazon.com/artifact/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-security/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-security/)

Question 7: Correct

Which Amazon EC2 pricing model provides is the most cost-effective for an always-up, right-sized database server running a project that will last 1 year?

*   On-Demand Instances
    
*   Convertible Reserved Instances
    
*   Spot Instances
    
*   Standard Reserved Instances
    
    (Correct)
    

#### Explanation

Reserved Instances (RIs) provide you with a significant discount (up to 72%) compared to On-Demand instance pricing. Standard reserved instances offer the most cost savings. RIs are based on a 1 or 3 year contract so they are suitable for workloads that will run for the duration of the contract period.

**CORRECT:** "Standard Reserved Instances" is the correct answer.

**INCORRECT:** "Convertible Reserved Instances" is incorrect. You have the flexibility to change families, OS types, and tenancies while benefitting from RI pricing when you use Convertible RIs. However, this is not required for a right-sized server.

**INCORRECT:** "On-Demand Instances" is incorrect. This pricing model offers not discounts.

**INCORRECT:** "Spot Instances" is incorrect. Though you can achieve greater cost savings with Spot instances, the instances can be terminated when AWS need the capacity back.

**References:**

[https://aws.amazon.com/ec2/pricing/reserved-instances/](https://aws.amazon.com/ec2/pricing/reserved-instances/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 8: Correct

Which of the options below are recommendations in the performance efficiency pillar of the well-architected framework? (choose 2)

*   Democratize advanced technologies
    
    (Correct)
    
*   Go global in days
    
*   Use serverless architectures
    
    (Correct)
    
*   Rarely experiment
    
*   Mechanical complexity
    

#### Explanation

The performance efficiency pillar includes the ability to use computing resources efficiently to meet system requirements and to maintain that efficiency as demand changes and technologies evolve.

There are five design principles for performance efficiency in the cloud:

– Democratize advanced technologies.

– Go global in minutes.

– Use serverless architectures.

– Experiment more often.

– Mechanical sympathy.

**CORRECT:** "Democratize advanced technologies" is a correct answer.

**CORRECT:** "Use serverless architectures" is also a correct answer.

**INCORRECT:** "Go global in days" is incorrect. Please refer to the design principles above.

**INCORRECT:** "Rarely experiment" is incorrect. Please refer to the design principles above.

**INCORRECT:** "Mechanical complexity" is incorrect. Please refer to the design principles above.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/)

Question 9: Correct

Which feature enables fast, easy, and secure transfers of files over long distances between a client and an Amazon S3 bucket?

*   S3 Static Websites
    
*   S3 Copy
    
*   Multipart Upload
    
*   S3 Transfer Acceleration
    
    (Correct)
    

#### Explanation

Amazon S3 Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and your Amazon S3 bucket. S3 Transfer Acceleration leverages Amazon CloudFront’s globally distributed AWS Edge Locations.

**CORRECT:** "S3 Transfer Acceleration" is the correct answer.

**INCORRECT:** "S3 Static Websites" is incorrect. Amazon S3 can also be used to host static websites but this does not assist with the performance of uploads to S3.

**INCORRECT:** "S3 Copy" is incorrect. With S3 copy you can create a copy of objects up to 5GB in size in a single atomic operation.

**INCORRECT:** "Multipart Upload" is incorrect. Multipart upload can be used to speed up uploads to S3.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html)

  

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-storage/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-storage/)

Question 10: Incorrect

Which of the following represent economic advantages of moving to the AWS cloud? (Select TWO.)

*   Reduce the need to manage applications
    
    (Incorrect)
    
*   Increase efficiencies through automation
    
    (Correct)
    
*   Reduce the rate of change
    
*   Reduce the need to manage infrastructure
    
    (Correct)
    
*   Increase time to market for new applications
    

#### Explanation

With the AWS Cloud you can increase efficiency through the use of automation and reduce the need to manage infrastructure, allowing you to concentrate on managing applications instead.

**CORRECT:** "Increase efficiencies through automation" is a correct answer.

**CORRECT:** "Reduce the need to manage infrastructure" is also a correct answer.

**INCORRECT:** "Reduce the need to manage applications" is incorrect. You do not reduce the need to manage applications in most cases.

**INCORRECT:** "Reduce the rate of change" is incorrect. Reducing the rate of change is not something organization’s strive for in the cloud (usually faster development cycles are preferred) so it does not represent a valid economic advantage/

**INCORRECT:** "Increase time to market for new applications" is incorrect. You want to reduce not increase time to market for new applications

**References:**

[https://d1.awsstatic.com/whitepapers/introduction-to-aws-cloud-economics-final.pdf](https://d1.awsstatic.com/whitepapers/introduction-to-aws-cloud-economics-final.pdf)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-computing-concepts/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-computing-concepts/)

Question 11: Incorrect

Which of the options below are recommendations in the security pillar of the well-architected framework? (Select TWO.)

*   Enable traceability
    
    (Correct)
    
*   Apply security at the application layer
    
    (Incorrect)
    
*   Automate security best practices
    
    (Correct)
    
*   Protect data when it is at rest only
    
*   Expect to be secure
    

#### Explanation

The security pillar includes the ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies

There are six design principles for security in the cloud:

– Implement a strong identity foundation.

– Enable traceability.

– Apply security at all layers.

– Automate security best practices.

– Protect data in transit and at rest.

– Prepare for security events.

**CORRECT:** "Enable traceability" is the correct answer.

**CORRECT:** "Automate security best practices" is the correct answer.

**INCORRECT:** "Apply security at the application layer" is incorrect. Please refer to the design principles above.

**INCORRECT:** "Protect data when it is at rest only" is incorrect. Please refer to the design principles above.

**INCORRECT:** "Expect to be secure" is incorrect. Please refer to the design principles above.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/)

Question 12: Correct

Which pricing options are available when using Amazon EC2 Reserved Instances? (Select TWO.)

*   Capacity upfront
    
*   All upfront
    
    (Correct)
    
*   Mainly upfront
    
*   Partial upfront
    
    (Correct)
    
*   Enterprise upfront
    

#### Explanation

Amazon EC2 Reserved Instances (RI) provide a significant discount (up to 75%) compared to On-Demand pricing and provide a capacity reservation when used in a specific Availability Zone. Payment options include All Upfront, Partial Upfront, and No Upfront.

**CORRECT:** "All upfront" is a correct answer.

**CORRECT:** "Partial upfront" is also a correct answer.

**INCORRECT:** "Capacity upfront" is incorrect as this is not a pricing option.

**INCORRECT:** "Mainly upfront" is incorrect as this is not a pricing option.

**INCORRECT:** "Enterprise upfront" is incorrect as this is not a pricing option.

**References:**

[https://aws.amazon.com/ec2/pricing/reserved-instances/](https://aws.amazon.com/ec2/pricing/reserved-instances/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 13: Incorrect

Under the AWS shared responsibility model what is AWS responsible for? (Select TWO.)

*   Physical security of the data center
    
    (Correct)
    
*   Replacement and disposal of disk drives
    
    (Correct)
    
*   Configuration of security groups
    
*   Patch management of operating systems
    
*   Encryption of customer data
    

#### Explanation

AWS are responsible for “Security **of** the Cloud” and customers are responsible for “Security **in** the Cloud”.

AWS are responsible for items such as the physical security of the DC, replacement of old disk drives, and patch management of the infrastructure.

Customers are responsible for items such as configuring security groups, network ACLs, patching their operating systems and encrypting their data

**CORRECT:** "Physical security of the data center" is the correct answer.

**CORRECT:** "Replacement and disposal of disk drives" is the correct answer.

**INCORRECT:** "Configuration of security groups" is incorrect as this is a customer responsibility.

**INCORRECT:** "Patch management of operating systems" is incorrect as this is a customer responsibility.

**INCORRECT:** "Encryption of customer data" is incorrect as this is a customer responsibility.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-shared-responsibility-model/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-shared-responsibility-model/)

Question 14: Correct

Which AWS service is known as a “serverless” service and runs code as functions triggered by events?

*   Amazon ECS
    
*   AWS Lambda
    
    (Correct)
    
*   Amazon CodeDeploy
    
*   Amazon Cognito
    

#### Explanation

AWS Lambda lets you run code as functions without provisioning or managing servers. Lambda-based applications (also referred to as serverless applications) are composed of functions triggered by events. With serverless computing, your application still runs on servers, but all the server management is done by AWS.

**CORRECT:** "AWS Lambda" is the correct answer.

**INCORRECT:** "Amazon ECS" is incorrect. Amazon Elastic Container Service (ECS) is a highly scalable, high performance container management service that supports Docker containers and allows you to easily run applications on a managed cluster of Amazon EC2 instances.

**INCORRECT:** "Amazon CodeDeploy" is incorrect. AWS CodeDeploy is a fully managed deployment service that automates software deployments to a variety of compute services such as Amazon EC2, AWS Lambda, and your on-premises servers.

**INCORRECT:** "Amazon Cognito" is incorrect. Amazon Cognito lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily.

**References:**

[https://aws.amazon.com/lambda/features/](https://aws.amazon.com/lambda/features/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-compute/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-compute/)

Question 15: Correct

Which statement best describes Amazon Route 53?

*   Amazon Route 53 is a service that enables routing within VPCs in an account
    
*   Amazon Route 53 is a highly available and scalable Domain Name System (DNS) service
    
    (Correct)
    
*   Amazon Route 53 enables hybrid cloud models by extending an organization's on-premise networks into the AWS cloud
    
*   Amazon Route 53 is a service for distributing incoming connections between a fleet of registered EC2 instances
    

#### Explanation

Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. It is designed to give developers and businesses an extremely reliable and cost effective way to route end users to Internet applications by translating names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers use to connect to each other. Amazon Route 53 is fully compliant with IPv6 as well.

**CORRECT:** "Amazon Route 53 is a highly available and scalable Domain Name System (DNS) service" is the correct answer.

**INCORRECT:** "Amazon Route 53 is a service that enables routing within VPCs in an account" is incorrect. The VPC router performs routing within a VPC.

**INCORRECT:** "Amazon Route 53 enables hybrid cloud models by extending an organization's on-premise networks into the AWS cloud" is incorrect. Direct Connect enables hybrid cloud models by extending an organization’s on-premise networks into the AWS cloud.

**INCORRECT:** "Amazon Route 53 is a service for distributing incoming connections between a fleet of registered EC2 instances" is incorrect. Auto Scaling is a service for distributing incoming connections between a fleet of registered EC2 instances.

**References:**

[https://aws.amazon.com/route53/](https://aws.amazon.com/route53/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/content-delivery-and-dns-services/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/content-delivery-and-dns-services/)

Question 16: Correct

Which service provides a way to convert video and audio files from their source format into versions that will playback on devices like smartphones, tablets and PCs?

*   Amazon Elastic Transcoder
    
    (Correct)
    
*   AWS Glue
    
*   Amazon Rekognition
    
*   Amazon Comprehend
    

#### Explanation

Amazon Elastic Transcoder is a highly scalable, easy to use and cost-effective way for developers and businesses to convert (or “transcode”) video and audio files from their source format into versions that will playback on devices like smartphones, tablets and PCs.

**CORRECT:** "Amazon Elastic Transcoder" is the correct answer.

**INCORRECT:** "AWS Glue" is incorrect. AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics.

**INCORRECT:** "Amazon Rekognition" is incorrect. Amazon Rekognition makes it easy to add image and video analysis to your applications.

**INCORRECT:** "Amazon Comprehend" is incorrect. Amazon Comprehend is a natural language processing (NLP) service that uses machine learning to find insights and relationships in text.

**References:**

[https://aws.amazon.com/elastictranscoder/](https://aws.amazon.com/elastictranscoder/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 17: Incorrect

When using AWS Organizations with consolidated billing what are two valid best practices? (Select TWO.)

*   Always enable multi-factor authentication (MFA) on the root account
    
    (Correct)
    
*   Always use a straightforward password on the root account
    
*   The paying account should be used for billing purposes only
    
    (Correct)
    
*   Use the paying account for deploying resources
    
    (Incorrect)
    
*   Never exceed the limit of 20 linked accounts
    

#### Explanation

When using AWS Organizations with consolidated billing, best practices include:

– Always enable multi-factor authentication (MFA) on the root account.

– Always use a strong and complex password on the root account.

– The Paying account should be used for billing purposes only. Do not deploy resources into the Paying account.

There is a default limit of 20 linked accounts but this can be extended and there is no reason why you should stick to a maximum of 20 accounts.

**CORRECT:** "Always enable multi-factor authentication (MFA) on the root account" is a correct answer.

**CORRECT:** "The paying account should be used for billing purposes only" is also a correct answer.

**INCORRECT:** "Always use a straightforward password on the root account" is incorrect as you should use a complex password.

**INCORRECT:** "Use the paying account for deploying resources" is incorrect as you should deploy resources in the linked accounts.

**INCORRECT:** "Never exceed the limit of 20 linked accounts" is incorrect as you can extend the default limit.

**References:**

[https://aws.amazon.com/organizations/](https://aws.amazon.com/organizations/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 18: Correct

Which of the options below are recommendations in the reliability pillar of the well-architected framework? (Select TWO.)

*   Use ad-hoc recovery procedures
    
*   Automatically recover from failure
    
    (Correct)
    
*   Scale vertically to increase aggregate system availability
    
*   Attempt to accurately estimate capacity requirements
    
*   Manage change in automation
    
    (Correct)
    

#### Explanation

The reliability pillar includes the ability of a system to recover from infrastructure or service disruptions, dynamically acquire computing resources to meet demand, and mitigate disruptions such as misconfigurations or transient network issues.

There are five design principles for reliability in the cloud:

– Test recovery procedures.

– Automatically recover from failure.

– Scale horizontally to increase aggregate system availability.

– Stop guessing capacity.

– Manage change in automation.

**CORRECT:** "Automatically recover from failure" is a correct answer.

**CORRECT:** "Manage change in automation" is also a correct answer.

**INCORRECT:** "Use ad-hoc recovery procedures" is incorrect. Please refer to the design principles above.

**INCORRECT:** "Scale vertically to increase aggregate system availability" is incorrect. Please refer to the design principles above.

**INCORRECT:** "Manage change in automation" is incorrect. Please refer to the design principles above.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/)

Question 19: Correct

Which AWS support plan comes with a Technical Account Manager (TAM)?

*   Basic
    
*   Developer
    
*   Business
    
*   Enterprise
    
    (Correct)
    

#### Explanation

Only the Enterprise plan comes with a TAM.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-30_03-14-17-ecbf115d83d23421c0d301a5f3fbd873.jpg)

**CORRECT:** "Enterprise" is the correct answer.

**INCORRECT:** "Basic" is incorrect as this plan does not come with a TAM.

**INCORRECT:** "Developer" is incorrect as this plan does not come with a TAM.

**INCORRECT:** "Business" is incorrect as this plan does not come with a TAM.

**References:**

[https://aws.amazon.com/premiumsupport/plans/](https://aws.amazon.com/premiumsupport/plans/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 20: Correct

Which service provides the ability to simply upload applications and have AWS handle the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring?

*   Amazon EC2
    
*   AWS Elastic Beanstalk
    
    (Correct)
    
*   Amazon EC2 Auto Scaling
    
*   AWS OpsWorks
    

#### Explanation

AWS Elastic Beanstalk can be used to quickly deploy and manage applications in the AWS Cloud. Developers upload applications and Elastic Beanstalk handles the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring. Considered a Platform as a Service (PaaS) solution. Supports Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker web applications.

**CORRECT:** "AWS Elastic Beanstalk" is the correct answer.

**INCORRECT:** "Amazon EC2" is incorrect. Amazon EC2 is an IaaS solution that provides unmanaged instances that you can deploy with a variety of operating systems.

**INCORRECT:** "Amazon EC2 Auto Scaling" is incorrect. Amazon EC2 Auto Scaling provides elasticity for your applications by automatically launching or terminating EC2 instances according to application load or schedules you define.

**INCORRECT:** "AWS OpsWorks" is incorrect. AWS OpsWorks provides a managed service for Chef and Puppet. This service is involved with automation and configuration management.

**References:**

[https://aws.amazon.com/elasticbeanstalk/](https://aws.amazon.com/elasticbeanstalk/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 21: Correct

You are concerned that you may be getting close to some of the default service limits for several AWS services. What AWS tool can be used to display current usage and limits?

*   AWS CloudWatch
    
*   AWS Personal Health Dashboard
    
*   AWS Trusted Advisor
    
    (Correct)
    
*   AWS Systems Manager
    

#### Explanation

Trusted Advisor is an online resource to help you reduce cost, increase performance, and improve security by optimizing your AWS environment. Trusted Advisor provides real time guidance to help you provision your resources following AWS best practices. Offers a Service Limits check (in the Performance category) that displays your usage and limits for some aspects of some services.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-30_03-17-22-9987968964dbc133622f84ead7ca157a.jpg)

**CORRECT:** "AWS Trusted Advisor" is the correct answer.

**INCORRECT:** "AWS CloudWatch" is incorrect. Amazon CloudWatch is a monitoring and management service built for developers, system operators, site reliability engineers (SRE), and IT managers.

**INCORRECT:** "AWS Personal Health Dashboard" is incorrect. AWS Personal Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you.

**INCORRECT:** "AWS Systems Manager" is incorrect. AWS Systems Manager gives you visibility and control of your infrastructure on AWS.

**References:**

[https://docs.aws.amazon.com/general/latest/gr/aws\_service\_limits.html](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 22: Correct

You need to run a production process that will use several EC2 instances and run constantly on an ongoing basis. The process cannot be interrupted or restarted without issue. What EC2 pricing model would be best for this workload?

*   Reserved instances
    
    (Correct)
    
*   Spot instances
    
*   On-demand instances
    
*   Flexible instances
    

#### Explanation

Reserved Instance (RIs) provide you with a significant discount (up to 75%) compared to On-Demand instance pricing. You have the flexibility to change families, OS types, and tenancies while benefitting from RI pricing when you use Convertible RIs.

In this scenario for a stable process that will run constantly on an ongoing basis RIs will be the most affordable solution.

**CORRECT:** "Reserved instances" is the correct answer.

**INCORRECT:** "Spot instances" is incorrect as the instance cannot be terminated.

**INCORRECT:** "On-demand instances" is incorrect as this would not be the most cost-effective option.

**INCORRECT:** "Flexible instances" is incorrect as there’s no such thing.

**References:**

[https://aws.amazon.com/ec2/pricing/reserved-instances/](https://aws.amazon.com/ec2/pricing/reserved-instances/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 23: Correct

Which AWS service does API Gateway integrate with to enable users from around the world to achieve the lowest possible latency for API requests and responses?

*   AWS Direct Connect
    
*   Amazon S3 Transfer Acceleration
    
*   Amazon CloudFront
    
    (Correct)
    
*   AWS Lambda
    

#### Explanation

Amazon CloudFront is used as the public endpoint for API Gateway. Provides reduced latency and distributed denial of service protection through the use of CloudFront.

**CORRECT:** "Amazon CloudFront" is the correct answer.

**INCORRECT:** "AWS Direct Connect" is incorrect. AWS Direct Connect is a cloud service solution that makes it easy to establish a dedicated network connection from your premises to AWS.

**INCORRECT:** "Amazon S3 Transfer Acceleration" is incorrect. Amazon S3 Transfer Acceleration is a bucket-level feature that enables faster data transfers to and from Amazon S3.

**INCORRECT:** "AWS Lambda" is incorrect. AWS Lambda lets you run code without provisioning or managing servers.

**References:**

[https://aws.amazon.com/cloudfront/](https://aws.amazon.com/cloudfront/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 24: Correct

Which of the below is a fully managed Amazon search service based on open source software?

*   AWS Elastic Beanstalk
    
*   AWS OpsWorks
    
*   Amazon CloudSearch
    
*   Amazon Elasticsearch
    
    (Correct)
    

#### Explanation

Amazon Elasticsearch Service is a fully managed service that makes it easy for you to deploy, secure, operate, and scale Elasticsearch to search, analyze, and visualize data in real-time. Elasticsearch is based on open source software.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-30_03-22-31-28a322ea0ed87f5e69139f418f1abb30.jpg)

**CORRECT:** "Amazon Elasticsearch" is the correct answer.

**INCORRECT:** "AWS Elastic Beanstalk" is incorrect. AWS Elastic Beanstalk is used for deploying and managing EC2 instances and related services on AWS.

**INCORRECT:** "AWS OpsWorks" is incorrect. AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet.

**INCORRECT:** "Amazon CloudSearch" is incorrect. Amazon CloudSearch is a managed service in the AWS Cloud. Unlike Elasticsearch, this is not based on open source software.

**References:**

[https://aws.amazon.com/elasticsearch-service/](https://aws.amazon.com/elasticsearch-service/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 25: Correct

Which service can an organization use to track API activity within their account?

*   AWS CloudTrail
    
    (Correct)
    
*   Amazon CloudWatch
    
*   AWS IAM
    
*   AWS CloudHSM
    

Question 26: Correct

What tool provides real time guidance to help you provision your resources following best practices in the areas of cost optimization, performance, security and fault tolerance?

*   AWS Inspector
    
*   AWS Trusted Advisor
    
    (Correct)
    
*   AWS Personal Health Dashboard
    
*   AWS IAM
    

#### Explanation

Trusted Advisor is an online resource that helps to reduce cost, increase performance and improve security by optimizing your AWS environment. Trusted Advisor provides real time guidance to help you provision your resources following best practices. Advisor will advise you on Cost Optimization, Performance, Security, and Fault Tolerance

**CORRECT:** "AWS Trusted Advisor" is the correct answer.

**INCORRECT:** "AWS Inspector" is incorrect. Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS.

**INCORRECT:** "AWS Personal Health Dashboard" is incorrect. AWS Personal Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you.

**INCORRECT:** "AWS IAM" is incorrect. AWS Identity and Access Management is an identity service that provide authentication and authorization services.

**References:**

[https://aws.amazon.com/premiumsupport/technology/trusted-advisor/](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-security/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-security/)

Question 27: Correct

What is the best way for an organization to transfer hundreds of terabytes of data from their on-premise data center into Amazon S3 with limited bandwidth available?

*   Use S3 Transfer Acceleration
    
*   Apply compression before uploading
    
*   Use AWS Snowball
    
    (Correct)
    
*   Use Amazon CloudFront
    

#### Explanation

Snowball is a petabyte-scale data transport solution that uses devices designed to be secure to transfer large amounts of data into and out of the AWS Cloud. Using Snowball addresses common challenges with large-scale data transfers including high network costs, long transfer times, and security concerns

**CORRECT:** "Use AWS Snowball" is the correct answer.

**INCORRECT:** "Use S3 Transfer Acceleration" is incorrect. Amazon S3 Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. However, for these volumes of data Snowball is a better choice.

**INCORRECT:** "Apply compression before uploading" is incorrect as for this volume of data Snowball should be used.

**INCORRECT:** "Use Amazon CloudFront" is incorrect as this cannot be used for uploading large quantities of data to Amazon S3.

**References:**

[https://aws.amazon.com/snowball/](https://aws.amazon.com/snowball/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-storage/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-storage/)

Question 28: Correct

Which database allows you to scale at the push of a button without incurring any downtime?

*   Amazon RDS
    
*   Amazon EMR
    
*   Amazon DynamoDB
    
    (Correct)
    
*   Amazon RedShift
    

#### Explanation

Amazon Dynamo DB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. Push button scaling means that you can scale the DB at any time without incurring downtime.

All other databases are based on EC2 instances and therefore you must increase the instance size to scale which will incur downtime.

**CORRECT:** "Amazon DynamoDB" is the correct answer.

**INCORRECT:** "Amazon RDS" is incorrect as explained above.

**INCORRECT:** "Amazon EMR" is incorrect as explained above.

**INCORRECT:** "Amazon RedShift" is incorrect as explained above.

**References:**

[https://aws.amazon.com/dynamodb/](https://aws.amazon.com/dynamodb/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-databases/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-databases/)

Question 29: Correct

What are the charges for using Amazon Glacier? (Select TWO.)

*   Data transferred into Glacier
    
*   Retrieval requests
    
    (Correct)
    
*   Data storage
    
    (Correct)
    
*   Enhanced networking
    
*   Number of Availability Zones
    

#### Explanation

With Amazon Glacier you pay for storage on a per GB / month basis, retrieval requests and quantity (based on expedited, standard, or bulk), and data transfer out of Glacier.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-30_03-32-21-c0f8ce130d356563df43826c17fe733b.jpg)

**CORRECT:** "Retrieval requests" is the correct answer.

**CORRECT:** "Data storage" is the correct answer.

**INCORRECT:** "Data transferred into Glacier" is incorrect. You do not pay for data transferred in and there are no minimum storage fees.

**INCORRECT:** "Enhanced networking" is incorrect. Enhanced networking is a feature of EC2.

**INCORRECT:** "Number of Availability Zones" is incorrect. You do not pay for the number of AZs.

**References:**

[https://aws.amazon.com/s3/storage-classes/](https://aws.amazon.com/s3/storage-classes/)

[https://aws.amazon.com/glacier/pricing/](https://aws.amazon.com/glacier/pricing/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 30: Correct

Which descriptions are correct regarding cloud deployment models? (Select TWO.)

*   With the public cloud the consumer organization typically owns and manages the infrastructure
    
*   With the private cloud the consumer organization typically incurs OPEX costs for usage
    
*   With the hybrid cloud, multiple private clouds are connected
    
*   With the public cloud the consumer organization typically incurs OPEX costs for usage
    
    (Correct)
    
*   With the private cloud the consumer organization typically owns and manages the infrastructure
    
    (Correct)
    

#### Explanation

With public cloud the consumer organization typically incurs OPEX costs as they do not own the infrastructure and just pay usage costs.

**CORRECT:** "With the public cloud the consumer organization typically incurs OPEX costs for usage" is a correct answer.

**CORRECT:** "With the private cloud the consumer organization typically owns and manages the infrastructure" is also a correct answer.

**INCORRECT:** "With the public cloud the consumer organization typically owns and manages the infrastructure" is incorrect as that is the situation with private clouds.

**INCORRECT:** "With the private cloud the consumer organization typically incurs OPEX costs for usage" is incorrect. With the private cloud the consumer organization typically owns the infrastructure and will often manage it themselves or use a third-party organization to manage it for them. This model is largely CAPEX driven.

**INCORRECT:** "With the hybrid cloud, multiple private clouds are connected" is incorrect. Hybrid clouds are created when you connect private and public clouds together.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-computing-concepts/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-computing-concepts/)

Question 31: Correct

Which of the following statements are correct about the benefits of AWS Direct Connect? (Select TWO.)

*   Quick to implement
    
*   Increased reliability (predictable performance)
    
    (Correct)
    
*   Lower cost than a VPN
    
*   Increased bandwidth (predictable bandwidth)
    
    (Correct)
    
*   Uses redundant paths across the Internet
    

#### Explanation

AWS Direct Connect is a network service that provides an alternative to using the Internet to connect customers’ on premise sites to AWS.

Data is transmitted through a private network connection between AWS and a customer’s data center or corporate network.

Benefits of AWS Direct Connect:

– Reduce cost when using large volumes of traffic.

– Increase reliability (predictable performance).

– Increase bandwidth (predictable bandwidth).

– Decrease latency.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-30_03-39-19-1fe5d5216c16b557ee582b2fc8e6db01.jpg)

**CORRECT:** "Increased reliability (predictable performance)" is a correct answer.

**CORRECT:** "Increased bandwidth (predictable bandwidth)" is also a correct answer.

**INCORRECT:** "Quick to implement" is incorrect. Direct Connect is not fast to implement as it can take weeks to months to setup (use VPN for fast deployment times).

**INCORRECT:** "Lower cost than a VPN" is incorrect. Direct Connect is more expensive than VPN.

**INCORRECT:** "Uses redundant paths across the Internet" is incorrect. Direct Connect uses private network connections, it does not use redundant paths over the Internet.

**References:**

[https://aws.amazon.com/directconnect/](https://aws.amazon.com/directconnect/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-networking/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-networking/)

Question 32: Correct

Which AWS service lets you use Chef and Puppet to automate how servers are configured, deployed, and managed across your Amazon EC2 instances or on-premises compute environments?

*   AWS Elastic Beanstalk
    
*   AWS CloudFormation
    
*   AWS Systems Manager
    
*   AWS OpsWorks
    
    (Correct)
    

#### Explanation

AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet. OpsWorks lets you use Chef and Puppet to automate how servers are configured, deployed, and managed across your Amazon EC2 instances or on-premises compute environments.

**CORRECT:** "AWS OpsWorks" is the correct answer.

**INCORRECT:** "AWS Elastic Beanstalk" is incorrect. This service does not use Chef or Puppet.

**INCORRECT:** "AWS CloudFormation" is incorrect. This service does not use Chef or Puppet.

**INCORRECT:** "AWS Systems Manager" is incorrect. This service does not use Chef or Puppet.

**References:**

[https://aws.amazon.com/opsworks/](https://aws.amazon.com/opsworks/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 33: Correct

Which AWS database service provides a fully managed data warehouse that can be analyzed using SQL tools and business intelligence tools?

*   Amazon RDS
    
*   Amazon DynamoDB
    
*   Amazon RedShift
    
    (Correct)
    
*   Amazon ElastiCache
    

#### Explanation

Amazon RedShift is a fully managed data warehouse service designed to handle petabytes of data for analysis. Data can be analyzed with standard SQL tools and business intelligence tools. RedShift allows you to run complex analytic queries against petabytes of structured data.

**CORRECT:** "Amazon RedShift" is the correct answer.

**INCORRECT:** "Amazon RDS" is incorrect. RDS is Amazon’s transactional relational database.

**INCORRECT:** "Amazon DynamoDB" is incorrect. DynamoDB is Amazon’s non-relational database service.

**INCORRECT:** "Amazon ElastiCache" is incorrect. ElastiCache is a data caching service that is used to help improve the speed/performance of web applications running on AWS.

**References:**

[https://aws.amazon.com/redshift/](https://aws.amazon.com/redshift/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-databases/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-databases/)

Question 34: Correct

Which service can be used to create sophisticated, interactive graph applications?

*   Amazon RedShift
    
*   Amazon Neptune
    
    (Correct)
    
*   AWS X-Ray
    
*   Amazon Athena
    

#### Explanation

Amazon Neptune is a fast, reliable, fully-managed graph database service that makes it easy to build and run applications that work with highly connected datasets. With Amazon Neptune, you can create sophisticated, interactive graph applications that can query billions of relationships in milliseconds.

**CORRECT:** "Amazon Neptune" is the correct answer.

**INCORRECT:** "Amazon RedShift" is incorrect. Amazon Redshift is a fast, scalable data warehouse that makes it simple and cost-effective to analyze all your data across your data warehouse and data lake.

**INCORRECT:** "AWS X-Ray" is incorrect. AWS X-Ray helps developers analyze and debug production, distributed applications, such as those built using a microservices architecture.

**INCORRECT:** "Amazon Athena" is incorrect. Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL.

**References:**

[https://aws.amazon.com/neptune/](https://aws.amazon.com/neptune/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 35: Correct

When using Amazon IAM, what authentication methods are available to use? (Select TWO.)

*   Client certificates
    
*   Access keys
    
    (Correct)
    
*   AWS KMS
    
*   Server certificates
    
    (Correct)
    
*   AES 256
    

#### Explanation

Supported authentication methods include console passwords, access keys and server certificates.

Access keys are a combination of an access key ID and a secret access key and can be used to make programmatic calls to AWS.

Server certificates are SSL/TLS certificates that you can use to authenticate with some AWS services.

**CORRECT:** "Access keys" is a correct answer.

**CORRECT:** "Server certificates" is also a correct answer.

**INCORRECT:** "Client certificates" is incorrect. Client certificates are not a valid IAM authentication method.

**INCORRECT:** "AWS KMS" is incorrect. AWS Key Management Service (KMS) is used for managing encryption keys and is not used for authentication..

**INCORRECT:** "AES 256" is incorrect. AES 256 is an encryption algorithm, not an authentication method.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/)

Question 36: Correct

Which statement best describes elasticity in the cloud?

*   The ability to scale resources up or down and only pay for what you use
    
    (Correct)
    
*   The ability for a system to recover from the failure of a single component
    
*   A flexible model of code development that results in faster deployment times
    
*   A pricing model that allows upfront payments and term commitments to reduce cost
    

#### Explanation

Elasticity is the ability to scale resources up or down and only pay for what you use. A great example is Auto Scaling which launches and terminates EC2 instances based on the amount of load.

**CORRECT:** "The ability to scale resources up or down and only pay for what you use" is the correct answer.

**INCORRECT:** "The ability for a system to recover from the failure of a single component" is incorrect. This is a description of fault tolerance.

**INCORRECT:** "A flexible model of code development that results in faster deployment times" is incorrect. This is a description of agile development.

**INCORRECT:** "A pricing model that allows upfront payments and term commitments to reduce cost" is incorrect. This is a description of reserved instances.

**References:**

[https://aws.amazon.com/architecture/well-architected/](https://aws.amazon.com/architecture/well-architected/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/)

Question 37: Incorrect

What are the benefits of using reserved instances? (Select TWO.)

*   Reduced cost
    
    (Correct)
    
*   More flexibility
    
    (Incorrect)
    
*   Reserve capacity
    
    (Correct)
    
*   Uses dedicated hardware
    
*   High availability
    

#### Explanation

With reserved instances you commit to a 1- or 3-year term and get a significant discount from the on-demand rate. You can also reserve capacity in an availability zone with reserved instances.

**CORRECT:** "Reduced cost" is a correct answer.

**CORRECT:** "Reserve capacity" is also a correct answer.

**INCORRECT:** "More flexibility" is incorrect. You don’t get more flexibility with reserved instances. If you need flexibility on-demand is better but more costly.

**INCORRECT:** "Uses dedicated hardware" is incorrect. Reserved instances are different to dedicated instances. Dedicates instances and dedicates hosts use dedicated hardware but reserved instances do not.

**INCORRECT:** "High availability" is incorrect. You do not get high availability with reserved instances; this is a pricing model.

**References:**

[https://aws.amazon.com/ec2/pricing/reserved-instances/](https://aws.amazon.com/ec2/pricing/reserved-instances/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 38: Correct

Which AWS tools can be used for automation? (Select TWO.)

*   AWS Elastic Beanstalk
    
    (Correct)
    
*   Elastic Load Balancing
    
*   AWS CloudFormation
    
    (Correct)
    
*   Amazon Elastic File System (EFS)
    
*   AWS Lambda
    

#### Explanation

AWS Elastic Beanstalk and AWS CloudFormation are both examples of automation. Beanstalk is a platform service that leverages the automation capabilities of CloudFormation to build out application architectures.

**CORRECT:** "AWS Elastic Beanstalk" is a correct answer.

**CORRECT:** "AWS CloudFormation" is also a correct answer.

**INCORRECT:** "Elastic Load Balancing" is incorrect. Elastic Load Balancing (ELB) is used for distributing incoming connections to Amazon EC2 instances. This is not an example of automation; it is load balancing.

**INCORRECT:** "Amazon Elastic File System (EFS)" is incorrect. Amazon EFS is a file system.

**INCORRECT:** "AWS Lambda" is incorrect. AWS Lambda is a compute service, not an automation service.

**References:**

[https://aws.amazon.com/elasticbeanstalk/](https://aws.amazon.com/elasticbeanstalk/)

[https://aws.amazon.com/cloudformation/](https://aws.amazon.com/cloudformation/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 39: Correct

Which IAM entity can be used for assigning permissions to AWS services?

*   IAM Access Key ID and Secret Access Key
    
*   IAM Policy
    
*   IAM Role
    
    (Correct)
    
*   Security Token Service (STS)
    

#### Explanation

With IAM Roles you can delegate permissions to resources for users and services without using permanent credentials (e.g. username and password). To do so you can create a role and assign an IAM policy to the role that has the permissions required.

**CORRECT:** "IAM Role" is the correct answer.

**INCORRECT:** "IAM Access Key ID and Secret Access Key" is incorrect. An access key ID and secret access key are assigned to IAM users and used for programmatic access using the API or CLI.

**INCORRECT:** "IAM Policy" is incorrect. An IAM policy is a policy document that is used to define permissions that can be applied to users, groups and roles. You don’t apply the policy to the service, you apply it to the role. The role is then used to assign permissions to the AWS service.

**INCORRECT:** "Security Token Service (STS)" is incorrect. This service is used for gaining temporary security credentials.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_roles\_create\_for-service.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-service.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/)

Question 40: Correct

How does Amazon EC2 Auto Scaling help with resiliency?

*   By distributing connections to EC2 instances
    
*   By launching and terminating instances as needed
    
    (Correct)
    
*   By changing instance types to increase capacity
    
*   By automating the failover of applications
    

#### Explanation

Amazon EC2 Auto Scaling launches and terminates instances as demand changes. This helps with resiliency and high availability as it can also be set to ensure a minimum number of instances are always available.

**CORRECT:** "By launching and terminating instances as needed" is the correct answer.

**INCORRECT:** "By distributing connections to EC2 instances" is incorrect. Auto Scaling is not responsible for distributing connections to EC2 instances, that is a job for an Elastic Load Balancer (ELB).

**INCORRECT:** "By changing instance types to increase capacity" is incorrect. Auto Scaling does not change the instance type. You have to create a new launch configuration if you need to increase your instance size, this is not automatic.

**INCORRECT:** "By automating the failover of applications" is incorrect. Auto Scaling does not do application failover.

**References:**

[https://aws.amazon.com/ec2/autoscaling/](https://aws.amazon.com/ec2/autoscaling/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/elastic-load-balancing-and-auto-scaling/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/elastic-load-balancing-and-auto-scaling/)

Question 41: Correct

Your CTO wants to move to cloud. What cost advantages are there to moving to cloud?

*   You provision only what you need and adjust to peak load
    
    (Correct)
    
*   You can reduce your marketing costs
    
*   You don’t need to pay for application licensing
    
*   You get free data transfer into and out of the cloud
    

#### Explanation

One of the best benefits of cloud is that you can launch what you need to and automatically adjust your resources as demand changes. This means you only ever pay for what you’re using.

**CORRECT:** "You provision only what you need and adjust to peak load" is the correct answer.

**INCORRECT:** "You can reduce your marketing costs" is incorrect. You don’t reduce marketing costs when moving to the cloud, your organization still needs to do the same amount of marketing.

**INCORRECT:** "You don’t need to pay for application licensing" is incorrect. It is not true that you don’t need to pay for application licensing in the cloud. You still pay for your application licenses when running on Amazon EC2.

**INCORRECT:** "You get free data transfer into and out of the cloud" is incorrect. You do not get free bi-directional data transfer into and out of the cloud. AWS charge for outbound data transfer.

**References:**

[https://aws.amazon.com/pricing/](https://aws.amazon.com/pricing/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 42: Incorrect

How does the consolidated billing feature of AWS Organizations treat Reserved Instances that were purchased by another account in the organization?

*   All accounts in the organization are treated as one account so any account can receive the hourly cost benefit
    
    (Correct)
    
*   Only the master account can benefit from the hourly cost benefit of the reserved instances
    
    (Incorrect)
    
*   All accounts in the organization are treated as one account for volume discounts but not for reserved instances
    
*   AWS Organizations does not support any volume or reserved instance benefits across accounts, it is just a method of aggregating bills
    

#### Explanation

For billing purposes, the consolidated billing feature of AWS Organizations treats all the accounts in the organization as one account. This means that all accounts in the organization can receive the hourly cost benefit of Reserved Instances that are purchased by any other account.

**CORRECT:** "All accounts in the organization are treated as one account so any account can receive the hourly cost benefit" is the correct answer.

**INCORRECT:** "Only the master account can benefit from the hourly cost benefit of the reserved instances" is incorrect as explained above.

**INCORRECT:** "All accounts in the organization are treated as one account for volume discounts but not for reserved instances" is incorrect as explained above..

**INCORRECT:** "AWS Organizations does not support any volume or reserved instance benefits across accounts, it is just a method of aggregating bills" is incorrect as explained above.

**References:**

[https://aws.amazon.com/organizations/](https://aws.amazon.com/organizations/)

**Save time with our exam-specific cheat sheets:**

[https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ri-behavior.html](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ri-behavior.html)

Question 43: Correct

Which of the below AWS services supports automated backups as a default configuration?

*   Amazon S3
    
*   Amazon RDS
    
    (Correct)
    
*   Amazon EC2
    
*   Amazon EBS
    

#### Explanation

Amazon RDS automated backups allow point in time recovery to any point within the retention period down to a second. When automated backups are turned on for your DB Instance, Amazon RDS automatically performs a full daily snapshot of your data (during your preferred backup window) and captures transaction logs (as updates to your DB Instance are made). Automated backups are enabled by default and data is stored on S3 and is equal to the size of the DB

**CORRECT:** "Amazon RDS" is the correct answer.

**INCORRECT:** "Amazon S3" is incorrect. Amazon S3 objects are replicated across multiple facilities. You can also archive data onto Amazon Glacier and use versioning to maintain copies of older versions of objects

**INCORRECT:** "Amazon EC2" is incorrect. EC2 instances using EBS volumes can be backed up by creating a snapshot of the EBS volume.

**INCORRECT:** "Amazon EBS" is incorrect. EC2 instances using EBS volumes can be backed up by creating a snapshot of the EBS volume.

**References:**

[https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER\_WorkingWithAutomatedBackups.html](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-databases/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-databases/)

Question 44: Incorrect

What are the advantages of Availability Zones? (Select TWO.)

*   They allow regional disaster recovery
    
    (Incorrect)
    
*   They provide fault isolation
    
    (Correct)
    
*   They enable the caching of data for faster delivery to end users
    
*   They are connected by low-latency network connections
    
    (Correct)
    
*   They enable you to connect your on-premises networks to AWS to form a hybrid cloud
    

#### Explanation

Each AWS region contains multiple distinct locations called Availability Zones (AZs). Each AZ is engineered to be isolated from failures in other AZs. An AZ is a data center, and in some cases, an AZ consists of multiple data centers.

AZs within a region provide inexpensive, low-latency network connectivity to other zones in the same region. This allows you to replicate your data across data centers in a synchronous manner so that failover can be automated and be transparent for your users.

**CORRECT:** "They provide fault isolation" is a correct answer.

**CORRECT:** "They are connected by low-latency network connections" is also a correct answer.

**INCORRECT:** "They allow regional disaster recovery" is incorrect. An AZ enables fault tolerance and high availability for your applications within a region not across regions.

**INCORRECT:** "They enable the caching of data for faster delivery to end users" is incorrect. CloudFront is the technology that is used to enable caching of data for faster delivery to end users.

**INCORRECT:** "They enable you to connect your on-premises networks to AWS to form a hybrid cloud" is incorrect. Direct Connect is the technology that is used to connect your on-premises network to AWS to form a hybrid cloud.

**References:**

[https://aws.amazon.com/about-aws/global-infrastructure/](https://aws.amazon.com/about-aws/global-infrastructure/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/)

Question 45: Correct

Which Amazon EC2 Reserved Instance type enables you to match your capacity reservation to predictable recurring dates and times?

*   Standard RI
    
*   Convertible RI
    
*   Scheduled RI
    
    (Correct)
    
*   Customized RI
    

#### Explanation

With RIs, you can choose the type that best fits your applications needs.

**Standard RIs**: These provide the most significant discount (up to 75% off On-Demand) and are best suited for steady-state usage.

**Convertible RIs**: These provide a discount (up to 54% off On-Demand) and the capability to change the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value. Like Standard RIs, Convertible RIs are best suited for steady-state usage.

**Scheduled RIs**: These are available to launch within the time windows you reserve. This option allows you to match your capacity reservation to a predictable recurring schedule that only requires a fraction of a day, a week, or a month.

**CORRECT:** "Scheduled RI" is the correct answer.

**INCORRECT:** "Standard RI" is incorrect as it does not allow you to match your capacity reservation to predictable recurring dates and times.

**INCORRECT:** "Convertible RI" is incorrect as it does not allow you to match your capacity reservation to predictable recurring dates and times.

**INCORRECT:** "Customized RI" is incorrect. This is not a valid type of RI.

**References:**

[https://aws.amazon.com/ec2/pricing/reserved-instances/](https://aws.amazon.com/ec2/pricing/reserved-instances/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 46: Correct

Which of the options below are recommendations in the cost optimization pillar of the well-architected framework? (choose 2)

*   Adopt a consumption model
    
    (Correct)
    
*   Adopt a capital expenditure model
    
*   Start spending money on data center operations
    
*   Analyze and attribute expenditure
    
    (Correct)
    
*   Manage your services independently
    

#### Explanation

The cost optimization pillar includes the ability to avoid or eliminate unneeded cost or suboptimal resource.

There are five design principles for cost optimization in the cloud:

– Adopt a consumption model.

– Measure overall efficiency.

– Stop spending money on data center operations.

– Analyze and attribute expenditure.

– Use managed services to reduce cost of ownership.

**CORRECT:** "Adopt a consumption model" is the correct answer.

**CORRECT:** "Analyze and attribute expenditure" is the correct answer.

**INCORRECT:** "Adopt a capital expenditure model" is incorrect. Please refer to the design principles above.

**INCORRECT:** "Start spending money on data center operations" is incorrect. Please refer to the design principles above.

**INCORRECT:** "Manage your services independently" is incorrect. Please refer to the design principles above.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/)

Question 47: Correct

What are Edge locations used for?

*   They are used for terminating VPN connections
    
*   They are used by CloudFront for caching content
    
    (Correct)
    
*   They are the public-facing APIs for Amazon S3
    
*   They are used by regions for inter-region connectivity
    

#### Explanation

An edge location is used by CloudFront and is the location where content is cached (separate to AWS regions/AZs). Requests are automatically routed to the nearest edge location. Edge locations are not tied to Availability Zones or regions

**CORRECT:** "They are used by CloudFront for caching content" is the correct answer.

**INCORRECT:** "They are used for terminating VPN connections" is incorrect. They have nothing to do with VPN connections.

**INCORRECT:** "They are the public-facing APIs for Amazon S3" is incorrect. Amazon S3 does not run from Edge Locations.

**INCORRECT:** "They are used by regions for inter-region connectivity" is incorrect. They are not used for connectivity between regions.

**References:**

[https://wa.aws.amazon.com/wat.concept.edge-location.en.html](https://wa.aws.amazon.com/wat.concept.edge-location.en.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/content-delivery-and-dns-services/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/content-delivery-and-dns-services/)

Question 48: Correct

What is the best way to apply an organizational system to EC2 instances so they can be identified by descriptors such as purpose or department?

*   Use descriptive hostnames
    
*   Organize the instances into separate subnets
    
*   Apply tags
    
    (Correct)
    
*   Use the instance meta-data
    

#### Explanation

To help you manage your instances, images, and other Amazon EC2 resources, you can optionally assign your own metadata to each resource in the form of A tag is a label that you assign to an AWS resource. Each tag consists of a _key_ and an optional _value_, both of which you define. Tags enable you to categorize your AWS resources in different ways, for example, by purpose, owner, or environment.

**CORRECT:** "Apply tags" is the correct answer.

**INCORRECT:** "Use descriptive hostnames" is incorrect. Using descriptive hostnames or is a messy way to try and organize resources and lacks the power and flexibility of tagging.

**INCORRECT:** "Organize the instances into separate subnets" is incorrect. Organizing instances into separate subnets is also not an ideal method for organizing resources.

**INCORRECT:** "Use the instance meta-data" is incorrect. Storing information in instance meta-data is possible but you need to retrieve the information, tags enable you to do this more easily.

**References:**

[https://aws.amazon.com/answers/account-management/aws-tagging-strategies/](https://aws.amazon.com/answers/account-management/aws-tagging-strategies/)

Question 49: Correct

To ensure the security of your AWS account, what are two AWS best practices for managing access keys? (Select TWO.)

*   Don’t create any access keys, use IAM roles instead
    
*   Don’t generate an access key for the root account user
    
    (Correct)
    
*   Where possible, use IAM roles with temporary security credentials
    
    (Correct)
    
*   Rotate access keys daily
    
*   Use MFA for access keys
    

#### Explanation

Best practices include:

– Don’t generate an access key for the root account user.

– Use Temporary Security Credentials (IAM Roles) Instead of Long-Term Access Keys.

– Manage IAM User Access Keys Properly.

**CORRECT:** "Don’t generate an access key for the root account user" is a correct answer.

**CORRECT:** "Where possible, use IAM roles with temporary security credentials" is also a correct answer.

**INCORRECT:** "Don’t create any access keys, use IAM roles instead" is incorrect. You should use IAM roles where possible, but AWS do not recommend that you don’t create any access keys as they also have a purpose

**INCORRECT:** "Rotate access keys daily" is incorrect. Rotating access keys is a recommended practice, but doing it daily would be excessive and hard to manage.

**INCORRECT:** "Use MFA for access keys" is incorrect. You can use MFA for securing accounts, but it does not secure access keys

**References:**

[https://docs.aws.amazon.com/general/latest/gr/aws-access-keys-best-practices.html](https://docs.aws.amazon.com/general/latest/gr/aws-access-keys-best-practices.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/)

Question 50: Correct

An Amazon EC2 instance running the Amazon Linux 2 AMI is billed in what increment?

*   Per second
    
    (Correct)
    
*   Per hour
    
*   Per CPU
    
*   Per GB
    

#### Explanation

Amazon EC2 instances running Linux are billed in one second increments, with a minimum of 60 seconds.

**CORRECT:** "Per second" is the correct answer.

**INCORRECT:** "Per hour" is incorrect. You do not pay per hour.

**INCORRECT:** "Per CPU" is incorrect. You do not pay per CPU.

**INCORRECT:** "Per GB" is incorrect. You pay for Amazon EBS on a per GB of provisioned storage basis.

**References:**

[https://aws.amazon.com/about-aws/whats-new/2017/10/announcing-amazon-ec2-per-second-billing/](https://aws.amazon.com/about-aws/whats-new/2017/10/announcing-amazon-ec2-per-second-billing/)

[https://d1.awsstatic.com/whitepapers/aws\_pricing\_overview.pdf](https://d1.awsstatic.com/whitepapers/aws_pricing_overview.pdf)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 51: Correct

To gain greater discounts, which services can be reserved? (Select TWO.)

*   Amazon RedShift
    
    (Correct)
    
*   Amazon S3
    
*   AWS Lambda
    
*   Amazon DynamoDB
    
    (Correct)
    
*   Amazon CloudWatch
    

#### Explanation

Reservations provide you with greater discounts, up to 75%, by paying for capacity ahead of time. Some of the services you can reserve include: EC2, DynamoDB, ElastiCache, RDS, and RedShift.

**CORRECT:** "Amazon RedShift" is a correct answer.

**CORRECT:** "Amazon DynamoDB" is also a correct answer.

**INCORRECT:** "Amazon S3" is incorrect. You cannot reserve Amazon S3, you pay for what you use.

**INCORRECT:** "AWS Lambda" is incorrect. AWS Lambda is a service that provides functions and cannot be reserved.

**INCORRECT:** "Amazon CloudWatch" is incorrect. You cannot reserve Amazon CloudWatch which is a monitoring service.

**References:**

[https://d1.awsstatic.com/whitepapers/aws\_pricing\_overview.pdf](https://d1.awsstatic.com/whitepapers/aws_pricing_overview.pdf)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 52: Correct

Which service allows an organization to view operational data from multiple AWS services through a unified user interface and automate operational tasks?

*   AWS Config
    
*   AWS OpsWorks
    
*   AWS Systems Manager
    
    (Correct)
    
*   Amazon CloudWatch
    

#### Explanation

AWS Systems Manager gives you visibility and control of your infrastructure on AWS. Systems Manager provides a unified user interface so you can view operational data from multiple AWS services and allows you to automate operational tasks across your AWS resources.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-30_04-40-52-f99182943e17749a30b48c6ea54406c9.jpg)

**CORRECT:** "AWS Systems Manager" is the correct answer.

**INCORRECT:** "AWS Config" is incorrect. AWS Config is a fully-managed service that provides you with an AWS resource inventory, configuration history, and configuration change notifications to enable security and regulatory compliance.

**INCORRECT:** "AWS OpsWorks" is incorrect. AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet.

**INCORRECT:** "Amazon CloudWatch" is incorrect. Amazon CloudWatch is a monitoring service for AWS cloud resources and the applications you run on AWS. You use CloudWatch for performance monitoring, not automating operational tasks.

**References:**

[https://aws.amazon.com/systems-manager/](https://aws.amazon.com/systems-manager/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 53: Correct

How can an organization track resource inventory and configuration history for the purpose of security and regulatory compliance?

*   Configure AWS Config with the resource types
    
    (Correct)
    
*   Create an Amazon CloudTrail trail
    
*   Implement Amazon GuardDuty
    
*   Run a report with AWS Artifact
    

#### Explanation

AWS Config is a fully-managed service that provides you with an AWS resource inventory, configuration history, and configuration change notifications to enable security and regulatory compliance.

**CORRECT:** "Configure AWS Config with the resource types" is the correct answer.

**INCORRECT:** "Create an Amazon CloudTrail trail" is incorrect. CloudTrail tracks API activity. This means it is used to monitor who does what on Amazon. It does not provide a resource inventory or configuration history.

**INCORRECT:** "Implement Amazon GuardDuty" is incorrect. Amazon GuardDuty offers threat detection and continuous security monitoring for malicious or unauthorized behavior to help you protect your AWS accounts and workloads.

**INCORRECT:** "Run a report with AWS Artifact" is incorrect. AWS Artifact is used for obtaining on-demand security and compliance reports and select online agreements. This service provides access to AWS security and compliance reports such as SOC and PCI. You don’t use Artifact to track your own resource inventory and configuration history.

**References:**

[https://docs.aws.amazon.com/config/latest/developerguide/gs-console.html](https://docs.aws.amazon.com/config/latest/developerguide/gs-console.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-security/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-security/)

Question 54: Correct

A security operations engineer needs to implement threat detection and monitoring for malicious or unauthorized behavior. Which service should be used?

*   AWS Shield
    
*   AWS KMS
    
*   AWS CloudHSM
    
*   AWS GuardDuty
    
    (Correct)
    

#### Explanation

Amazon GuardDuty offers threat detection and continuous security monitoring for malicious or unauthorized behavior to help you protect your AWS accounts and workloads.

**CORRECT:** "AWS GuardDuty" is the correct answer.

**INCORRECT:** "AWS Shield" is incorrect. AWS Shield is a managed Distributed Denial of Service (DDoS) protection service.

**INCORRECT:** "AWS KMS" is incorrect. AWS Key Management Service gives you centralized control over the encryption keys used to protect your data.

**INCORRECT:** "AWS CloudHSM" is incorrect. AWS CloudHSM is a cloud-based hardware security module (HSM) that enables you to easily generate and use your own encryption keys on the AWS Cloud.

**References:**

[https://aws.amazon.com/guardduty/](https://aws.amazon.com/guardduty/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-security/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/cloud-security/)

Question 55: Correct

Which authentication method is used to authenticate programmatic calls to AWS services?

*   Console password
    
*   Server certificate
    
*   Key pair
    
*   Access keys
    
    (Correct)
    

#### Explanation

Access keys are a combination of an access key ID and a secret access key. They are used to make programmatic calls to AWS using the API.

**CORRECT:** "Access keys" is the correct answer.

**INCORRECT:** "Console password" is incorrect. Console passwords are used for signing users into the AWS Management Console, not for making programmatic calls to AWS services.

**INCORRECT:** "Server certificate" is incorrect. Server certificates can be used to authenticate to some AWS services using HTTPS.

**INCORRECT:** "Key pair" is incorrect. Key pairs should not be confused with access keys. Key pairs are used for authenticating to Amazon EC2 instances.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/)

Question 56: Correct

What is a benefit of moving an on-premises database to Amazon Relational Database Service (RDS)?

*   There is no need to manage operating systems
    
    (Correct)
    
*   You can scale vertically without downtime
    
*   There is no database administration required
    
*   You can run any database engine
    

#### Explanation

With Amazon RDS, which is a managed service, you do not need to manage operating systems. This reduces operational costs.

**CORRECT:** "There is no need to manage operating systems" is the correct answer.

**INCORRECT:** "You can scale vertically without downtime" is incorrect. You cannot scale vertically without downtime. When scaling with RDS you must change the instance type, and this requires a short period of downtime while the instances’ operating system reboots.

**INCORRECT:** "There is no database administration required" is incorrect. There is still database administration required in the cloud. You don’t manage the underlying operating system but still need to manage your own tables and data within the DB.

**INCORRECT:** "You can run any database engine" is incorrect. You cannot run any database engine with RDS. The options are MySQL, Microsoft SQL, MariaDB, Oracle, PostgreSQL and Aurora.

**References:**

[https://aws.amazon.com/rds/features/](https://aws.amazon.com/rds/features/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-databases/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-databases/)

Question 57: Correct

What are the benefits of using Amazon Rekognition with image files?

*   Can be used to resize images
    
*   Can be used to identify objects in an image
    
    (Correct)
    
*   Can be used to transcode audio
    
*   Can help with image compression
    

#### Explanation

Rekognition Image is a deep learning powered image recognition service that detects objects, scenes, and faces; extracts text; recognizes celebrities; and identifies inappropriate content in images. It also allows you to search and compare faces.

**CORRECT:** "Can be used to identify objects in an image" is the correct answer.

**INCORRECT:** "Can be used to resize images" is incorrect. You cannot use Rekognition to resize images.

**INCORRECT:** "Can be used to transcode audio" is incorrect. You should use the Elastic Transcoder service to transcode audio.

**INCORRECT:** "Can help with image compression" is incorrect. You cannot use Rekognition to compress images.

**References:**

[https://aws.amazon.com/rekognition/image-features/](https://aws.amazon.com/rekognition/image-features/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/additional-aws-services-tools/)

Question 58: Correct

Which IAM entity is associated with an access key ID and secret access key?

*   IAM Group
    
*   IAM Role
    
*   IAM Policy
    
*   IAM User
    
    (Correct)
    

#### Explanation

An access key ID and secret access key are used to sign programmatic requests to AWS. They are associated with an IAM user.

You cannot associate an access key ID and secret access key with an IAM Group, Role or Policy.

**CORRECT:** "IAM User" is the correct answer.

**INCORRECT:** "IAM Group" is incorrect as explained above.

**INCORRECT:** "IAM Role" is incorrect as explained above.

**INCORRECT:** "IAM Policy" is incorrect as explained above.

**References:**

[https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html#access-keys-and-secret-access-keys](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html#access-keys-and-secret-access-keys)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/)

Question 59: Correct

Which IAM entity can be used for assigning permissions to multiple users?

*   IAM User
    
*   IAM Group
    
    (Correct)
    
*   IAM Role
    
*   IAM password policy
    

#### Explanation

Groups are collections of users and have policies attached to them. You can use groups to assign permissions to multiple users. To do this place the users in the group and then create an IAM policy with the correct permissions and attach it to the group.

You do not use an IAM User, Role, or password policy to assign permissions to multiple users.

**CORRECT:** "IAM Group" is the correct answer.

**INCORRECT:** "IAM User" is incorrect as explained above.

**INCORRECT:** "IAM Role" is incorrect as explained above.

**INCORRECT:** "IAM password policy" is incorrect as explained above.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_groups.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_groups.html)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/identity-and-access-management/)

Question 60: Incorrect

Which service can be used to cost-effectively move exabytes of data into AWS?

*   AWS Snowmobile
    
    (Correct)
    
*   AWS Snowball
    
    (Incorrect)
    
*   S3 Transfer Acceleration
    
*   S3 Cross-Region Replication (CRR)
    

#### Explanation

With AWS Snowmobile you can move 100PB per snowmobile. AWS call this an “Exabyte-scale data transfer service”.

**CORRECT:** "AWS Snowmobile" is the correct answer.

**INCORRECT:** "AWS Snowball" is incorrect. With AWS Snowball you can move up to 80TB per device. AWS call this a “petabyte-scale data transfer service”.

**INCORRECT:** "S3 Transfer Acceleration" is incorrect. S3 Transfer Acceleration is meant speed up uploads to Amazon S3 but would not be used for exabytes of data.

**INCORRECT:** "S3 Cross-Region Replication (CRR)" is incorrect. S3 Cross-Region Replication is used for copying data between regions, not into AWS. It is also unsuitable for moving such as huge amount of data.

**References:**

[https://aws.amazon.com/snowmobile/](https://aws.amazon.com/snowmobile/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-storage/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-storage/)

Question 61: Incorrect

Which AWS services are associated with Edge Locations? (Select TWO.)

*   Amazon CloudFront
    
    (Correct)
    
*   AWS Direct Connect
    
    (Incorrect)
    
*   AWS Shield
    
    (Correct)
    
*   Amazon EBS
    
*   AWS Config
    

#### Explanation

Edge Locations are parts of the Amazon CloudFront content delivery network (CDN) that are all around the world and are used to get content closer to end-users for better performance.

AWS Shield which protects against Distributed Denial of Service (DDoS) attacks is available globally on Amazon CloudFront Edge Locations.

**CORRECT:** "Amazon CloudFront" is a correct answer.

**CORRECT:** "AWS Shield" is also a correct answer.

**INCORRECT:** "AWS Direct Connect" is incorrect. AWS Direct Connect is a networking service used for creating a hybrid cloud between on-premises and AWS Cloud using a private network connection

**INCORRECT:** "Amazon EBS" is incorrect. Amazon EBS is a storage service.

**INCORRECT:** "AWS Config" is incorrect. AWS Config is used for evaluating the configuration state of AWS resources.

**References:**

[https://aws.amazon.com/shield/](https://aws.amazon.com/shield/)

[https://aws.amazon.com/cloudfront/](https://aws.amazon.com/cloudfront/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/content-delivery-and-dns-services/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/content-delivery-and-dns-services/)

Question 62: Correct

Which service can be used to easily create multiple accounts?

*   AWS IAM
    
*   AWS CloudFormation
    
*   AWS Organizations
    
    (Correct)
    
*   Amazon Connect
    

#### Explanation

AWS Organizations can be used for automating AWS account creation via the Organizations API.

**CORRECT:** "AWS Organizations" is the correct answer.

**INCORRECT:** "AWS IAM" is incorrect. You cannot use IAM for creating accounts.

**INCORRECT:** "AWS CloudFormation" is incorrect. You could theoretically use AWS CloudFormation to automate the account creation along with some scripting, but that is certainly not an easy way to reach this result.

**INCORRECT:** "Amazon Connect" is incorrect. Amazon Connect is a self-service, cloud-based contact center service that makes it easy for businesses to deliver better customer service at a lower cost.

**References:**

[https://docs.aws.amazon.com/organizations/latest/userguide/orgs\_manage\_accounts\_create.html](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_create.html)

[https://aws.amazon.com/blogs/security/how-to-use-aws-organizations-to-automate-end-to-end-account-creation/](https://aws.amazon.com/blogs/security/how-to-use-aws-organizations-to-automate-end-to-end-account-creation/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 63: Correct

What is a specific benefit of an Enterprise Support plan?

*   Included Technical Support Manager
    
*   Included AWS Solutions Architect
    
*   Included Cloud Support Associate
    
*   Included Technical Account Manager
    
    (Correct)
    

#### Explanation

Only the Enterprise Support plan gets a Technical Account Manager (TAM).

You do not get an AWS Solutions Architect with any plan.

Cloud Support Associates are provided in the Developer plan.

There’s no such thing as a Technical Support Manager in the AWS support plans.

**CORRECT:** "Included Technical Account Manager" is the correct answer.

**INCORRECT:** "Included Technical Support Manager" is incorrect as explained above.

**INCORRECT:** "Included AWS Solutions Architect" is incorrect as explained above.

**INCORRECT:** "Included Cloud Support Associate" is incorrect as explained above.

**References:**

[https://aws.amazon.com/premiumsupport/plans/](https://aws.amazon.com/premiumsupport/plans/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 64: Incorrect

You have been running an on-demand Amazon EC2 instance running Linux for 4hrs, 5 minutes and 6 seconds. How much time will you be billed for?

*   5hrs
    
    (Incorrect)
    
*   4hrs, 6mins
    
*   4hrs, 5mins, and 6 seconds
    
    (Correct)
    
*   4hrs
    

#### Explanation

On-demand, Reserved and Spot Amazon EC2 Linux instances are charged per second with a minimum charge of 1 minute. Therefore, as the minimum has been exceeded, exactly 4hrs, 5mins and 6 seconds will be charged.

**CORRECT:** "4hrs, 5mins, and 6 seconds" is the correct answer.

**INCORRECT:** "5hrs" is incorrect as explained above.

**INCORRECT:** "4hrs, 6mins" is incorrect as explained above.

**INCORRECT:** "4hrs" is incorrect as explained above.

**References:**

[https://aws.amazon.com/blogs/aws/new-per-second-billing-for-ec2-instances-and-ebs-volumes/](https://aws.amazon.com/blogs/aws/new-per-second-billing-for-ec2-instances-and-ebs-volumes/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-billing-and-pricing/)

Question 65: Correct

Which of the below is an example of an architectural benefit of moving to the cloud?

*   Elasticity
    
    (Correct)
    
*   Monolithic services
    
*   Proprietary hardware
    
*   Vertical scalability
    

#### Explanation

A key architectural benefit of moving to the cloud is that you get elasticity. This means your applications can scale as demand increases and scale back as demand decreases. This reduces cost as you only pay for what you use, when you need it.

**CORRECT:** "Elasticity" is the correct answer.

**INCORRECT:** "Monolithic services" is incorrect. Monolithic services are not a design patter of the public cloud. Developers and architects prefer service oriented or micro-service architectures instead.

**INCORRECT:** "Proprietary hardware" is incorrect. You do not get to choose your hardware in AWS as the infrastructure on which your services run is managed and operated by AWS. So you cannot use proprietary hardware.

**INCORRECT:** "Vertical scalability" is incorrect. Vertical scalability is not unique to the cloud, nor is it something we aspire to as architects. Most of the time horizontal scalability is preferred and is something that the AWS cloud provides for many services.

**References:**

[https://aws.amazon.com/architecture/](https://aws.amazon.com/architecture/)

**Save time with our exam-specific cheat sheets:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/architecting-for-the-cloud/)

Retake test

Continue

Settings

*   Report abuse
    

Fullscreen