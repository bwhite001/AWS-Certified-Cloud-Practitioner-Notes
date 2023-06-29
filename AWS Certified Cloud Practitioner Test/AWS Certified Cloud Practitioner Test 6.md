AWS Certified Cloud Practitioner: Test 6 - Results
--------------------------------------------------

All knowledge areas

*   All knowledge areas
    
*   AWS Shared Responsibility Model
    
*   AWS Support
    
*   AWS Security, Identity, & Compliance
    
*   AWS Management & Governance
    
*   AWS Application Integration
    
*   AWS Compute
    
*   AWS Storage
    
*   AWS Cloud Benefits
    
*   AWS Cost Management
    
*   AWS Networking & Content Delivery
    
*   AWS Database
    
*   AWS Cloud Architecture & Design
    
*   AWS Analytics
    
Question 1:
Under the AWS shared responsibility model, which of the following are customer responsibilities? (Select TWO.)

*   Setting up server-side encryption on an Amazon S3 bucket
    
    (Correct)
    
*   Physical security of data center facilities
    
*   Compute capacity availability
    
*   Network and ﬁrewall conﬁgurations
    
    (Correct)
    
*   Amazon RDS instance patching
    

#### Explanation

As a customer on AWS you take responsibility for encrypting data. This includes encrypting data at rest and data in transit. Another security responsibility the customer owns is setting network and firewall configurations. For instance, you must configure Network ACLs and Security Groups and any operating system-level firewalls on your EC2 instances.

**CORRECT:** "Setting up server-side encryption on an Amazon S3 bucket" is a correct answer.

**CORRECT:** "Network and ﬁrewall conﬁgurations" is also a correct answer.

**INCORRECT:** "Amazon RDS instance patching" is incorrect. With RDS you can define the maintenance window but AWS actually perform the patching for you.

**INCORRECT:** "Physical security of data center facilities" is incorrect as this is security of the cloud and is an AWS responsibility.

**INCORRECT:** "Compute capacity availability" is incorrect as this is an AWS responsibility.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 2:
Which AWS support plans provide 24x7 access to customer service?

*   Business
    
*   Developer
    
*   All plans
    
    (Correct)
    
*   Basic
    

#### Explanation

All support plans provide 24×7 access to customer service, documentation, whitepapers, and support forums.

**CORRECT:** "All plans" is the correct answer.

**INCORRECT:** "Basic" is incorrect as explained above.

**INCORRECT:** "Business" is incorrect as explained above.

**INCORRECT:** "Developer" is incorrect as explained above.

**References:**

[https://aws.amazon.com/premiumsupport/plans/](https://aws.amazon.com/premiumsupport/plans/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 3:
Your manager has asked you to explain some of the security features available in the AWS cloud. How can you describe the function of Amazon CloudHSM?

*   It is a firewall for use with web applications
    
*   It is a Public Key Infrastructure (PKI)
    
*   It provides server-side encryption for S3 objects
    
*   It can be used to generate, use and manage encryption keys in the cloud
    
    (Correct)
    

#### Explanation

AWS CloudHSM is a cloud-based hardware security module (HSM) that allows you to easily add secure key storage and high-performance crypto operations to your AWS applications.

CloudHSM has no upfront costs and provides the ability to start and stop HSMs on-demand, allowing you to provision capacity when and where it is needed quickly and cost-effectively.

CloudHSM is a managed service that automates time-consuming administrative tasks, such as hardware provisioning, software patching, high availability, and backups.

**CORRECT:** "It can be used to generate, use and manage encryption keys in the cloud" is the correct answer.

**INCORRECT:** "It provides server-side encryption for S3 objects" is incorrect. CloudHSM performs key management but it does not perform encryption of S3 objects.

**INCORRECT:** "It is a Public Key Infrastructure (PKI)" is incorrect. It can be used to generate asymmetric keys, however it is not a PKI.

**INCORRECT:** "It is a firewall for use with web applications" is incorrect as it does not provide any firewall functionality.

**References:**

[https://aws.amazon.com/cloudhsm/details/](https://aws.amazon.com/cloudhsm/details/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 4:
Which AWS service or feature helps restrict the AWS service, resources, and individual API actions the users and roles in each member account can access?

*   AWS Shield
    
*   AWS Firewall Manager
    
*   AWS Organizations
    
    (Correct)
    
*   Amazon Cognito
    

#### Explanation

AWS Organizations offers the following policy types:

Service control policies (SCPs) offer central control over the maximum available permissions for all of the accounts in your organization.

Tag policies help you standardize tags across resources in your organization's accounts.

SCPs are used to restrict access within member accounts. For instance you can create an SCP that restricts a specific API action such as deploying a particular Amazon EC2 instance type. The policy would then prevent anyone, including administrators, from being able to launch EC2 instances using that instance type.

**CORRECT:** "AWS Organizations" is the correct answer.

**INCORRECT:** "Amazon Cognito" is incorrect as this service is used for providing sign-in and sign-up services for mobile applications.

**INCORRECT:** "AWS Shield" is incorrect as this is a security service for protecting against DDoS attacks.

**INCORRECT:** "AWS Firewall Manager" is incorrect as this service is used for managing various security services within AWS.

**References:**

[https://docs.aws.amazon.com/organizations/latest/userguide/orgs\_manage\_policies\_scp.html](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scp.html)

Question 5:
Which resource should you use to access AWS security and compliance reports?

*   AWS Artifact
    
    (Correct)
    
*   AWS IAM
    
*   AWS Organizations
    
*   AWS Business Associate Addendum (BAA)
    

#### Explanation

AWS Artifact, available in the console, is a self-service audit artifact retrieval portal that provides our customers with on-demand access to AWS’ compliance documentation and AWS agreements.

**CORRECT:** "AWS Artifact" is the correct answer.

**INCORRECT:** "AWS Business Associate Addendum (BAA)" is incorrect. The Business Associate Addendum (BAA) is an agreement you can choose to accept within AWS Artifact Agreements.

**INCORRECT:** "AWS IAM" is incorrect. AWS Identity and Access Management (IAM) is the service used for creating and managing users, groups, roles and policies.

**INCORRECT:** "AWS Organizations" is incorrect. AWS Organizations helps you centrally govern your environment as you grow and scale your workloads on AWS. Using AWS Organizations, you can automate account creation, create groups of accounts to reflect your business needs, and apply policies for these groups for governance.

**References:**

[https://aws.amazon.com/artifact/](https://aws.amazon.com/artifact/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 6:
Which of the following is NOT a best practice for protecting the root user of an AWS account?

*   Don’t share the root user credentials   
*   Lock away the AWS root user access keys   
*   Remove administrative permissions   
    
    (Correct)
    
*   Enable MFA   

#### Explanation

You cannot remove administrative permissions from the root user of an AWS account. Therefore, you must protect the account through creating a complex password, enabling MFA, locking away access keys (assuming they’re even required), and not sharing the account details.

**CORRECT:** "Remove administrative permissions" is the correct answer.

**INCORRECT:** "Don’t share the root user credentials" is incorrect as this is a best practice.

**INCORRECT:** "Enable MFA" is incorrect as this is a best practice.

**INCORRECT:** "Lock away the AWS root user access keys" is incorrect as this is a best practice.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 7:
A Cloud Practitioner is creating the business process workflows associated with an order fulfilment system. Which AWS service can assist with coordinating tasks across distributed application components?

*   Amazon SNS
    
*   Amazon SQS
    
*   Amazon SWF
    
    (Correct)
    
*   AWS STS
    

#### Explanation

Amazon Simple Workflow Service (SWF) is a web service that makes it easy to coordinate work across distributed application components. SWF enables applications for a range of use cases, including media processing, web application back-ends, business process workflows, and analytics pipelines, to be designed as a coordination of tasks.

**CORRECT:** "Amazon SWF" is the correct answer.

**INCORRECT:** "AWS STS" is incorrect. AWS Security Token Service (STS) is used for requesting temporary credentials..

**INCORRECT:** "Amazon SQS" is incorrect. Amazon Simple Queue Service (SQS) is a message queue used for decoupling application components.

**INCORRECT:** "Amazon SNS" is incorrect. Amazon Simple Notification Service (SNS) is a web service that makes it easy to set up, operate, and send notifications from the cloud. SNS supports notifications over multiple transports including HTTP/HTTPS, Email/Email-JSON, SQS and SMS.

**References:**

[https://aws.amazon.com/swf/](https://aws.amazon.com/swf/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 8:
Which AWS service is suitable for an event-driven workload?

*   Amazon EC2
    
*   AWS Elastic Beanstalk
    
*   Amazon Open 3D Engine
    
*   AWS Lambda
    
    (Correct)
    

#### Explanation

AWS Lambda is an event-driven service. For example you can configure an Amazon S3 bucket with event notifications that trigger an AWS Lambda function when data is uploaded to an S3 bucket.

**CORRECT:** "AWS Lambda" is the correct answer.

**INCORRECT:** "Amazon EC2" is incorrect as this is not an event-driven service.

**INCORRECT:** "AWS Elastic Beanstalk" is incorrect as this is not an event-driven service.

**INCORRECT:** "Amazon Open 3D Engine" is incorrect as this is a game engine service.

**References:**

[https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html](https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 9:
Which service allows you to monitor and troubleshoot systems using system and application log files generated by those systems?

*   CloudTrail Logs
    
*   CloudWatch Logs
    
    (Correct)
    
*   CloudWatch Metrics
    
*   CloudTrail Metrics
    

#### Explanation

Amazon CloudWatch Logs lets you monitor and troubleshoot your systems and applications using your existing system, application and custom log files. CloudWatch Logs can be used for real time application and system monitoring as well as long term log retention.

**CORRECT:** "CloudWatch Logs" is the correct answer.

**INCORRECT:** "CloudTrail Logs" is incorrect. CloudTrail is used for logging who does what in AWS by recording API calls. It is used for auditing, not performance or system operational monitoring.

**INCORRECT:** "CloudWatch Metrics" is incorrect. CloudWatch metrics are the standard method by which CloudWatch collects data

**INCORRECT:** "CloudTrail Metrics" is incorrect. CloudTrail does not record metrics, it records logs.

**References:**

[https://aws.amazon.com/cloudtrail/](https://aws.amazon.com/cloudtrail/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-monitoring-and-logging-services/](https://digitalcloud.training/aws-monitoring-and-logging-services/)

Question 10:
Which of the authentication options below can be used to authenticate using AWS APIs? (Select TWO.)

*   Server certificates   
    
    (Correct)
    
*   Server passwords   
*   Access keys   
    
    (Correct)
    
*   Key pairs   
*   Security groups   

#### Explanation

Access keys are long-term credentials for an IAM user or the AWS account root user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API (directly or using the AWS SDK).

Server certificates are SSL/TLS certificates that you can use to authenticate with some AWS services.

**CORRECT:** "Access keys" is a correct answer.

**CORRECT:** "Server certificates" is also a correct answer.

**INCORRECT:** "Key pairs" is incorrect. Key pairs are used for encrypting logon information when accessing EC2 instances.

**INCORRECT:** "Server passwords" is incorrect. A server password cannot be used to authenticate with an API.

**INCORRECT:** "Security groups" is incorrect. Security groups are an instance-level firewall used for controlling access to AWS resources.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_server-certs.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_server-certs.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 11:
Which of the following acts as a virtual ﬁrewall at the Amazon EC2 instance level to control traffic for one or more instances?

*   Security groups
    
    (Correct)
    
*   Route table
    
*   Network Access Control Lists (ACL)
    
*   Virtual private gateways (VPG)
    

#### Explanation

A security group is an instance-level firewall that can be used to control traffic the that reaches (ingress/inbound) and is sent out from (egress/outbound) your EC2 instances. Rules are created for inbound or outbound traffic. A security group can be attached to multiple EC2 instances.

**CORRECT:** "Security groups" is the correct answer.

**INCORRECT:** "Network Access Control Lists (ACL)" is incorrect as this is subnet-level firewall. You do not attach a Network ACL to an instance, you attach it to a subnet.

**INCORRECT:** "Virtual private gateways (VPG)" is incorrect. A VPG is the Amazon side of an AWS Managed VPN.

**INCORRECT:** "Route table" is incorrect as this is not a firewall but a table of routes for directing traffic between subnets within a VPC.

**References:**

[https://docs.aws.amazon.com/vpc/latest/userguide/VPC\_SecurityGroups.html](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 12:
Which AWS Glacier data access option retrieves data from an archive in 1-5 minutes?

*   Accelerated
    
*   Express
    
*   Expedited
    
    (Correct)
    
*   Standard
    

#### Explanation

Expedited retrievals allow you to quickly access your data when occasional urgent requests for a subset of archives are required. For all but the largest archives (250 MB+), data accessed using Expedited retrievals are typically made available within 1–5 minutes.

**CORRECT:** "Expedited" is the correct answer.

**INCORRECT:** "Standard" is incorrect. Standard takes 3-5 hours.

**INCORRECT:** "Express" is incorrect as this is not a retrieval option.

**INCORRECT:** "Accelerated" is incorrect as this is not a retrieval option.

**References:**

[https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive-two-steps.html](https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive-two-steps.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 13:
Which of the statements below does NOT characterize cloud computing?

*   With cloud computing you get to benefit from massive economies of scale   
*   Cloud computing allows you to swap variable expense for capital expense   
    
    (Correct)
    
*   With cloud computing you can increase your speed and agility   
*   Cloud computing is the on-demand delivery of compute power   

#### Explanation

Cloud computing is not a one-off capital expense, it is an ongoing operating expense. The caveat to this is that if you purchase reserved capacity you have an option to partially or fully pay upfront. However, it is still an operating cost as you do not own and depreciate the assets.

**CORRECT:** "Cloud computing allows you to swap variable expense for capital expense" is the correct answer.

**INCORRECT:** "Cloud computing is the on-demand delivery of compute power" is incorrect as this is a valid statement.

**INCORRECT:** "With cloud computing you get to benefit from massive economies of scale" is incorrect as this is a valid statement.

**INCORRECT:** "With cloud computing you can increase your speed and agility" is incorrect as this is a valid statement.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 14:
Which feature of Amazon S3 enables you to create rules to control the transfer of objects between different storage classes?

*   Object sharing
    
*   Versioning
    
*   Lifecycle management
    
    (Correct)
    
*   Bucket policies
    

#### Explanation

To manage your objects so that they are stored cost effectively throughout their lifecycle, configure their _Amazon S3 Lifecycle_. An _S3 Lifecycle configuration_ is a set of rules that define actions that Amazon S3 applies to a group of objects. There are two types of actions:

• **Transition actions**—Define when objects transition to another storage class. For example, you might choose to transition objects to the S3 Standard-IA storage class 30 days after you created them, or archive objects to the S3 Glacier storage class one year after creating them.

• **Expiration actions**—Define when objects expire. Amazon S3 deletes expired objects on your behalf. The lifecycle expiration costs depend on when you choose to expire objects.

**CORRECT:** "Lifecycle management" is the correct answer.

**INCORRECT:** "Object sharing" is incorrect. Object sharing refers to the ability to make any object publicly available via a URL.

**INCORRECT:** "Versioning" is incorrect. Versioning enabled you to automatically keep multiple versions of an object (when enabled).

**INCORRECT:** "Bucket policies" is incorrect. Bucket policies are used for controlling access to buckets, they can’t be used to move data between storage classes.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 15:
To reduce cost, which of the following services support reservations? (Select TWO.)

*   Amazon ElastiCache   
    
    (Correct)
    
*   AWS Elastic Beanstalk   
*   Amazon S3   
*   Amazon RedShift   
    
    (Correct)
    
*   Amazon CloudFormation   

#### Explanation

Amazon ElastiCache and Amazon Redshift both support reserved nodes. Reservations can be used to gain a large discount from the on-demand rate in exchange for the commitment to a contract for 1 or 3 years.

**CORRECT:** "Amazon ElastiCache" is a correct answer.

**CORRECT:** "Amazon RedShift" is also a correct answer.

**INCORRECT:** "Amazon CloudFormation" is incorrect as you do not pay for CloudFormation.

**INCORRECT:** "AWS Elastic Beanstalk" is incorrect as you do not pay for Elastic Beanstalk.

**INCORRECT:** "Amazon S3" is incorrect as you pay for usage and cannot reserve capacity.

**References:**

[https://d1.awsstatic.com/whitepapers/aws\_pricing\_overview.pdf](https://d1.awsstatic.com/whitepapers/aws_pricing_overview.pdf)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 16:
What advantages does the AWS cloud provide in relation to cost? (Select TWO.)

*   Enterprise licensing discounts
    
*   Itemized power costs
    
*   One-off payments for on-demand resources
    
*   Fine-grained billing
    
    (Correct)
    
*   Ability to turn off resources and not pay for them
    
    (Correct)
    

#### Explanation

With the AWS cloud you get fine-grained billing and can turn off resources you are not using easily and not have to pay for them (pay for what you use model).

**CORRECT:** "Fine-grained billing" is a correct answer.

**CORRECT:** "Ability to turn off resources and not pay for them" is also a correct answer.

**INCORRECT:** "One-off payments for on-demand resources" is incorrect. You do not get the option for one-off payments for on-demand resources. You can for reserved instances which can be paid all upfront.

**INCORRECT:** "Enterprise licensing discounts" is incorrect. You do not get enterprise licensing discounts from AWS and you do not pay anything for power as the cost is built in.

**INCORRECT:** "Itemized power costs" is incorrect. You do not get any power costs on your bill

**References:**

[https://aws.amazon.com/ec2/pricing/](https://aws.amazon.com/ec2/pricing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 17:
Which of the following are NOT features of AWS IAM? (Select TWO.)

*   Shared access to your AWS account
    
*   PCI DSS compliance
    
*   Charged for what you use
    
    (Correct)
    
*   Identity federation
    
*   Logon using local user accounts
    
    (Correct)
    

#### Explanation

You cannot use IAM to create local user accounts on any system. You are also not charged for what you use, IAM is free to use

The other options are all features of AWS IAM.

**CORRECT:** "Logon using local user accounts" is the correct answer.

**CORRECT:** "Charged for what you use" is the correct answer.

**INCORRECT:** "Shared access to your AWS account" is incorrect as explained above.

**INCORRECT:** "Identity federation" is incorrect as explained above.

**INCORRECT:** "PCI DSS compliance" is incorrect as explained above.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 18:
You are evaluating AWS services that can assist with creating scalable application environments. Which of the statements below best describes the Elastic Load Balancer service?

*   Automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, and IP addresses   
    
    (Correct)
    
*   A network service that provides an alternative to using the Internet to connect customers’ on-premise sites to AWS   
*   A highly available and scalable Domain Name System (DNS) service   
*   Helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application   

#### Explanation

Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, and IP addresses.

Elastic Load Balancing provides fault tolerance for applications by automatically balancing traffic across targets – Amazon EC2 instances, containers and IP addresses – and Availability Zones while ensuring only healthy targets receive traffic.

**CORRECT:** "Automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, and IP addresses" is the correct answer.

**INCORRECT:** "Helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application" is incorrect as this describes EC2 Auto Scaling.

**INCORRECT:** "A highly available and scalable Domain Name System (DNS) service" is incorrect as this describes Amazon Route 53.

**INCORRECT:** "A network service that provides an alternative to using the Internet to connect customers’ on-premise sites to AWS" is incorrect as this describes AWS Direct Connect.

**References:**

[https://aws.amazon.com/elasticloadbalancing/](https://aws.amazon.com/elasticloadbalancing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/auto-scaling-and-elastic-load-balancing/](https://digitalcloud.training/auto-scaling-and-elastic-load-balancing/)

Question 19:
Which pricing model will interrupt a running Amazon EC2 instance if capacity becomes temporarily unavailable?

*   On-Demand Instances
    
*   Spot Instances
    
    (Correct)
    
*   Standard Reserved Instances
    
*   Convertible Reserved Instances
    

#### Explanation

Amazon EC2 Spot Instances let you take advantage of unused EC2 capacity in the AWS cloud. Spot Instances are available at up to a 90% discount compared to On-Demand prices. When AWS need to reclaim the capacity you get a 2 minute warning and then your instances are terminated.

With all other pricing models your instances will not be terminated by AWS once they are running.

**CORRECT:** "Spot Instances" is the correct answer.

**INCORRECT:** "On-Demand Instances" is incorrect as explained above.

**INCORRECT:** "Standard Reserved Instances" is incorrect as explained above.

**INCORRECT:** "Convertible Reserved Instances" is incorrect as explained above.

**References:**

[https://aws.amazon.com/ec2/spot/](https://aws.amazon.com/ec2/spot/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 20:
Under the AWS Shared Responsibility Model, who is responsible for what? (Select TWO.)

*   AWS are responsible for networking infrastructure
    
    (Correct)
    
*   AWS are responsible for network and firewall configuration
    
*   Customers are responsible for networking traffic protection
    
    (Correct)
    
*   Customers are responsible for edge locations
    
*   Customers are responsible for compute infrastructure
    

#### Explanation

AWS is responsible for protecting the infrastructure that runs all of the services offered in the AWS Cloud. Customers are responsible for security in the cloud and responsibilities vary by service.

Customers are responsible for networking traffic protection. This includes applying encryption and using security groups and Network ACLs.

AWS are responsible for networking infrastructure. The underlying networking equipment is maintained by AWS.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-59-12-415f9b5ea1d76142f14a05ad0c7b0c5e.png)

**CORRECT:** "Customers are responsible for networking traffic protection" is a correct answer.

**CORRECT:** "AWS are responsible for networking infrastructure" is also a correct answer.

**INCORRECT:** "Customers are responsible for compute infrastructure" is incorrect. AWS are responsible for compute infrastructure

**INCORRECT:** "AWS are responsible for network and firewall configuration" is incorrect. Customers are responsible for network and firewall configuration.

**INCORRECT:** "Customers are responsible for edge locations" is incorrect. AWS are responsible for edge locations.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 21:
In which ways does AWS’ pricing model benefit organizations?

*   Reduce the cost of maintaining idle resources
    
    (Correct)
    
*   Eliminates licensing costs
    
*   Reduces the people cost of application development
    
*   Focus spend on capital expenditure, rather than operational expenditure
    

#### Explanation

Using AWS you can provision only what you need and adjust resources automatically and elastically. This reduces the amount of resources that are sitting idle which reduces cost.

**CORRECT:** "Reduce the cost of maintaining idle resources" is the correct answer.

**INCORRECT:** "Eliminates licensing costs" is incorrect. AWS does not eliminate licensing costs or application development costs as you still need to licence and develop your application.

**INCORRECT:** "Focus spend on capital expenditure, rather than operational expenditure" is incorrect. AWS allows you to focus your spend on operational costs, not capital costs.

**INCORRECT:** "Reduces the people cost of application development" is incorrect as you still need people to develop applications.

**References:**

[https://aws.amazon.com/pricing/](https://aws.amazon.com/pricing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 22:
Under the shared responsibility model, which of the following tasks are the responsibility of the AWS customer? (Select TWO.)

*   Ensuring that users have received security training in the use of AWS services
    
    (Correct)
    
*   Ensuring that AWS NTP servers are set to the correct time
    
*   Ensuring that hardware is disposed of properly
    
*   Ensuring that application data is encrypted at rest
    
    (Correct)
    
*   Ensuring that access to data centers is restricted
    

#### Explanation

As a customer on AWS you take responsibility for encrypting data. This includes encrypting data at rest and data in transit. It’s also a customer’s responsibility to properly train their staff in security best practices and procedures for the AWS services they use.

**CORRECT:** "Ensuring that application data is encrypted at rest" is a correct answer.

**CORRECT:** "Ensuring that users have received security training in the use of AWS services" is also a correct answer.

**INCORRECT:** "Ensuring that AWS NTP servers are set to the correct time" is incorrect. Network Time Protocol (NTP) servers are an AWS responsibility.

**INCORRECT:** "Ensuring that access to data centers is restricted" is incorrect as this is security of the cloud and is an AWS responsibility.

**INCORRECT:** "Ensuring that hardware is disposed of properly" is incorrect as this is an AWS responsibility.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 23:
Your manager has asked you to explain the benefits of using IAM groups. Which of the below statements are valid benefits? (Select TWO.)

*   Provide the ability to nest groups to create an organizational hierarchy   
*   Provide the ability to create custom permission policies   
*   Enables you to attach IAM permission policies to more than one user at a time   
    
    (Correct)
    
*   You can restrict access to the subnets in your VPC   
*   Groups let you specify permissions for multiple users, which can make it easier to manage the permissions for those users   
    
    (Correct)
    

#### Explanation

Groups are collections of users and have policies attached to them. This enables you to organize groups of users by job function or role and apply relevant policies to the group.

You can use groups to assign permissions to users and should follow the principal of least privilege when assigning permissions.

**CORRECT:** "Groups let you specify permissions for multiple users, which can make it easier to manage the permissions for those users" is a correct answer.

**CORRECT:** "Enables you to attach IAM permission policies to more than one user at a time" is also a correct answer.

**INCORRECT:** "You can restrict access to the subnets in your VPC" is incorrect as this describes Network ACLs.

**INCORRECT:** "Provide the ability to create custom permission policies" is incorrect as this describes IAM policies.

**INCORRECT:** "Provide the ability to nest groups to create an organizational hierarchy" is incorrect. You cannot nest groups (groups within groups).

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 24:
Which AWS service provides the ability to detect inadvertent data leaks of personally identiﬁable information (PII) and user credential data?

*   Amazon Inspector
    
*   AWS Shield
    
*   Amazon GuardDuty
    
*   Amazon Macie
    
    (Correct)
    

#### Explanation

Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data in Amazon S3.

Macie applies machine learning and pattern matching techniques to the Amazon S3 buckets you select to identify and alert you to sensitive data, such as personally identifiable information (PII).

![](https://img-b.udemycdn.com/redactor/raw/2020-06-07_22-22-24-421419ceb8e3b6dfc54797c98dc97e58.JPG)

**CORRECT:** "Amazon Macie" is the correct answer.

**INCORRECT:** "Amazon GuardDuty" is incorrect. This is a service that analyzes your resources using anomaly detection and machine learning. It does not detect personally identifiable information.

**INCORRECT:** "Amazon Inspector" is incorrect. Amazon Inspector automatically assesses applications for exposure, vulnerabilities, and deviations from best practices. It does not detect personally identifiable information.

**INCORRECT:** "AWS Shield" is incorrect. This service is involved with protecting your resources of distributed denial of service (DDoS) attacks.

**References:**

[https://aws.amazon.com/macie/](https://aws.amazon.com/macie/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 25:
Which of the following statements about AWS’s pay-as-you-go pricing model is correct?

*   It requires payment up front for AWS services
    
*   It is relevant only for Amazon EC2, Amazon S3, and Amazon DynamoDB
    
*   It reduces operational expenditures
    
*   It results in reduced capital expenditures
    
    (Correct)
    

#### Explanation

The pay-as-you-go pricing model means you only pay for the services and consumption you actually use. You are charged for compute, storage and outbound data transfer. This model reduces capital expenditure as you pay a monthly bill (operational expenditure).

**CORRECT:** "It results in reduced capital expenditures" is the correct answer.

**INCORRECT:** "It requires payment up front for AWS services" is incorrect. You can pay upfront for some services such as EC2 reserved instances to get better pricing but most services are offered on a consumption basis.

**INCORRECT:** "It is relevant only for Amazon EC2, Amazon S3, and Amazon DynamoDB" is incorrect. This is not true most AWS services are offered on a pay-as-you-go pricing model.

**INCORRECT:** "It reduces operational expenditures" is incorrect. This is not true, it reduces capital expenditures.

**References:**

[https://aws.amazon.com/pricing/](https://aws.amazon.com/pricing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 26:
What methods are available for scaling an Amazon RDS database? (Select TWO.)

*   You can scale up by moving to a larger instance size
    
    (Correct)
    
*   You can scale out by implementing Elastic Load Balancing
    
*   You can scale up automatically using AWS Auto Scaling
    
*   You can scale out automatically with EC2 Auto Scaling
    
*   You can scale up by increasing storage capacity
    
    (Correct)
    

#### Explanation

To handle a higher load in your database, you can vertically scale up your master database with a simple push of a button. There are currently over 18 instance sizes that you can choose from when resizing your RDS MySQL, PostgreSQL, MariaDB, Oracle, or Microsoft SQL Server instance.

For Amazon Aurora, you have 5 memory-optimized instance sizes to choose from. The wide selection of instance types allows you to choose the best resource and cost for your database server.

In addition to scaling your master database vertically, you can also improve the performance of a read-heavy database by using read replicas to horizontally scale your database. RDS MySQL, PostgreSQL, and MariaDB can have up to 5 read replicas, and Amazon Aurora can have up to 15 read replicas.

**CORRECT:** "You can scale up by moving to a larger instance size" is a correct answer.

**CORRECT:** "You can scale up by increasing storage capacity" is also a correct answer.

**INCORRECT:** "You can scale out automatically with EC2 Auto Scaling" is incorrect. You cannot use EC2 Auto Scaling with Amazon RDS.

**INCORRECT:** "You can scale out by implementing Elastic Load Balancing" is incorrect. You cannot use Elastic Load Balancing with RDS.

**INCORRECT:** "You can scale up automatically using AWS Auto Scaling" is incorrect. You cannot use EC2 Auto Scaling or AWS (Application) Auto Scaling to automatically scale your RDS database. EC2 Auto Scaling is involved with launching additional instances (scale out) and this is not a method of scaling an RDS database. Application auto scaling is involved with automatically adjusting the assignment of resources to the database which is not supported with RDS (you can do it with DynamoDB).

**References:**

[https://aws.amazon.com/blogs/database/scaling-your-amazon-rds-instance-vertically-and-horizontally/](https://aws.amazon.com/blogs/database/scaling-your-amazon-rds-instance-vertically-and-horizontally/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 27:
Where do Amazon Identity and Access Management (IAM) accounts need to be created for a global organization?

*   Create them globally, and then replicate them regionally
    
*   Just create them once, as IAM is a global service
    
    (Correct)
    
*   In each geographical area where the users are located
    
*   In each region where the users are located
    

#### Explanation

IAM is a global service so you only need to create your users once and can then use those user accounts anywhere globally. The other options are all incorrect. as you do not create IAM accounts regionally, replicate them regionally, or create them within geographical areas.

**CORRECT:** "Just create them once, as IAM is a global service" is the correct answer.

**INCORRECT:** "In each region where the users are located" is incorrect as explained above.

**INCORRECT:** "Create them globally, and then replicate them regionally" is incorrect as explained above.

**INCORRECT:** "In each geographical area where the users are located" is incorrect as explained above.

**References:**

[https://aws.amazon.com/iam/](https://aws.amazon.com/iam/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 28:
How can you deploy your EC2 instances so that if a single data center fails you still have instances available?

*   Across subnets   
*   Across Availability Zones   
    
    (Correct)
    
*   Across regions   
*   Across VPCs   

#### Explanation

An AZ spans one or more data centers and each AZ is physically isolated from other AZs and connected by high speed networking. If you want to deploy a highly available application you should spread your instances across AZs and they will be resilient to the failure of a single DC

**CORRECT:** "Across Availability Zones" is the correct answer.

**INCORRECT:** "Across regions" is incorrect. You could deploy your instances across separate regions but this is not necessary to create a highly available application and introduces complexity and cost. For example you may need multiple ELBs (one per region), complex name resolution and potential data transfer charges.

**INCORRECT:** "Across subnets" is incorrect. Subnets are created within AZs. Therefore, if you deploy resources into multiple subnets within an AZ and a data center fails, you may lose all of your instances.

**INCORRECT:** "Across VPCs" is incorrect. You should deploy across AZs within a VPC.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-global-infrastructure/](https://digitalcloud.training/aws-global-infrastructure/)

Question 29:
How can a database administrator reduce operational overhead for a MySQL database?

*   Migrate the database onto an EC2 instance
    
*   Migrate the database onto an Amazon RDS instance
    
    (Correct)
    
*   Migrate the database onto AWS Lambda
    
*   Use AWS CloudFormation to manage operations
    

#### Explanation

Amazon RDS is a managed database service that supports MySQL. The DBA can reduce operational overhead by moving to RDS and having less work to do to manage the database.

**CORRECT:** "Migrate the database onto an Amazon RDS instance" is the correct answer.

**INCORRECT:** "Migrate the database onto an EC2 instance" is incorrect. Migrating onto an EC2 instance will not reduce operational overhead as the DBA will still need to manage both the operating system and the database.

**INCORRECT:** "Migrate the database onto AWS Lambda" is incorrect. AWS Lambda provides functions as a service. It therefore a compute service, not a database service and cannot be used to run a MySQL database.

**INCORRECT:** "Use AWS CloudFormation to manage operations" is incorrect. AWS CloudFormation is used for automating the deployment of infrastructure on AWS, not for automating operations.

**References:**

[https://aws.amazon.com/rds/](https://aws.amazon.com/rds/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 30:
A web application running on AWS has been received malicious requests from the same set of IP addresses.

Which AWS service can help secure the application and block the malicious trafﬁc?

*   Amazon GuardDuty
    
*   AWS IAM
    
*   Amazon SNS
    
*   AWS WAF
    
    (Correct)
    

#### Explanation

The AWS Web Application Firewall (WAF) is used to protect web applications or APIs against common web exploits. Rules can be created that block traffic based on source IP address.

**CORRECT:** "AWS WAF" is the correct answer.

**INCORRECT:** "AWS IAM" is incorrect. The Identity and Access Management service is used for creating users, groups, roles and policies. It is not used for controlling network access.

**INCORRECT:** "Amazon GuardDuty" is incorrect. This is a service that analyzes your resources using anomaly detection and machine learning. It can alert and trigger other tools to take action but it is not a network firewall service.

**INCORRECT:** "Amazon SNS" is incorrect as this is service is used for sending notifications using a publisher/subscriber model.

**References:**

[https://aws.amazon.com/waf/](https://aws.amazon.com/waf/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 31:
How can a systems administrator specify a script to be run on an EC2 instance during launch?

*   Metadata
    
*   User Data
    
    (Correct)
    
*   AWS Config
    
*   Run Command
    

#### Explanation

When you launch an instance in Amazon EC2, you have the option of passing user data to the instance that can be used to perform common automated configuration tasks and even run scripts after the instance starts.

You can pass two types of user data to Amazon EC2: shell scripts and cloud-init directives. User data is data that is supplied by the user at instance launch in the form of a script. User data is limited to 16KB. User data and meta data are not encrypted.

**CORRECT:** "User Data" is the correct answer.

**INCORRECT:** "Metadata" is incorrect as metadata retrieves information about the instance.

**INCORRECT:** "Run Command" is incorrect as this operates separately to the launch process.

**INCORRECT:** "AWS Config" is incorrect as this service stores configuration information relating to AWS services.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 32:
Which HTTP code indicates a successful upload of an object to Amazon S3?

*   300
    
*   200
    
    (Correct)
    
*   400
    
*   500
    

#### Explanation

HTTP response status codes indicate whether a specific HTTP request has been successfully completed.

\- A HTTP 200 codes indicates a successful upload.

\- A HTTP 300 code indicates a redirection.

\- A HTTP 400 code indicates a client error.

\- A HTTP 500 code indicates a server error.

**CORRECT:** "200" is the correct answer.

**INCORRECT:** "300" is incorrect as explained above.

**INCORRECT:** "400" is incorrect as explained above.

**INCORRECT:** "500" is incorrect as explained above.

**References:**

[https://en.wikipedia.org/wiki/List\_of\_HTTP\_status\_codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 33:
A company is using the AWS CLI and programmatic access of AWS resources from its on-premises network.

What is a mandatory requirement in this scenario?

*   Using an AWS access key and a secret key
    
    (Correct)
    
*   Using an AWS Direct Connect connection
    
*   Using Amazon API Gateway
    
*   Using an Amazon EC2 key pair
    

#### Explanation

Access keys are long-term credentials for an IAM user or the AWS account root user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API (directly or using the AWS SDK).

Access keys consist of two parts: an access key ID (for example, AKIAIOSFODNN7EXAMPLE) and a secret access key (for example, wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY). Like a user name and password, you must use both the access key ID and secret access key together to authenticate your requests.

**CORRECT:** "Using an AWS access key and a secret key" is the correct answer.

**INCORRECT:** "Using an AWS Direct Connect connection" is incorrect. It is not a requirement that you use a Direct Connect connection. You can access public services via the API using the internet. For private services you can use Direct Connect, a VPN, or a bastion host.

**INCORRECT:** "Using Amazon API Gateway" is incorrect. You do not need API Gateway for programmatic access to the AWS API.

**INCORRECT:** "Using an Amazon EC2 key pair" is incorrect. A key pair is used to securely access EC2 resources and should not be confused with access keys.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 34:
A startup eCommerce company needs to quickly deliver new website features in an iterative manner, minimizing the time to market.

Which AWS Cloud feature allows this?

*   Elasticity
    
*   Reliability
    
*   High availability
    
*   Agility
    
    (Correct)
    

#### Explanation

In a cloud computing environment, new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes.

This results in a dramatic increase in agility for the organization, since the cost and time it takes to experiment and develop is significantly lower.

**CORRECT:** "Agility" is the correct answer.

**INCORRECT:** "High availability" is incorrect as this is associated with increased resilience, not agility.

**INCORRECT:** "Elasticity" is incorrect as this associated with the ability to adjust to demand and reduce the need to guess capacity requirements.

**INCORRECT:** "Reliability" is incorrect as this does not assist with bringing features to market faster.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 35:
Which AWS service can be used to run Docker containers?

*   Amazon RedShift
    
*   AWS Fargate
    
    (Correct)
    
*   Amazon ECR
    
*   Amazon AMI
    

#### Explanation

AWS Fargate is a serverless compute engine for containers that works with both Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes Service (EKS).

Fargate makes it easy for you to focus on building your applications. Fargate removes the need to provision and manage servers, lets you specify and pay for resources per application, and improves security through application isolation by design.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-07_22-42-45-acde8a35319513a05dce946ea8472d0c.jpg)

**CORRECT:** "AWS Fargate" is the correct answer.

**INCORRECT:** "Amazon RedShift” is incorrect. Amazon RedShift is a data warehousing solution, and is unable to run containers.

**INCORRECT:** "Amazon ECR" is incorrect. Amazon Elastic Container Registry (ECR) is a fully-managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images

**INCORRECT:** "Amazon AMI" is incorrect. Amazon Machine Images (AMI) store configuration information for Amazon EC2 instances.

**References:**

[https://aws.amazon.com/fargate/](https://aws.amazon.com/fargate/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 36:
Which AWS database service is schema-less and can be scaled dynamically without incurring downtime?

*   Amazon RedShift
    
*   Amazon RDS
    
*   Amazon Aurora
    
*   Amazon DynamoDB
    
    (Correct)
    

#### Explanation

Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. Push button scaling means that you can scale the DB at any time without incurring downtime. DynamoDB is schema-less.

All other options are SQL type of databases and therefore have a schema. They also rely on EC2 instances so cannot be scaled dynamically without incurring downtime (you have to change instance types).

**CORRECT:** "Amazon DynamoDB" is the correct answer.

**INCORRECT:** "Amazon RDS" is incorrect as explained above.

**INCORRECT:** "Amazon Aurora" is incorrect as explained above.

**INCORRECT:** "Amazon RedShift" is incorrect as explained above.

**References:**

[https://aws.amazon.com/dynamodb/](https://aws.amazon.com/dynamodb/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 37:
What is the most efficient way to establish network connectivity from on-premises to multiple VPCs in different AWS Regions?

*   Use AWS VPN
    
*   Use AWS Client VPN
    
*   Use an AWS Transit Gateway
    
    (Correct)
    
*   Use AWS Direct Connect
    

#### Explanation

AWS Transit Gateway is a service that enables customers to connect their Amazon Virtual Private Clouds (VPCs) and their on-premises networks to a single gateway.

![](https://img-b.udemycdn.com/redactor/raw/2020-10-12_00-44-31-a03766b495f07dd6399182b36419b7cf.png)

With AWS Transit Gateway, you only have to create and manage a single connection from the central gateway into each Amazon VPC, on-premises data center or remote office across your network. Transit Gateway acts as a hub that controls how traffic is routed among all the connected networks which act like spokes.

**CORRECT:** "Use an AWS Transit Gateway" is the correct answer. Please refer to explanation provided above.

**INCORRECT:** "Use AWS Direct Connect" is incorrect as this only connects you to a single Amazon VPC, not multiple VPCs in different Regions.

**INCORRECT:** "Use AWS VPN" is incorrect as this is a point-to-point connection between an on-premises location and a single Amazon VPC.

**INCORRECT:** "Use AWS Client VPN" is incorrect as this service allows end users to connect to AWS using a VPN client.

**References:**

[https://aws.amazon.com/transit-gateway/](https://aws.amazon.com/transit-gateway/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 38:
What is an example of scaling vertically?

*   Increasing the instance size with Amazon RDS   
    
    (Correct)
    
*   Adding read replicas to an Amazon RDS database   
*   AWS Lambda adding concurrently executing functions   
*   AWS Auto Scaling adding more EC2 instances   

#### Explanation

A good example of vertical scaling is changing the instance size of an EC2 instance or RDS database to one with more CPU and RAM.

All of the other options are examples of scaling horizontally.

**CORRECT:** "Increasing the instance size with Amazon RDS" is the correct answer.

**INCORRECT:** "AWS Auto Scaling adding more EC2 instances" is incorrect as explained above.

**INCORRECT:** "AWS Lambda adding concurrently executing functions" is incorrect as explained above.

**INCORRECT:** "Adding read replicas to an Amazon RDS database" is incorrect as explained above.

**References:**

[https://aws.amazon.com/blogs/database/scaling-your-amazon-rds-instance-vertically-and-horizontally/](https://aws.amazon.com/blogs/database/scaling-your-amazon-rds-instance-vertically-and-horizontally/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 39:
What type of cloud computing service type do AWS Elastic Beanstalk and Amazon RDS correspond to?   

*   SaaS
    
*   PaaS
    
    (Correct)
    
*   Hybrid
    
*   IaaS
    

#### Explanation

Both Elastic Beanstalk and RDS are services that are managed at the platform level meaning you don’t need to manage the infrastructure level yourself. Therefore, tasks like OS management and patching are performed for you.

**CORRECT:** "PaaS" is the correct answer.

**INCORRECT:** "IaaS" is incorrect. IaaS is a model where the underlying hardware platform and hypervisor are managed for you and you are delivered tools and interfaces for working with operating system instances.

**INCORRECT:** "SaaS" is incorrect. SaaS is a model where the whole stack is managed for you right up to the application and you are delivered working software that you can customize and populate with data.

**INCORRECT:** "Hybrid" is incorrect. Hybrid is a type of cloud delivery model in which you consume both public and private cloud and connect the two together.

**References:**

[https://aws.amazon.com/types-of-cloud-computing/](https://aws.amazon.com/types-of-cloud-computing/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 40:
The AWS Cost Management tools give users the ability to do which of the following? (Select TWO.)

*   Break down AWS costs by day, service, and linked AWS account
    
    (Correct)
    
*   Move data stored in Amazon S3 to a more cost-effective storage class
    
*   Create budgets and receive notiﬁcations if current or forecasted usage exceeds the budgets
    
    (Correct)
    
*   Terminate any AWS resource automatically if budget thresholds are exceeded
    
*   Switch automatically to Reserved Instances or Spot Instances, whichever is most cost-effective
    

#### Explanation

AWS has a set of solutions to help you with cost management and optimization. This includes services, tools, and resources to organize and track cost and usage data, enhance control through consolidated billing and access permission, enable better planning through budgeting and forecasts, and further lower cost with resources and pricing optimizations.

However, these tools do not terminate all resources, manipulate resources, or make changes to pricing models. It is however possible to terminate some resources using AWS Budgets Actions.

**CORRECT:** "Break down AWS costs by day, service, and linked AWS account" is the correct answer.

**CORRECT:** "Create budgets and receive notiﬁcations if current or forecasted usage exceeds the budgets" is the correct answer.

**INCORRECT:** "Terminate any AWS resource automatically if budget thresholds are exceeded" is incorrect as explained above.

**INCORRECT:** "Switch automatically to Reserved Instances or Spot Instances, whichever is most cost-effective" is incorrect as explained above.

**INCORRECT:** "Move data stored in Amazon S3 to a more cost-effective storage class" is incorrect as explained above.

**References:**

[https://aws.amazon.com/aws-cost-management/](https://aws.amazon.com/aws-cost-management/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 41:
Based on the shared responsibility model, which of the following security and compliance tasks is AWS responsible for?

*   Updating operating systems
    
*   Encrypting data in transit
    
*   Granting access to individuals and services
    
*   Updating Amazon EC2 host firmware
    
    (Correct)
    

#### Explanation

**AWS are responsible for updating Amazon EC2 host firmware. This is considered “security of the cloud”. All other tasks are the responsibility of the customer.**

**CORRECT:** "Updating Amazon EC2 host firmware" is the correct answer.

**INCORRECT:** "Granting access to individuals and services" is incorrect. This is something a customer must perform to control access to the resources they use on AWS.

**INCORRECT:** "Encrypting data in transit" is incorrect. Encryption at rest and in-transit is a customer responsibility.

**INCORRECT:** "Updating operating systems" is incorrect. Customers are responsible for patching operating systems on Amazon EC2. AWS are only responsible for the host servers.

**References:**

[https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-shared-responsibility-model/](https://digitalcloud.training/certification-training/aws-certified-cloud-practitioner/aws-shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

Question 42:
Your company has recently migrated to AWS. How can your CTO monitor the organization’s costs?

*   AWS CloudTrail
    
*   AWS Consolidated Billing
    
*   AWS Cost Explorer
    
    (Correct)
    
*   AWS Simple Monthly calculator
    

#### Explanation

AWS Cost Explorer – enables you to visualize your usage patterns over time and to identify your underlying cost drivers.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_07-17-08-0a39938b4ffa1bdd68c8281e38b57533.jpg)

**CORRECT:** "AWS Cost Explorer" is the correct answer.

**INCORRECT:** "AWS CloudTrail" is incorrect. AWS CloudTrail provides a record of API activity in your account. I.e. who did what to which resource..

**INCORRECT:** "AWS Consolidated Billing" is incorrect. AWS Consolidated Billing is a feature of AWS Organizations that allows you to consolidate billing across multiple linked accounts and benefit from volume pricing discounts.

**INCORRECT:** "AWS Simple Monthly calculator" is incorrect. AWS Simple Monthly calculator – shows you how much you would pay in AWS if you move your resources.

**References:**

[https://aws.amazon.com/aws-cost-management/aws-cost-explorer/](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 43:
How can a company facilitate the sharing of data over private connections between two accounts they own within a region?

*   Create an internal ELB
    
*   Create a VPC peering connection
    
    (Correct)
    
*   Configure matching CIDR address ranges
    
*   Create a subnet peering connection
    

#### Explanation

A VPC peering connection helps you to facilitate the transfer of data. For example, if you have more than one AWS account, you can peer the VPCs across those accounts to create a file sharing network. You can also use a VPC peering connection to allow other VPCs to access resources you have in one of your VPCs.

**CORRECT:** "Create a VPC peering connection" is the correct answer.

**INCORRECT:** "Create an internal ELB" is incorrect. An internal ELB will not help you to transfer data between accounts.

**INCORRECT:** "Create a subnet peering connection" is incorrect. You cannot peer subnets.

**INCORRECT:** "Configure matching CIDR address ranges" is incorrect. Configuring matching CIDR address ranges will not mean you can route between accounts. Also, you cannot peer with an account with a matching (or overlapping) address range.

**References:**

[https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 44:
Which of the following are examples of horizontal scaling? (Select TWO.)

*   Add more instances as demand increases
    
    (Correct)
    
*   Automatic scaling using services such as AWS Auto Scaling
    
    (Correct)
    
*   Scalability is limited by maximum instance size
    
*   Add more CPU/RAM to existing instances as demand increases
    
*   Requires a restart to scale up or down
    

#### Explanation

With horizontal scaling you add more instances to a fleet of instances to service demand as it increases. This can be achieved automatically by using AWS Auto Scaling to add instances in response to CloudWatch performance metrics.

With vertical scaling you are adding CPU, RAM or storage to an existing instance. This may involve modifying the instance type which typically requires a restart. With vertical scaling on AWS scalability is limited by the maximum instance size.

**CORRECT:** "Add more instances as demand increases" is a correct answer.

**CORRECT:** "Automatic scaling using services such as AWS Auto Scaling" is also a correct answer.

**INCORRECT:** "Add more CPU/RAM to existing instances as demand increases" is incorrect as this is an example of vertical scaling.

**INCORRECT:** "Requires a restart to scale up or down" is incorrect as horizontal scaling does not require a restart of existing instances/applications.

**INCORRECT:** "Scalability is limited by maximum instance size" is incorrect as with horizontal scaling you add more instances.

**References:**

[https://aws.amazon.com/architecture/](https://aws.amazon.com/architecture/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 45:
You need to connect your company’s on-premise network into AWS and would like to establish an AWS managed VPN service. Which of the following configuration items needs to be setup on the Amazon VPC side of the connection?

*   A Virtual Private Gateway
    
    (Correct)
    
*   A Firewall
    
*   A Customer Gateway
    
*   A Network Address Translation device
    

#### Explanation

A _virtual private gateway_ is the VPN concentrator on the Amazon side of the VPN connection. You create a virtual private gateway and attach it to the VPC from which you want to create the VPN connection.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_06-00-42-2d7fa5a52ec9fac36aaf872b9f780794.png)

**CORRECT:** "A Virtual Private Gateway" is the correct answer.

**INCORRECT:** "A Customer Gateway" is incorrect. A _customer gateway_ is a physical device or software application on your side of the VPN connection.

**INCORRECT:** "A Network Address Translation device" is incorrect. NAT devices and firewalls are not required for an AWS managed VPN.

**INCORRECT:** "A Firewall" is incorrect. A firewall is not required for a VPN connection.

**References:**

[https://docs.aws.amazon.com/vpc/latest/userguide/VPC\_VPN.html#VPN](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_VPN.html#VPN)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 46:
Which type of AWS database is ideally suited to analytics using SQL queries?

*   Amazon RedShift
    
    (Correct)
    
*   Amazon S3
    
*   Amazon RDS
    
*   Amazon DynamoDB
    

#### Explanation

Amazon Redshift is a fast, fully managed data warehouse that makes it simple and cost-effective to analyze all your data using standard SQL and existing Business Intelligence (BI) tools. RedShift is a SQL based data warehouse used for **analytics** applications.

**CORRECT:** "Amazon RedShift" is the correct answer.

**INCORRECT:** "Amazon DynamoDB" is incorrect. Amazon DynamoDB is a NoSQL type of database and is not suited to analytics using SQL queries.

**INCORRECT:** "Amazon RDS" is incorrect. Amazon RDS is a transactional DB, not an analytics DB.

**INCORRECT:** "Amazon S3" is incorrect. Amazon S3 is an object storage solution not a database.

**References:**

[https://aws.amazon.com/redshift/](https://aws.amazon.com/redshift/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 47:
Which AWS service makes it easy to coordinate the components of distributed applications as a series of steps in a visual workflow?

*   Amazon SWF   
*   Amazon SES   
*   Amazon SNS   
*   AWS Step Functions   
    
    (Correct)
    

#### Explanation

AWS Step Functions lets you coordinate multiple AWS services into serverless workflows so you can build and update apps quickly. AWS Step Functions lets you build visual workflows that enable fast translation of business requirements into technical requirements.

**CORRECT:** "AWS Step Functions" is the correct answer.

**INCORRECT:** "Amazon SWF" is incorrect. Amazon SWF helps developers build, run, and scale background jobs that have parallel or sequential steps. SWF is not a visual workflow tool.

**INCORRECT:** "Amazon SNS" is incorrect. Amazon Simple Notification Service (SNS) is a highly available, durable, secure, fully managed pub/sub messaging service.

**INCORRECT:** "Amazon SES" is incorrect. Amazon Simple Email Service (Amazon SES) is a cloud-based email sending service designed to help digital marketers and application developers send marketing, notification, and transactional emails.

**References:**

[https://aws.amazon.com/step-functions/](https://aws.amazon.com/step-functions/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 48:
Which AWS Cloud design principles can help increase reliability? (Select TWO.)

*   Adopting a consumption model
    
*   Automatically recovering from failure
    
    (Correct)
    
*   Measuring overall efﬁciency
    
*   Using monolithic architecture
    
*   Testing recovery procedures
    
    (Correct)
    

#### Explanation

Recovery procedures should always be tested ahead of any outage of disaster recovery situation. This is the only way to be sure your recovery procedures are effective.

When designing systems it is also a good practice to implement automatic recovery when possible. This reduces or eliminates the operational burden and potential downtime associated with a failure of a system or application component.

**CORRECT:** "Testing recovery procedures" is the correct answer.

**CORRECT:** "Automatically recovering from failure" is the correct answer.

**INCORRECT:** "Using monolithic architecture" is incorrect. A monolithic architecture means you have multiple components of an application running on a single system. This results in a bigger issue if that system fails. A distributed architecture is preferred.

**INCORRECT:** "Measuring overall efﬁciency" is incorrect. Efficiency has more of a bearing on cost management than reliability.

**INCORRECT:** "Adopting a consumption model" is incorrect. A consumption model has benefits more aligned with cost and agility than reliability.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 49:
How can a company configure automatic, asynchronous copying of objects in Amazon S3 buckets across regions?

*   This is done by default by AWS
    
*   By configuring multi-master replication
    
*   Using cross-region replication
    
    (Correct)
    
*   Using lifecycle actions
    

#### Explanation

_Cross-region replication_ (CRR) enables automatic, asynchronous copying of objects across buckets in different AWS Regions. Buckets configured for cross-region replication can be owned by the same AWS account or by different account

**CORRECT:** "Using cross-region replication" is the correct answer.

**INCORRECT:** "This is done by default by AWS" is incorrect as this is not true.

**INCORRECT:** "By configuring multi-master replication" is incorrect. Multi-master replication is not something you can do with Amazon S3 (Amazon Aurora has this feature).

**INCORRECT:** "Using lifecycle actions" is incorrect. Lifecycle actions cannot be configured to move to another storage class in a different region.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/crr.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/crr.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 50:
Which AWS service can serve a static website?

*   Amazon Route 53
    
*   AWS X-Ray
    
*   Amazon S3
    
    (Correct)
    
*   Amazon QuickSight
    

#### Explanation

You can use Amazon S3 to host a static website. On a _static_ website, individual webpages include static content. They might also contain client-side scripts.

To host a static website on Amazon S3, you configure an Amazon S3 bucket for website hosting and then upload your website content to the bucket. When you configure a bucket as a static website, you must enable website hosting, set permissions, and create and add an index document. Depending on your website requirements, you can also configure redirects, web traffic logging, and a custom error document.

**CORRECT:** "Amazon S3" is the correct answer.

**INCORRECT:** "Amazon Route 53" is incorrect. This is an intelligent DNS service.

**INCORRECT:** "Amazon QuickSight" is incorrect. Amazon QuickSight is a fast, cloud-powered business intelligence service that makes it easy to deliver insights to everyone in your organization.

**INCORRECT:** "AWS X-Ray" is incorrect. This is used for tracing and debugging applications.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 51:
Which AWS security tool uses an agent installed in EC2 instances and assesses applications for vulnerabilities and deviations from best practices?   

*   AWS Personal Health Dashboard   
*   AWS Trusted Advisor   
*   AWS Inspector   
    
    (Correct)
    
*   AWS TCO Calculator   

#### Explanation

Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. Inspector automatically assesses applications for vulnerabilities or deviations from best practices. Inspector uses an agent installed on EC2 instances.

**CORRECT:** "AWS Inspector" is the correct answer.

**INCORRECT:** "AWS Trusted Advisor" is incorrect. Trusted Advisor is an online resource that helps to reduce cost, increase performance and improve security by optimizing your AWS environment.

**INCORRECT:** "AWS Personal Health Dashboard" is incorrect. AWS Personal Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you.

**INCORRECT:** "AWS TCO Calculator" is incorrect. The AWS TCO calculator can be used to compare the cost of running your applications in an on-premises or colocation environment to AWS.

**References:**

[https://aws.amazon.com/inspector/](https://aws.amazon.com/inspector/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 52:
What do you need to log into the AWS console?

*   Certificate   
*   User name and password   
    
    (Correct)
    
*   Key pair   
*   Access key and secret ID   

#### Explanation

You can log into the AWS console using a user name and password. You cannot log in to the AWS console using a key pair, access key & secret ID or certificate.

**CORRECT:** "User name and password" is the correct answer.

**INCORRECT:** "Key pair" is incorrect as explained above.

**INCORRECT:** "Access key and secret ID" is incorrect as explained above.

**INCORRECT:** "Certificate" is incorrect as explained above.

**References:**

[https://aws.amazon.com/console/](https://aws.amazon.com/console/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 53:
Which AWS technology enables you to group resources that share one or more tags?

*   Resource groups   
    
    (Correct)
    
*   Consolidation groups   
*   Tag groups   
*   Organization groups   

#### Explanation

You can use _resource groups_ to organize your AWS resources. Resource groups make it easier to manage and automate tasks on large numbers of resources at one time.

Resource groups make it easy to group resources using the tags that are assigned to them. You can group resources that share one or more tags.

**CORRECT:** "Resource groups" is the correct answer.

**INCORRECT:** "Tag groups" is incorrect as this is not a feature.

**INCORRECT:** "Organization groups" is incorrect as this is not a feature.

**INCORRECT:** "Consolidation groups" is incorrect as this is not a feature.

**References:**

[https://docs.aws.amazon.com/ARG/latest/userguide/welcome.html](https://docs.aws.amazon.com/ARG/latest/userguide/welcome.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 54:
What is the name for the top-level container used to hold objects within Amazon S3?

*   Folder
    
*   Instance Store
    
*   Bucket
    
    (Correct)
    
*   Directory
    

#### Explanation

Amazon S3 is an object-based storage system. You upload your objects into buckets.

**CORRECT:** "Bucket" is the correct answer.

**INCORRECT:** "Folder" is incorrect. Though S3 is a flat structure (not hierarchical), folders can be used for grouping objects. However, this is not the top-level container.

**INCORRECT:** "Directory" is incorrect. Directories are usually associated with filesystems rather than object-based storage systems.

**INCORRECT:** "Instance Store" is incorrect. An Instance Store is a type of ephemeral block-based storage service available to EC2 instances.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingBucket.html#create-bucket-intro](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingBucket.html#create-bucket-intro)

[https://docs.aws.amazon.com/AmazonS3/latest/user-guide/using-folders.html](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/using-folders.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 55:
According to the AWS Well-Architected Framework, what change management steps should be taken to achieve reliability in the AWS Cloud? (Select TWO.)

*   Use AWS Conﬁg to generate an inventory of AWS resources
    
    (Correct)
    
*   Use service limits to prevent users from creating or making changes to AWS resources
    
*   Use AWS Certiﬁcate Manager to create a catalog of approved services
    
*   Use Amazon GuardDuty to record API activity to an S3 bucket
    
*   Use AWS CloudTrail to record AWS API calls into an auditable log ﬁle
    
    (Correct)
    

#### Explanation

AWS Config can be used to track the configuration state of your resources and how the state has changed over time. With CloudTrail you can audit who made what API calls on what resources at what time. This can help with identifying changes that cause reliability issues.

**CORRECT:** "Use AWS Conﬁg to generate an inventory of AWS resources" is the correct answer.

**CORRECT:** "Use AWS CloudTrail to record AWS API calls into an auditable log ﬁle" is the correct answer.

**INCORRECT:** "Use service limits to prevent users from creating or making changes to AWS resources" is incorrect. Service limits result in a maximum limit for launching resources, but you can still make changes to existing resources (so long as you don’t exceed the limit).

**INCORRECT:** "Use AWS Certiﬁcate Manager to create a catalog of approved services" is incorrect. Certificate manager is used for issuing and managing SSL/TLS certificates, it does not maintain a catalog of approved services.

**INCORRECT:** "Use Amazon GuardDuty to record API activity to an S3 bucket" is incorrect. GuardDuty does not record API activity to an S3 bucket.

**References:**

[https://d1.awsstatic.com/whitepapers/architecture/AWS-Reliability-Pillar.pdf](https://d1.awsstatic.com/whitepapers/architecture/AWS-Reliability-Pillar.pdf)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 56:
Which type of scaling does Amazon EC2 Auto Scaling provide?

*   Horizontal
    
    (Correct)
    
*   Vertical
    
*   Linear
    
*   Incremental
    

#### Explanation

Amazon EC2 Auto Scaling scales horizontally by adding launching and terminating EC2 instances based on actual demand for your application.

**CORRECT:** "Horizontal" is the correct answer.

**INCORRECT:** "Vertical" is incorrect as EC2 auto scaling scales horizontally.

**INCORRECT:** "Linear" is incorrect as this is not the way Auto Scaling works.

**INCORRECT:** "Incremental" is incorrect as this is not the way Auto Scaling works.

**References:**

[https://aws.amazon.com/ec2/autoscaling/](https://aws.amazon.com/ec2/autoscaling/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 57:
Which AWS service is designed to be used for operational analytics?

*   Amazon EMR
    
*   Amazon Athena
    
*   Amazon QuickSight
    
*   Amazon Elasticsearch Service
    
    (Correct)
    

#### Explanation

Amazon Elasticsearch Service is involved with operational analytics such as application monitoring, log analytics and clickstream analytics. Amazon Elasticsearch Service allows you to search, explore, filter, aggregate, and visualize your data in near real-time.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-10_06-37-18-f73850ac43d8e730c601ad05331d5fb6.jpg)

**CORRECT:** "Amazon Elasticsearch Service" is the correct answer.

**INCORRECT:** "Amazon EMR" is incorrect. For big data processing using the Spark and Hadoop frameworks, Amazon EMR provides a managed service for processing vast amounts data.

**INCORRECT:** "Amazon Athena" is incorrect. Amazon Athena is used to analyze data directly in S3 and Glacier using standard SQL queries.

**INCORRECT:** "Amazon QuickSight" is incorrect. Amazon QuickSight provides a fast, cloud-powered business analytics service, that that makes it easy to build stunning visualizations and rich dashboards that can be accessed from any browser or mobile device.

**References:**

[https://aws.amazon.com/elasticsearch-service/](https://aws.amazon.com/elasticsearch-service/)

[https://aws.amazon.com/big-data/datalakes-and-analytics/](https://aws.amazon.com/big-data/datalakes-and-analytics/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 58:
Where are Amazon EBS snapshots stored?

*   On an Amazon EBS instance store
    
*   On an Amazon EFS filesystem
    
*   On Amazon S3
    
    (Correct)
    
*   Within the EBS block store
    

#### Explanation

You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are _incremental_ backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved.

**CORRECT:** "On Amazon S3" is the correct answer.

**INCORRECT:** "On an Amazon EBS instance store" is incorrect as explained above.

**INCORRECT:** "On an Amazon EFS filesystem" is incorrect as explained above.

**INCORRECT:** "Within the EBS block store" is incorrect as explained above.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 59:
Which AWS technology can be referred to as a “virtual hard disk in the cloud”?

*   Amazon EBS volume
    
    (Correct)
    
*   Amazon ENI
    
*   Amazon EFS Filesystem
    
*   Amazon S3 Bucket
    

#### Explanation

An Amazon Elastic Block Store (EBS) volume is often described as a “virtual hard disk in the cloud”. EBS volumes are block-level storage volumes that are attached to EC2 instances much as you would attach a virtual hard disk to a virtual machine in a virtual infrastructure.

**CORRECT:** "Amazon EBS volume" is the correct answer.

**INCORRECT:** "Amazon EFS Filesystem" is incorrect. An Amazon EFS filesystem is a file-level storage system that is accessed using the NFS protocol. Filesystems are mounted at the file, rather than the block level and are therefore not similar to a virtual hard disk.

**INCORRECT:** "Amazon S3 Bucket" is incorrect. Amazon S3 is an object-level storage service and is not mounted or attached. You use a REST API over HTTPS to access objects in an object store.

**INCORRECT:** "Amazon ENI" is incorrect. An Amazon Elastic Network Interface is a networking construct, not a storage construct.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 60:
According to the AWS Shared Responsibility Model, which of the following is a shared control?

*   Operating system patching
    
*   Awareness and training
    
    (Correct)
    
*   Protection of infrastructure
    
*   Client-side data encryption
    

#### Explanation

Shared Controls are controls which apply to both the infrastructure layer and customer layers, but in completely separate contexts or perspectives. In a shared control, AWS provides the requirements for the infrastructure and the customer must provide their own control implementation within their use of AWS services. Examples include patch management, configuration management, and awareness and training.

**CORRECT:** "Awareness and training" is the correct answer.

**INCORRECT:** "Operating system patching" is incorrect. Though patch management is a shared control, operating system patching specifically is a customer responsibility.

**INCORRECT:** "Protection of infrastructure" is incorrect. Protection of infrastructure is solely an AWS responsibility.

**INCORRECT:** "Client-side data encryption" is incorrect. Client and server-side data encryption are both customer responsibilities.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 61:
Which type of Elastic Load Balancer operates at the TCP connection level?

*   Network Load Balancer (NLB)
    
    (Correct)
    
*   Application Load Balancer (ALB)   
*   Amazon Route 53 Load Balancer
    
*   Classic Load Balancer (CLB)
    

#### Explanation

A Network Load Balancer functions at the fourth layer of the Open Systems Interconnection (OSI) model. NLBs direct connections based on information at the TCP connection level.

**CORRECT:** "Network Load Balancer (NLB)" is the correct answer.

**INCORRECT:** "Application Load Balancer (ALB)" is incorrect. ALBs process traffic at the application level (layer 7) based on information in the HTTP/HTTPS headers.

**INCORRECT:** "Classic Load Balancer (CLB)" is incorrect. CLBs process traffic at the TCP, SSL, HTTP and HTTPS levels (layer 4 & 7).

**INCORRECT:** "Amazon Route 53 Load Balancer" is incorrect. There is no feature called a load balancer that is associated with Route 53. You can perform a type of load balancing using multivalue answer routing.

**References:**

[https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/auto-scaling-and-elastic-load-balancing/](https://digitalcloud.training/auto-scaling-and-elastic-load-balancing/)

Question 62:
Your organization has offices around the world and some employees travel between offices. How should their accounts be setup?

*   IAM is a global service, just create the users in one place
    
    (Correct)
    
*   Enable MFA for the accounts
    
*   Set the user account as a “global” account when created
    
*   Create a separate account in IAM within each region in which they will travel
    

#### Explanation

IAM is a global service and all users that are created are able to login to the AWS Management Console from any location.

**CORRECT:** "IAM is a global service, just create the users in one place" is the correct answer.

**INCORRECT:** "Create a separate account in IAM within each region in which they will travel" is incorrect. You do not create separate IAM accounts in different regions as IAM is a global service.

**INCORRECT:** "Set the user account as a “global” account when created" is incorrect. There is no such thing as setting the account as “global”.

**INCORRECT:** "Enable MFA for the accounts" is incorrect. Enabling multi-factor authentication is a good security practice but not necessary to enable users to travel to different locations.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction\_identity-management.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction_identity-management.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 63:
What is the easiest way to store a backup of an EBS volume on Amazon S3?

*   Use S3 lifecycle actions to backup the volume   
*   Write a custom script to copy the data into a bucket   
*   Create a snapshot of the volume   
    
    (Correct)
    
*   Use Amazon Kinesis to process the data and store the results in S3   

#### Explanation

You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are _incremental_ backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved.

**CORRECT:** "Create a snapshot of the volume" is the correct answer.

**INCORRECT:** "Write a custom script to copy the data into a bucket" is incorrect. Writing a custom script could work but would not be the easiest method.

**INCORRECT:** "Use S3 lifecycle actions to backup the volume" is incorrect. You cannot apply S3 lifecycle actions to EBS volumes.

**INCORRECT:** "Use Amazon Kinesis to process the data and store the results in S3" is incorrect. Amazon Kinesis is used for processing streaming data, not data in EBS volumes.

**References:**

[https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 64:
What are the advantages of running a database service such as Amazon RDS in the cloud versus deploying on-premise? (Select TWO.)

*   You can use any database software you like, allowing greater flexibility   
*   Scalability is improved as it is quicker to implement and there is an abundance of capacity   
    
    (Correct)
    
*   There are no costs for replicating data between DBs in different data centers or regions   
*   You have full control of the operating system and can install your own operational tools   
*   High availability is easier to implement due to built-in functionality for deploying read replicas and multi-AZ   
    
    (Correct)
    

#### Explanation

The advantages of using Amazon RDS include being able to easily scale by increasing your instance type without having to go through a long procurement cycle for getting new hardware or worrying about whether capacity exists on your existing private cloud infrastructure. You can also implement fault tolerance and scalability features through multi-AZ and read replicas easily

With Amazon RDS you do not have control of the operating system and you cannot use any database software you like as you are restricted to a list of several engines. There are costs for replicating data between AZs and regions so this must be taken into account in any cost analysis.

**CORRECT:** "Scalability is improved as it is quicker to implement and there is an abundance of capacity" is a correct answer.

**CORRECT:** "High availability is easier to implement due to built-in functionality for deploying read replicas and multi-AZ" is also a correct answer.

**INCORRECT:** "You have full control of the operating system and can install your own operational tools" is incorrect as explained above.

**INCORRECT:** "You can use any database software you like, allowing greater flexibility" is incorrect as explained above.

**INCORRECT:** "There are no costs for replicating data between DBs in different data centers or regions" is incorrect as explained above.

**References:**

[https://aws.amazon.com/rds/](https://aws.amazon.com/rds/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 65:
Which of the following are pillars from the six pillars of the AWS Well-Architected Framework? (Select TWO.)

*   Resilience   
*   Confidentiality   
*   Sustainability
    
    (Correct)
    
*   Operational excellence   
    
    (Correct)
    
*   Economics   

#### Explanation

The six pillars of the AWS Well-Architected Framework are operation excellence, security, reliability, performance efficiency, cost optimization and sustainability.

**CORRECT:** "Operational excellence" is a correct answer.

**CORRECT:** "Sustainability" is also a correct answer.

**INCORRECT:** "Resilience" is incorrect as this is not one of the five pillars.

**INCORRECT:** "Confidentiality" is incorrect as this is not one of the five pillars.

**INCORRECT:** "Economics" is incorrect as this is not one of the five pillars.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Continue

Retake test

Settings

*   Report abuse
    

Fullscreen