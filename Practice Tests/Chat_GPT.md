**You:**


AWS security group have allow and deny rulea
------------------
**ChatGPT:**


Yes, AWS Security Groups allow you to define inbound and outbound rules to control traffic to and from your Amazon EC2 instances. These rules can include both allow and deny rules, depending on your requirements.

When configuring a security group, you can specify rules that allow inbound traffic from specific IP addresses or ranges, or you can allow traffic from specific security groups. These rules define the allowed sources and ports for incoming traffic.

Similarly, you can also define outbound rules to control the traffic leaving your instances. You can specify the destination IP addresses or ranges and the allowed ports or protocols for outbound connections.

The rules in a security group are evaluated in order, starting with the first rule, and the action (allow or deny) is applied based on the first rule that matches the traffic. If there is no rule that matches the traffic, the default behavior is to deny the traffic.

It's important to carefully configure your security group rules to ensure that your instances are protected while allowing the necessary traffic for your applications.
------------------
**You:**


What about an acl
------------------
**ChatGPT:**


In AWS, an Access Control List (ACL) is another layer of security that can be applied at the network level. While security groups operate at the instance level (firewall rules), ACLs operate at the subnet level (traffic control).

ACLs are stateless and provide granular control over inbound and outbound traffic by allowing or denying traffic based on rules. They can be used to control traffic between subnets or between your VPC and the Internet.

Here are a few key points about ACLs in AWS:

Subnet Level: ACLs are associated with subnets in a Virtual Private Cloud (VPC). Each subnet can have one ACL, and multiple subnets can share the same ACL.

Numbered Rules: ACLs use numbered rules to evaluate traffic. Rules are processed in order, and the first matching rule is applied. If no rule matches, a default rule is applied.

Allow and Deny Rules: Like security groups, ACLs support both allow and deny rules. You can specify rules to allow or deny traffic based on source IP addresses, destination IP addresses, ports, or protocols.

Ingress and Egress: ACLs have separate sets of rules for inbound (ingress) and outbound (egress) traffic. This allows you to have fine-grained control over the traffic entering and leaving the subnets.

Stateless: Unlike security groups, ACLs are stateless, meaning that you must explicitly allow both inbound and outbound traffic for a particular flow if you want it to be bidirectional.

Rule Evaluation: Rules in an ACL are evaluated in ascending order based on their rule number. AWS evaluates the lowest numbered rule first and continues until it finds a match.

ACLs provide an additional layer of security beyond security groups by allowing you to control traffic at the subnet level. They can be useful when you need more advanced traffic control or want to apply specific rules to a group of subnets within your VPC.
------------------
**You:**


AWS NAT
------------------
**ChatGPT:**


In AWS, NAT (Network Address Translation) is a service that allows instances in private subnets to communicate with the Internet or other AWS services while preserving their private IP addresses. NAT is commonly used in scenarios where instances in a private subnet need outbound internet access or when you want to provide access to specific AWS services.

There are two types of NAT in AWS:

NAT Gateway: NAT Gateway is a managed service provided by AWS. It allows instances in private subnets to access the internet for downloading patches, software updates, or accessing external resources. NAT Gateway provides high availability and scalability without any management overhead. It is recommended for most use cases where outbound internet access is required.

NAT Instance: NAT Instance is an EC2 instance that you can configure manually to perform network address translation. It is deployed in a public subnet and routes traffic from instances in private subnets to the internet. NAT Instances can be used in scenarios where advanced network configurations or protocols are needed, but they require manual configuration and management.

Here are some key points to know about NAT in AWS:

Inbound Traffic: By default, NAT instances and NAT Gateways do not allow inbound traffic initiated from the internet. They are designed for outbound communication from private instances.

Elastic IP: Both NAT instances and NAT Gateways require an Elastic IP (EIP) address to function. An EIP is a static public IP address that you can associate with the NAT instance or NAT Gateway.

High Availability: NAT Gateways are highly available within an Availability Zone (AZ) and can automatically failover to another AZ. They provide better availability and scalability compared to NAT Instances, which require manual configurations for high availability.

Performance: NAT Gateways offer better performance and higher bandwidth compared to NAT Instances, as they are a managed service optimized for NAT.

Cost: NAT Gateways have an hourly charge for usage and data transfer fees. NAT Instances incur EC2 instance costs along with data transfer fees. The cost considerations may vary based on your specific requirements.

NAT in AWS enables instances in private subnets to securely access the internet or other AWS services while keeping their private IP addresses hidden. It provides a vital component for building secure and scalable architectures in AWS.
------------------
**You:**


Which of the following AWS services support VPC Endpoint Gateway for a private connection from a VPC? (Select two)
------------------
**ChatGPT:**


The AWS services that support VPC Endpoint Gateway for a private connection from a VPC are as follows:

Amazon S3 (Simple Storage Service): Amazon S3 allows you to create a VPC Endpoint Gateway, which enables private connectivity from your VPC to S3 without requiring traffic to traverse the internet. This allows you to securely access S3 buckets from your VPC without exposing them to the public internet.

DynamoDB (Amazon DynamoDB): DynamoDB also supports VPC Endpoint Gateway. By creating a VPC Endpoint Gateway for DynamoDB, you can access DynamoDB tables from your VPC privately, without the need for internet gateway or NAT gateway.

These services offer VPC Endpoint Gateway functionality, allowing you to establish private connectivity from your VPC to the respective services. By utilizing VPC Endpoint Gateways, you can enhance security and network performance by eliminating the need for traffic to flow through the public internet.
------------------
**You:**


A research group wants to use EC2 instances to run a scientific computation application that has a fault tolerant architecture. The application needs high-performance hardware disks that provide fast I/O performance. As a Cloud Practitioner, which of the following storage options would you recommend as the MOST cost-effective solution?
------------------
**ChatGPT:**


As a Cloud Practitioner, for a research group wanting to run a fault-tolerant scientific computation application on EC2 instances with a focus on cost-effectiveness, I would recommend considering the Amazon Elastic Block Store (EBS) as the storage option.

Amazon EBS provides block-level storage volumes that can be attached to EC2 instances. It offers different types of EBS volumes with varying performance characteristics. For high-performance requirements, I would suggest using the following EBS volume types:

Provisioned IOPS SSD (io1): This EBS volume type is designed to deliver high I/O performance for applications with critical or demanding workloads. It allows you to specify the amount of storage capacity and the desired number of IOPS (Input/Output Operations Per Second) for your application.

General Purpose SSD (gp3): This EBS volume type provides a balance of price and performance. It offers baseline performance with the ability to burst up to higher levels for short durations. It is a cost-effective option for applications that require decent I/O performance but don't have extremely demanding workloads.

Both of these EBS volume types can provide the necessary high-performance hardware disks for the scientific computation application. However, the gp3 volume type tends to be more cost-effective compared to io1, as it offers burstable performance and lower pricing per GB.

Additionally, you can further optimize cost by choosing the appropriate volume size and IOPS level based on your workload requirements. It's recommended to analyze the application's I/O patterns and performance needs to determine the most suitable EBS volume type, size, and IOPS configuration for your specific use case.
------------------
**You:**


Which of the following AWS Support plans provide access to only core checks from the AWS Trusted Advisor Best Practice Checks? (Select two)
------------------
**ChatGPT:**


The AWS Support plans that provide access to only core checks from the AWS Trusted Advisor Best Practice Checks are as follows:

Basic Support: The Basic Support plan provides access to core checks from the AWS Trusted Advisor Best Practice Checks. This plan offers a set of general guidance and access to basic support features such as documentation, community forums, and customer service for account and billing inquiries.

Developer Support: The Developer Support plan also includes access to core checks from the AWS Trusted Advisor Best Practice Checks. In addition to the Basic Support features, Developer Support offers technical support for development and testing environments, with a faster response time compared to Basic Support.

Both the Basic Support and Developer Support plans provide access to the core checks of AWS Trusted Advisor Best Practice Checks. These checks help identify potential security, performance, and cost optimization issues in your AWS resources. However, it's important to note that advanced checks from Trusted Advisor, as well as other advanced support features, are not available with these plans and require higher-tier support plans such as Business or Enterprise Support.
------------------
**You:**


The DevOps team at an e-commerce company is trying to debug performance issues for its serverless application built using a microservices architecture. As a Cloud Practitioner, which AWS service would you recommend addressing this use-case?
------------------
**ChatGPT:**


As a Cloud Practitioner, I would recommend utilizing AWS X-Ray to address the performance issues for the serverless application built with a microservices architecture.

AWS X-Ray is a service that helps developers analyze and debug distributed applications, including serverless applications. It provides insights into the performance and behavior of individual components and the interactions between various microservices.

Here are some key features of AWS X-Ray that make it suitable for debugging performance issues in a serverless microservices application:

Distributed Tracing: AWS X-Ray allows you to trace requests as they flow through different microservices in your application. It captures information about the duration, latency, and errors at each step, giving you visibility into the performance bottlenecks and potential issues within your microservices architecture.

Service Maps: With X-Ray, you can generate service maps that visualize the connections and dependencies between your microservices. This helps you understand the overall architecture and identify any components causing performance issues or introducing latency.

Performance Analysis: X-Ray provides detailed insights into the performance of individual microservices. It helps pinpoint the specific areas where performance degradation may be occurring, allowing you to optimize and troubleshoot accordingly.

Integration with AWS Services: X-Ray integrates with various AWS services, including AWS Lambda (for serverless functions) and AWS Elastic Beanstalk (for application deployment). This enables seamless monitoring and analysis of performance for serverless applications built on these services.

By utilizing AWS X-Ray, the DevOps team can gain valuable insights into the performance of their serverless application's microservices architecture. They can identify bottlenecks, trace requests, and troubleshoot any latency issues, ultimately improving the overall performance and user experience of the e-commerce application.
------------------
**You:**


AWS Shield Advanced provides expanded DDoS attack protection for web applications running on which of the following resources? (Select two)
------------------
**ChatGPT:**


AWS Shield Advanced provides expanded DDoS (Distributed Denial of Service) attack protection for web applications running on the following resources:

Elastic Load Balancers (ELB): AWS Shield Advanced offers DDoS protection for web applications that are fronted by Elastic Load Balancers (ELB). ELB acts as a scalable and highly available load balancer, distributing traffic across multiple instances, and AWS Shield Advanced helps protect these ELBs from DDoS attacks.

Amazon CloudFront: AWS Shield Advanced also provides DDoS protection for web applications that use Amazon CloudFront as their content delivery network (CDN). CloudFront is a globally distributed CDN that caches content at edge locations, improving performance and reducing latency. Shield Advanced ensures the availability and resilience of CloudFront distributions by defending against DDoS attacks.

By utilizing AWS Shield Advanced, organizations can enhance the security of their web applications running on ELBs and CloudFront. It offers advanced DDoS protection capabilities, including real-time monitoring, automatic mitigation, and access to AWS DDoS Response Team (DRT) assistance during attacks, ensuring the reliability and availability of web applications even in the face of DDoS threats.
------------------
**You:**


Route 53?
------------------
**ChatGPT:**


I apologize for the oversight. AWS Shield Advanced also provides expanded DDoS attack protection for web applications running on Amazon Route 53.

Amazon Route 53 is a scalable and highly available domain name system (DNS) web service provided by AWS. It enables organizations to route end users to their applications by translating domain names into IP addresses.

With AWS Shield Advanced, web applications using Amazon Route 53 for DNS resolution can benefit from enhanced DDoS protection. Shield Advanced helps mitigate DDoS attacks targeting Route 53, ensuring the availability and performance of DNS services and protecting against disruptions caused by malicious traffic.

By leveraging AWS Shield Advanced with Amazon Route 53, organizations can strengthen their overall DDoS defense strategy, safeguarding the DNS infrastructure and maintaining the accessibility of their web applications.
------------------
**You:**


API gateway?
------------------
**ChatGPT:**


I apologize for the confusion. AWS Shield Advanced does not provide DDoS attack protection specifically for Amazon API Gateway.

However, Amazon API Gateway does come with its built-in DDoS protection measures. API Gateway automatically handles the majority of DDoS attacks by using managed infrastructure and implementing throttling and request rate limiting. These measures help protect API Gateway endpoints from excessive and malicious traffic.

While AWS Shield Advanced does not directly cover API Gateway, it provides comprehensive DDoS protection for other AWS services such as Elastic Load Balancers (ELB), Amazon CloudFront, and Amazon Route 53 as previously mentioned.

To enhance the security of your API Gateway endpoints, it is recommended to combine the built-in DDoS protection features of API Gateway with other AWS services such as AWS WAF (Web Application Firewall) and AWS Shield Standard for additional layers of protection against common web application threats and volumetric attacks.
------------------
**You:**


Global accelerator 
------------------
**ChatGPT:**


You are correct. AWS Global Accelerator provides DDoS protection as part of its service offering.

AWS Global Accelerator is a networking service that improves the availability and performance of applications by routing user traffic through the AWS global network infrastructure. It uses AWS edge locations to direct traffic to the nearest application endpoint, reducing latency and providing a more consistent user experience.

As part of its service, AWS Global Accelerator provides DDoS protection. It leverages the scale and global reach of the AWS network to detect and mitigate DDoS attacks, helping to ensure the availability and performance of your applications.

The DDoS protection offered by AWS Global Accelerator includes the following features:

Traffic Engineering: Global Accelerator intelligently routes traffic to the nearest healthy endpoint, distributing the load and reducing the impact of DDoS attacks on individual endpoints.

Anycast IP Addresses: Global Accelerator uses Anycast IP addresses, which are advertised across multiple AWS edge locations. This distribution of IP addresses helps absorb and mitigate DDoS traffic, improving the resilience of your applications.

AWS Shield Standard: Global Accelerator incorporates AWS Shield Standard, a built-in DDoS protection service provided by AWS. Shield Standard helps protect against common and most frequently observed DDoS attacks.

By using AWS Global Accelerator, you can benefit from its DDoS protection capabilities along with improved performance and availability for your applications, especially in scenarios where low latency and global reach are crucial.
------------------
**You:**


According to the AWS Cloud Adoption Framework (AWS CAF), what are two tasks that a company should perform when planning to migrate to the AWS Cloud and aiming to become more responsive to customer inquiries and feedback as part of their organizational transformation?
------------------
**ChatGPT:**


According to the AWS Cloud Adoption Framework (AWS CAF), when planning to migrate to the AWS Cloud and aiming to become more responsive to customer inquiries and feedback as part of an organizational transformation, there are two tasks that a company should perform:

Define Customer Engagement: The company should establish a clear understanding of how they will engage with customers in the cloud environment. This involves defining the channels and methods through which customer inquiries and feedback will be received, processed, and responded to. It may include leveraging AWS services like Amazon Simple Queue Service (SQS), Amazon Simple Notification Service (SNS), or AWS Lambda functions to manage and automate customer interactions.

Establish Feedback Loops: The company should create mechanisms to capture, analyze, and act upon customer feedback effectively. This involves implementing processes to collect customer feedback, whether it be through surveys, user forums, or other means, and integrating those feedback loops into the decision-making and product development cycles. By regularly reviewing and acting on customer feedback, the company can become more responsive to customer needs and continuously improve their products and services.

By performing these tasks, the company can enhance their customer-centric approach and leverage the capabilities of the AWS Cloud to effectively engage with customers, capture feedback, and respond quickly, enabling organizational transformation and improved responsiveness to customer inquiries and feedback.
------------------
**You:**


Organize your teams around bureaucratic design principles

Create new analytical insights with existing products and services

Organize your teams around products and value streams

Leverage legacy infrastructure for cost efficiencies

Leverage agile methods to rapidly iterate and evolve
------------------
**ChatGPT:**


When planning to migrate to the AWS Cloud and aiming to become more responsive to customer inquiries and feedback as part of an organizational transformation, the following two tasks align with the principles of the AWS Cloud Adoption Framework (AWS CAF):

Organize your teams around products and value streams: This task focuses on adopting a product-oriented approach to organizing teams. Instead of traditional siloed departments or functional areas, teams are structured around specific products or value streams. This enables cross-functional collaboration and empowers teams to take end-to-end ownership of delivering value to customers. By organizing teams in this manner, the company can improve responsiveness, agility, and the ability to align with customer needs.

Leverage agile methods to rapidly iterate and evolve: Agile methodologies, such as Scrum or Kanban, promote iterative and incremental development, fostering faster feedback loops and continuous improvement. By embracing agile methods, teams can respond more quickly to customer inquiries and feedback, adapt to changing requirements, and deliver value in shorter cycles. Agile practices encourage transparency, collaboration, and continuous learning, enabling teams to iterate on their products and services based on customer insights.

These tasks align with the AWS CAF's focus on organizational readiness and agility. By organizing teams around products and value streams and leveraging agile methods, the company can foster a customer-centric culture, enhance responsiveness, and drive continuous improvement in their cloud migration and organizational transformation journey.
------------------
**You:**


Which AWS Route 53 routing policy would you use to route traffic to multiple resources and also choose how much traffic is routed to each resource?
------------------
**ChatGPT:**


The AWS Route 53 routing policy that allows you to route traffic to multiple resources and control the distribution of traffic among them is called "Weighted Routing."

With Weighted Routing, you can assign weights (or percentages) to different resources (such as EC2 instances or load balancers) and specify how much traffic should be routed to each resource. This allows you to distribute the traffic load across multiple resources based on your desired proportions.

Here's how it works:

Assign Weights: You assign a weight to each resource, indicating the proportion of traffic you want to direct to that resource. The weights are specified as numeric values, with higher values representing a higher proportion of traffic.

DNS Resolution: When a DNS query is made, Route 53 uses the weighted distribution algorithm to route traffic based on the assigned weights. For example, if you have two resources with weights of 70 and 30, Route 53 will route 70% of the traffic to the resource with the higher weight and 30% to the resource with the lower weight.

Proportional Traffic Distribution: The weighted routing policy ensures that the distribution of traffic matches the specified proportions. This allows you to control the traffic distribution among resources and implement various deployment strategies like blue/green deployments or A/B testing.

By using the Weighted Routing policy in Route 53, you can effectively manage and distribute traffic across multiple resources while maintaining control over the proportion of traffic directed to each resource.
------------------
**You:**


Which of the following AWS Support plans provide access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software? (Select two)
------------------
**ChatGPT:**


The AWS Support plans that provide access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software are as follows:

Business Support: The Business Support plan offers access to guidance, configuration, and troubleshooting for AWS interoperability with third-party software. It provides technical support for AWS services and products, including assistance with integrating and optimizing third-party software within the AWS environment.

Enterprise Support: The Enterprise Support plan also provides access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software. It offers personalized support, architectural reviews, and hands-on guidance to help optimize the use of AWS services in conjunction with third-party software solutions.

Both the Business Support and Enterprise Support plans offer comprehensive technical support, including assistance with interoperability challenges and ensuring the smooth integration of third-party software with AWS services. These plans provide access to AWS Support engineers who can provide guidance, configuration advice, and troubleshooting assistance to address any issues related to third-party software in the AWS ecosystem.
------------------
**You:**


3:48

↑

38/65

59:23

Finish test

Question 38:

Which of the following are correct statements regarding the AWS Global Infrastructure? (Select two)

Each Availability Zone (AZ) consists of one or more discrete data centers

Each AWS Region consists of a minimum of three Availability Zones (AZ)

Each Availability Zone (AZ) consists of two or more discrete data centers

Each AWS Region consists of a minimum of two Availability Zones (AZ)

Each AWS Region consists of two or more Edge Locations
------------------
**ChatGPT:**


The correct statements regarding the AWS Global Infrastructure are:

Each Availability Zone (AZ) consists of one or more discrete data centers.
Each AWS Region consists of a minimum of three Availability Zones (AZ).

Explanation:

An Availability Zone (AZ) is a distinct location within a region, typically comprising one or more data centers with redundant power, networking, and cooling.
AWS Regions are geographical areas around the world, each consisting of multiple Availability Zones.
To ensure high availability and fault tolerance, AWS recommends a minimum of three Availability Zones within each Region.
Edge Locations, on the other hand, are part of the AWS global network infrastructure and are used for content caching and distribution purposes. They are not directly related to the structure of Availability Zones or Regions.

Therefore, the correct statements are that each Availability Zone consists of one or more discrete data centers, and each AWS Region consists of a minimum of three Availability Zones.
------------------
**You:**


Which AWS Service can be used to mitigate a Distributed Denial of Service (DDoS) attack?
------------------
**ChatGPT:**


AWS provides several services to help mitigate Distributed Denial of Service (DDoS) attacks. One of the key services specifically designed for DDoS protection is AWS Shield.

AWS Shield is a managed DDoS protection service that safeguards applications running on AWS against various types of DDoS attacks. There are two tiers of AWS Shield:

AWS Shield Standard: This is the base level of protection that is automatically provided to all AWS customers at no additional cost. It offers protection against common and most frequently observed DDoS attacks. AWS Shield Standard is built into many AWS services, including Amazon CloudFront, Elastic Load Balancing, and Amazon Route 53.

AWS Shield Advanced: This is an additional, premium service that provides more advanced DDoS protection features and greater customization options. AWS Shield Advanced offers increased protection against larger and more sophisticated DDoS attacks. It provides real-time monitoring, attack mitigation, and access to the AWS DDoS Response Team (DRT) for assistance during attacks.

Both AWS Shield Standard and AWS Shield Advanced work by automatically detecting and mitigating DDoS attacks, helping to maintain the availability of your applications and protect your infrastructure.

In addition to AWS Shield, other AWS services such as Amazon CloudFront, AWS WAF (Web Application Firewall), and AWS Global Accelerator also contribute to DDoS protection by offering features like traffic filtering, anomaly detection, and scalable edge infrastructure.

By utilizing AWS Shield, along with other complementary services, you can enhance the resilience of your applications and infrastructure against DDoS attacks in the AWS environment.
------------------
**You:**


3:49

↓

40/65

58:07

Finish test

Question 40:

The DevOps team at an IT company is moving 500 GB of data from an EC2 instance to an S3 bucket in the same region. Which of the following scenario captures the correct charges for this data transfer?

The company would be charged for both the outbound data transfer from EC2 instance as well as the inbound data transfer into the S3 bucket

The company would only be charged for the inbound data transfer into the S3 bucket

The company would not be charged for this data transfer

The company would only be charged for the outbound data transfer from EC2 instance
------------------
**ChatGPT:**


In the given scenario of moving 500 GB of data from an EC2 instance to an S3 bucket in the same region, the correct charges for this data transfer would be:

The company would be charged for both the outbound data transfer from the EC2 instance as well as the inbound data transfer into the S3 bucket.

Explanation:

AWS data transfer charges are applied for data moving across different AWS services, even within the same region.
In this case, when data is transferred from the EC2 instance to the S3 bucket, it is considered outbound data transfer from the EC2 instance and inbound data transfer into the S3 bucket.
AWS charges for both outbound and inbound data transfer separately based on the amount of data transferred.
Therefore, the company would incur charges for both the outbound data transfer from the EC2 instance and the inbound data transfer into the S3 bucket.

So, the correct answer is: The company would be charged for both the outbound data transfer from the EC2 instance as well as the inbound data transfer into the S3 bucket.
------------------
**You:**


Compared to the on-demand instance prices, what is the highest possible discount offered for spot instances?
------------------
**ChatGPT:**


The highest possible discount offered for Amazon EC2 Spot Instances compared to on-demand instance prices can vary depending on factors such as supply and demand dynamics in the Spot Instance market. However, historically, Spot Instances have been known to offer discounts of up to 90% off the on-demand prices.

Spot Instances are a cost-effective option for workloads that are flexible with regard to their start and end times. The pricing of Spot Instances is determined by the Spot market, where prices fluctuate based on supply and demand. Customers bid on the maximum price they are willing to pay for a Spot Instance, and if their bid exceeds the current Spot price, their instance will be provisioned. The Spot price is determined by AWS and fluctuates over time.

The discount offered for Spot Instances can be significantly higher than on-demand prices due to the flexible nature of Spot pricing. Spot Instances allow users to take advantage of spare EC2 capacity in the AWS infrastructure at discounted rates, making it an attractive option for cost optimization.

It's important to note that while Spot Instances can provide significant cost savings, they are subject to potential interruptions. If the Spot price exceeds the customer's bid, the instance may be terminated. Therefore, Spot Instances are best
------------------
**You:**


3:52

↓

42/65

55:02

Finish test

Question 42:

Which of the following are the advantages of cloud computing? (Select three)

Trade capital expense for variable expense

Allocate a few months of planning for your infrastructure capacity needs

Spend money on building and maintaining data centers

Trade variable expense for capital expense

Benefit from massive economies of scale

Go global in minutes and deploy applications in multiple regions around the world with just a few clicks
------------------
**ChatGPT:**


The advantages of cloud computing are as follows:

Trade capital expense for variable expense: Cloud computing allows organizations to pay for IT resources on a pay-as-you-go basis. Instead of upfront capital expenditures for hardware and infrastructure, businesses can incur variable expenses based on their actual usage. This flexibility helps in cost optimization and aligning expenses with actual needs.

Benefit from massive economies of scale: Cloud service providers, such as AWS, operate on a large scale, enabling them to achieve economies of scale. This results in lower infrastructure costs, which are passed on to customers. Organizations can benefit from this cost advantage by leveraging cloud services rather than building and maintaining their own costly infrastructure.

Go global in minutes and deploy applications in multiple regions around the world with just a few clicks: Cloud computing enables organizations to expand their reach globally quickly and easily. Cloud service providers have a global infrastructure footprint, allowing businesses to deploy applications in multiple regions with minimal effort. This provides scalability, low-latency access to customers in different geographic locations, and the ability to meet regulatory and compliance requirements in specific regions.

The options that correctly capture the advantages of cloud computing are:

Trade capital expense for variable expense
Benefit from massive economies of scale
Go global in minutes and deploy applications in multiple regions around the world with just a few clicks.
------------------
**You:**


3:53

↑

43/65

53:45

Finish test

Question 43:

A silicon valley based healthcare startup stores anonymized patient health data on Amazon S3. The CTO further wants to ensure that any sensitive data on S3 is discovered and identified to prevent any sensitive data leaks. As a Cloud Practitioner, which AWS service would you recommend addressing this use-case?

Amazon Polly

Amazon Macie

AWS Glue

AWS Secrets Manager
------------------
**ChatGPT:**


To address the use-case of discovering and identifying sensitive data stored on Amazon S3 to prevent data leaks, the recommended AWS service would be Amazon Macie.

Amazon Macie is a fully managed service that uses machine learning and pattern matching techniques to automatically discover, classify, and protect sensitive data stored in AWS. It helps organizations identify and understand sensitive data like personally identifiable information (PII), financial information, healthcare records, and more.

In the given scenario, the healthcare startup wants to ensure that any sensitive data on Amazon S3, such as patient health data, is discovered and identified to prevent any potential leaks. Amazon Macie can analyze the content of S3 objects, identify sensitive data using pre-configured or custom-defined data types, and generate alerts or take remediation actions based on policies.

By utilizing Amazon Macie, the healthcare startup can enhance their data security posture and comply with relevant regulations and privacy requirements. It provides automated data discovery and classification, reducing the risk of data exposure and helping to prevent unauthorized access or breaches of sensitive information.
------------------
**You:**


3:54

↓

44/65

53:03 Finish test

Question 44:

A company runs an application on a fleet of EC2 instances. The company wants to automate the traditional maintenance job of running timely assessments and checking for OS vulnerabilities. As a Cloud Practitioner, which service will you suggest for this use case?

Amazon Inspector

AWS Shield

Amazon Macie

Amazon GuardDuty
------------------
**ChatGPT:**


For automating timely assessments and checking for OS vulnerabilities on a fleet of EC2 instances, the recommended AWS service is Amazon Inspector.

Amazon Inspector is an automated security assessment service that helps identify security vulnerabilities and deviations from best practices in applications deployed on Amazon EC2 instances. It analyzes the network, file system, and process activity of EC2 instances to provide a comprehensive security assessment.

In the given scenario, the company wants to automate the maintenance task of running assessments and checking for OS vulnerabilities. Amazon Inspector can help achieve this by providing automated security assessments and vulnerability scanning for the EC2 instances in their fleet.

By utilizing Amazon Inspector, the company can schedule recurring assessments, receive detailed findings reports, and gain insights into potential security vulnerabilities or misconfigurations in their EC2 instances. This automation simplifies the process of identifying and addressing security issues, ensuring that the fleet of EC2 instances remains secure and protected against common vulnerabilities.
------------------
**You:**


3:55

↑

45/65

52:10

Finish test

Question 45:

Which type of cloud computing does Amazon Elastic Compute Cloud (EC2) represent?

Infrastructure as a Service (IaaS)

Network as a Service (NaaS)

Platform as a Service (PaaS)

Software as a Service (SaaS)
------------------
**ChatGPT:**


Amazon Elastic Compute Cloud (EC2) represents Infrastructure as a Service (IaaS) in the context of cloud computing.

Infrastructure as a Service (IaaS) is a cloud computing model that provides virtualized computing resources over the internet. With IaaS, users can provision and manage virtual machines (VMs) or instances, storage, networks, and other fundamental computing resources. The cloud service provider, in this case, Amazon Web Services (AWS), is responsible for the underlying infrastructure, including servers, networking, and data centers, while the user has control over the operating systems, applications, and configurations within the virtual machines.

Amazon EC2 is a core service of AWS that offers resizable compute capacity in the form of virtual machines or instances. It allows users to launch, manage, and terminate instances as needed, providing them with full control over their computing resources in the cloud. Users can choose from a variety of instance types, operating systems, and configurations to meet their specific requirements.

Therefore, Amazon EC2 is an example of Infrastructure as a Service (IaaS) within the AWS cloud computing portfolio.
------------------
**You:**


4:02

↓

46/65

45:08

Finish test

Question 46:

A big data analytics company is moving its IT infrastructure from an on-premises data center to AWS Cloud. The company has some server-bound software licenses that it wants to use on AWS. As a Cloud Practitioner, which of the following EC2 instance types would you recommend to the company?

Dedicated Host

On-Demand Instance

Dedicated Instance

Reserved Instance (RI)
------------------
**ChatGPT:**


If a big data analytics company wants to use server-bound software licenses on AWS, I would recommend using Dedicated Instances or Dedicated Hosts, depending on their specific requirements.

Dedicated Instances are EC2 instances that run on hardware dedicated to a single AWS account. They provide the benefits of EC2 instances, such as scalability and flexibility, while ensuring that the instances run on hardware exclusively dedicated to the company's use. Dedicated Instances can be launched using On-Demand pricing, allowing the company to pay for compute capacity on an as-needed basis.

Dedicated Hosts, on the other hand, are physical servers dedicated to a single AWS account. The company can have more control over the underlying host infrastructure, including the ability to bring your own licenses (BYOL) for server-bound software. By using Dedicated Hosts, the company can place EC2 instances on dedicated physical servers and leverage their existing licenses.

The choice between Dedicated Instances and Dedicated Hosts depends on factors such as license mobility requirements, cost considerations, and the level of control desired over the underlying hardware.

It's important to note that while Reserved Instances (RI) offer cost savings for long-term commitments, they are not specifically designed to address the requirement of using server-bound software licenses. RIs provide capacity reservations but do not offer the same level of dedicated hardware isolation as Dedicated Instances or Dedicated Hosts.

Therefore, for using server-bound software licenses on AWS, I would recommend either Dedicated Instances or Dedicated Hosts, depending on the specific needs and preferences of the big data analytics company.
------------------
**You:**


4:06

47/65

41:49

Finish test

Question 47:

A multi-national corporation wants to get expert professional advice on migrating to AWS and managing their applications on AWS Cloud. Which of the following entities would you recommend for this engagement?

Concierge Support Team

APN Technology Partner

AWS Trusted Advisor

APN Consulting Partner
------------------
**ChatGPT:**


For expert professional advice on migrating to AWS and managing applications on the AWS Cloud, I would recommend engaging with an APN Consulting Partner.

APN stands for Amazon Partner Network, which is a global partner program by AWS. APN Consulting Partners are professional services firms that have demonstrated expertise in helping customers design, architect, build, migrate, and manage workloads on AWS. They possess a deep understanding of AWS services and best practices and can provide guidance and support throughout the entire cloud adoption journey.

By engaging with an APN Consulting Partner, the multi-national corporation can leverage their expertise and experience to plan and execute a successful migration to AWS. These partners offer a wide range of services, including architecture design, workload assessment, cost optimization, security implementation, and ongoing management of applications on the AWS Cloud.

While AWS Trusted Advisor provides automated best practice checks and recommendations, it is not specifically focused on providing expert professional advice for migrations or application management. The Concierge Support Team primarily assists with general guidance and support related to billing and account management.

APN Technology Partners, on the other hand, are independent software vendors (ISVs) that develop and offer software solutions that are integrated with AWS services. While they can provide valuable technology solutions, they may not be the ideal choice for comprehensive migration and application management advice.

Therefore, for the engagement requiring expert professional advice on migrating to AWS and managing applications, I would recommend partnering with an APN Consulting Partner.
------------------
**You:**


4:07

48/65

41:07

Finish test

Question 48:

A company wants to improve the resiliency of its flagship application so it wants to move from its traditional database system to a managed AWS database service to support active-active configuration in both the East and West US AWS regions. The active-active configuration with cross- region support is the prime criteria for any database solution that the company considers.

Which AWS database service is the right fit for this requirement?

Amazon Relational Database Service (Amazon RDS) for MYSQL

Amazon DynamoDB with DynamoDB Accelerator

Amazon DynamoDB with global tables

Amazon Aurora with multi-master clusters
------------------
**ChatGPT:**


For achieving an active-active configuration with cross-region support, the AWS database service that would be the right fit for this requirement is Amazon Aurora with multi-master clusters.

Amazon Aurora is a relational database service offered by AWS that is compatible with MySQL and PostgreSQL. It is designed for high availability, durability, and performance. Aurora supports a multi-master replication feature that allows for read and write operations to be distributed across multiple database instances.

By utilizing Aurora's multi-master clusters, the company can set up active-active configurations in both the East and West US AWS regions. The multi-master feature enables read and write access to be distributed across multiple instances in different regions, providing resiliency and ensuring that the application remains operational even if one region faces an outage.

Amazon RDS for MySQL is a managed relational database service, but it does not offer native multi-master capabilities for active-active configurations across regions.

Amazon DynamoDB with DynamoDB Accelerator (DAX) is a fully managed NoSQL database service, but it does not provide native support for multi-master configurations across regions.

Amazon DynamoDB with global tables, on the other hand, is a suitable option for global-scale applications that require multi-region replication, but it does not provide full active-active capabilities as it focuses on eventual consistency rather than immediate consistency.

Therefore, for the company's requirement of an active-active configuration with cross-region support, the recommended AWS database service would be Amazon Aurora with multi-master clusters.
------------------
**You:**


4:07

49/65

40:24 Finish test

Question 49:

According to the AWS Shared Responsibility Model, which of the following are responsibilities of AWS? (Select two)

Creating S3 bucket policies for appropriate user access

Replacing faulty hardware of Amazon EC2 instances

Creating IAM role for accessing Amazon EC2 instances

Enabling Multi Factor Authentication on AWS accounts in your organization

Maintaining Amazon S3 data in different availability zones to keep it durable
------------------
**ChatGPT:**


According to the AWS Shared Responsibility Model, the responsibilities of AWS include:

Replacing faulty hardware of Amazon EC2 instances: AWS is responsible for the underlying infrastructure, including the physical hardware of EC2 instances. If there is a hardware failure, AWS takes care of replacing the faulty hardware to ensure the availability of the service.

Maintaining Amazon S3 data in different availability zones to keep it durable: AWS ensures the durability of data stored in Amazon S3 by automatically replicating it across multiple availability zones within a region. This redundancy helps protect against data loss in the event of hardware or facility failures.

The other options mentioned in the question are the responsibilities of the customer or user of AWS services:

Creating S3 bucket policies for appropriate user access: This is the responsibility of the customer to configure and manage access controls, including bucket policies, to control user access to S3 buckets.

Creating IAM role for accessing Amazon EC2 instances: Customers are responsible for managing IAM (Identity and Access Management) roles and policies to control access to EC2 instances.

Enabling Multi-Factor Authentication (MFA) on AWS accounts in your organization: Customers are responsible for enabling and managing MFA for their AWS accounts to provide an additional layer of security.

Therefore, the correct options based on the AWS Shared Responsibility Model are:

Replacing faulty hardware of Amazon EC2 instances (AWS responsibility)
Maintaining Amazon S3 data in different availability zones to keep it durable (AWS responsibility)
------------------
**You:**


4:08

↓

50/65

39:47 Finish test

Question 50:

Which of the following Amazon S3 storage classes takes the most time to retrieve data (also known as first byte latency)?

Amazon S3 Intelligent-Tiering

Amazon S3 Standard

Amazon S3 Glacier Deep Archive

Amazon S3 Glacier Flexible Retrieval
------------------
**ChatGPT:**


Among the given options, the Amazon S3 storage class that takes the most time to retrieve data (also known as first byte latency) is Amazon S3 Glacier Deep Archive.

Amazon S3 Glacier Deep Archive is designed for long-term archival storage of data with infrequent access. It offers the lowest cost per gigabyte but has a longer retrieval time compared to other storage classes. Retrieving data from Amazon S3 Glacier Deep Archive can take several hours, as it involves a retrieval process that needs to be initiated before the data becomes accessible.

Amazon S3 Intelligent-Tiering and Amazon S3 Standard have lower retrieval times compared to Amazon S3 Glacier Deep Archive. They provide faster access to data, with Amazon S3 Intelligent-Tiering automatically moving data between two access tiers based on usage patterns, and Amazon S3 Standard offering immediate access to data.

Amazon S3 Glacier Flexible Retrieval is a retrieval option within the Amazon S3 Glacier storage class. It allows for expedited or standard retrievals, depending on the urgency of data access requirements. Expedited retrievals offer faster access than standard retrievals but have higher costs associated with them.

Therefore, among the given options, Amazon S3 Glacier Deep Archive has the longest retrieval time (first byte latency) when compared to the other Amazon S3 storage classes.
------------------
**You:**


4:09

↓

51/65

38:58

Finish test

Question 51:

A web application stores all of its data on Amazon S3 buckets. A client has mandated that data be encrypted before sending it to Amazon S3.

Which of the following is the right technique for

encrypting data as needed by the customer?

Enable server-side encryption with Amazon S3 Managed Keys (SSE-S3)

Enable client-side encryption using AWS encryption SDK

Enable server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS)

Encryption is enabled by default for all the objects written to Amazon S3. Additional configuration is not required
------------------
**ChatGPT:**


To encrypt data as needed by the customer before sending it to Amazon S3, the right technique would be to enable client-side encryption using the AWS Encryption SDK.

Client-side encryption involves encrypting the data on the client-side before it is uploaded to Amazon S3. The AWS Encryption SDK provides a set of libraries and APIs that enable developers to easily encrypt and decrypt data using strong encryption algorithms. With client-side encryption, the customer has full control over the encryption process, including key management and encryption algorithms.

The other options mentioned in the question are related to server-side encryption options in Amazon S3:

Enable server-side encryption with Amazon S3 Managed Keys (SSE-S3): With this option, Amazon S3 manages the encryption keys used to encrypt and decrypt the data. The keys are stored and managed by AWS, providing a convenient encryption solution. However, the encryption and decryption process happens on the server-side, not the client-side.

Enable server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS): This option allows you to use AWS KMS to manage the encryption keys used by Amazon S3. With SSE-KMS, the encryption and decryption process also happens on the server-side.

Encryption is enabled by default for all the objects written to Amazon S3. Additional configuration is not required: This statement is not entirely accurate. While Amazon S3 provides default encryption options, such as SSE-S3 and SSE-KMS, they need to be explicitly enabled for each S3 bucket or object. By default, encryption is not applied to objects unless the customer enables it.

Therefore, for encrypting data as needed by the customer before sending it to Amazon S3, the recommended technique is to enable client-side encryption using the AWS Encryption SDK.
------------------
**You:**


4:10

↓

52/65

38:05 Finish test

Question 52:

Which of the following are the storage services offered by the AWS Cloud? (Select two)

Amazon Elastic File System (Amazon EFS)

Amazon Elastic Compute Cloud (Amazon EC2)

Amazon Simple Queue Service (SQS)

Amazon Simple Storage Service (Amazon S3)

Amazon Simple Notification Service (SNS)
------------------
**ChatGPT:**


The storage services offered by the AWS Cloud are:

Amazon Simple Storage Service (Amazon S3): Amazon S3 is an object storage service that provides secure, durable, and scalable storage for various types of data. It is commonly used for storing and retrieving large amounts of unstructured data, such as images, videos, documents, backups, and log files.

Amazon Elastic File System (Amazon EFS): Amazon EFS is a scalable and fully managed file storage service that supports the Network File System (NFS) protocol. It provides shared file storage that can be accessed concurrently from multiple EC2 instances, making it suitable for workloads that require shared file access.

The other options mentioned in the question are not storage services:

Amazon Elastic Compute Cloud (Amazon EC2): Amazon EC2 is a virtual server infrastructure service that provides resizable compute capacity in the cloud. It allows users to launch and manage virtual machines (EC2 instances) to run their applications.

Amazon Simple Queue Service (SQS): SQS is a fully managed message queuing service that enables decoupling and asynchronous communication between distributed components of an application. It is primarily used for building distributed systems and facilitating communication between different services.

Amazon Simple Notification Service (SNS): SNS is a fully managed messaging service that enables the publishing and delivery of messages to subscribers or endpoints. It is used for sending notifications, alerts, and other event-driven communications to various subscribers, such as email, SMS, mobile push, and more.

Therefore, the correct options for the storage services offered by the AWS Cloud are:

Amazon Simple Storage Service (Amazon S3)
Amazon Elastic File System (Amazon EFS)
------------------
**You:**


4:10

↑

53/65

37:27

Finish test

A Project Manager, working on AWS for the first time, is confused about how credits are used in AWS. There are two credits available in the manager's account. Credit one is for $100, expires July 2022, and can be used for either Amazon S3 or Amazon EC2. Credit two is for $50, expires December 2022, and can be used only for Amazon EC2. The manager's AWS account has incurred two charges: $1000 for Amazon EC2 and $500 for Amazon S3.

What will be the outcome on the overall bill once the credits are used? (Select two)

Then, credit two is applied to $500 for Amazon S3 usage

Then, credit two is applied to the

remaining $900 of Amazon EC2 usage

Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge

<

။။
------------------
**ChatGPT:**


Based on the provided information, the outcome on the overall bill once the credits are used will be:

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge.

Credit one can be used for either Amazon S3 or Amazon EC2, and since it has a higher value of $100, it will be applied to the Amazon EC2 charge of $1000. After applying credit one, the remaining balance for Amazon EC2 will be $900.

Then, credit two is applied to the remaining $900 of Amazon EC2 usage.

Credit two is specifically for Amazon EC2 and has a value of $50. Since there is a remaining balance of $900 for Amazon EC2 after applying credit one, credit two can be applied to further reduce the cost. After applying credit two, the remaining balance for Amazon EC2 will be $850.

Therefore, the correct outcomes on the overall bill once the credits are used are:

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge.
Then, credit two is applied to the remaining $900 of Amazon EC2 usage.

The other options mentioned in the question are not correct:

Then, credit two is applied to $500 for Amazon S3 usage: Credit two cannot be applied to Amazon S3 as it is specifically for Amazon EC2.
Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones: Both credits can be used in the same billing cycle if they are applicable to the respective services.
------------------
**You:**


4:10

↑

53/65

37:27

Finish test

A Project Manager, working on AWS for the first time, is confused about how credits are used in AWS. There are two credits available in the manager's account. Credit one is for $100, expires July 2022, and can be used for either Amazon S3 or Amazon EC2. Credit two is for $50, expires December 2022, and can be used only for Amazon EC2. The manager's AWS account has incurred two charges: $1000 for Amazon EC2 and $500 for Amazon S3.

What will be the outcome on the overall bill once the credits are used? (Select two)

Then, credit two is applied to $500 for Amazon S3 usage

Then, credit two is applied to the

remaining $900 of Amazon EC2 usage

Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge

<

။။
------------------
**ChatGPT:**


I apologize for the confusion. The correct outcomes on the overall bill once the credits are used are:

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge.

Credit one can be used for either Amazon S3 or Amazon EC2, and since it has a higher value of $100, it will be applied to the Amazon EC2 charge of $1000. After applying credit one, the remaining balance for Amazon EC2 will be $900.

Only one credit can be used in one billing cycle, and the customer has a choice to choose from the available ones.

Since credit two is specifically for Amazon EC2 and cannot be used for Amazon S3, it cannot be applied to the $500 charge for Amazon S3 usage. Therefore, credit two will not be used in this case.

Therefore, the correct outcomes on the overall bill once the credits are used are:

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge.
Only one credit can be used in one billing cycle, and the customer has a choice to choose from the available ones.

Apologies for the previous incorrect response.
------------------
**You:**


4:13

↓

54/65

34:33

Finish test

Question 54:

Which of the following AWS services has encryption enabled by default?

Amazon Elastic File System (Amazon EFS)

Amazon Elastic Block Store (Amazon EBS)

AWS CloudTrail Logs

Amazon Relational Database Service (Amazon RDS)
------------------
**ChatGPT:**


The correct answer is:

AWS CloudTrail Logs

AWS CloudTrail Logs have encryption enabled by default. CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. When you create a trail in CloudTrail, the log files generated by the service are automatically encrypted using AWS Key Management Service (AWS KMS). This ensures that the log files are encrypted at rest and provides an additional layer of security for your audit trail.

The other services mentioned, namely Amazon Elastic File System (Amazon EFS), Amazon Elastic Block Store (Amazon EBS), and Amazon Relational Database Service (Amazon RDS), do not have encryption enabled by default. Encryption for these services needs to be explicitly configured by the user.
------------------
**You:**


4:14

55/65

33:44 Finish test

Question 55:

A company needs a storage solution for a project wherein the data is accessed less frequently but needs rapid access when required. Which S3 storage class is the MOST cost-effective for the given use- case?

Amazon S3 Glacier (S3 Glacier)

Amazon S3 Standard-Infrequent Access (S3 Standard-IA)

Amazon S3 Standard

Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)
------------------
**ChatGPT:**


The correct answer is:

Amazon S3 Glacier (S3 Glacier)

Amazon S3 Glacier is the most cost-effective storage class for data that is accessed less frequently but needs rapid access when required. It is designed for long-term data archival and offers the lowest storage costs among the S3 storage classes.

Amazon S3 Standard-Infrequent Access (S3 Standard-IA) is also suitable for data that is accessed less frequently, but it has higher storage costs compared to Amazon S3 Glacier. S3 Standard-IA is designed for data that requires less frequent access but still needs quick retrieval when requested.

Amazon S3 Standard and Amazon S3 Intelligent-Tiering are not the most cost-effective options for the given use-case. Amazon S3 Standard is the default storage class and provides immediate access to data but has higher costs. Amazon S3 Intelligent-Tiering automatically moves data between different storage tiers based on its access patterns, which may not be the most cost-effective option for data accessed less frequently.

Therefore, for the given use-case, Amazon S3 Glacier is the most cost-effective storage class.
------------------
**You:**


4:51

↑

57/65

27:31

Finish test

Question 57:

A startup wants to provision an EC2 instance for the lowest possible cost for a long-term duration but needs to make sure that the instance would never be interrupted. As a Cloud Practitioner, which of the following options would you recommend?

EC2 Spot Instance

EC2 Dedicated Host

EC2 On-Demand Instance

EC2 Reserved Instance (RI)
------------------
**ChatGPT:**


The correct answer is:

EC2 Reserved Instance (RI)

For the lowest possible cost for a long-term duration and the assurance of uninterrupted usage, EC2 Reserved Instances (RI) would be the recommended option. Reserved Instances provide a significant discount compared to On-Demand Instances in exchange for a commitment of usage over a specified term, typically one or three years. By reserving capacity in advance, the startup can optimize costs and ensure the instance availability without the risk of interruption.

EC2 Spot Instances offer the lowest cost among the EC2 instance types but come with the risk of interruption. Spot Instances are ideal for workloads that are flexible and can handle interruptions, such as batch processing, data analysis, or CI/CD pipelines.

EC2 Dedicated Hosts are physical servers dedicated to a specific AWS account and provide visibility and control over the underlying infrastructure but are typically more expensive compared to other instance types.

EC2 On-Demand Instances provide instances with no upfront commitments or long-term contracts, allowing for flexibility but at a higher cost compared to Reserved Instances.

Considering the requirement for the lowest cost, long-term duration, and the assurance of no interruption, EC2 Reserved Instances would be the recommended option.
------------------
**You:**


4:52

↓

58/65

26:18 Finish test

Question 58:

Which of the following entities applies patches to the underlying OS for Amazon Aurora?

The AWS customer by using AWS Systems Manager

The AWS customer by SSHing on the instances

The AWS Support after receiving a request from the customer

The AWS Product Team automatically
------------------
**ChatGPT:**


The correct answer is:

The AWS Product Team automatically

For Amazon Aurora, the AWS Product Team takes care of applying patches to the underlying operating system. Amazon Aurora is a managed database service provided by AWS, and the AWS Product Team is responsible for managing and maintaining the underlying infrastructure, including patching the operating system.

As a customer, you do not need to manually apply patches or SSH into the instances to perform OS-level maintenance. AWS handles these tasks transparently, allowing you to focus on managing your database and applications without worrying about the underlying infrastructure.

AWS Systems Manager is a service that provides centralized visibility and control over your AWS resources, including managing and automating operational tasks. While you can use AWS Systems Manager for various management tasks, such as automation, patch management, and configuration management, it is not necessary to use it specifically for patching the underlying OS of Amazon Aurora.

AWS Support assists customers with technical issues and provides guidance and recommendations. However, they do not directly apply patches to the underlying OS of Amazon Aurora.

In summary, the AWS Product Team automatically applies patches to the underlying OS for Amazon Aurora, relieving customers of that responsibility.
------------------
**You:**


4:53

↓

59/65

25:48

Finish test

Question 59:

A company wants to identify the optimal AWS resource configuration for its workloads so that the company can reduce costs and increase workload performance. Which of the following services can be used to meet this requirement?

AWS Cost Explorer

AWS Compute Optimizer

AWS Systems Manager

AWS Budgets
------------------
**ChatGPT:**


The correct answer is:

AWS Compute Optimizer

AWS Compute Optimizer is the service that can be used to identify the optimal AWS resource configuration for workloads. It uses machine learning algorithms to analyze historical resource utilization and provide recommendations for right-sizing your AWS resources.

By leveraging AWS Compute Optimizer, you can gain insights into your workload's performance and resource utilization patterns. The service will provide specific recommendations on which EC2 instance types and sizes, as well as Auto Scaling group configurations, are best suited for your workloads. This helps you optimize your resources to achieve a balance between cost and performance.

AWS Cost Explorer, on the other hand, is a service that provides comprehensive cost visibility and analysis of your AWS spending. It helps you understand your cost patterns, identify cost drivers, and forecast future costs. While AWS Cost Explorer provides valuable cost-related insights, it does not specifically focus on workload performance optimization.

AWS Systems Manager is a management service that provides a unified interface for managing your AWS resources. It offers features such as automation, parameter management, patch management, and more. While AWS Systems Manager can help with managing resources, it does not provide specific recommendations for optimizing resource configurations.

AWS Budgets is a service that allows you to set and track cost and usage budgets for your AWS accounts. It helps you monitor your spending and receive alerts when your costs or usage exceed predefined thresholds. While AWS Budgets helps with cost management and monitoring, it does not provide recommendations for optimizing resource configurations.

In summary, for identifying the optimal AWS resource configuration for workloads, AWS Compute Optimizer is the recommended service to use.
------------------
**You:**


4:53

↓

60/65

25:09 Finish test

Question 60:

Which of the following is the MOST cost-effective option to purchase an EC2 Reserved Instance (RI)?

No upfront payment option with standard 1-year term

All upfront payment option with the standard 1-year term

No upfront payment option with standard

3-years term

Partial upfront payment option with standard 3-years term
------------------
**ChatGPT:**


The correct answer is:

All upfront payment option with the standard 1-year term

When purchasing an EC2 Reserved Instance (RI), the most cost-effective option is to choose the all upfront payment option with the standard 1-year term.

Reserved Instances offer significant cost savings compared to On-Demand instances, as they provide a capacity reservation and a discounted hourly rate for the instance usage. RI pricing options include No upfront, Partial upfront, and All upfront payment options, and the term can be either 1 year or 3 years.

Among these options, choosing the all upfront payment option with the standard 1-year term provides the highest cost savings. By making an upfront payment for the entire 1-year term, you receive the maximum discount on the hourly rate for the instance.

The no upfront payment option with the standard 1-year term would have a slightly higher hourly rate compared to the all upfront payment option. The no upfront payment option with the standard 3-year term and the partial upfront payment option with the standard 3-year term offer longer-term commitments but do not provide the same level of cost savings as the all upfront payment option with the standard 1-year term.

It's important to note that the cost-effectiveness of the RI options may vary depending on your specific usage patterns and requirements. It's recommended to analyze your usage and financial goals before selecting the appropriate RI payment option.
------------------
**You:**


4:55

↓

61/65

23:27 Finish test

Question 61:

Which AWS services can be used to facilitate

organizational change management, part of the Reliability pillar of AWS Well-Architected Framework? (Select three)

Amazon Inspector

Amazon GuardDuty

AWS Config

Amazon CloudWatch

AWS CloudTrail

AWS Trusted Advisor
------------------
**ChatGPT:**


The correct answers are:

AWS Config
AWS CloudTrail
AWS Trusted Advisor

These three AWS services can be used to facilitate organizational change management as part of the Reliability pillar of the AWS Well-Architected Framework.

AWS Config: AWS Config provides a detailed inventory of your AWS resources and tracks changes to resource configurations over time. It helps you assess, audit, and evaluate the configurations of your resources, making it easier to manage and track changes in your environment.

AWS CloudTrail: AWS CloudTrail provides a record of actions taken by a user, role, or AWS service in your AWS account. It captures API calls and logs important information about those calls, such as the identity of the caller, the time of the call, and the request parameters. This helps with auditing, compliance, and troubleshooting.

AWS Trusted Advisor: AWS Trusted Advisor is an automated tool that analyzes your AWS environment and provides recommendations for optimizing security, performance, cost, and fault tolerance. It helps identify potential issues and suggests improvements to enhance the reliability of your infrastructure.

Amazon Inspector, Amazon GuardDuty, and Amazon CloudWatch are valuable services but are not specifically focused on facilitating organizational change management as described in the question.
------------------
**You:**


4:56

↓

62/65

22:37 Finish test

Question 62:

An IT company is planning to migrate from an on- premises environment to AWS Cloud. Which of the following expense areas would result in cost savings when the company moves to AWS Cloud? (Select two)

Project manager salary

Data center physical security expenditure

Data center hardware infrastructure expenditure

SaaS application license fee

Developer salary
------------------
**ChatGPT:**


The correct answers are:

Data center hardware infrastructure expenditure
SaaS application license fee

When an IT company migrates from an on-premises environment to the AWS Cloud, it can realize cost savings in several areas. However, in the context of the given options, the two expense areas that would result in cost savings are:

Data center hardware infrastructure expenditure: By migrating to the AWS Cloud, the company no longer needs to invest in and maintain its own hardware infrastructure. AWS provides a scalable and flexible infrastructure as a service (IaaS) model, allowing companies to leverage cloud resources instead of purchasing and maintaining physical hardware.

SaaS application license fee: In the AWS Cloud, companies can take advantage of various software as a service (SaaS) offerings provided by AWS and its partners. These SaaS applications are typically available on a pay-as-you-go or subscription basis, eliminating the need for upfront license fees or long-term commitments associated with traditional software licensing.

While there may be other areas where cost savings can be achieved, such as reduced maintenance and management costs, the given options specifically highlight the areas where cost savings are most likely to be realized.
------------------
**You:**


4:57

↓

63/65

21:53

Finish test

Question 63:

What are the advantages that AWS Cloud offers over a traditional on-premises IT infrastructure? (Select two)

Trade capital expense for variable expense

Eliminate guessing on your infrastructure capacity needs

Increase speed and agility by keeping servers and other required resources ready before time in your data centers

Make a capacity decision before deploying an application, to reduce costs

Provide lower latency to applications by maintaining servers on-premises
------------------
**ChatGPT:**


The correct answers are:

Trade capital expense for variable expense
Eliminate guessing on your infrastructure capacity needs

The advantages that AWS Cloud offers over a traditional on-premises IT infrastructure include:

Trade capital expense for variable expense: With AWS Cloud, companies can pay for the resources and services they use on a variable expense model, rather than making upfront investments in hardware and infrastructure. This allows for greater flexibility and cost optimization, as companies can scale their resources up or down based on their actual needs.

Eliminate guessing on your infrastructure capacity needs: AWS Cloud provides the ability to scale resources on-demand, allowing companies to dynamically adjust their infrastructure capacity based on changing requirements. This eliminates the need for upfront capacity planning and reduces the risk of overprovisioning or underutilization of resources.

The other options mentioned in the question ("Increase speed and agility by keeping servers and other required resources ready before time in your data centers" and "Make a capacity decision before deploying an application, to reduce costs") are not advantages of AWS Cloud over a traditional on-premises IT infrastructure. These statements do not accurately represent the benefits of using AWS Cloud and may lead to confusion. Additionally, the statement "Provide lower latency to applications by maintaining servers on-premises" is incorrect, as AWS Cloud's global infrastructure and content delivery network (CDN) can provide low-latency access to applications and content from multiple locations around the world.
------------------
**You:**


5:00

↓

64/65

18:33

Finish test

Question 64:

An e-commerce company has deployed an RDS database in a single Availability Zone (AZ). The engineering team wants to ensure that in case of an AZ outage, the database should continue working on the same endpoint without any manual administrative intervention. Which of the following solutions can address this use-case?

Configure the database in RDS read replica mode with automatic failover to the standby

Deploy the database via AWS Elastic Beanstalk

Provision the database via AWS CloudFormation

Configure the database in RDS Multi-AZ deployment with automatic failover to the standby
------------------
**ChatGPT:**


The solution that can address the use-case described is:

Configure the database in RDS Multi-AZ deployment with automatic failover to the standby.

By configuring the RDS database in a Multi-AZ deployment, AWS automatically provisions and maintains a synchronous standby replica of the database in a different Availability Zone (AZ). In the event of an AZ outage, AWS automatically fails over to the standby replica, promoting it to the primary database instance. This failover process is handled by AWS without the need for manual administrative intervention. By using Multi-AZ deployment with automatic failover, the e-commerce company can ensure high availability and continuity of their database operations even in the event of an AZ outage.

The other options mentioned in the question ("Configure the database in RDS read replica mode with automatic failover to the standby" and "Deploy the database via AWS Elastic Beanstalk" and "Provision the database via AWS CloudFormation") do not specifically address the requirement of maintaining the database on the same endpoint without manual intervention during an AZ outage. RDS read replicas, AWS Elastic Beanstalk, and AWS CloudFormation have other purposes and functionalities, but they do not provide the same level of automated failover and high availability as the Multi-AZ deployment with automatic failover option.
------------------
**You:**


5:01

↑

65/65

17:56 Finish test

Question 65:

Which of the following AWS services can be used to connect a company's on-premises environment to a VPC without using the public internet?

Internet Gateway

AWS Direct Connect

VPC Endpoint

AWS Site-to-Site VPN
------------------
**ChatGPT:**


The AWS service that can be used to connect a company's on-premises environment to a Virtual Private Cloud (VPC) without using the public internet is:

AWS Direct Connect

AWS Direct Connect establishes a dedicated network connection between an on-premises data center and an AWS Direct Connect location. This dedicated connection bypasses the public internet, providing a more reliable and consistent network experience. With AWS Direct Connect, you can establish private connectivity between your on-premises environment and your VPC, allowing you to access AWS resources securely and directly.

The other options mentioned in the question ("Internet Gateway," "VPC Endpoint," and "AWS Site-to-Site VPN") have different purposes:

An Internet Gateway is used to connect a VPC to the internet, allowing communication between resources in the VPC and the public internet.
A VPC Endpoint enables private connectivity between a VPC and other AWS services without traversing the internet. However, it does not establish connectivity with an on-premises environment.
AWS Site-to-Site VPN is used to create an encrypted tunnel between an on-premises network and an AWS VPC over the public internet, providing secure communication.
------------------
**You:**


5:06

↓

1/65

1:29:58

Finish test

Question 1:

Which tool will help you review your workloads against current AWS best practices for cost optimization, security, and performance improvement and then obtain advice to architect them better?

Amazon CloudWatch

AWS Cost Explorer

AWS Trusted Advisor

Amazon Inspector
------------------
**ChatGPT:**


The tool that will help you review your workloads against current AWS best practices for cost optimization, security, and performance improvement and provide advice to architect them better is:

AWS Trusted Advisor

AWS Trusted Advisor is a service that provides real-time guidance to help you optimize your AWS resources, improve security and performance, and reduce costs. It evaluates your AWS environment based on AWS best practices and provides recommendations across various categories, including cost optimization, security, performance, and fault tolerance. By using AWS Trusted Advisor, you can identify areas for improvement and implement changes to optimize your workloads based on industry best practices.
------------------
**You:**


5:07

↓

2/65

1:29:02

Finish test

Question 2:

Which of the following options can be used to access and manage all AWS services (Select three)?

AWS Software Development Kit (SDK)

AWS Management Console

AWS Systems Manager

AWS Secrets Manager

Amazon API Gateway

AWS Command Line Interface (AWS CLI)
------------------
**ChatGPT:**


The options that can be used to access and manage all AWS services are:

AWS Management Console: The AWS Management Console is a web-based interface that allows you to access and manage all of your AWS services. It provides a graphical user interface (GUI) to interact with various AWS resources, configure settings, and monitor your applications.

AWS Command Line Interface (AWS CLI): The AWS CLI is a command-line tool that allows you to interact with AWS services through the command line. It provides a set of commands for managing AWS resources, automating tasks, and scripting. The AWS CLI is available for Windows, macOS, and Linux.

AWS Software Development Kit (SDK): The AWS SDKs are software development kits that provide libraries, code samples, and documentation for various programming languages. The SDKs allow you to programmatically access and manage AWS services in your applications. AWS SDKs are available for popular programming languages such as Java, Python, .NET, and more.

Note: While AWS Systems Manager and AWS Secrets Manager are powerful services for managing and securing your AWS resources, they are not directly used to access and manage all AWS services like the three options mentioned above.
------------------
**You:**


5:08

↓

3/65

1:28:20

Finish test

Question 3:

The engineering team at an IT company wants to monitor the CPU utilization for its fleet of Amazon Elastic Compute Cloud (Amazon EC2) instances and send an email to the administrator if the utilization exceeds 80%. As a Cloud Practitioner, which AWS services would you recommend to build this solution? (Select two)

Amazon Simple Notification Service (SNS)

Amazon CloudWatch

Amazon Simple Queue Service (SOS)

AWS Lambda

AWS CloudTrail
------------------
**ChatGPT:**


To build the solution for monitoring CPU utilization of Amazon EC2 instances and sending an email notification if the utilization exceeds 80%, the recommended AWS services are:

Amazon CloudWatch: Amazon CloudWatch is a monitoring and observability service provided by AWS. It allows you to collect and track metrics, logs, and events from various AWS resources, including Amazon EC2 instances. You can configure CloudWatch to collect CPU utilization metrics for the EC2 instances and set up alarms to trigger actions when certain thresholds are met, such as when the CPU utilization exceeds 80%.

Amazon Simple Notification Service (SNS): Amazon SNS is a fully managed messaging service that enables you to send notifications to various endpoints, including email, SMS, mobile push, and more. Once you have configured the CloudWatch alarm to trigger when CPU utilization exceeds 80%, you can configure an SNS topic as the action for the alarm. When the alarm is triggered, an email notification can be sent to the administrator via SNS.

Note: AWS Lambda and AWS CloudTrail are not directly related to building this specific solution. AWS Lambda is a serverless compute service used for running code in response to events, and AWS CloudTrail is a service for auditing and monitoring API calls made within your AWS account.
------------------
**You:**


5:09

↓

4/65

1:27:12

Finish test

Question 4:

Which of the following are examples of Horizontal Scalability (aka Elasticity)? (Select two)

Modify an EC2 instance type from t2.nano to u-12tb1.metal

Elastic Load Balancing (ELB)

Read Replicas in Amazon Relational Database Service (Amazon RDS)

Modify a Database instance to higher CPU and RAM

Add a bigger CPU to a computer
------------------
**ChatGPT:**


The examples of Horizontal Scalability, also known as Elasticity, are:

Elastic Load Balancing (ELB): Elastic Load Balancing is a service provided by AWS that automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, and IP addresses. It helps in achieving horizontal scalability by allowing you to add or remove instances based on the demand, thus scaling the application horizontally.

Read Replicas in Amazon RDS: Amazon RDS provides a managed database service, and it allows you to create read replicas of your primary database. Read replicas are copies of the primary database that can handle read traffic, thereby distributing the load and improving performance. By adding read replicas, you can horizontally scale the read capacity of your database system.

Note: The other options mentioned, such as modifying an EC2 instance type, modifying a database instance to higher CPU and RAM, and adding a bigger CPU to a computer, are related to vertical scalability (scaling up), where you increase the resources of a single instance to handle more load.
------------------
**You:**


5:11

↑

5/65

1:25:35

Finish test

Question 5:

Which AWS service can be used to store, manage, and deploy Docker container images?

AWS Lambda

Amazon Elastic Container Registry (Amazon ECR)

Amazon Elastic Container Service (Amazon ECS)

Amazon Elastic Compute Cloud (Amazon

EC2)
------------------
**ChatGPT:**


The AWS service that can be used to store, manage, and deploy Docker container images is Amazon Elastic Container Registry (Amazon ECR). Amazon ECR is a fully managed container registry service that makes it easy to store, manage, and deploy Docker container images. It provides a secure and scalable repository for storing Docker images, allowing you to easily share and distribute container images within your organization or with other AWS accounts. Amazon ECR integrates seamlessly with other AWS services like Amazon ECS (Elastic Container Service) and AWS Fargate, making it a convenient choice for container image management in the AWS ecosystem.
------------------
**You:**


5:12

↓

6/65

1:24:29

Finish test

Question 6:

A company's flagship application runs on a fleet of Amazon Elastic Compute Cloud (Amazon EC2) instances. As per the new policies, the system administrators are looking for the best way to provide secure shell access to Amazon Elastic Compute Cloud (Amazon EC2) instances without opening new ports or using public IP addresses.

Which tool/service will help you achieve this requirement?

AWS Systems Manager Session Manager

Amazon Inspector

Amazon Elastic Compute Cloud (Amazon EC2) Instance Connect

Amazon Route 53
------------------
**ChatGPT:**


The tool/service that will help achieve the requirement of providing secure shell access to Amazon EC2 instances without opening new ports or using public IP addresses is AWS Systems Manager Session Manager.

AWS Systems Manager Session Manager is a fully managed service that allows you to establish secure shell (SSH) connections to your Amazon EC2 instances directly from the AWS Management Console, without the need for bastion hosts, open ports, or public IP addresses. It provides a secure and auditable method for accessing your instances using the AWS Systems Manager console or the AWS CLI. With Session Manager, you can centrally manage access permissions, log session data, and control the level of access to your instances. It eliminates the need to manage SSH keys and simplifies the process of accessing your EC2 instances securely.
------------------
**You:**


5:13

↓

7/65

1:23:35

Finish test

Question 7:

What is the primary benefit of deploying an Amazon RDS Multi-AZ database with one standby?

Amazon RDS Multi-AZ reduces database usage costs

Amazon RDS Multi-AZ improves database performance for read-heavy workloads

Amazon RDS Multi-AZ protects the database from a regional failure

Amazon RDS Multi-AZ enhances database availability
------------------
**ChatGPT:**


The primary benefit of deploying an Amazon RDS Multi-AZ database with one standby is that it enhances database availability.

When you deploy an Amazon RDS Multi-AZ database, a standby replica is automatically created in a different Availability Zone (AZ) within the same AWS Region. The standby replica synchronously replicates data from the primary database instance. In the event of a planned or unplanned outage affecting the primary instance or its AZ, Amazon RDS automatically fails over to the standby replica, promoting it as the new primary instance.

By deploying a Multi-AZ database, you improve the availability of your database because in the event of a failure of the primary instance or its AZ, Amazon RDS automatically switches to the standby replica, minimizing downtime and providing continuous availability of your database. This enhances the reliability and resilience of your application by ensuring that the database remains accessible even during infrastructure failures or maintenance activities.
------------------
**You:**


5:13

↓

8/65

1:22:50

Finish test

Question 8:

Due to regulatory and compliance reasons, an organization is supposed to use a hardware device for any data encryption operations in the cloud. Which AWS service can be used to meet this compliance requirement?

AWS Trusted Advisor

AWS Key Management Service (AWS KMS)

AWS CloudHSM

AWS Secrets Manager
------------------
**ChatGPT:**


To meet the compliance requirement of using a hardware device for data encryption operations in the cloud, the organization can utilize AWS CloudHSM (Hardware Security Module).

AWS CloudHSM is a service that provides dedicated hardware security modules in the AWS Cloud. It enables you to generate and use encryption keys securely within the hardware modules. CloudHSMs are tamper-resistant devices that provide secure key storage and cryptographic operations. They help organizations meet regulatory and compliance requirements that mandate the use of hardware-based key management and encryption.

By using AWS CloudHSM, the organization can have a dedicated hardware device for encryption operations, ensuring the desired level of security and compliance. The sensitive data can be encrypted and decrypted using the keys stored in the CloudHSM, providing an additional layer of protection and meeting regulatory requirements.
------------------
**You:**


5:14

9/65

1:21:59

Finish test

Question 9:

Which of the following statements are true about AWS Lambda? (Select two)

AWS Lambda allows you to orchestrate and manage Docker containers to facilitate complex containerized applications on AWS

AWS Lambda lets you run code without provisioning or managing servers

You pay for the compute time you consume for AWS Lambda

AWS Lambda allows you to install databases on the underlying serverless Operating System

AWS Lambda provides access to the underlying operating system to control its behavior through code
------------------
**ChatGPT:**


The correct statements about AWS Lambda are:

AWS Lambda lets you run code without provisioning or managing servers. With Lambda, you can focus on writing and uploading your code, and AWS takes care of the underlying infrastructure, automatically scaling and managing the compute resources required to run your code.

You pay for the compute time you consume for AWS Lambda. AWS Lambda follows a pay-per-use pricing model where you are billed based on the number of requests and the duration of your code execution. You are not charged for idle time or when your code is not running.

The incorrect statements are:

AWS Lambda allows you to orchestrate and manage Docker containers to facilitate complex containerized applications on AWS. This statement is incorrect. While AWS provides services like Amazon Elastic Container Service (ECS) and AWS Fargate for managing Docker containers, Lambda itself is a serverless compute service and does not directly orchestrate or manage Docker containers.

AWS Lambda allows you to install databases on the underlying serverless Operating System. This statement is incorrect. AWS Lambda is primarily focused on running stateless code functions and does not provide direct access to the underlying operating system or support for installing and managing databases. For databases, AWS offers services like Amazon RDS, Amazon DynamoDB, and others.
------------------
**You:**


5:15

↓

10/65

1:21:03

Finish test

Question 10:

Which of the following AWS services is essential for implementing security of resources in AWS Cloud?

AWS Identity and Access Management (IAM)

AWS Shield

Amazon CloudWatch

AWS Web Application Firewall (AWS WAF)
------------------
**ChatGPT:**


The correct answer is: AWS Identity and Access Management (IAM).

AWS Identity and Access Management (IAM) is an essential service for implementing security of resources in AWS Cloud. IAM enables you to manage user identities and their access to AWS resources. With IAM, you can create and manage IAM users, groups, and roles, and define fine-grained permissions to control access to AWS services and resources.

While AWS Shield, Amazon CloudWatch, and AWS Web Application Firewall (WAF) are important services for enhancing security in AWS, they focus on specific aspects of security:

AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that helps safeguard web applications running on AWS.
Amazon CloudWatch is a monitoring service that collects and tracks metrics, logs, and events from various AWS resources, providing visibility into the operational health and performance of your infrastructure.
AWS Web Application Firewall (WAF) is a web application firewall that helps protect web applications from common web exploits and attacks.

However, when it comes to implementing security for resources in AWS, AWS Identity and Access Management (IAM) plays a fundamental role in managing user access and permissions.
------------------
**You:**


5:16

↓

11/65

1:20:23

Finish test

Question 11:

Which AWS service can be used to provision resources to run big data workloads on Hadoop clusters?

AWS Batch

Amazon EMR

AWS Step Functions

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


The correct answer is: Amazon EMR.

Amazon EMR (Elastic MapReduce) is the AWS service that can be used to provision resources to run big data workloads on Hadoop clusters. Amazon EMR simplifies the process of setting up, managing, and scaling Hadoop clusters by providing a managed platform that includes popular frameworks like Apache Hadoop, Apache Spark, and Presto.

With Amazon EMR, you can easily launch clusters of EC2 instances preconfigured with the necessary software for running big data applications. It handles the provisioning and management of the underlying infrastructure, allowing you to focus on analyzing and processing your data.

AWS Batch is a different service that is focused on running batch computing workloads, which may or may not be specific to big data processing.

AWS Step Functions is a serverless workflow orchestration service that helps you coordinate multiple AWS services to build complex applications or workflows.

Amazon Elastic Compute Cloud (Amazon EC2) is a foundational AWS service that provides resizable compute capacity in the cloud, but it is not specifically designed for provisioning resources to run big data workloads on Hadoop clusters.
------------------
**You:**


5:17

↓

12/65

1:19:28

| Finish test

Question 12:

A data analytics company stores its data on Amazon Simple Storage Service (Amazon S3) and wants to do SQL based analysis on this data with minimum effort. As a Cloud Practitioner, which of the following AWS services will you suggest for this use case?

Amazon Athena

Amazon Aurora

Amazon DynamoDB

Amazon Redshift
------------------
**ChatGPT:**


For the given use case of performing SQL-based analysis on data stored in Amazon S3 with minimum effort, the recommended AWS service is Amazon Athena.

Amazon Athena is an interactive query service that allows you to analyze data directly from Amazon S3 using standard SQL queries. It does not require any infrastructure setup or data loading as it directly integrates with the data stored in S3. You can simply define a schema for your data using Athena, and then run SQL queries to extract insights and perform analysis on the data.

Amazon Aurora is a MySQL and PostgreSQL compatible relational database service. While it is suitable for running SQL-based analysis, it is typically used for transactional workloads and may involve more setup and management overhead compared to Amazon Athena for analyzing data stored in S3.

Amazon DynamoDB is a fully managed NoSQL database service and may not be the best choice for performing SQL-based analysis. It is optimized for low-latency, high-scale applications, and its query capabilities are focused on NoSQL operations rather than traditional SQL queries.

Amazon Redshift is a fully managed data warehousing service that is specifically designed for analytics and reporting. It is a powerful solution for running SQL-based analysis on large datasets, but it requires data to be loaded into the Redshift cluster before analysis. In this case, since the data is already stored in Amazon S3, using Amazon Athena would be a more convenient and efficient choice.

Therefore, for the given use case, the recommended AWS service is Amazon Athena.
------------------
**You:**


5:18

↓

13/65

1:18:30

Finish test

Question 13:

Multi-AZ deployment is an example of which of the

following?

High Availability

Scale out

Scale up

Performance Efficiency
------------------
**ChatGPT:**


Multi-AZ deployment is an example of High Availability.

High Availability refers to the ability of a system or service to remain operational and accessible even in the event of component failures or disruptions. In the case of Amazon Web Services (AWS), Multi-AZ deployment is a feature available for certain services, such as Amazon RDS (Relational Database Service) and Amazon Elasticache, that provides automatic replication of resources across multiple Availability Zones (AZs).

In a Multi-AZ deployment, the primary resource is replicated to a standby resource in a different AZ. This standby resource can quickly take over if the primary resource becomes unavailable due to a failure or planned maintenance. This redundancy ensures that the service remains highly available and minimizes downtime.

Therefore, Multi-AZ deployment is an example of High Availability in AWS.
------------------
**You:**


5:18

↓

14/65

1:18:04

Finish test

Question 14:

Which Amazon Route 53 routing policy would you use to improve the performance for your customers by routing the requests to the AWS endpoint that provides the fastest experience?

Weighted routing

Failover routing

Latency-based routing

Simple routing
------------------
**ChatGPT:**


The Amazon Route 53 routing policy that you would use to improve the performance for your customers by routing requests to the AWS endpoint that provides the fastest experience is Latency-based routing.

Latency-based routing allows you to route traffic based on the lowest network latency to provide the best user experience. With this routing policy, Route 53 measures the latency between the end user and each available endpoint and directs the traffic to the endpoint with the lowest latency.

By using latency-based routing, you can ensure that your customers are directed to the AWS endpoint that can provide the fastest response time based on their geographical location. This helps to minimize latency and improve the overall performance of your application or service.

Therefore, the correct answer is Latency-based routing.
------------------
**You:**


5:19

↓

15/65

1:17:35

Finish test

Question 15:

A company wants a fully managed, flexible, and scalable file storage system, with low latency access, for its Windows-based applications. Which AWS service is the right choice for the company?

Amazon Elastic File System (Amazon EFS)

Amazon Elastic Block Storage (Amazon EBS)

Amazon FSX for Windows File Server

Amazon FSX for Lustre
------------------
**ChatGPT:**


The right choice for a fully managed, flexible, and scalable file storage system with low latency access for Windows-based applications in AWS would be Amazon FSx for Windows File Server.

Amazon FSx for Windows File Server is a fully managed native Windows file system that is built on Windows Server and integrated with other AWS services. It provides shared file storage that is accessible from multiple Amazon EC2 instances and supports the SMB protocol, making it suitable for Windows-based applications.

With Amazon FSx for Windows File Server, you can achieve low latency access to your file data, as it uses SSD storage and is optimized for high performance. It also offers features such as automatic backups, data deduplication, and integration with AWS Directory Service for managing user access and authentication.

Therefore, the correct answer is Amazon FSx for Windows File Server.
------------------
**You:**


5:20

↓

16/65

1:16:31

Finish test

Question 16:

Which of the following use-cases is NOT supported by Amazon Rekognition?

Detect text in a photo

Quickly resize photos to create thumbnails

Identify person in a photo

Label objects in a photo
------------------
**ChatGPT:**


The use-case that is NOT supported by Amazon Rekognition is "Quickly resize photos to create thumbnails."

Amazon Rekognition is a deep learning-based image and video analysis service provided by AWS. It offers a wide range of capabilities for image and video analysis, including object and scene detection, facial analysis, text detection, and celebrity recognition. However, resizing photos to create thumbnails is not a supported feature of Amazon Rekognition.

To resize photos and create thumbnails, you would typically use image processing libraries or services specifically designed for that purpose, such as AWS Lambda with image processing libraries or Amazon S3 image resizing capabilities.

Therefore, the correct answer is "Quickly resize photos to create thumbnails."
------------------
**You:**


5:20

17/65

1:15:58 Finish test

Which of the following statements are correct about the AWS root user account? (Select two)

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies

Root user credentials should only be shared with managers requiring administrative responsibilities to complete their jobs

Root user access credentials are the email address and password used to create the AWS account

Root user account password cannot be changed once it is set

It is highly recommended to enable Multi- Factor Authentication (MFA) for root user account
------------------
**ChatGPT:**


The correct statements about the AWS root user account are:

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies.
It is highly recommended to enable Multi-Factor Authentication (MFA) for the root user account.

Explanation:

When you create an AWS account, the email address and password used during the account creation process become the root user access credentials. The root user has full administrative privileges by default, including access to all AWS resources and services. However, it is recommended to avoid using the root user account for everyday tasks and instead create individual IAM users with appropriate permissions.

It is crucial to secure the root user account since it has full control over the AWS account. One way to enhance security is by enabling Multi-Factor Authentication (MFA) for the root user. MFA adds an extra layer of protection by requiring an additional verification method, such as a one-time password generated by a virtual or hardware MFA device, in addition to the password.

Therefore, the correct statements are:

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies.
It is highly recommended to enable Multi-Factor Authentication (MFA) for the root user account.
------------------
**You:**


5:21

↓

18/65

1:15:13

Finish test

Question 18:

An online gaming company wants to block users from certain geographies from accessing its content. Which AWS service can be used to accomplish this task?

AWS Shield

Amazon CloudWatch

Security group

AWS Web Application Firewall (AWS WAF)
------------------
**ChatGPT:**


To block users from certain geographies from accessing its content, the online gaming company can use AWS WAF (Web Application Firewall).

AWS WAF is a web application firewall that helps protect web applications from common web exploits. It allows you to define customizable rules to filter and block specific traffic based on various criteria, including geographic location. By configuring AWS WAF with geolocation-based rules, the company can block access to its content from specific geographies.

Therefore, the correct answer is:

AWS Web Application Firewall (AWS WAF)
------------------
**You:**


5:22

↓

19/65

1:14:37

Finish test

Question 19:

A retail company has multiple AWS accounts for each of its departments. Which of the following AWS services can be used to set up consolidated billing and a single payment method for these AWS accounts?

AWS Budgets

AWS Organizations

AWS Secrets Manager

AWS Cost Explorer
------------------
**ChatGPT:**


To set up consolidated billing and a single payment method for multiple AWS accounts, the retail company can use AWS Organizations.

AWS Organizations is a service that enables the central management of multiple AWS accounts. It allows you to create an organization that can contain multiple accounts, and provides features such as consolidated billing, fine-grained access control, and centralized policy management. With AWS Organizations, you can consolidate the billing for all the accounts in your organization, making it easier to manage and track costs.

Therefore, the correct answer is:

AWS Organizations
------------------
**You:**


5:23

↑

20/65

1:13:37

Finish test

Question 20:

An organization has a complex IT architecture involving a lot of system dependencies and it wants to track the history of changes to each resource. Which AWS service will help the organization track the history of configuration changes for all the resources?

AWS CloudFormation

AWS Config

AWS Service Catalog

AWS CloudTrail
------------------
**ChatGPT:**


To track the history of configuration changes for all resources in an organization's complex IT architecture, the appropriate AWS service is AWS Config.

AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources over time. It keeps track of the configuration changes and provides a detailed view of the configuration history, including who made the changes, when they were made, and what the changes were. AWS Config also allows you to set up rules and notifications to ensure compliance and detect any configuration drift.

Therefore, the correct answer is:

AWS Config
------------------
**You:**


5:24

↑

21/65

1:12:37

Finish test

Question 21:

As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?

Customer Data

Identity and Access Management

Server-side Encryption (SSE)

Edge Location Management
------------------
**ChatGPT:**


According to the AWS Shared Responsibility Model, AWS takes responsibility for the security and compliance of the underlying infrastructure and services, while the customer is responsible for certain aspects related to their usage of AWS services.

Out of the options provided, "Server-side Encryption (SSE)" is the responsibility of AWS from a security and compliance point of view. AWS ensures the implementation and management of server-side encryption for its services. This means that AWS is responsible for encrypting the data at rest within its services, providing mechanisms for key management, and ensuring compliance with relevant security standards.

The other options, "Customer Data," "Identity and Access Management," and "Edge Location Management," are the responsibilities of the customer.

Therefore, the correct answer is:

Server-side Encryption (SSE)
------------------
**You:**


5:25

↑

22/65

1:11:56

Finish test

Question 22:

Which AWS compute service provides the EASIEST way to access resizable compute capacity in the cloud with support for per-second billing and access to the underlying OS?

Amazon Elastic Container Service (Amazon ECS)

Amazon Elastic Compute Cloud (Amazon EC2)

Amazon Lightsail

AWS Lambda
------------------
**ChatGPT:**


The AWS compute service that provides the easiest way to access resizable compute capacity in the cloud, with support for per-second billing and access to the underlying operating system (OS), is Amazon Elastic Compute Cloud (Amazon EC2).

Amazon EC2 offers virtual servers in the cloud, allowing users to choose from various instance types with different compute, memory, storage, and networking capabilities. It provides flexibility and control over the underlying infrastructure, including the choice of operating system, configuration, and management of the instances.

With per-second billing, users are billed for the exact number of seconds that their instances are running, providing cost savings for short-lived workloads. Additionally, users have administrative access to the underlying OS, allowing them to configure and manage the instances as needed.

Therefore, the correct answer is:

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**You:**


5:26

↑

23/65

1:10:49

Finish test

Question 23:

An IT company wants to run a log backup process every Monday at 2 AM. The usual runtime of the process is 5 minutes. As a Cloud Practitioner, which AWS services would you recommend to build a serverless solution for this use-case? (Select two)

Amazon Elastic Compute Cloud (Amazon EC2)

Amazon CloudWatch

AWS Lambda

AWS Systems Manager

AWS Step Function
------------------
**ChatGPT:**


As a Cloud Practitioner, I would recommend using the following AWS services to build a serverless solution for the specified use case:

AWS Lambda: AWS Lambda allows you to run code without provisioning or managing servers. You can create a Lambda function that contains the log backup process and schedule it to run at the desired time using AWS CloudWatch Events. Lambda functions are event-driven, so you can configure them to execute on a schedule, such as every Monday at 2 AM.

Amazon CloudWatch: Amazon CloudWatch is a monitoring and observability service that can be used to schedule and trigger AWS Lambda functions. You can create a CloudWatch Events rule that triggers the Lambda function at the specified time and day. CloudWatch Events provides a cron expression syntax that allows you to define the schedule for recurring events.

By using AWS Lambda and Amazon CloudWatch together, you can build a serverless solution to run the log backup process every Monday at 2 AM without the need to provision or manage servers.

Therefore, the correct answers are:

AWS Lambda
Amazon CloudWatch
------------------
**You:**


5:27

24/65

1:09:42

Finish test

Question 24:

Which AWS technology/service helps you to scale your resources to match supply with demand while still keeping your cloud solution cost-effective?

AWS Cost Explorer

AWS Auto Scaling

O AWS OpsWorks

AWS CloudFormation
------------------
**ChatGPT:**


The AWS technology/service that helps you scale your resources to match supply with demand while keeping your cloud solution cost-effective is AWS Auto Scaling.

AWS Auto Scaling allows you to automatically adjust the number of Amazon EC2 instances in your application based on predefined conditions. It helps you maintain optimal performance and cost efficiency by scaling resources up or down as needed. You can define scaling policies that are based on metrics such as CPU utilization, network traffic, or custom metrics, and Auto Scaling will automatically add or remove instances to meet the desired capacity.

By using AWS Auto Scaling, you can ensure that your application can handle varying levels of traffic and workload without overprovisioning resources, thus optimizing costs.

Therefore, the correct answer is:

AWS Auto Scaling
------------------
**You:**


5:27

24/65

1:09:42

Finish test

Question 24:

Which AWS technology/service helps you to scale your resources to match supply with demand while still keeping your cloud solution cost-effective?

AWS Cost Explorer

AWS Auto Scaling

O AWS OpsWorks

AWS CloudFormation
------------------
**ChatGPT:**


The AWS technology/service that helps you scale your resources to match supply with demand while keeping your cloud solution cost-effective is AWS Auto Scaling.

AWS Auto Scaling allows you to automatically adjust the number of Amazon EC2 instances in your application based on predefined conditions. It helps you maintain optimal performance and cost efficiency by scaling resources up or down as needed. You can define scaling policies that are based on metrics such as CPU utilization, network traffic, or custom metrics, and Auto Scaling will automatically add or remove instances to meet the desired capacity.

By using AWS Auto Scaling, you can ensure that your application can handle varying levels of traffic and workload without overprovisioning resources, thus optimizing costs.

Therefore, the correct answer is:

AWS Auto Scaling
------------------
**You:**


5:27

25/65

1:09:09

Finish test

Question 25:

Which AWS service would you use to send alerts

when the costs for your AWS account exceed your budgeted amount?

AWS Pricing Calculator

AWS Organizations

AWS Budgets

AWS Cost Explorer
------------------
**ChatGPT:**


The AWS service you would use to send alerts when the costs for your AWS account exceed your budgeted amount is AWS Budgets.

AWS Budgets allows you to set custom budget thresholds for your AWS costs and usage. You can specify a budgeted amount and define the desired time period for the budget. When the actual costs exceed the budgeted amount, AWS Budgets can send alerts to specified recipients via email or Amazon Simple Notification Service (SNS).

By using AWS Budgets, you can closely monitor your AWS spending and receive timely notifications when your costs exceed the defined budget, enabling you to take necessary actions to control your expenses.

Therefore, the correct answer is:

AWS Budgets
------------------
**You:**


5:29

↑

26/65

1:07:59

Finish test

Question 26:

AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Elastic File System (Amazon EFS)

Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions

AWS Lambda functions, Amazon Simple Storage Service (Amazon S3)

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EC2 Auto Scaling groups

Amazon Elastic File System (Amazon EFS), AWS Lambda functions
------------------
**ChatGPT:**


AWS Compute Optimizer delivers recommendations for the following AWS resources:

Amazon Elastic Compute Cloud (Amazon EC2) instances
Amazon EC2 Auto Scaling groups

AWS Compute Optimizer analyzes the configuration and utilization of these resources to provide recommendations for optimizing their performance and cost-efficiency. It uses machine learning algorithms to analyze historical resource utilization patterns and compare them to AWS's best practices to identify areas for improvement.

Therefore, the correct answer is:

Amazon Elastic Compute Cloud (Amazon EC2) instances
Amazon EC2 Auto Scaling groups
------------------
**You:**


5:30

↑

27/65

1:06:48

| Finish test

Question 27:

Which of the following AWS services can be used to prevent Distributed Denial-of-Service (DDoS) attack? (Select three)

AWS Web Application Firewall (AWS WAF)

AWS Trusted Advisor

Amazon Inspector

AWS Shield

Amazon CloudFront with Amazon Route 53

AWS CloudHSM
------------------
**ChatGPT:**


The following AWS services can be used to prevent Distributed Denial-of-Service (DDoS) attacks:

AWS Web Application Firewall (AWS WAF): AWS WAF helps protect web applications from common web exploits and DDoS attacks by allowing you to define customizable security rules that control access to your applications.

AWS Shield: AWS Shield is a managed Distributed Denial-of-Service (DDoS) protection service that safeguards applications running on AWS against the most common and frequently observed DDoS attack patterns.

Amazon CloudFront with Amazon Route 53: Amazon CloudFront is a content delivery network (CDN) service that can be used to improve the performance and availability of web applications. It includes DDoS protection capabilities. Amazon Route 53 is a scalable domain name system (DNS) web service that can be used in conjunction with CloudFront to provide DDoS protection and load balancing.

Therefore, the correct answer is:

AWS Web Application Firewall (AWS WAF)
AWS Shield
Amazon CloudFront with Amazon Route 53
------------------
**You:**


10:24

5G

↓

28/65

1:04:15

Finish test

Question 28:

An organization is planning to move its infrastructure from the on-premises datacenter to AWS Cloud. As a Cloud Practioner, which options would you recommend so that the organization can identify the right AWS services to build solutions on AWS Cloud (Select two)?

AWS Partner Network (APN)

AWS Organizations

AWS CloudTrail

AWS Service Catalog

Amazon CloudWatch
------------------
**ChatGPT:**


As a Cloud Practitioner, I would recommend the following options for the organization to identify the right AWS services to build solutions on AWS Cloud:

AWS Partner Network (APN): The AWS Partner Network provides access to a vast ecosystem of AWS partners who can offer expertise and guidance in selecting and implementing the right AWS services for specific use cases. They can help with solution architecture, best practices, and implementation support.

AWS Service Catalog: AWS Service Catalog allows organizations to create and manage curated catalogs of approved AWS services that are pre-configured with recommended settings and configurations. It helps in standardizing the selection and provisioning of AWS services within an organization, ensuring compliance and best practices.

Therefore, the correct options are:

AWS Partner Network (APN)
AWS Service Catalog
------------------
**You:**


10:24

5G

↓

29/65

1:03:26

Finish test

Question 29:

Which characteristic of Cloud Computing imparts the ability to acquire resources as you need and release when you no longer need them?

Reliability

Resiliency

Durability

Elasticity
------------------
**ChatGPT:**


The characteristic of Cloud Computing that imparts the ability to acquire resources as you need and release them when you no longer need them is Elasticity. Elasticity allows users to scale their resource usage up or down based on demand, enabling efficient resource allocation and cost optimization. It provides the flexibility to quickly and easily add or remove resources as required, ensuring that you only pay for the resources you actually use.
------------------
**You:**


10:26

5G

↓

30/65

1:01:32

Finish test

Question 30:

Which AWS service should be used when you want to run container applications, but want to avoid the operational overhead of scaling, patching, securing, and managing servers?

Amazon Elastic Container Service (Amazon ECS) - Fargate launch type

Amazon Elastic Container Service

(Amazon ECS) - EC2 launch type

AWS Lambda

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


The AWS service that should be used when you want to run container applications without the operational overhead of scaling, patching, securing, and managing servers is Amazon Elastic Container Service (Amazon ECS) - Fargate launch type. With Amazon ECS using the Fargate launch type, you can focus on running and managing your containers without the need to provision or manage the underlying infrastructure. Fargate handles the scaling, patching, and management of the underlying infrastructure, allowing you to run containers in a serverless manner.
------------------
**You:**


10:27

5G

↓

31/65

1:01:02

Finish test

Question 31:

Which of the following statement is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?

Both inbound data transfer and outbound data transfer are charged

Only outbound data transfer is charged

Only inbound data transfer is charged

Neither inbound nor outbound data transfer are charged
------------------
**ChatGPT:**


The correct statement regarding the AWS pricing policy for data transfer charges into or out of an AWS Region is:

Both inbound data transfer and outbound data transfer are charged.

AWS charges for both inbound and outbound data transfer when data is transferred between your resources in an AWS Region and the internet or between AWS Regions. The pricing varies based on the amount of data transferred and the transfer type (e.g., data transfer between EC2 instances and the internet, or between AWS services within the same Region).
------------------
**You:**


10:28

5G

↓

32/65

59:54

Finish test

Question 32:

A developer has written a simple web application in PHP and he wants to just upload his code to AWS Cloud and have AWS handle the deployment automatically but still wants access to the underlying operating system for further enhancements. As a Cloud Practioner, which of the following AWS services would you recommend for this use-case?

AWS CloudFormation

AWS Elastic Beanstalk

Amazon Elastic Container Service (Amazon ECS)

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


For the given use case, as a Cloud Practitioner, I would recommend using AWS Elastic Beanstalk.

AWS Elastic Beanstalk is a fully managed service that makes it easy to deploy and run applications in multiple languages, including PHP. It abstracts away the underlying infrastructure and handles the deployment and scaling automatically based on the application's needs. With Elastic Beanstalk, the developer can simply upload their code and AWS will handle the deployment, including provisioning the necessary resources such as EC2 instances and load balancers.

Elastic Beanstalk also provides access to the underlying operating system if further enhancements or customization are required. It allows you to customize and configure the underlying infrastructure, including setting environment variables, scaling options, and more. This gives the developer the flexibility to make OS-level changes while still benefiting from the managed deployment and scaling capabilities provided by Elastic Beanstalk.
------------------
**You:**


10:29

5G

↓

33/65

59:15

Finish test

Question 33:

An organization deploys its IT infrastructure in a combination of its on-premises data center along with AWS Cloud. How would you categorize this deployment model?

Cloud deployment

Mixed deployment

Private deployment

Hybrid deployment
------------------
**ChatGPT:**


The deployment model described, where an organization deploys its IT infrastructure in a combination of its on-premises data center and AWS Cloud, is categorized as a hybrid deployment.

In a hybrid deployment model, an organization leverages both on-premises infrastructure and cloud services to meet its IT needs. This allows for a combination of resources, applications, and services to be hosted both in the organization's own data center and in the cloud. The hybrid deployment model offers flexibility and enables organizations to leverage the benefits of both on-premises infrastructure and cloud services, while also maintaining control over certain resources and data that may need to remain on-premises due to specific requirements or regulations.

In this scenario, the organization can utilize AWS Cloud services for certain workloads, while keeping other workloads on-premises in their own data center. The hybrid deployment model allows for seamless integration and communication between the on-premises infrastructure and the cloud, enabling organizations to leverage the scalability, agility, and cost-efficiency of the cloud while also leveraging their existing investments in on-premises infrastructure.
------------------
**You:**


10:30

5G

↓

34/65

58:28

Finish test

Question 34:

A fleet of Amazon EC2 instances spread across different Availability Zones (AZ) needs to access, edit and share file-based data stored centrally on a system. As a Cloud Practitioner, which AWS service would you recommend for this use-case?

Amazon Simple Storage Service (Amazon S3)

Amazon Elastic Block Store (Amazon

EBS)

Amazon Elastic File System (Amazon EFS)

EC2 Instance Store
------------------
**ChatGPT:**


For the given use case, where a fleet of Amazon EC2 instances spread across different Availability Zones (AZ) needs to access, edit, and share file-based data stored centrally on a system, the recommended AWS service would be Amazon Elastic File System (Amazon EFS).

Amazon EFS provides a scalable and fully managed file storage service that is designed to be highly available and durable. It offers a file system that can be mounted on multiple EC2 instances concurrently, allowing them to access and share the same data. It is well-suited for scenarios where multiple instances need to collaborate and share file-based data.

Key features of Amazon EFS include:

Elastic Scalability: Amazon EFS automatically scales storage capacity as per demand, so you don't need to worry about managing storage limits or performance.

Multi-AZ Durability: Data stored in Amazon EFS is automatically replicated across multiple Availability Zones, providing high durability and availability.

Shared Access: Multiple EC2 instances across different AZs can simultaneously access and modify files within the same Amazon EFS file system.

Compatibility: Amazon EFS supports the Network File System version 4 (NFSv4) protocol, which is compatible with most Linux-based applications and EC2 instances.

By using Amazon EFS, the fleet of EC2 instances can access and share the centrally stored file-based data, allowing for collaboration and efficient data management across multiple instances and Availability Zones.
------------------
**You:**


10:31

5G

↑

35/65

57:23

Finish test

Question 35:

Which AWS service publishes up-to-the-minute information on the general status and availability of all AWS services in all the Regions of AWS Cloud?

Amazon CloudWatch

AWS CloudFormation

AWS Health Dashboard - service health

AWS Health Dashboard - Your account

health
------------------
**ChatGPT:**


The AWS service that publishes up-to-the-minute information on the general status and availability of all AWS services in all the Regions of AWS Cloud is AWS Health Dashboard - service health.

The AWS Health Dashboard provides real-time visibility into the status of AWS services. It offers information on service disruptions, outages, and other events that may affect the availability and performance of AWS services. The dashboard provides a centralized view of the health of various AWS services across different regions.

By monitoring the AWS Health Dashboard - service health, users can stay informed about any ongoing issues or disruptions in AWS services and take necessary actions to mitigate the impact on their applications or infrastructure. It helps users stay updated on the overall health and availability of AWS services and plan their operations accordingly.
------------------
**You:**


10:31

5G

↑

36/65

56:47

Finish test

Question 36:

Which of the following AWS services are global in scope? (Select two)

Amazon Simple Storage Service (Amazon S3)

Amazon Relational Database Service (Amazon RDS)

AWS Identity and Access Management (AWS IAM)

Amazon CloudFront

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


The two AWS services that are global in scope are:

AWS Identity and Access Management (AWS IAM): AWS IAM is a global service that enables you to manage access to your AWS resources. It allows you to create and manage users, groups, and roles to control who can access your AWS resources and what actions they can perform.

Amazon CloudFront: Amazon CloudFront is a global content delivery network (CDN) service that delivers static and dynamic web content, including images, videos, and application data, to end-users with low latency and high transfer speeds. CloudFront has edge locations distributed worldwide, making it a global service.

Both AWS IAM and Amazon CloudFront operate across multiple AWS Regions and are designed to provide global functionality and scalability.
------------------
**You:**


10:32

5G

↑

37/65

56:08

Finish test

Which of the following is the correct statement regarding the AWS Storage services?

Amazon Simple Storage Service (Amazon S3) is block based storage, Amazon Elastic Block Store (Amazon EBS) is object based storage and Amazon Elastic File System (Amazon EFS) is file based storage

Amazon Simple Storage Service (Amazon S3) is object based storage, Amazon Elastic Block Store (Amazon EBS) is block based storage and Amazon Elastic File System (Amazon EFS) is file based storage

Amazon Simple Storage Service (Amazon S3) is file based storage, Amazon Elastic Block Store (Amazon EBS) is block based storage and Amazon Elastic File System (Amazon EFS) is object based storage

Amazon Simple Storage Service (Amazon S3) is object based storage, Amazon Elastic Block Store (Amazon EBS) is file based storage and Amazon Elastic File System (Amazon EFS) is block based storage
------------------
**ChatGPT:**


The correct statement regarding the AWS Storage services is:

Amazon Simple Storage Service (Amazon S3) is object-based storage, Amazon Elastic Block Store (Amazon EBS) is block-based storage, and Amazon Elastic File System (Amazon EFS) is file-based storage.

Amazon Simple Storage Service (Amazon S3) is a scalable object storage service that allows you to store and retrieve data, such as files and documents, in the form of objects. It provides durability, high availability, and supports various storage classes for different use cases.

Amazon Elastic Block Store (Amazon EBS) is a block-level storage service that provides persistent block storage volumes for use with Amazon EC2 instances. It is designed for applications that require low-latency, high-performance storage, and provides features like snapshotting and replication.

Amazon Elastic File System (Amazon EFS) is a file storage service that provides scalable and fully managed file systems for use with Amazon EC2 instances. It allows multiple instances to access the same file system concurrently and provides features like automatic scaling and high availability.

Therefore, the correct statement is that Amazon S3 is object-based storage, Amazon EBS is block-based storage, and Amazon EFS is file-based storage.
------------------
**You:**


10:33

5G

↓

38/65

55:09 Finish test

Question 38:

A customer has created a VPC and a subnet within AWS Cloud. Which of the following statements is correct?

A subnet spans all of the Availability Zones (AZ) in the Region whereas an Amazon Virtual Private Cloud (Amazon VPC) spans only one Availability Zone (AZ) in the Region

Both the Amazon Virtual Private Cloud (Amazon VPC) and the subnet span only one Availability Zone (AZ) in the Region

Both the Amazon Virtual Private Cloud (Amazon VPC) and the subnet span all of the Availability Zones (AZ) in the Region

An Amazon Virtual Private Cloud (Amazon VPC) spans all of the Availability Zones (AZ) in the Region whereas a subnet spans only one Availability Zone (AZ) in the Region
------------------
**ChatGPT:**


The correct statement regarding a customer creating a VPC and a subnet within AWS Cloud is:

An Amazon Virtual Private Cloud (Amazon VPC) spans all of the Availability Zones (AZ) in the Region, whereas a subnet spans only one Availability Zone (AZ) in the Region.

An Amazon Virtual Private Cloud (Amazon VPC) is a logically isolated section of the AWS Cloud where you can launch AWS resources. It can span multiple Availability Zones within a Region, allowing you to distribute your resources across multiple data centers for high availability and fault tolerance.

A subnet, on the other hand, is a range of IP addresses in your VPC. It is a subdivision of a VPC and is associated with a specific Availability Zone. Each subnet resides in a single Availability Zone and can span multiple Availability Zones if you create subnets in each one.

Therefore, the correct statement is that an Amazon VPC spans all of the Availability Zones (AZ) in the Region, whereas a subnet spans only one Availability Zone (AZ) in the Region.
------------------
**You:**


10:34

↓

39/65

54:19

Finish test

Question 39:

According to the AWS Shared Responsibility Model, which of the following are responsibilities of the customer for Amazon RDS?

Applying patches to the Amazon Relational Database Service (Amazon RDS) database

Database encryption

Managing the underlying server hardware on which Amazon Relational Database Service (Amazon RDS) runs

Applying patches to the underlying OS
------------------
**ChatGPT:**


According to the AWS Shared Responsibility Model, the following are responsibilities of the customer for Amazon RDS:

Applying patches to the underlying OS: The customer is responsible for applying patches to the underlying operating system of the Amazon RDS instances. This includes installing security updates and patches provided by the operating system vendor.

Database encryption: The customer is responsible for managing and configuring encryption of their data in Amazon RDS. This includes enabling and managing encryption at rest and encryption in transit for the database.

On the other hand, the following responsibility is not the customer's responsibility for Amazon RDS:

Applying patches to the Amazon RDS database: AWS takes care of applying patches to the Amazon RDS database engine. AWS manages the maintenance and patching of the database engine to ensure it remains up-to-date and secure.

As for the responsibility of managing the underlying server hardware on which Amazon RDS runs, it is the responsibility of AWS, not the customer.

Therefore, the correct options are:

Applying patches to the underlying OS
Database encryption
------------------
**You:**


10:36

↓

40/65

52:18

Finish test

Question 40:

A startup is looking for 24x7 phone based technical support for its AWS account. Which of the following is the MOST cost-effective AWS support plan for this use-case?

AWS Enterprise On-Ramp Support

AWS Business Support

AWS Enterprise Support

AWS Developer Support
------------------
**ChatGPT:**


For the given use case of a startup looking for 24x7 phone-based technical support, the most cost-effective AWS support plan would be AWS Business Support.

AWS Business Support provides 24x7 access to customer service and technical support via email, chat, and phone. It offers a broad range of support for AWS services and includes general guidance, best practices, and assistance with service-specific inquiries. It is designed to meet the needs of businesses at a lower cost compared to higher-tier support plans.

AWS Enterprise On-Ramp Support is a limited-time plan available for new AWS customers that provides guidance and support during the initial onboarding and migration phase.

AWS Enterprise Support is a comprehensive support plan designed for enterprise customers with mission-critical workloads. It offers a higher level of support, including a Technical Account Manager (TAM) and architectural guidance, but it may be more costly for a startup.

AWS Developer Support is a plan designed for individual developers or small teams and provides technical support during business hours. It may not offer the level of coverage required for 24x7 phone-based support.

Therefore, for a startup seeking cost-effective 24x7 phone-based technical support, AWS Business Support would be the most suitable option.
------------------
**You:**


10:37

↑

41/65

51:31

Finish test

Question 41:

A social media company wants to protect its web application from common web exploits such as SQL injection and cross-site scripting. Which of the following AWS services can be used to address this use-case?

Amazon Inspector

AWS Web Application Firewall (AWS WAF)

AWS CloudWatch

Amazon GuardDuty
------------------
**ChatGPT:**


To protect a web application from common web exploits such as SQL injection and cross-site scripting, the appropriate AWS service to use is AWS Web Application Firewall (AWS WAF).

AWS WAF helps protect web applications from common attack patterns by allowing you to create rules that control the traffic to your application. It enables you to define customizable web security rules to filter out malicious traffic and block common attack patterns. With AWS WAF, you can mitigate SQL injection, cross-site scripting, and other web-based attacks.

Amazon Inspector is a security assessment service that helps identify vulnerabilities and security issues in your application deployments. While it can provide insights into potential security weaknesses, it does not specifically focus on protecting against web exploits like SQL injection or cross-site scripting.

AWS CloudWatch is a monitoring and observability service that collects and tracks metrics, logs, and events. While it can help detect unusual behavior and provide insights into your application's performance, it is not specifically designed for protecting against web exploits.

Amazon GuardDuty is a threat detection service that analyzes data sources across AWS accounts and services to identify potential malicious activity. While it can help detect and alert on various types of threats, it does not provide specific protection against web exploits.

Therefore, the most appropriate AWS service to address the use-case of protecting a web application from common web exploits is AWS Web Application Firewall (AWS WAF).
------------------
**You:**


10:37

↑

42/65

50:46

Finish test

Question 42:

Which Amazon Elastic Compute Cloud (Amazon EC2) pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that instance would not be interrupted?

Dedicated Host

On-demand Instance

Spot Instance

Reserved Instance (RI)
------------------
**ChatGPT:**


The most cost-effective and flexible pricing model for Amazon Elastic Compute Cloud (Amazon EC2) instances, without a long-term commitment or upfront payment, is the Spot Instance pricing model.

Spot Instances allow you to bid on spare EC2 instances' capacity, which can result in significant cost savings compared to On-Demand or Reserved Instances. With Spot Instances, you specify the maximum price you are willing to pay per hour, and if the current Spot price is below your bid price, your instance will run. However, it's important to note that the availability of Spot Instances is subject to fluctuation based on supply and demand. If the Spot price exceeds your bid price, your instance may be interrupted and terminated.

While Spot Instances offer great cost savings, they are not suitable for applications that require continuous, uninterrupted availability. If your instance is terminated due to changes in Spot prices, you may need to handle the interruption gracefully or have mechanisms in place to recover and continue processing.

Dedicated Hosts provide you with dedicated physical servers for your EC2 instances, but they are not the most cost-effective option, as they involve additional costs for the dedicated hardware.

On-Demand Instances provide you with instances that are billed per hour or per second, with no upfront commitment. They offer flexibility but are generally more expensive compared to Spot Instances or Reserved Instances.

Reserved Instances (RI) allow you to make a capacity reservation for a specific instance type in a specific region. They require a commitment for a term of 1 or 3 years, offering discounted pricing compared to On-Demand Instances. However, they do involve upfront payments and are not as flexible as Spot Instances.

Therefore, for a cost-effective and flexible pricing model with no long-term commitment or upfront payment, the most suitable option is the Spot Instance pricing model.
------------------
**You:**


10:38

↓

43/65

50:07 Finish test

Question 43:

Which of the following solutions can you use to connect your on-premises network with AWS Cloud (Select two)?

Amazon Route 53

AWS Virtual Private Network (VPN)

Amazon Virtual Private Cloud (Amazon VPC)

AWS Direct Connect

Internet Gateway
------------------
**ChatGPT:**


To connect your on-premises network with AWS Cloud, you can use the following solutions:

AWS Virtual Private Network (VPN): AWS VPN allows you to establish a secure and encrypted connection between your on-premises network and your Amazon Virtual Private Cloud (Amazon VPC). It uses the Internet as the transport medium and provides secure access to your resources in the AWS Cloud.

AWS Direct Connect: AWS Direct Connect enables you to establish a dedicated network connection between your on-premises network and AWS. With Direct Connect, you can bypass the public Internet and achieve a more reliable and consistent network performance. It provides a private and dedicated connection to AWS services, which is particularly beneficial for data-intensive workloads or sensitive data transfer.

Amazon Route 53 is a scalable domain name system (DNS) web service that translates domain names into IP addresses. While it is not directly used for connecting on-premises networks to AWS Cloud, it is commonly used for DNS routing and traffic management within AWS.

Amazon Virtual Private Cloud (Amazon VPC) is the networking layer for your AWS resources. It allows you to create isolated virtual networks in the AWS Cloud. While it provides network isolation and control within the AWS environment, it does not directly connect your on-premises network to AWS. However, you can use VPN or Direct Connect in combination with Amazon VPC to establish connectivity.

Internet Gateway is a horizontally scalable, redundant, and highly available VPC component that allows communication between your VPC and the Internet. It is used for Internet connectivity within the AWS environment but does not provide direct connectivity between on-premises networks and AWS Cloud.

Therefore, the correct options for connecting your on-premises network with AWS Cloud are AWS Virtual Private Network (VPN) and AWS Direct Connect.
------------------
**You:**


10:39

↓

44/65

49:26

Finish test

Question 44:

Which of the following AWS services are always free to use (Select two)?

AWS Auto Scaling

Amazon Simple Storage Service (Amazon S3)

Amazon Elastic Compute Cloud (Amazon

EC2)

Amazon DynamoDB

AWS Identity and Access Management (AWS IAM)
------------------
**ChatGPT:**


Among the given options, the following AWS services are always free to use:

AWS Identity and Access Management (AWS IAM): AWS IAM is the service used for managing user identities and access to AWS resources. The core features of IAM, such as creating and managing users, groups, and permissions, are available for free. However, there may be charges for certain advanced features or specific usage scenarios.

Amazon Simple Storage Service (Amazon S3): Amazon S3 is a scalable object storage service that allows you to store and retrieve data. There is a free tier available for Amazon S3, which includes a certain amount of storage, data transfer, and requests each month. As long as you stay within the free tier limits, you can use Amazon S3 for free.

Please note that while the core services of AWS Auto Scaling, Amazon Elastic Compute Cloud (Amazon EC2), and Amazon DynamoDB are not always free, there may be free usage tiers or specific usage scenarios where limited usage is available for free. However, these services typically incur charges based on usage beyond the free tier or specific service limits.

Therefore, the correct options for AWS services that are always free to use are AWS Identity and Access Management (AWS IAM) and Amazon Simple Storage Service (Amazon S3).
------------------
**You:**


10:40

↑

45/65

48:36

Finish test

Question 45:

What foundational capability under the operations perspective is part of the AWS Cloud Adoption Framework (AWS CAF)?

Vulnerability management

Application portfolio management

Platfrom engineering

Performance and capacity management
------------------
**ChatGPT:**


Among the given options, the foundational capability under the operations perspective that is part of the AWS Cloud Adoption Framework (AWS CAF) is Performance and capacity management.

The AWS Cloud Adoption Framework (CAF) is a framework designed to help organizations adopt the cloud and define their cloud strategy. It provides a structured approach for planning and implementing cloud adoption, covering various perspectives including business, people, governance, platform, security, and operations.

Performance and capacity management is an essential aspect of operating in the cloud. It involves monitoring and optimizing the performance of cloud resources and ensuring that sufficient capacity is available to meet the demands of the applications and services running in the cloud. This includes activities such as monitoring resource utilization, scaling resources as needed, and optimizing performance for cost-efficiency.

Therefore, the correct option for the foundational capability under the operations perspective in the AWS Cloud Adoption Framework (AWS CAF) is Performance and capacity management.
------------------
**You:**


10:41

↓

46/65

47:47

Finish test

Question 46:

Which of the following AWS services allows a database to have flexible schema and supports document data models?

Amazon Redshift

Amazon Aurora

Amazon Relational Database Service (Amazon RDS)

Amazon DynamoDB
------------------
**ChatGPT:**


Among the given options, the AWS service that allows a database to have a flexible schema and supports document data models is Amazon DynamoDB.

Amazon DynamoDB is a fully managed NoSQL database service provided by AWS. It is designed to provide fast and predictable performance with seamless scalability. DynamoDB allows you to store and retrieve data using flexible document data models, which means you can have a dynamic schema and store data in the form of JSON-like documents.

With DynamoDB, you can create tables with different attributes for each item, providing flexibility in defining the structure of your data. This allows you to adapt to changing requirements without needing to modify the entire database schema.

Therefore, the correct option for an AWS service that supports flexible schema and document data models is Amazon DynamoDB.
------------------
**You:**


10:41

↓

47/65

47:04

Finish test

Question 47:

Which of the following statements is INCORRECT about AWS Auto Scaling?

You can automatically remove unhealthy instances

You can automatically register new instances to a load balancer

You can scale out and add more Amazon Elastic Compute Cloud (Amazon EC2) instances to match an increase in demand as well as scale in and remove Amazon Elastic Compute Cloud (Amazon EC2) instances to match a reduced demand

You can automatically deploy AWS Shield when a DDoS attack is detected
------------------
**ChatGPT:**


The incorrect statement about AWS Auto Scaling is:

"You can automatically deploy AWS Shield when a DDoS attack is detected."

AWS Auto Scaling is a service that allows you to automatically adjust the number of Amazon EC2 instances in a scalable manner based on predefined conditions or metrics. It helps you maintain the desired application availability and performance by dynamically scaling your resources.

While AWS Shield is a DDoS (Distributed Denial-of-Service) protection service provided by AWS, it is not directly related to AWS Auto Scaling. AWS Shield is designed to protect your applications and infrastructure against DDoS attacks by providing automatic mitigation and protection. It operates independently of AWS Auto Scaling.

Therefore, the statement that is incorrect about AWS Auto Scaling is that it can automatically deploy AWS Shield when a DDoS attack is detected.
------------------
**You:**


10:42

↑

48/65

46:22

Finish test

Question 48:

What are the different gateway types supported by

AWS Storage Gateway service?

Tape Gateway, File Gateway and Block Gateway

Tape Gateway, Object Gateway and Volume Gateway

Tape Gateway, File Gateway and Volume Gateway

Object Gateway, File Gateway and Block Gateway
------------------
**ChatGPT:**


The different gateway types supported by the AWS Storage Gateway service are:

Tape Gateway: It provides a virtual tape library (VTL) interface for backup and archival workloads. It allows you to store data in Amazon S3 and Glacier using industry-standard backup applications.

File Gateway: It provides a file interface to store and retrieve objects in Amazon S3. It supports Network File System (NFS) and Server Message Block (SMB) protocols, allowing you to seamlessly integrate it with existing applications and on-premises file-based workloads.

Volume Gateway: It provides block storage volumes that can be mounted as iSCSI devices by your on-premises or EC2-based applications. It offers two configurations:

a. Stored Volumes: It stores your data locally and asynchronously backs up point-in-time snapshots to Amazon S3 for durability. This configuration is suitable for primary storage, where low-latency access to frequently accessed data is required.

b. Cached Volumes: It stores only frequently accessed data locally and stores the entire dataset in Amazon S3. This configuration optimizes storage costs while still providing low-latency access to frequently accessed data.

Therefore, the correct answer is: Tape Gateway, File Gateway, and Volume Gateway.
------------------
**You:**


10:43

↑

49/65

45:44

Finish test

Question 49:

The AWS Well-Architected Framework provides guidance on building cloud based applications using AWS best practices. Which of the following options are the pillars mentioned in the AWS Well- Architected Framework? (Select two)

Reliability

Elasticity

Scalability

Availability

Cost Optimization
------------------
**ChatGPT:**


The pillars mentioned in the AWS Well-Architected Framework are:

Reliability: This pillar focuses on the ability of a system to recover from failures and continue to function as expected. It includes aspects such as fault tolerance, high availability, and disaster recovery.

Cost Optimization: This pillar focuses on optimizing costs by making efficient use of resources and eliminating unnecessary expenses. It includes aspects such as choosing the right pricing models, monitoring resource usage, and optimizing for cost-effective solutions.

Therefore, the correct options are Reliability and Cost Optimization.
------------------
**You:**


10:43

↑

50/65

45:16

Finish test

Question 50:

Which service gives a personalized view of the status of the AWS services that are part of your Cloud architecture so that you can quickly assess the impact on your business when AWS service(s) are experiencing issues?

AWS Health - Service Health Dashboard

Amazon Inspector

Amazon CloudWatch

AWS Health - Your Account Health Dashboard
------------------
**ChatGPT:**


The service that gives a personalized view of the status of the AWS services that are part of your Cloud architecture is "AWS Health - Your Account Health Dashboard." It provides real-time information and notifications about the health of your AWS resources, services, and accounts, allowing you to assess the impact on your business when AWS services are experiencing issues.
------------------
**You:**


10:44

51/65

44:39

Finish test

Question 51:

Which of the following is correct about AWS Developer Support plan?

Allows unlimited contacts to open unlimited cases

Allows unlimited contacts to open a limited number of cases per month

Allows one contact to open a limited number of cases per month

Allows one contact to open unlimited cases

<

>
------------------
**ChatGPT:**


The correct statement about the AWS Developer Support plan is that it allows one contact to open a limited number of cases per month. The specific number of cases allowed may vary depending on the terms of the support plan.
------------------
**You:**


10:44

52/65

44:05 Finish test

Question 52:

Which AWS service helps with global application availability and performance using the AWS global network?

Elastic Load Balancing (ELB)

Amazon CloudFront

AWS Global Accelerator

Amazon Route 53
------------------
**ChatGPT:**


The AWS service that helps with global application availability and performance using the AWS global network is AWS Global Accelerator.
------------------
**You:**


10:45

↑

53/65

43:37

Finish test

Question 53:

Which of the following statement is correct for a Security Group and a Network Access Control List (Network ACL)?

Security Group acts as a firewall at the instance level whereas Network Access Control List (Network ACL) acts as a firewall at the subnet level

Security Group acts as a firewall at the Availability Zone (AZ) level whereas Network Access Control List (Network ACL) acts as a firewall at the VPC level

Security Group acts as a firewall at the subnet level whereas Network Access Control List (Network ACL) acts as a firewall at the instance level

Security Group acts as a firewall at the VPC level whereas Network Access Control List (Network ACL) acts as a firewall at the Availability Zone (AZ) level
------------------
**ChatGPT:**


The correct statement is: Security Group acts as a firewall at the instance level whereas Network Access Control List (Network ACL) acts as a firewall at the subnet level.
------------------
**You:**


10:46

↑

54/65

42:52

Finish test

Question 54:

Access Key ID and Secret Access Key are tied to which of the following AWS Identity and Access Management (AWS IAM) entities?

IAM User Group

IAM User

IAM Role

IAM Policy
------------------
**ChatGPT:**


Access Key ID and Secret Access Key are tied to an IAM User in AWS Identity and Access Management (AWS IAM).
------------------
**You:**


10:46

↓

55/65

42:27

Finish test

Question 55:

What are the fundamental drivers of cost with AWS Cloud?

Compute, Storage and Outbound Data Transfer

Compute, Storage and Inbound Data Transfer

Compute, Databases and Inbound Data Transfer

Compute, Databases and Outbound Data Transfer
------------------
**ChatGPT:**


The fundamental drivers of cost with AWS Cloud are Compute, Storage, and Outbound Data Transfer.
------------------
**You:**


10:47

↑

56/65

41:32

Finish test

Question 56:

Which AWS service enables users to find, buy, and immediately start using software solutions in their AWS environment?

AWS Systems Manager

AWS Marketplace

AWS Config

AWS OpsWorks
------------------
**ChatGPT:**


The AWS service that enables users to find, buy, and immediately start using software solutions in their AWS environment is called AWS Marketplace.
------------------
**You:**


10:47

↑

57/65

41:03 Finish test

Question 57:

As per the AWS Shared Responsibility Model, which of the following is a responsibility of the customer from a security and compliance point of view?

Configuration management for AWS global infrastructure

Patching/fixing flaws within the AWS infrastructure

Availability Zone (AZ) infrastructure management

Managing patches of the guest operating system on Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


As per the AWS Shared Responsibility Model, managing patches of the guest operating system on Amazon Elastic Compute Cloud (Amazon EC2) is a responsibility of the customer from a security and compliance point of view.
------------------
**You:**


10:48

↑

58/65

40:24

Finish test

Question 58:

An e-commerce company wants to assess its applications deployed on Amazon Elastic Compute Cloud (Amazon EC2) instances for vulnerabilities and deviations from AWS best practices. Which AWS service can be used to facilitate this?

Amazon Inspector

AWS CloudHSM

AWS Secrets Manager

AWS Trusted Advisor
------------------
**ChatGPT:**


To assess applications deployed on Amazon EC2 instances for vulnerabilities and deviations from AWS best practices, the e-commerce company can use Amazon Inspector.
------------------
**You:**


10:49

↑

59/65

39:49 Finish test

Question 59:

Which of the following AWS services comes under the Software as a Service (SaaS) Cloud Computing Type?

Elastic Load Balancing (ELB)

Amazon Elastic Compute Cloud (Amazon EC2)

Amazon Rekognition

AWS Elastic Beanstalk
------------------
**ChatGPT:**


Amazon Rekognition is the AWS service that falls under the Software as a Service (SaaS) Cloud Computing Type.
------------------
**You:**


10:49

↓

60/65

39:19

Finish test

Question 60:

A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?

AWS Direct Connect

AWS Wavelength

AWS Local Zones

AWS Edge Locations
------------------
**ChatGPT:**


To provide low-latency access to end-users in various locations, the gaming company can leverage the AWS CloudFront service with its global network of AWS Edge Locations. AWS CloudFront is a content delivery network (CDN) that helps deliver content with low latency and high data transfer speeds. It caches content at Edge Locations closest to end-users, reducing the distance and time taken to access the content, thereby improving the user experience.
------------------
**You:**


10:50

↓

61/65

38:15 Finish test

Question 61:

Which of the following AWS services are part of the

AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)

Amazon CloudWatch

AWS CloudTrail

AWS CloudFormation

AWS Trusted Advisor

Service Quotas
------------------
**ChatGPT:**


The AWS services that are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework are:

Amazon CloudWatch: It provides monitoring and observability for AWS resources and applications, helping detect and respond to operational issues.

AWS Trusted Advisor: It provides guidance on best practices and helps optimize AWS resources for reliability, security, performance, and cost.

These services contribute to ensuring the reliability of applications and systems deployed in the AWS Cloud.
------------------
**You:**


10:52

↓

62/65

37:06 Finish test

Question 62:

A photo sharing web application wants to store thumbnails of user-uploaded images on Amazon Simple Storage Service (Amazon S3). The thumbnails are rarely used but need to be immediately accessible from the web application. The thumbnails can be regenerated easily if they are lost. Which is the most cost-effective way to store these thumbnails on Amazon Simple Storage Service (Amazon S3)?

Use Amazon S3 Standard to store the thumbnails

Use Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) to store the thumbnails

Use Amazon S3 Glacier Flexible Retrieval to store the thumbnails

Use Amazon S3 Standard-Infrequent Access (S3 Standard-IA) to store the thumbnails
------------------
**ChatGPT:**


The most cost-effective way to store the thumbnails on Amazon Simple Storage Service (Amazon S3) in this scenario would be to use Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA).

Amazon S3 One Zone-IA is designed for data that can be easily re-created or is non-critical, and it offers a lower storage cost compared to Amazon S3 Standard. It stores data in a single availability zone, which reduces the cost but also means that the data is not replicated across multiple availability zones for higher durability.

Since the thumbnails can be easily regenerated if they are lost, and immediate accessibility is required from the web application, using Amazon S3 One Zone-IA provides a cost-effective solution while still meeting the requirements of the application.
------------------
**You:**


10:52

↓

63/65

36:24

Finish test

Question 63:

A company is using a message broker service on its on-premises application and wants to move this messaging functionality to AWS Cloud. Which of the following AWS services is the right choice to move the existing functionality easily?

Amazon Kinesis Data Streams

Amazon Simple Notification Service (Amazon SNS)

Amazon MQ

Amazon Simple Queue Service (Amazon sas)
------------------
**ChatGPT:**


To move the existing messaging functionality from an on-premises application to AWS Cloud, the right choice of AWS service would be Amazon MQ.

Amazon MQ is a managed message broker service that supports multiple messaging protocols and provides compatibility with existing applications. It supports industry-standard messaging protocols such as AMQP, MQTT, and STOMP, making it easier to migrate existing messaging functionality to AWS without making significant changes to the application code.

By using Amazon MQ, the company can seamlessly transition its message broker service to the cloud while maintaining compatibility with its on-premises application.
------------------
**You:**


10:53

↓

64/65

35:54 Finish test

Question 64:

Which policy describes prohibited uses of the web services offered by Amazon Web Services?

AWS Applicable Use Policy

AWS Fair Use Policy

AWS Trusted Advisor

AWS Acceptable Use Policy
------------------
**ChatGPT:**


The policy that describes prohibited uses of the web services offered by Amazon Web Services (AWS) is the AWS Acceptable Use Policy.

The AWS Acceptable Use Policy outlines the terms and conditions that govern the usage of AWS services. It specifies the activities that are prohibited and not allowed when using AWS services. This policy sets the guidelines for acceptable behavior and usage of AWS resources to ensure the security, reliability, and integrity of the services for all users.

It is important for users of AWS services to adhere to the AWS Acceptable Use Policy to maintain a safe and secure environment for themselves and other users of the platform.
------------------
**You:**


10:53

↑

65/65

35:27

Finish test

Question 65:

Which AWS support plan provides access to a designated Technical Account Manager (TAM)?

AWS Enterprise Support

AWS Developer Support

AWS Business Support

AWS Enterprise On-Ramp Support
------------------
**ChatGPT:**


The AWS support plan that provides access to a designated Technical Account Manager (TAM) is the AWS Enterprise Support plan.

The AWS Enterprise Support plan is a comprehensive support offering designed for enterprise customers. It includes a range of benefits and features to assist customers in operating and scaling their AWS environments. One of the key features of the AWS Enterprise Support plan is access to a designated Technical Account Manager (TAM).

A Technical Account Manager (TAM) is an AWS expert who works closely with the customer to understand their business goals and technical requirements. The TAM provides personalized guidance, architectural reviews, and best practices recommendations to help optimize the customer's use of AWS services. The TAM serves as a single point of contact within AWS, offering proactive assistance and support to address the customer's specific needs.

Overall, the AWS Enterprise Support plan with access to a designated Technical Account Manager (TAM) is ideal for customers who require a higher level of personalized support and guidance for their AWS deployments.
------------------
**You:**


Question 17: Incorrect
Which of the following statements are correct about the AWS root user account? (Select two)






Explanation
Correct options:

Root user access credentials are the email address and password used to create the AWS account

It is highly recommended to enable Multi Factor Authentication (MFA) for root user account

The Email address and the password used for signing up for AWS services are the AWS root user account credentials. Root user account, therefore, has full permissions on all AWS resources under that account. Restricting root user account access is not possible. As a best practice, Multi-Factor Authentication (MFA) should be set on the root user account. The root user account password can be changed after account creation. For all employees performing various administrative jobs, create individual user accounts using AWS IAM, and give administrative permissions as needed.

AWS Root User Account Security Best Practices:

 via - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

 via - https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials

Incorrect options:

Root user account password cannot be changed once it is set - This is incorrect. Like any other user credentials, the root user password can be changed after creation.

Root user credentials should only be shared with managers requiring administrative responsibilities to complete their jobs - This is a dangerous practice. Root user credentials should only be used only for some limited account-specific activity and root user credentials should be never be shared with anyone.

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies - Root user account permissions cannot be restricted, whoever has access to these credentials can perform any operation for that AWS account. The root user credentials should be kept safely.

References:

https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html

Question 21: Incorrect
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?





Explanation
Correct option:

Edge Location Management

Security and Compliance is a shared responsibility between AWS and the customer. The AWS Shared Responsibility Model can help relieve the customer’s operational burden as AWS operates, manages, and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates.

AWS is responsible for security "of" the cloud. This covers their global infrastructure elements including Regions, Availability Zones (AZ), and Edge Locations.

Incorrect options:

Customer Data

Identity and Access Management

Server-side Encryption (SSE)

The customer is responsible for security "in" the cloud. Customers are responsible for managing their data including encryption options and using Identity and Access Management tools for implementing appropriate access control policies as per their organization requirements. For abstracted services, such as Amazon S3 and Amazon DynamoDB, AWS operates the infrastructure layer, the operating system, and platforms, and customers access the endpoints to store and retrieve data. Therefore, these three options fall under the responsibility of the customer according to the AWS shared responsibility model.

Exam Alert:

Please review the AWS Shared Responsibility Model in detail as you can expect multiple questions on this topic in the exam:  via - https://aws.amazon.com/compliance/shared-responsibility-model/

Reference:

https://aws.amazon.com/compliance/shared-responsibility-model/

Question 26: Incorrect
AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)






Explanation
Correct options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EC2 Auto Scaling groups

Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions

AWS Compute Optimizer helps you identify the optimal AWS resource configurations, such as Amazon EC2 instance types, Amazon EBS volume configurations, and AWS Lambda function memory sizes, using machine learning to analyze historical utilization metrics. AWS Compute Optimizer delivers recommendations for selected types of EC2 instances, EC2 Auto Scaling groups, Amazon EBS volumes, and AWS Lambda functions.

AWS Compute Optimizer calculates an individual performance risk score for each resource dimension of the recommended instance, including CPU, memory, EBS throughput, EBS IOPS, disk throughput, disk throughput, network throughput, and network packets per second (PPS).

AWS Compute Optimizer provides EC2 instance type and size recommendations for EC2 Auto Scaling groups with a fixed group size, meaning desired, minimum, and maximum are all set to the same value and have no scaling policy attached.

AWS Compute Optimizer supports IOPS and throughput recommendations for General Purpose (SSD) (gp3) volumes and IOPS recommendations for Provisioned IOPS (io1 and io2) volumes.

AWS Compute Optimizer helps you optimize two categories of Lambda functions. The first category includes Lambda functions that may be over-provisioned in memory sizes. The second category includes compute-intensive Lambda functions that may benefit from additional CPU power.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Elastic File System (Amazon EFS)

Amazon Elastic File System (Amazon EFS), AWS Lambda functions

AWS Lambda functions, Amazon Simple Storage Service (Amazon S3)

AWS Compute Optimizer does not provide optimization recommendations for S3 and EFS, so these options are incorrect.

Reference:

https://aws.amazon.com/compute-optimizer/faqs/

Question 31: Incorrect
Which of the following statement is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?





Explanation
Correct option:

Only outbound data transfer is charged

One of the main benefits of cloud services is the ability it gives you to optimize costs to match your needs, even as those needs change. AWS services do not have complex dependencies or licensing requirements, so you can get exactly what you need to build innovative, cost-effective solutions using the latest technology.

There are three fundamental drivers of cost with AWS: compute, storage, and outbound data transfer. These characteristics vary somewhat, depending on the AWS product and pricing model you choose. Outbound data to the internet from all AWS regions is billed at region-specific, tiered data transfer rates. Inbound data transfer into all AWS regions from the internet is free.

Incorrect options:

Only inbound data transfer is charged

Both inbound data transfer and outbound data transfer are charged

Neither inbound nor outbound data transfer are charged

These three options contradict the explanation provided above, so these options are incorrect.

Reference:

https://d0.awsstatic.com/whitepapers/aws_pricing_overview.pdf

Question 42: Incorrect
Which Amazon Elastic Compute Cloud (Amazon EC2) pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that instance would not be interrupted?





Explanation
Correct option:

On-Demand Instance - An On-Demand Instance is an instance that you use on-demand. You have full control over its lifecycle — you decide when to launch, stop, hibernate, start, reboot, or terminate it. There is no long-term commitment required when you purchase On-Demand Instances. There is no upfront payment and you pay only for the seconds that your On-Demand Instances are running. The price per second for running an On-Demand Instance is fixed. On-demand instances cannot be interrupted.

EC2 Pricing Options Overview:  via - https://aws.amazon.com/ec2/pricing/

Incorrect options:

Reserved Instance (RI) - Reserved Instance (RI) provides you with significant savings on your Amazon EC2 costs compared to On-Demand Instance pricing. Reserved Instances (RI) are not physical instances, but rather a billing discount applied to the use of On-Demand Instances in your account. You can purchase a Reserved Instance (RI) for a one-year or three-year commitment, with the three-year commitment offering a bigger discount. You will be charged for the entire duration, irrespective of your usage. So this option is not correct for the given use-case.

Spot Instance - A Spot Instance is an unused EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. Spot Instances are well-suited for data analysis, batch jobs, background processing, and optional tasks. These can be terminated at short notice, so these are not suitable for critical workloads that need to run at a specific point in time. So this option is not correct for the given use-case.

Dedicated Host - Amazon EC2 Dedicated Host allows you to use your eligible software licenses from vendors such as Microsoft and Oracle on Amazon EC2 so that you get the flexibility and cost-effectiveness of using your licenses, but with the resiliency, simplicity, and elasticity of AWS. An Amazon EC2 Dedicated Host is a physical server fully dedicated for your use, so you can help address corporate compliance requirement. A Dedicated Host is not cost-efficient compared to an On-Demand instance. So this option is not correct.

Reference:

https://aws.amazon.com/ec2/pricing/

Question 44: Incorrect
Which of the following AWS services are always free to use (Select two)?






Explanation
Correct options:

AWS Identity and Access Management (AWS IAM) - AWS Identity and Access Management (AWS IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. IAM is a feature of your AWS account offered at no additional charge.

AWS Auto Scaling - AWS Auto Scaling monitors your applications and automatically adjusts the capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes. AWS Auto Scaling is available at no additional charge. You pay only for the AWS resources needed to run your applications and Amazon CloudWatch monitoring fees.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) - Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. This is not a free service. You pay for what you use or depending on the plan you choose.

Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. S3 service is not free and you pay to depend on the storage class you choose for your data.

Amazon DynamoDB - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB is not free and you are charged for reading, writing, and storing data in your DynamoDB tables, along with any optional features you choose to enable.

References:

https://aws.amazon.com/iam/

https://aws.amazon.com/autoscaling/

Question 51: Incorrect
Which of the following is correct about AWS Developer Support plan?





Explanation
Correct option:

Allows one contact to open unlimited cases

AWS Developer Support plan allows one primary contact to open unlimited cases.

Incorrect options:

Allows one contact to open a limited number of cases per month - As mentioned earlier, the AWS Developer Support plan allows one primary contact to open unlimited cases. So this option is incorrect.

Allows unlimited contacts to open unlimited cases - This is true for AWS Business Support, AWS Enterprise On-Ramp Support and AWS Enterprise Support plans. So this is incorrect for AWS Developer Support plan.

Allows unlimited contacts to open a limited number of cases per month - This is a made-up option and has been added as a distractor.

Reference:

https://aws.amazon.com/premiumsupport/plans/

Question 60: Incorrect
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?





Explanation
Correct option:

AWS Local Zones

AWS Local Zones allow you to use select AWS services, like compute and storage services, closer to more end-users, providing them very low latency access to the applications running locally. AWS Local Zones are also connected to the parent region via Amazon’s redundant and very high bandwidth private network, giving applications running in AWS Local Zones fast, secure, and seamless access to the rest of AWS services.

You should use AWS Local Zones to deploy workloads closer to your end-users for low-latency requirements. AWS Local Zones have their connection to the internet and support AWS Direct Connect, so resources created in the Local Zone can serve local end-users with very low-latency communications.

Various AWS services such as Amazon Elastic Compute Cloud (EC2), Amazon Virtual Private Cloud (VPC), Amazon Elastic Block Store (EBS), Amazon FSx, Amazon Elastic Load Balancing, Amazon EMR, Amazon ElastiCache, and Amazon Relational Database Service (RDS) are available locally in the AWS Local Zones. You can also use services that orchestrate or work with local services such as Amazon EC2 Auto Scaling, Amazon EKS clusters, Amazon ECS clusters, Amazon EC2 Systems Manager, Amazon CloudWatch, AWS CloudTrail, and AWS CloudFormation. AWS Local Zones also provide a high-bandwidth, secure connection to the AWS Region, allowing you to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

Incorrect options:

AWS Edge Locations - An AWS Edge location is a site that CloudFront uses to cache copies of the content for faster delivery to users at any location.

AWS Wavelength - AWS Wavelength extends the AWS cloud to a global network of 5G edge locations to enable developers to innovate and build a whole new class of applications that require ultra-low latency. Wavelength Zones provide a high-bandwidth, secure connection to the parent AWS Region, allowing developers to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

AWS Direct Connect - AWS Direct Connect is a cloud service that links your network directly to AWS, bypassing the internet to deliver more consistent, lower-latency performance. When creating a new connection, you can choose a hosted connection provided by an AWS Direct Connect Delivery Partner, or choose a dedicated connection from AWS—and deploy at over 100 AWS Direct Connect locations around the world. AWS Direct Connect provides consistently high bandwidth, low-latency access and it is generally used between on-premises data centers and AWS network. Direct Connect is overkill for the given requirement.

Reference:

https://aws.amazon.com/about-aws/global-infrastructure/localzones/

Question 61: Incorrect
Which of the following AWS services are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)






Explanation
Correct options:

AWS Trusted Advisor

Service Quotas

Foundations are part of the Reliability pillar of the AWS Well-Architected Framework. AWS states that before architecting any system, foundational requirements that influence reliability should be in place. The services that are part of foundations are: Amazon VPC, AWS Trusted Advisor, AWS Service Quotas (formerly called AWS Service Limits).

AWS Trusted Advisor is an online tool that provides you real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement. Whether establishing new workflows, developing applications, or as part of ongoing improvement, recommendations provided by Trusted Advisor regularly help keep your solutions provisioned optimally.

Service Quotas enables you to view and manage your quotas for AWS services from a central location. Quotas, also referred to as limits in AWS, are the maximum values for the resources, actions, and items in your AWS account. Each AWS service defines its quotas and establishes default values for those quotas.

Incorrect options:

AWS CloudTrail - AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides the event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command-line tools, and other AWS services. Think account-specific activity and audit; think CloudTrail.

AWS CloudFormation - AWS CloudFormation provides a common language to model and provision AWS and third-party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all Regions and accounts. Think infrastructure as code; think CloudFormation.

Amazon CloudWatch - Amazon CloudWatch is a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers. CloudWatch provides data and actionable insights to monitor applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health. This is an excellent service for building Resilient systems. Think resource performance monitoring, events, and alerts; think CloudWatch.

Reference:

https://wa.aws.amazon.com/wat.pillar.reliability.en.html
------------------
**ChatGPT:**


Apologies for the incorrect answers provided in my previous responses. Here are the correct answers for the questions you pointed out:

Question 17: Incorrect
Which of the following statements are correct about the AWS root user account? (Select two)

Correct options:

Root user access credentials are the email address and password used to create the AWS account.
It is highly recommended to enable Multi-Factor Authentication (MFA) for the root user account.

Explanation:
The root user account credentials are the email address and password used to create the AWS account. The root user has full permissions on all AWS resources and cannot have its access restricted. However, it is highly recommended to enable Multi-Factor Authentication (MFA) for the root user account to enhance security and protect against unauthorized access.

References:

AWS Identity and Access Management User Guide - Root user
AWS Identity and Access Management User Guide - Best Practices for Managing AWS Access Keys

Question 21: Incorrect
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?

Correct option:

Edge Location Management

Explanation:
According to the AWS Shared Responsibility Model, AWS is responsible for the security "of" the cloud, which includes managing and securing the underlying infrastructure, global network, and edge locations. Edge locations are part of AWS's infrastructure and are responsible for caching and delivering content to end-users, making their management a responsibility of AWS.

References:

AWS Shared Responsibility Model

Question 26: Incorrect
AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)

Correct options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EC2 Auto Scaling groups
Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions

Explanation:
AWS Compute Optimizer provides recommendations for optimizing resource configurations using machine learning. It delivers recommendations for Amazon EC2 instances, EC2 Auto Scaling groups, Amazon EBS volumes, and AWS Lambda functions. It helps identify optimal instance types, volume configurations, and memory sizes for Lambda functions based on historical utilization metrics.

References:

AWS Compute Optimizer FAQs

Question 31: Incorrect
Which of the following statements is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?

Correct option:

Only outbound data transfer is charged

Explanation:
According to AWS pricing policy, outbound data transfer from all AWS regions to the internet is billed at region-specific, tiered data transfer rates. However, inbound data transfer into all AWS regions from the internet is free.

References:

AWS Pricing Overview

Question 42: Incorrect
Which Amazon Elastic Compute Cloud (Amazon EC2) pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that the instance would not be interrupted?

Correct option:

On-Demand Instance

Explanation:
The On-Demand Instance pricing model in Amazon EC2 is the most cost-effective and flexible option. It does not require a long-term resource commitment or upfront payment. You pay only for the seconds that your On-Demand Instances are running. On-Demand Instances guarantee that the instance will not be interrupted.

References:

Amazon EC2 Pricing

Question 44: Incorrect
Which of the following AWS services are.
------------------
**You:**


Question 44: Incorrect
Which of the following AWS services are always free to use (Select two)?






Explanation
Correct options:

AWS Identity and Access Management (AWS IAM) - AWS Identity and Access Management (AWS IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. IAM is a feature of your AWS account offered at no additional charge.

AWS Auto Scaling - AWS Auto Scaling monitors your applications and automatically adjusts the capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes. AWS Auto Scaling is available at no additional charge. You pay only for the AWS resources needed to run your applications and Amazon CloudWatch monitoring fees.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) - Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. This is not a free service. You pay for what you use or depending on the plan you choose.

Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. S3 service is not free and you pay to depend on the storage class you choose for your data.

Amazon DynamoDB - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB is not free and you are charged for reading, writing, and storing data in your DynamoDB tables, along with any optional features you choose to enable.

References:

https://aws.amazon.com/iam/

https://aws.amazon.com/autoscaling/

Question 51: Incorrect
Which of the following is correct about AWS Developer Support plan?





Explanation
Correct option:

Allows one contact to open unlimited cases

AWS Developer Support plan allows one primary contact to open unlimited cases.

Incorrect options:

Allows one contact to open a limited number of cases per month - As mentioned earlier, the AWS Developer Support plan allows one primary contact to open unlimited cases. So this option is incorrect.

Allows unlimited contacts to open unlimited cases - This is true for AWS Business Support, AWS Enterprise On-Ramp Support and AWS Enterprise Support plans. So this is incorrect for AWS Developer Support plan.

Allows unlimited contacts to open a limited number of cases per month - This is a made-up option and has been added as a distractor.

Reference:

https://aws.amazon.com/premiumsupport/plans/

Question 60: Incorrect
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?





Explanation
Correct option:

AWS Local Zones

AWS Local Zones allow you to use select AWS services, like compute and storage services, closer to more end-users, providing them very low latency access to the applications running locally. AWS Local Zones are also connected to the parent region via Amazon’s redundant and very high bandwidth private network, giving applications running in AWS Local Zones fast, secure, and seamless access to the rest of AWS services.

You should use AWS Local Zones to deploy workloads closer to your end-users for low-latency requirements. AWS Local Zones have their connection to the internet and support AWS Direct Connect, so resources created in the Local Zone can serve local end-users with very low-latency communications.

Various AWS services such as Amazon Elastic Compute Cloud (EC2), Amazon Virtual Private Cloud (VPC), Amazon Elastic Block Store (EBS), Amazon FSx, Amazon Elastic Load Balancing, Amazon EMR, Amazon ElastiCache, and Amazon Relational Database Service (RDS) are available locally in the AWS Local Zones. You can also use services that orchestrate or work with local services such as Amazon EC2 Auto Scaling, Amazon EKS clusters, Amazon ECS clusters, Amazon EC2 Systems Manager, Amazon CloudWatch, AWS CloudTrail, and AWS CloudFormation. AWS Local Zones also provide a high-bandwidth, secure connection to the AWS Region, allowing you to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

Incorrect options:

AWS Edge Locations - An AWS Edge location is a site that CloudFront uses to cache copies of the content for faster delivery to users at any location.

AWS Wavelength - AWS Wavelength extends the AWS cloud to a global network of 5G edge locations to enable developers to innovate and build a whole new class of applications that require ultra-low latency. Wavelength Zones provide a high-bandwidth, secure connection to the parent AWS Region, allowing developers to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

AWS Direct Connect - AWS Direct Connect is a cloud service that links your network directly to AWS, bypassing the internet to deliver more consistent, lower-latency performance. When creating a new connection, you can choose a hosted connection provided by an AWS Direct Connect Delivery Partner, or choose a dedicated connection from AWS—and deploy at over 100 AWS Direct Connect locations around the world. AWS Direct Connect provides consistently high bandwidth, low-latency access and it is generally used between on-premises data centers and AWS network. Direct Connect is overkill for the given requirement.

Reference:

https://aws.amazon.com/about-aws/global-infrastructure/localzones/

Question 61: Incorrect
Which of the following AWS services are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)






Explanation
Correct options:

AWS Trusted Advisor

Service Quotas

Foundations are part of the Reliability pillar of the AWS Well-Architected Framework. AWS states that before architecting any system, foundational requirements that influence reliability should be in place. The services that are part of foundations are: Amazon VPC, AWS Trusted Advisor, AWS Service Quotas (formerly called AWS Service Limits).

AWS Trusted Advisor is an online tool that provides you real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement. Whether establishing new workflows, developing applications, or as part of ongoing improvement, recommendations provided by Trusted Advisor regularly help keep your solutions provisioned optimally.

Service Quotas enables you to view and manage your quotas for AWS services from a central location. Quotas, also referred to as limits in AWS, are the maximum values for the resources, actions, and items in your AWS account. Each AWS service defines its quotas and establishes default values for those quotas.

Incorrect options:

AWS CloudTrail - AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides the event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command-line tools, and other AWS services. Think account-specific activity and audit; think CloudTrail.

AWS CloudFormation - AWS CloudFormation provides a common language to model and provision AWS and third-party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all Regions and accounts. Think infrastructure as code; think CloudFormation.

Amazon CloudWatch - Amazon CloudWatch is a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers. CloudWatch provides data and actionable insights to monitor applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health. This is an excellent service for building Resilient systems. Think resource performance monitoring, events, and alerts; think CloudWatch.

Reference:

https://wa.aws.amazon.com/wat.pillar.reliability.en.html
------------------
**ChatGPT:**


Apologies for the incorrect answers provided in my previous responses. Here are the correct answers for the questions you pointed out:

Question 44: Incorrect
Which of the following AWS services are always free to use (Select two)?

Correct options:

AWS Identity and Access Management (AWS IAM)
AWS Auto Scaling

Explanation:
AWS Identity and Access Management (AWS IAM) is a service that enables you to manage access to AWS services and resources securely. It is available at no additional charge. AWS IAM allows you to create and manage AWS users, groups, and permissions.

AWS Auto Scaling is a service that automatically adjusts the capacity of your applications based on predefined scaling policies. The AWS Auto Scaling service itself is available at no additional charge. However, you still pay for the AWS resources (e.g., EC2 instances) that are launched as part of the scaling activities.

References:

AWS IAM Pricing
AWS Auto Scaling Pricing

Question 51: Incorrect
Which of the following is correct about AWS Developer Support plan?

Correct option:

Allows one primary contact to open unlimited cases

Explanation:
The AWS Developer Support plan allows one primary contact to open unlimited cases. It provides technical support for developers and is suitable for non-production environments and early-stage startups.

References:

AWS Support Plans

Question 60: Incorrect
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?

Correct option:

AWS Wavelength

Explanation:
AWS Wavelength is the AWS service that provides the necessary low-latency access to end-users. It extends the AWS cloud to the edge of 5G networks, allowing developers to deploy their applications in close proximity to mobile network operators' 5G infrastructure. This enables ultra-low-latency communication between the application and end-users, resulting in a great user experience for gaming and other latency-sensitive applications.

References:

AWS Wavelength

Question 61: Incorrect
Which of the following AWS services are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)

Correct options:

AWS Trusted Advisor
Service Quotas

Explanation:
AWS Trusted Advisor is a service that provides real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement. It is part of the AWS Foundation services for the Reliability pillar.

Service Quotas (formerly called AWS Service Limits) is a service that enables you to view and manage your quotas for AWS services from a central location. Quotas define the maximum values for resources, actions, and items in your AWS account. It is also part of the AWS Foundation services for the Reliability pillar.

References:

AWS Trusted Advisor
Service Quotas
------------------
**You:**


6 Practice Exams | AWS Certified Cloud Practitioner CLF-C01
Start
Practice Test 1: Practice Test #1 - AWS Certified Cloud Practitioner
Start
Practice Test 2: Practice Test #2 - AWS Certified Cloud Practitioner
Start
Practice Test 3: Practice Test #3 - AWS Certified Cloud Practitioner
Start
Practice Test 4: Practice Test #4 - AWS Certified Cloud Practitioner
Start
Practice Test 5: Practice Test #5 - AWS Certified Cloud Practitioner
Start
Practice Test 6: Practice Test #6 - AWS Certified Cloud Practitioner
Practice Test 2: Practice Test #2 - AWS Certified Cloud Practitioner
Practice Test #2 - AWS Certified Cloud Practitioner - Results
Chart
Pie chart with 4 slices.
End of interactive chart.
Attempt 1
Question 17: Incorrect
Which of the following statements are correct about the AWS root user account? (Select two)






Explanation
Correct options:

Root user access credentials are the email address and password used to create the AWS account

It is highly recommended to enable Multi Factor Authentication (MFA) for root user account

The Email address and the password used for signing up for AWS services are the AWS root user account credentials. Root user account, therefore, has full permissions on all AWS resources under that account. Restricting root user account access is not possible. As a best practice, Multi-Factor Authentication (MFA) should be set on the root user account. The root user account password can be changed after account creation. For all employees performing various administrative jobs, create individual user accounts using AWS IAM, and give administrative permissions as needed.

AWS Root User Account Security Best Practices:

 via - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

 via - https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials

Incorrect options:

Root user account password cannot be changed once it is set - This is incorrect. Like any other user credentials, the root user password can be changed after creation.

Root user credentials should only be shared with managers requiring administrative responsibilities to complete their jobs - This is a dangerous practice. Root user credentials should only be used only for some limited account-specific activity and root user credentials should be never be shared with anyone.

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies - Root user account permissions cannot be restricted, whoever has access to these credentials can perform any operation for that AWS account. The root user credentials should be kept safely.

References:

https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html

Question 21: Incorrect
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?





Explanation
Correct option:

Edge Location Management

Security and Compliance is a shared responsibility between AWS and the customer. The AWS Shared Responsibility Model can help relieve the customer’s operational burden as AWS operates, manages, and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates.

AWS is responsible for security "of" the cloud. This covers their global infrastructure elements including Regions, Availability Zones (AZ), and Edge Locations.

Incorrect options:

Customer Data

Identity and Access Management

Server-side Encryption (SSE)

The customer is responsible for security "in" the cloud. Customers are responsible for managing their data including encryption options and using Identity and Access Management tools for implementing appropriate access control policies as per their organization requirements. For abstracted services, such as Amazon S3 and Amazon DynamoDB, AWS operates the infrastructure layer, the operating system, and platforms, and customers access the endpoints to store and retrieve data. Therefore, these three options fall under the responsibility of the customer according to the AWS shared responsibility model.

Exam Alert:

Please review the AWS Shared Responsibility Model in detail as you can expect multiple questions on this topic in the exam:  via - https://aws.amazon.com/compliance/shared-responsibility-model/

Reference:

https://aws.amazon.com/compliance/shared-responsibility-model/

Question 26: Incorrect
AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)






Explanation
Correct options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EC2 Auto Scaling groups

Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions

AWS Compute Optimizer helps you identify the optimal AWS resource configurations, such as Amazon EC2 instance types, Amazon EBS volume configurations, and AWS Lambda function memory sizes, using machine learning to analyze historical utilization metrics. AWS Compute Optimizer delivers recommendations for selected types of EC2 instances, EC2 Auto Scaling groups, Amazon EBS volumes, and AWS Lambda functions.

AWS Compute Optimizer calculates an individual performance risk score for each resource dimension of the recommended instance, including CPU, memory, EBS throughput, EBS IOPS, disk throughput, disk throughput, network throughput, and network packets per second (PPS).

AWS Compute Optimizer provides EC2 instance type and size recommendations for EC2 Auto Scaling groups with a fixed group size, meaning desired, minimum, and maximum are all set to the same value and have no scaling policy attached.

AWS Compute Optimizer supports IOPS and throughput recommendations for General Purpose (SSD) (gp3) volumes and IOPS recommendations for Provisioned IOPS (io1 and io2) volumes.

AWS Compute Optimizer helps you optimize two categories of Lambda functions. The first category includes Lambda functions that may be over-provisioned in memory sizes. The second category includes compute-intensive Lambda functions that may benefit from additional CPU power.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Elastic File System (Amazon EFS)

Amazon Elastic File System (Amazon EFS), AWS Lambda functions

AWS Lambda functions, Amazon Simple Storage Service (Amazon S3)

AWS Compute Optimizer does not provide optimization recommendations for S3 and EFS, so these options are incorrect.

Reference:

https://aws.amazon.com/compute-optimizer/faqs/

Question 31: Incorrect
Which of the following statement is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?





Explanation
Correct option:

Only outbound data transfer is charged

One of the main benefits of cloud services is the ability it gives you to optimize costs to match your needs, even as those needs change. AWS services do not have complex dependencies or licensing requirements, so you can get exactly what you need to build innovative, cost-effective solutions using the latest technology.

There are three fundamental drivers of cost with AWS: compute, storage, and outbound data transfer. These characteristics vary somewhat, depending on the AWS product and pricing model you choose. Outbound data to the internet from all AWS regions is billed at region-specific, tiered data transfer rates. Inbound data transfer into all AWS regions from the internet is free.

Incorrect options:

Only inbound data transfer is charged

Both inbound data transfer and outbound data transfer are charged

Neither inbound nor outbound data transfer are charged

These three options contradict the explanation provided above, so these options are incorrect.

Reference:

https://d0.awsstatic.com/whitepapers/aws_pricing_overview.pdf

Question 42: Incorrect
Which Amazon Elastic Compute Cloud (Amazon EC2) pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that instance would not be interrupted?





Explanation
Correct option:

On-Demand Instance - An On-Demand Instance is an instance that you use on-demand. You have full control over its lifecycle — you decide when to launch, stop, hibernate, start, reboot, or terminate it. There is no long-term commitment required when you purchase On-Demand Instances. There is no upfront payment and you pay only for the seconds that your On-Demand Instances are running. The price per second for running an On-Demand Instance is fixed. On-demand instances cannot be interrupted.

EC2 Pricing Options Overview:  via - https://aws.amazon.com/ec2/pricing/

Incorrect options:

Reserved Instance (RI) - Reserved Instance (RI) provides you with significant savings on your Amazon EC2 costs compared to On-Demand Instance pricing. Reserved Instances (RI) are not physical instances, but rather a billing discount applied to the use of On-Demand Instances in your account. You can purchase a Reserved Instance (RI) for a one-year or three-year commitment, with the three-year commitment offering a bigger discount. You will be charged for the entire duration, irrespective of your usage. So this option is not correct for the given use-case.

Spot Instance - A Spot Instance is an unused EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. Spot Instances are well-suited for data analysis, batch jobs, background processing, and optional tasks. These can be terminated at short notice, so these are not suitable for critical workloads that need to run at a specific point in time. So this option is not correct for the given use-case.

Dedicated Host - Amazon EC2 Dedicated Host allows you to use your eligible software licenses from vendors such as Microsoft and Oracle on Amazon EC2 so that you get the flexibility and cost-effectiveness of using your licenses, but with the resiliency, simplicity, and elasticity of AWS. An Amazon EC2 Dedicated Host is a physical server fully dedicated for your use, so you can help address corporate compliance requirement. A Dedicated Host is not cost-efficient compared to an On-Demand instance. So this option is not correct.

Reference:

https://aws.amazon.com/ec2/pricing/

Question 44: Incorrect
Which of the following AWS services are always free to use (Select two)?






Explanation
Correct options:

AWS Identity and Access Management (AWS IAM) - AWS Identity and Access Management (AWS IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. IAM is a feature of your AWS account offered at no additional charge.

AWS Auto Scaling - AWS Auto Scaling monitors your applications and automatically adjusts the capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes. AWS Auto Scaling is available at no additional charge. You pay only for the AWS resources needed to run your applications and Amazon CloudWatch monitoring fees.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) - Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. This is not a free service. You pay for what you use or depending on the plan you choose.

Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. S3 service is not free and you pay to depend on the storage class you choose for your data.

Amazon DynamoDB - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB is not free and you are charged for reading, writing, and storing data in your DynamoDB tables, along with any optional features you choose to enable.

References:

https://aws.amazon.com/iam/

https://aws.amazon.com/autoscaling/

Question 51: Incorrect
Which of the following is correct about AWS Developer Support plan?





Explanation
Correct option:

Allows one contact to open unlimited cases

AWS Developer Support plan allows one primary contact to open unlimited cases.

Incorrect options:

Allows one contact to open a limited number of cases per month - As mentioned earlier, the AWS Developer Support plan allows one primary contact to open unlimited cases. So this option is incorrect.

Allows unlimited contacts to open unlimited cases - This is true for AWS Business Support, AWS Enterprise On-Ramp Support and AWS Enterprise Support plans. So this is incorrect for AWS Developer Support plan.

Allows unlimited contacts to open a limited number of cases per month - This is a made-up option and has been added as a distractor.

Reference:

https://aws.amazon.com/premiumsupport/plans/

Question 60: Incorrect
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?





Explanation
Correct option:

AWS Local Zones

AWS Local Zones allow you to use select AWS services, like compute and storage services, closer to more end-users, providing them very low latency access to the applications running locally. AWS Local Zones are also connected to the parent region via Amazon’s redundant and very high bandwidth private network, giving applications running in AWS Local Zones fast, secure, and seamless access to the rest of AWS services.

You should use AWS Local Zones to deploy workloads closer to your end-users for low-latency requirements. AWS Local Zones have their connection to the internet and support AWS Direct Connect, so resources created in the Local Zone can serve local end-users with very low-latency communications.

Various AWS services such as Amazon Elastic Compute Cloud (EC2), Amazon Virtual Private Cloud (VPC), Amazon Elastic Block Store (EBS), Amazon FSx, Amazon Elastic Load Balancing, Amazon EMR, Amazon ElastiCache, and Amazon Relational Database Service (RDS) are available locally in the AWS Local Zones. You can also use services that orchestrate or work with local services such as Amazon EC2 Auto Scaling, Amazon EKS clusters, Amazon ECS clusters, Amazon EC2 Systems Manager, Amazon CloudWatch, AWS CloudTrail, and AWS CloudFormation. AWS Local Zones also provide a high-bandwidth, secure connection to the AWS Region, allowing you to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.
------------------
**ChatGPT:**


Incorrect options:

AWS Snowball - AWS Snowball is a petabyte-scale data transport solution that uses secure appliances to transfer large amounts of data into and out of AWS. It is not specifically designed for low-latency access to end-users.

Amazon Elastic File System (Amazon EFS) - Amazon EFS is a fully managed file system service that provides scalable and highly available file storage for use with Amazon EC2 instances. It is not specifically designed to deliver low-latency gameplay to end-users.

Amazon RDS Multi-AZ - Amazon RDS Multi-AZ is a high-availability feature of Amazon RDS that provides automatic failover capability for database instances. While it helps ensure high availability, it does not specifically address low-latency access for gaming applications.

Reference:

https://aws.amazon.com/about-aws/global-infrastructure/localzones/
------------------
**You:**


11:09

↑

1/65

1:29:49

Finish test

Question 1:

Which AWS service can be used to automate code deployment to Amazon Elastic Compute Cloud (Amazon EC2) instances as well as on-premises instances?

AWS CloudFormation

AWS CodeCommit

AWS CodeDeploy

AWS CodePipeline
------------------
**ChatGPT:**


The correct answer is:

AWS CodeDeploy

AWS CodeDeploy is the AWS service that can be used to automate code deployment to Amazon EC2 instances as well as on-premises instances. It is a fully managed deployment service that automates software deployments to a variety of compute services, including Amazon EC2, Lambda, and on-premises servers. With AWS CodeDeploy, you can deploy your applications in a consistent and reliable manner, allowing you to rapidly release new features and updates.

AWS CloudFormation is a service that provides infrastructure as code and allows you to create and manage AWS resources using templates. It is used for provisioning and managing resources, but it does not directly handle code deployment.

AWS CodeCommit is a fully managed source control service that hosts private Git repositories. It provides a secure and scalable platform for storing and version-controlling your code, but it does not handle code deployment.

AWS CodePipeline is a fully managed continuous delivery service that helps you automate the release pipelines for your applications. It provides a workflow for building, testing, and deploying your code changes, but it does not directly deploy code to instances.

So, the correct answer is:

AWS CodeDeploy
------------------
**You:**


11:10

↑

2/65

1:28:23

Finish test

Question 2:

AWS Identity and Access Management (AWS IAM) policies are written as JSON documents. Which of the following are mandatory elements of an IAM policy?

Effect, Action

Effect, Sid

Action, Condition

Sid, Principal
------------------
**ChatGPT:**


The correct answer is:

Effect, Action

In AWS Identity and Access Management (IAM), policies are written as JSON documents. The mandatory elements of an IAM policy are the "Effect" and "Action" elements.

"Effect" specifies whether the policy statement allows or denies access. It can have two possible values: "Allow" or "Deny".

"Action" specifies the actions or operations that are allowed or denied. Actions are defined as a combination of a service namespace and an action name, such as "s3:GetObject" or "ec2:RunInstances".

The "Sid" element is optional and stands for "Statement ID". It is used to provide a unique identifier for the policy statement. It can be useful when you want to refer to a specific statement within a policy for management or troubleshooting purposes.

The "Principal" element is also optional and defines the AWS identities (users, groups, or roles) to which the policy applies. It specifies the entity that is allowed or denied access to the specified resources. If not specified, the policy applies to all principals.

So, in summary, the mandatory elements of an IAM policy are "Effect" and "Action".
------------------
**You:**


←

3/65

1:27:25

| Finish test

Question 3:

Which AWS service will you use if you have to move large volumes of on-premises data to AWS Cloud from a remote location with limited bandwidth?

AWS Snowball

AWS Direct Connect

AWS Virtual Private Network (VPN)

AWS Transit Gateway

<

>
------------------
**ChatGPT:**


The correct answer is:

AWS Snowball

If you need to move large volumes of on-premises data to AWS Cloud from a remote location with limited bandwidth, you can use AWS Snowball. AWS Snowball is a service that allows you to transfer large amounts of data to and from AWS using physical storage devices.

Here's how AWS Snowball works:

You request a Snowball device from the AWS Management Console.
AWS ships the Snowball device to your location.
You connect the Snowball device to your on-premises environment and transfer your data onto the device.
Once the data transfer is complete, you ship the Snowball device back to AWS.
AWS imports the data from the Snowball device into your designated S3 bucket.
You can then access and use your data in AWS Cloud.

AWS Snowball helps overcome limitations of limited bandwidth and high network costs by providing a physical device for data transfer. It ensures secure data transfer and minimizes the time required to move large volumes of data to AWS Cloud.

AWS Direct Connect, AWS Virtual Private Network (VPN), and AWS Transit Gateway are different services used for establishing network connectivity between your on-premises environment and AWS Cloud, but they are not specifically designed for moving large volumes of data like AWS Snowball.
------------------
**You:**


11:12

↑

4/65

1:26:43

| Finish test

Question 4:

Which of the following are correct statements regarding the AWS Shared Responsibility Model? (Select two)

Configuration Management is the responsibility of the customer

AWS is responsible for training AWS and customer employees on AWS products and services

For a service like Amazon EC2, that falls under Infrastructure as a Service (IaaS), AWS is responsible for maintaining guest operating system

For abstracted services like Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms

AWS is responsible for Security 'of' the Cloud
------------------
**ChatGPT:**


The correct statements regarding the AWS Shared Responsibility Model are:

Configuration Management is the responsibility of the customer.
AWS is responsible for Security 'of' the Cloud.

In the AWS Shared Responsibility Model:

AWS is responsible for the security 'of' the cloud, which means they are responsible for securing the underlying infrastructure that supports the AWS services. This includes aspects such as the physical security of data centers, network infrastructure, and hardware maintenance.

The customer is responsible for security 'in' the cloud, which means they are responsible for configuring and securing their applications, data, and operating systems that are deployed on AWS. This includes tasks such as configuring access controls, implementing security patches, and managing user access.

Regarding the other statements:

AWS is not responsible for training AWS and customer employees on AWS products and services. Training and education on AWS products and services are typically the responsibility of the customer or can be obtained through AWS training resources.

For a service like Amazon EC2, which falls under Infrastructure as a Service (IaaS), AWS is responsible for maintaining the underlying infrastructure, including the physical host, virtualization layer, and network connectivity. However, the responsibility for maintaining the guest operating system, including patching and updates, lies with the customer.

For abstracted services like Amazon S3, AWS operates the infrastructure layer, which includes the physical storage and network connectivity, but the responsibility for the operating system and platforms used by the customer applications lies with the customer.

Therefore, the correct statements are the ones mentioned at the beginning.
------------------
**You:**


11:14

↑

5/65

1:25:03

Finish test

Question 5:

Which of the following are recommended best practices for AWS Identity and Access Management (AWS IAM) service? (Select two)

Grant maximum privileges to avoid assigning privileges again

Rotate credentials regularly

Share AWS account root user access keys with other administrators

Create a minimum number of accounts and share these account credentials among employees

Enable multi-factor authentication (MFA) for all users
------------------
**ChatGPT:**


The recommended best practices for AWS Identity and Access Management (AWS IAM) service are:

Rotate credentials regularly: It is a good practice to rotate access keys and passwords for IAM users on a regular basis. This helps mitigate the risk of unauthorized access if credentials are compromised.

Enable multi-factor authentication (MFA) for all users: Enabling MFA adds an extra layer of security to user accounts by requiring users to provide an additional authentication factor, such as a time-based one-time password (TOTP) generated by a virtual MFA device or a hardware MFA token, in addition to their regular password.

The other options mentioned are not recommended best practices:

Granting maximum privileges to avoid assigning privileges again is not a recommended practice. Instead, the principle of least privilege should be followed, where users are given only the minimum privileges necessary to perform their tasks. This helps reduce the potential impact of compromised credentials.

Sharing AWS account root user access keys with other administrators is not recommended. It is best to create individual IAM users for administrators and grant them appropriate permissions. Sharing root user access keys increases the risk of unauthorized access and makes it difficult to track actions performed by individual administrators.

Creating a minimum number of accounts and sharing account credentials among employees is also not recommended. Each employee should have their own individual IAM account to ensure accountability and traceability of actions. Sharing account credentials can lead to security vulnerabilities and difficulties in managing access control.

Therefore, the correct answers are rotating credentials regularly and enabling multi-factor authentication (MFA) for all users.
------------------
**You:**


11:15

↑

6/65

1:24:14

Finish test

Question 6:

Which of the following statements is correct regarding the Amazon Elastic File System (Amazon EFS) storage service?

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system only in one Availability Zone (AZ)

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ) but not across VPCs and Regions

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ) and VPCs but not across Regions

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ), Regions and VPCs
------------------
**ChatGPT:**


The correct statement regarding the Amazon Elastic File System (Amazon EFS) storage service is:

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ), Regions, and VPCs.

Amazon EFS provides a scalable and fully managed file storage service for use with Amazon EC2 instances. It is designed to provide shared file storage that can be accessed by multiple EC2 instances simultaneously. Amazon EFS file systems are accessible across multiple Availability Zones within a region, allowing high availability and durability. Additionally, EC2 instances in different VPCs and even different AWS regions can access the same Amazon EFS file system, making it a versatile and flexible storage option.

Therefore, the correct option is "EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ), Regions, and VPCs."
------------------
**You:**


11:16

↑

7/65

1:22:48

| Finish test

Question 7:

Which of the following AWS entities provides the information required to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance?

Amazon Elastic Block Store (Amazon EBS)

Amazon Machine Image (AMI)

AWS Lambda

Amazon Elastic File System (Amazon EFS)
------------------
**ChatGPT:**


The entity that provides the information required to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance is an Amazon Machine Image (AMI).

An Amazon Machine Image (AMI) is a template that contains the necessary information to launch an EC2 instance. It includes the root file system, launch permissions, and any other data required to start an instance. AMIs can be created and customized by users or obtained from the AWS Marketplace.

When launching an EC2 instance, you typically select an AMI that suits your needs, such as a specific operating system and software configuration. The AMI provides the base image from which the instance is created.

Therefore, the correct option is "Amazon Machine Image (AMI)."
------------------
**You:**


11:17

↑

8/65

1:21:30

Finish test

Question 8:

Which feature of AWS Cloud offers the ability to

innovate faster and rapidly develop, test and launch software applications?

Cost savings

Ability to deploy globally in minutes

Elasticity

Agility
------------------
**ChatGPT:**


The feature of AWS Cloud that offers the ability to innovate faster and rapidly develop, test, and launch software applications is "Agility."

Agility refers to the capability of quickly and easily adapting to changing business needs and requirements. AWS provides a wide range of services and tools that enable developers to rapidly develop, test, and deploy applications. With AWS, developers can leverage managed services, automation, and scalable infrastructure to speed up the development and deployment process.

By using AWS services like AWS Lambda for serverless computing, AWS CodeCommit and AWS CodePipeline for continuous integration and continuous delivery (CI/CD), and AWS Elastic Beanstalk for application deployment and management, developers can achieve greater agility in their software development lifecycle.

Therefore, the correct option is "Agility."
------------------
**You:**


11:18

↑

9/65

1:20:58

| Finish test

Question 9:

AWS Lambda pricing is based on which of the following criteria? (Select two)

The number of lines of code for the AWS

Lambda function

The size of the deployment package for the AWS Lambda function

The time it takes for the AWS Lambda function to execute

Number of requests for the AWS Lambda function

The language runtime of the AWS Lambda function
------------------
**ChatGPT:**


AWS Lambda pricing is based on the following criteria:

The time it takes for the AWS Lambda function to execute: AWS Lambda pricing is based on the duration of the function's execution, measured in increments of 100 milliseconds. You are billed for the actual time it takes for your function to run.

Number of requests for the AWS Lambda function: AWS Lambda pricing is also based on the number of requests made to your function. You are charged for each request made to your function, regardless of the amount of compute time used.

Therefore, the correct options are:

The time it takes for the AWS Lambda function to execute
Number of requests for the AWS Lambda function
------------------
**You:**


11:19

↑

10/65

1:20:13

Finish test

Question 10:

Which AWS service protects your AWS account by monitoring malicious activity and detecting threats?

Amazon GuardDuty

Amazon CloudWatch

AWS CloudTrail

AWS Trusted Advisor
------------------
**ChatGPT:**


The AWS service that protects your AWS account by monitoring malicious activity and detecting threats is Amazon GuardDuty. Amazon GuardDuty is a threat detection service that continuously monitors for malicious activity and unauthorized behavior within your AWS environment. It analyzes events, such as API calls and network traffic, to identify potential threats and security vulnerabilities.
------------------
**You:**


11:20

↑

11/65

1:19:17

Finish test

Question 11:

Which of the following Cloud Computing models does the 'gmail' service represent?

Infrastructure as a Service (IaaS)

Software as a Service (SaaS)

Function as a Service (FaaS)

Platform as a Service (PaaS)
------------------
**ChatGPT:**


The 'gmail' service represents the Software as a Service (SaaS) cloud computing model. Software as a Service (SaaS) provides users with access to software applications over the internet without the need for installation and management of the underlying infrastructure or software. Gmail is a web-based email service provided by Google, and users can access it through a web browser without needing to manage any infrastructure or software components.
------------------
**You:**


11:20

↓

12/65

1:18:45

Finish test

Question 12:

Which AWS service can help you create data-driven

business cases for transitioning your business from on-premises to AWS Cloud?

AWS Trusted Advisor

AWS Migration Evaluator

AWS Billing and Cost Management

AWS Budgets
------------------
**ChatGPT:**


The AWS service that can help you create data-driven business cases for transitioning your business from on-premises to AWS Cloud is AWS Migration Evaluator. AWS Migration Evaluator provides a comprehensive view of your on-premises environment and helps you assess the cost savings and other benefits of migrating to the AWS Cloud. It analyzes your on-premises infrastructure, applications, and data to provide insights and recommendations for migration. By using AWS Migration Evaluator, you can gather data and insights to build a business case for transitioning your business to the AWS Cloud.
------------------
**You:**


11:21

↑

13/65

1:18:08

Finish test

Question 13:

An AWS user is trying to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance in a given region. What is the region-specific constraint that the Amazon Machine Image (AMI) must meet so that it can be used for this Amazon Elastic Compute Cloud (Amazon EC2) instance?

You can use an Amazon Machine Image (AMI) from a different region, but it degrades the performance of the Amazon EC2 instance

You should use an Amazon Machine Image (AMI) from the same region, as it improves the performance of the Amazon EC2 instance

You must use an Amazon Machine Image (AMI) from the same region as that of the Amazon EC2 instance. The region of the Amazon Machine Image (AMI) has no bearing on the performance of the Amazon EC2 instance

An Amazon Machine Image (AMI) is a

<
------------------
**ChatGPT:**


An AWS user trying to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance in a given region must use an Amazon Machine Image (AMI) from the same region as that of the instance. The region-specific constraint requires the AMI and the EC2 instance to be in the same region. The region of the AMI has no direct impact on the performance of the EC2 instance, but it is necessary for compatibility and availability within the chosen region. Therefore, to ensure proper functionality and compatibility, it is recommended to use an AMI from the same region as the EC2 instance.
------------------
**You:**


11:22

↓

14/65

1:16:53

Finish test

Question 14:

A startup wants to set up its IT infrastructure on AWS Cloud. The CTO would like to receive detailed reports that break down the startup's AWS costs by the hour in an Amazon Simple Storage Service (Amazon S3) bucket. As a Cloud Practitioner, which AWS service would you recommend for this use-case?

AWS Budgets

AWS Cost Explorer

AWS Pricing Calculator

AWS Cost & Usage Report (AWS CUR)
------------------
**ChatGPT:**


As a Cloud Practitioner, I would recommend using the AWS Cost & Usage Report (AWS CUR) for the given use-case. The AWS Cost & Usage Report provides detailed information about your AWS costs and usage. It can break down costs by the hour and provide comprehensive reports on cost allocation, usage patterns, and resource utilization. You can configure the report to be delivered to an Amazon Simple Storage Service (Amazon S3) bucket, allowing you to store and analyze the data at your convenience. The AWS CUR offers flexibility and customization options to meet your specific reporting needs and provides valuable insights into your AWS cost management.
------------------
**You:**


11:24

↓

15/65

1:15:29

Finish test

Question 15:

Which of the following use cases is best suited for Amazon EFS Standard-Infrequent Access (EFS Standard-IA) storage class?

Object storage for workloads that need sub-second latency speeds for accessing the data

Use as boot volume for highly available Amazon Elastic Compute Cloud (Amazon EC2) instances

Storing data in a single AWS Availability Zone (AZ)

Storing files in an accessible location to satisfy audit requirements
------------------
**ChatGPT:**


The use case that is best suited for Amazon EFS Standard-Infrequent Access (EFS Standard-IA) storage class is "Storing files in an accessible location to satisfy audit requirements."

Amazon EFS Standard-IA is designed for workloads that require infrequent access to data but still need the ability to quickly retrieve it when necessary. It provides a lower-cost storage option compared to Amazon EFS Standard, while still offering the same level of durability and scalability. This storage class is ideal for storing files that need to be readily accessible to meet audit requirements, ensuring that data can be retrieved efficiently when needed.
------------------
**You:**


Which Amazon EC2 pricing model provides is the most cost-effective for an always-up, right-sized database server running a project that will last 1 year?
------------------
**ChatGPT:**


For an always-up, right-sized database server running a project that will last 1 year, the most cost-effective Amazon EC2 pricing model would typically be the Reserved Instances (RI) pricing model.

Reserved Instances allow you to reserve capacity for your Amazon EC2 instances in advance, offering significant cost savings compared to On-Demand instances. By committing to a specific instance type and term length (such as 1 year), you can receive a discounted hourly rate for your instances. This pricing model is well-suited for workloads that require long-term usage and have predictable utilization patterns.

By utilizing Reserved Instances, you can optimize your costs for the entire duration of your project while ensuring that your database server is always up and running at the right size. It's important to analyze your usage requirements and workload patterns to determine the appropriate instance type and the number of Reserved Instances needed to meet your specific needs.
------------------
**You:**


Which of the options below are recommendations in the performance efficiency pillar of the well-architected framework? (choose 2)
------------------
**ChatGPT:**


In the Performance Efficiency pillar of the AWS Well-Architected Framework, the following options are recommendations:

Selecting the Right Resource Types: Choose the appropriate AWS resource types that align with the needs of your workload. This involves considering factors such as compute, storage, database, and network resources. By selecting the right resource types, you can optimize performance and cost-effectiveness.

Designing for Elasticity: Design your architecture to scale horizontally or vertically based on workload demands. Elasticity allows your system to automatically handle varying levels of traffic or load by adding or removing resources dynamically. This ensures that your application can efficiently handle peak loads without over-provisioning and incurring unnecessary costs during low-demand periods.

These recommendations aim to optimize the performance of your workload while ensuring efficient resource utilization and cost-effectiveness.
------------------
**You:**


Which of the options are recommendations in the performance efficiency pillar of the well-architected framework?
------------------
**ChatGPT:**


Apologies for the confusion in my previous response. In the Performance Efficiency pillar of the AWS Well-Architected Framework, the following are recommendations:

Selection of Right Compute Resource: Choose the appropriate compute resource types based on the workload requirements. Consider factors such as CPU, memory, and network performance to ensure the selected compute resource can handle the expected workload efficiently.

Scalable and Elastic Architecture: Design your architecture to be scalable and elastic, allowing it to automatically adjust resources based on workload demands. This enables your application to handle varying levels of traffic and load without performance degradation.

Efficient Storage Management: Optimize storage usage by selecting the appropriate storage types and configurations. Use techniques like data compression, deduplication, and tiered storage to reduce costs and improve performance.

Caching: Implement caching mechanisms to reduce latency and improve performance. Use services like Amazon ElastiCache or Amazon CloudFront to cache frequently accessed data and reduce the load on backend resources.

Performance Monitoring and Analysis: Implement monitoring and analysis tools to gain insights into system performance. Use services like Amazon CloudWatch to monitor key metrics and identify performance bottlenecks or areas for optimization.

These recommendations focus on optimizing the performance of your architecture, ensuring efficient resource utilization, scalability, and monitoring to deliver a high-performing and cost-effective solution.
------------------
**You:**


Which of the options below are recommendations in the performance efficiency
pillar of the well-architected framework? (choose 2)

D Democratize advanced technologies

I: Go global in days

Use serverless architectures

[:I Rarely experiment
------------------
**ChatGPT:**


In the Performance Efficiency pillar of the well-architected framework, the recommendations are:

Use serverless architectures: Serverless architectures, such as AWS Lambda, can improve performance efficiency by abstracting the underlying infrastructure management. They automatically scale based on demand, allowing you to focus on writing code and optimizing the application logic rather than managing servers.

Democratize advanced technologies: This recommendation suggests making advanced technologies accessible to all teams within your organization. By democratizing advanced technologies, you can empower teams to leverage tools, services, and best practices that can enhance performance efficiency and innovation.

The options "Go global in days" and "Rarely experiment" are not specific recommendations in the Performance Efficiency pillar of the well-architected framework.
------------------
**You:**


Vhich feature enables fast, easy, and secure transfers of files over long distances
tetween a client and an Amazon 83 bucket?
O 53 Static Websites |
O 53 Copy |
Q Multipart Upload |
O 53 Transfer Acceleration |
------------------
**ChatGPT:**


The feature that enables fast, easy, and secure transfers of files over long distances between a client and an Amazon S3 bucket is "Transfer Acceleration." Transfer Acceleration is an Amazon S3 feature that utilizes Amazon CloudFront's globally distributed edge locations to accelerate file uploads to and downloads from S3 buckets. It improves transfer speeds by optimizing the network path between the client and the S3 bucket, making it ideal for scenarios where data needs to be transferred over long distances.
------------------
**You:**


Question 10:
Which of the following represent economic advantages of moving to the AWS cloud? (Select TWO.)
I:| Reduce the need to manage applications
El Increase efficiencies through automation
|:| Reduce the rate of change
[:I Reduce the need to manage infrastructure
[:I Increase time to market for new applications'
------------------
**ChatGPT:**


The economic advantages of moving to the AWS cloud include:

Reduce the need to manage applications: By leveraging AWS cloud services, organizations can offload the responsibility of managing applications to AWS, reducing the overhead and cost associated with maintaining and supporting complex applications.

Increase efficiencies through automation: AWS provides a wide range of automation tools and services that can streamline and optimize various operational tasks, leading to increased efficiencies and cost savings.

Therefore, the correct options are:

Reduce the need to manage applications
Increase efficiencies through automation
------------------
**You:**


Question 11:

Which of the options below are recommendations in the security pillar of the well-architected
framework? (Select TWO.)

I:I Enable traceability

|:| Apply security at the application layer

B Automate security best practices

[:I Protect data when it is at rest only

[:I Expect to be secure
------------------
**ChatGPT:**


In the security pillar of the well-architected framework, the following are recommendations:

Enable traceability: Implement mechanisms to track and monitor user activities and API calls, enabling auditing and investigation in case of security incidents.

Apply security at the application layer: Implement security measures and best practices directly within the application code and architecture to protect against common security vulnerabilities.

Therefore, the correct options are:

Enable traceability
Apply security at the application layer
------------------
**You:**


Question 12:
Which pricing options are available when using Amazon EC2 Reserved Instances? (Select TWO.)
El Capacity upfront
I] All upfront
I] Mainly upfront
El Partial upfront
El Enterprise upfront
------------------
**ChatGPT:**


When using Amazon EC2 Reserved Instances, the following pricing options are available:

All upfront: Pay for the entire reservation term upfront and receive the highest discount compared to other options.

Partial upfront: Make a partial upfront payment and pay the remaining balance in monthly installments over the reservation term.

Therefore, the correct options are:

All upfront
Partial upfront
------------------
**You:**


El Physical security of the data center |
[:I Replacement and disposal of disk drives |
El Configuration of security groups |
[:I Patch management of operating systems |
[:I Encryption of customer data |
------------------
**ChatGPT:**


In the security pillar of the well-architected framework, the following options are recommendations:

Physical security of the data center: Implement measures to ensure the physical security of the data center where the infrastructure is hosted.

Replacement and disposal of disk drives: Establish processes for secure replacement and disposal of disk drives to prevent unauthorized access to data.

Configuration of security groups: Properly configure security groups to control inbound and outbound traffic to resources.

Patch management of operating systems: Implement regular patch management practices to keep operating systems up to date and address security vulnerabilities.

Encryption of customer data: Implement encryption mechanisms to protect customer data at rest and in transit.

Therefore, the correct options are:

Physical security of the data center
Replacement and disposal of disk drives
------------------
**You:**


Under the AWS shared responsibility model what is AWS responsible for? (Select TWO.)
------------------
**ChatGPT:**


Under the AWS shared responsibility model, AWS is responsible for the following:

Security "of" the Cloud: AWS is responsible for protecting the infrastructure that runs the cloud services, including hardware, software, and networking components. This includes measures such as data center security, network security, and infrastructure-level security.

Compliance with regulations and standards: AWS ensures that its infrastructure meets industry-specific compliance requirements and regulatory standards, such as HIPAA for healthcare data, PCI DSS for payment card data, and GDPR for personal data protection.

Therefore, the correct options are:

Security "of" the Cloud
Compliance with regulations and standards
------------------
**You:**


Question 13:
Under the AWS shared responsibility model what is AWS responsible for? (Select TWO.)
I] Physical security of the data center
I] Replacement and disposal of disk drives
I] Configuration of security groups
I] Patch management of operating systems
I] Encryption of customer data
------------------
**ChatGPT:**


Under the AWS shared responsibility model, AWS is responsible for the following:

Physical security of the data center: AWS is responsible for securing the physical infrastructure of its data centers, including access controls, monitoring, and environmental safeguards.

Replacement and disposal of disk drives: AWS is responsible for managing the replacement and disposal of disk drives used within its infrastructure to ensure data security.

Therefore, the correct options are:

Physical security of the data center
Replacement and disposal of disk drives
------------------
**You:**


Question 16:
Which service provides a way to convert video and audio files from their source format into versions
that will playback on devices like smartphones, tablets and PCs?
0 Amazon Elastic Transcoder
Q Aws Glue
0 Amazon Rekognition
0 Amazon Comprehend
------------------
**ChatGPT:**


The service that provides a way to convert video and audio files into versions that can be played back on devices like smartphones, tablets, and PCs is Amazon Elastic Transcoder.

Therefore, the correct option is:

Amazon Elastic Transcoder
------------------
**You:**


When using AWS Organizations with consolidated billing what are two valid best practices? (Select
TWO.)

I] Always enable multi-factor authentication (MFA) on the root account

|:| Always use a straightforward password on the root account

I] The paying account should be used for billing purposes only

|:| Use the paying account for deploying resources

|:| Never exceed the limit of 20 linked accounts
------------------
**ChatGPT:**


When using AWS Organizations with consolidated billing, two valid best practices are:

The paying account should be used for billing purposes only: It is recommended to designate one AWS account as the paying account and use it solely for managing billing and payment. This helps in centralizing the billing process and simplifying cost management.

Use the paying account for deploying resources: It is common practice to use the paying account for deploying resources, as it provides better visibility and control over the overall AWS usage and costs. By deploying resources from the paying account, you can easily track and manage the expenses associated with those resources.

The other options mentioned:

Always enable multi-factor authentication (MFA) on the root account: While enabling MFA is a good security practice, it is not specifically related to AWS Organizations with consolidated billing.

Always use a straightforward password on the root account: Using a straightforward password is not a recommended security practice, and it is generally advised to use strong, complex passwords.

Never exceed the limit of 20 linked accounts: AWS Organizations allows you to have more than 20 linked accounts, so this option is not a valid best practice.

Therefore, the correct options are:

The paying account should be used for billing purposes only
Use the paying account for deploying resources
------------------
**You:**


Which of the options below are recommendations in the reliability pillar of the well-architected
framework? (Select TWO.)

I:| Use ad-hoc recovery procedures

El Automatically recover from failure

|:| Scale vertically to increase aggregate system availability

[:I Attempt to accurately estimate capacity requirements

[:I Manage change in automation
------------------
**ChatGPT:**


In the reliability pillar of the well-architected framework, the following options are recommendations:

Automatically recover from failure: It is recommended to design your system in a way that allows for automatic recovery from failures. This can involve implementing mechanisms such as automated scaling, fault tolerance, and automated healing of resources.

Manage change in automation: Automating change management processes helps to reduce the risk of errors and increases the reliability of the system. By using automation tools and processes, you can ensure that changes are applied consistently and reliably across your infrastructure.

The other options mentioned:

Use ad-hoc recovery procedures: Ad-hoc recovery procedures are not recommended as they can be error-prone and lack consistency.

Scale vertically to increase aggregate system availability: Scaling vertically (increasing the size or capacity of individual resources) may improve performance but does not directly address system availability or reliability.

Attempt to accurately estimate capacity requirements: While estimating capacity requirements is important, it is not a specific recommendation in the reliability pillar of the well-architected framework.

Therefore, the correct options are:

Automatically recover from failure
Manage change in automation
------------------
**You:**


Question 19:
Which AWS support plan comes with a Technical Account Manager (TAM)?
0 Developer
0 Enterprise
------------------
**ChatGPT:**


The AWS support plan that comes with a Technical Account Manager (TAM) is the "Enterprise" support plan. The Technical Account Manager provides personalized support and acts as a single point of contact for the customer, helping them with their AWS environment, architectural guidance, and proactive assistance.
------------------
**You:**


Question 20:
Which service provides the ability to simply upload applications and have AWS handle the deployment
details of capacity provisioning, load balancing, auto-scaling, and application health monitoring?
0 Amazon EC2
Q AWS Elastic Beanstalk
0 Amazon EC2 Auto Scaling
O AWS OpsWorks
------------------
**ChatGPT:**


The service that provides the ability to simply upload applications and have AWS handle the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring is "AWS Elastic Beanstalk". AWS Elastic Beanstalk is a fully managed service that makes it easy to deploy, run, and scale applications quickly by abstracting the underlying infrastructure complexities. It allows you to focus on your application code while AWS takes care of the deployment and management tasks.
------------------
**You:**


You are concerned that you may be getting close to some of the default service limits for several AWS
services. What AWS tool can be used to display current usage and limits?

0 AWS CloudWatch

O AWS Personal Health Dashboard

O AWS Trusted Advisor

0 AWS Systems Manager
------------------
**ChatGPT:**


The AWS tool that can be used to display current usage and limits, and provide recommendations for optimizing your AWS resources, is "AWS Trusted Advisor". AWS Trusted Advisor is a service that helps you optimize your AWS infrastructure, security, and cost by providing real-time guidance. It provides checks and recommendations in various categories, including service limits, to ensure you are utilizing AWS resources efficiently and staying within the prescribed limits.
------------------
**You:**


Question 22:

You need to run a production process that will use several EC2 instances and run constantly on an
ongoing basis. The process cannot be interrupted or restarted without issue. What EC2 pricing model
would be best for this workload?

0 Reserved instances

0 Spot instances

0 On-demand instances

0 Flexible instances
------------------
**ChatGPT:**


For a production process that requires uninterrupted and continuous usage of EC2 instances, the best EC2 pricing model would be "Reserved Instances". Reserved Instances allow you to reserve capacity for a specified duration, providing a significant discount compared to On-Demand instances. Reserved Instances are well-suited for workloads that require continuous, long-term usage, such as production processes that run constantly without interruption. By reserving the capacity, you ensure that the instances will be available for your workload, and you can optimize costs by committing to a specific term and payment option.
------------------
**You:**


AWS security group have allow and deny rulea
------------------
**ChatGPT:**


Yes, AWS Security Groups allow you to define inbound and outbound rules to control traffic to and from your Amazon EC2 instances. These rules can include both allow and deny rules, depending on your requirements.

When configuring a security group, you can specify rules that allow inbound traffic from specific IP addresses or ranges, or you can allow traffic from specific security groups. These rules define the allowed sources and ports for incoming traffic.

Similarly, you can also define outbound rules to control the traffic leaving your instances. You can specify the destination IP addresses or ranges and the allowed ports or protocols for outbound connections.

The rules in a security group are evaluated in order, starting with the first rule, and the action (allow or deny) is applied based on the first rule that matches the traffic. If there is no rule that matches the traffic, the default behavior is to deny the traffic.

It's important to carefully configure your security group rules to ensure that your instances are protected while allowing the necessary traffic for your applications.
------------------
**You:**


What about an acl
------------------
**ChatGPT:**


In AWS, an Access Control List (ACL) is another layer of security that can be applied at the network level. While security groups operate at the instance level (firewall rules), ACLs operate at the subnet level (traffic control).

ACLs are stateless and provide granular control over inbound and outbound traffic by allowing or denying traffic based on rules. They can be used to control traffic between subnets or between your VPC and the Internet.

Here are a few key points about ACLs in AWS:

Subnet Level: ACLs are associated with subnets in a Virtual Private Cloud (VPC). Each subnet can have one ACL, and multiple subnets can share the same ACL.

Numbered Rules: ACLs use numbered rules to evaluate traffic. Rules are processed in order, and the first matching rule is applied. If no rule matches, a default rule is applied.

Allow and Deny Rules: Like security groups, ACLs support both allow and deny rules. You can specify rules to allow or deny traffic based on source IP addresses, destination IP addresses, ports, or protocols.

Ingress and Egress: ACLs have separate sets of rules for inbound (ingress) and outbound (egress) traffic. This allows you to have fine-grained control over the traffic entering and leaving the subnets.

Stateless: Unlike security groups, ACLs are stateless, meaning that you must explicitly allow both inbound and outbound traffic for a particular flow if you want it to be bidirectional.

Rule Evaluation: Rules in an ACL are evaluated in ascending order based on their rule number. AWS evaluates the lowest numbered rule first and continues until it finds a match.

ACLs provide an additional layer of security beyond security groups by allowing you to control traffic at the subnet level. They can be useful when you need more advanced traffic control or want to apply specific rules to a group of subnets within your VPC.
------------------
**You:**


AWS NAT
------------------
**ChatGPT:**


In AWS, NAT (Network Address Translation) is a service that allows instances in private subnets to communicate with the Internet or other AWS services while preserving their private IP addresses. NAT is commonly used in scenarios where instances in a private subnet need outbound internet access or when you want to provide access to specific AWS services.

There are two types of NAT in AWS:

NAT Gateway: NAT Gateway is a managed service provided by AWS. It allows instances in private subnets to access the internet for downloading patches, software updates, or accessing external resources. NAT Gateway provides high availability and scalability without any management overhead. It is recommended for most use cases where outbound internet access is required.

NAT Instance: NAT Instance is an EC2 instance that you can configure manually to perform network address translation. It is deployed in a public subnet and routes traffic from instances in private subnets to the internet. NAT Instances can be used in scenarios where advanced network configurations or protocols are needed, but they require manual configuration and management.

Here are some key points to know about NAT in AWS:

Inbound Traffic: By default, NAT instances and NAT Gateways do not allow inbound traffic initiated from the internet. They are designed for outbound communication from private instances.

Elastic IP: Both NAT instances and NAT Gateways require an Elastic IP (EIP) address to function. An EIP is a static public IP address that you can associate with the NAT instance or NAT Gateway.

High Availability: NAT Gateways are highly available within an Availability Zone (AZ) and can automatically failover to another AZ. They provide better availability and scalability compared to NAT Instances, which require manual configurations for high availability.

Performance: NAT Gateways offer better performance and higher bandwidth compared to NAT Instances, as they are a managed service optimized for NAT.

Cost: NAT Gateways have an hourly charge for usage and data transfer fees. NAT Instances incur EC2 instance costs along with data transfer fees. The cost considerations may vary based on your specific requirements.

NAT in AWS enables instances in private subnets to securely access the internet or other AWS services while keeping their private IP addresses hidden. It provides a vital component for building secure and scalable architectures in AWS.
------------------
**You:**


Which of the following AWS services support VPC Endpoint Gateway for a private connection from a VPC? (Select two)
------------------
**ChatGPT:**


The AWS services that support VPC Endpoint Gateway for a private connection from a VPC are as follows:

Amazon S3 (Simple Storage Service): Amazon S3 allows you to create a VPC Endpoint Gateway, which enables private connectivity from your VPC to S3 without requiring traffic to traverse the internet. This allows you to securely access S3 buckets from your VPC without exposing them to the public internet.

DynamoDB (Amazon DynamoDB): DynamoDB also supports VPC Endpoint Gateway. By creating a VPC Endpoint Gateway for DynamoDB, you can access DynamoDB tables from your VPC privately, without the need for internet gateway or NAT gateway.

These services offer VPC Endpoint Gateway functionality, allowing you to establish private connectivity from your VPC to the respective services. By utilizing VPC Endpoint Gateways, you can enhance security and network performance by eliminating the need for traffic to flow through the public internet.
------------------
**You:**


A research group wants to use EC2 instances to run a scientific computation application that has a fault tolerant architecture. The application needs high-performance hardware disks that provide fast I/O performance. As a Cloud Practitioner, which of the following storage options would you recommend as the MOST cost-effective solution?
------------------
**ChatGPT:**


As a Cloud Practitioner, for a research group wanting to run a fault-tolerant scientific computation application on EC2 instances with a focus on cost-effectiveness, I would recommend considering the Amazon Elastic Block Store (EBS) as the storage option.

Amazon EBS provides block-level storage volumes that can be attached to EC2 instances. It offers different types of EBS volumes with varying performance characteristics. For high-performance requirements, I would suggest using the following EBS volume types:

Provisioned IOPS SSD (io1): This EBS volume type is designed to deliver high I/O performance for applications with critical or demanding workloads. It allows you to specify the amount of storage capacity and the desired number of IOPS (Input/Output Operations Per Second) for your application.

General Purpose SSD (gp3): This EBS volume type provides a balance of price and performance. It offers baseline performance with the ability to burst up to higher levels for short durations. It is a cost-effective option for applications that require decent I/O performance but don't have extremely demanding workloads.

Both of these EBS volume types can provide the necessary high-performance hardware disks for the scientific computation application. However, the gp3 volume type tends to be more cost-effective compared to io1, as it offers burstable performance and lower pricing per GB.

Additionally, you can further optimize cost by choosing the appropriate volume size and IOPS level based on your workload requirements. It's recommended to analyze the application's I/O patterns and performance needs to determine the most suitable EBS volume type, size, and IOPS configuration for your specific use case.
------------------
**You:**


Which of the following AWS Support plans provide access to only core checks from the AWS Trusted Advisor Best Practice Checks? (Select two)
------------------
**ChatGPT:**


The AWS Support plans that provide access to only core checks from the AWS Trusted Advisor Best Practice Checks are as follows:

Basic Support: The Basic Support plan provides access to core checks from the AWS Trusted Advisor Best Practice Checks. This plan offers a set of general guidance and access to basic support features such as documentation, community forums, and customer service for account and billing inquiries.

Developer Support: The Developer Support plan also includes access to core checks from the AWS Trusted Advisor Best Practice Checks. In addition to the Basic Support features, Developer Support offers technical support for development and testing environments, with a faster response time compared to Basic Support.

Both the Basic Support and Developer Support plans provide access to the core checks of AWS Trusted Advisor Best Practice Checks. These checks help identify potential security, performance, and cost optimization issues in your AWS resources. However, it's important to note that advanced checks from Trusted Advisor, as well as other advanced support features, are not available with these plans and require higher-tier support plans such as Business or Enterprise Support.
------------------
**You:**


The DevOps team at an e-commerce company is trying to debug performance issues for its serverless application built using a microservices architecture. As a Cloud Practitioner, which AWS service would you recommend addressing this use-case?
------------------
**ChatGPT:**


As a Cloud Practitioner, I would recommend utilizing AWS X-Ray to address the performance issues for the serverless application built with a microservices architecture.

AWS X-Ray is a service that helps developers analyze and debug distributed applications, including serverless applications. It provides insights into the performance and behavior of individual components and the interactions between various microservices.

Here are some key features of AWS X-Ray that make it suitable for debugging performance issues in a serverless microservices application:

Distributed Tracing: AWS X-Ray allows you to trace requests as they flow through different microservices in your application. It captures information about the duration, latency, and errors at each step, giving you visibility into the performance bottlenecks and potential issues within your microservices architecture.

Service Maps: With X-Ray, you can generate service maps that visualize the connections and dependencies between your microservices. This helps you understand the overall architecture and identify any components causing performance issues or introducing latency.

Performance Analysis: X-Ray provides detailed insights into the performance of individual microservices. It helps pinpoint the specific areas where performance degradation may be occurring, allowing you to optimize and troubleshoot accordingly.

Integration with AWS Services: X-Ray integrates with various AWS services, including AWS Lambda (for serverless functions) and AWS Elastic Beanstalk (for application deployment). This enables seamless monitoring and analysis of performance for serverless applications built on these services.

By utilizing AWS X-Ray, the DevOps team can gain valuable insights into the performance of their serverless application's microservices architecture. They can identify bottlenecks, trace requests, and troubleshoot any latency issues, ultimately improving the overall performance and user experience of the e-commerce application.
------------------
**You:**


AWS Shield Advanced provides expanded DDoS attack protection for web applications running on which of the following resources? (Select two)
------------------
**ChatGPT:**


AWS Shield Advanced provides expanded DDoS (Distributed Denial of Service) attack protection for web applications running on the following resources:

Elastic Load Balancers (ELB): AWS Shield Advanced offers DDoS protection for web applications that are fronted by Elastic Load Balancers (ELB). ELB acts as a scalable and highly available load balancer, distributing traffic across multiple instances, and AWS Shield Advanced helps protect these ELBs from DDoS attacks.

Amazon CloudFront: AWS Shield Advanced also provides DDoS protection for web applications that use Amazon CloudFront as their content delivery network (CDN). CloudFront is a globally distributed CDN that caches content at edge locations, improving performance and reducing latency. Shield Advanced ensures the availability and resilience of CloudFront distributions by defending against DDoS attacks.

By utilizing AWS Shield Advanced, organizations can enhance the security of their web applications running on ELBs and CloudFront. It offers advanced DDoS protection capabilities, including real-time monitoring, automatic mitigation, and access to AWS DDoS Response Team (DRT) assistance during attacks, ensuring the reliability and availability of web applications even in the face of DDoS threats.
------------------
**You:**


Route 53?
------------------
**ChatGPT:**


I apologize for the oversight. AWS Shield Advanced also provides expanded DDoS attack protection for web applications running on Amazon Route 53.

Amazon Route 53 is a scalable and highly available domain name system (DNS) web service provided by AWS. It enables organizations to route end users to their applications by translating domain names into IP addresses.

With AWS Shield Advanced, web applications using Amazon Route 53 for DNS resolution can benefit from enhanced DDoS protection. Shield Advanced helps mitigate DDoS attacks targeting Route 53, ensuring the availability and performance of DNS services and protecting against disruptions caused by malicious traffic.

By leveraging AWS Shield Advanced with Amazon Route 53, organizations can strengthen their overall DDoS defense strategy, safeguarding the DNS infrastructure and maintaining the accessibility of their web applications.
------------------
**You:**


API gateway?
------------------
**ChatGPT:**


I apologize for the confusion. AWS Shield Advanced does not provide DDoS attack protection specifically for Amazon API Gateway.

However, Amazon API Gateway does come with its built-in DDoS protection measures. API Gateway automatically handles the majority of DDoS attacks by using managed infrastructure and implementing throttling and request rate limiting. These measures help protect API Gateway endpoints from excessive and malicious traffic.

While AWS Shield Advanced does not directly cover API Gateway, it provides comprehensive DDoS protection for other AWS services such as Elastic Load Balancers (ELB), Amazon CloudFront, and Amazon Route 53 as previously mentioned.

To enhance the security of your API Gateway endpoints, it is recommended to combine the built-in DDoS protection features of API Gateway with other AWS services such as AWS WAF (Web Application Firewall) and AWS Shield Standard for additional layers of protection against common web application threats and volumetric attacks.
------------------
**You:**


Global accelerator 
------------------
**ChatGPT:**


You are correct. AWS Global Accelerator provides DDoS protection as part of its service offering.

AWS Global Accelerator is a networking service that improves the availability and performance of applications by routing user traffic through the AWS global network infrastructure. It uses AWS edge locations to direct traffic to the nearest application endpoint, reducing latency and providing a more consistent user experience.

As part of its service, AWS Global Accelerator provides DDoS protection. It leverages the scale and global reach of the AWS network to detect and mitigate DDoS attacks, helping to ensure the availability and performance of your applications.

The DDoS protection offered by AWS Global Accelerator includes the following features:

Traffic Engineering: Global Accelerator intelligently routes traffic to the nearest healthy endpoint, distributing the load and reducing the impact of DDoS attacks on individual endpoints.

Anycast IP Addresses: Global Accelerator uses Anycast IP addresses, which are advertised across multiple AWS edge locations. This distribution of IP addresses helps absorb and mitigate DDoS traffic, improving the resilience of your applications.

AWS Shield Standard: Global Accelerator incorporates AWS Shield Standard, a built-in DDoS protection service provided by AWS. Shield Standard helps protect against common and most frequently observed DDoS attacks.

By using AWS Global Accelerator, you can benefit from its DDoS protection capabilities along with improved performance and availability for your applications, especially in scenarios where low latency and global reach are crucial.
------------------
**You:**


According to the AWS Cloud Adoption Framework (AWS CAF), what are two tasks that a company should perform when planning to migrate to the AWS Cloud and aiming to become more responsive to customer inquiries and feedback as part of their organizational transformation?
------------------
**ChatGPT:**


According to the AWS Cloud Adoption Framework (AWS CAF), when planning to migrate to the AWS Cloud and aiming to become more responsive to customer inquiries and feedback as part of an organizational transformation, there are two tasks that a company should perform:

Define Customer Engagement: The company should establish a clear understanding of how they will engage with customers in the cloud environment. This involves defining the channels and methods through which customer inquiries and feedback will be received, processed, and responded to. It may include leveraging AWS services like Amazon Simple Queue Service (SQS), Amazon Simple Notification Service (SNS), or AWS Lambda functions to manage and automate customer interactions.

Establish Feedback Loops: The company should create mechanisms to capture, analyze, and act upon customer feedback effectively. This involves implementing processes to collect customer feedback, whether it be through surveys, user forums, or other means, and integrating those feedback loops into the decision-making and product development cycles. By regularly reviewing and acting on customer feedback, the company can become more responsive to customer needs and continuously improve their products and services.

By performing these tasks, the company can enhance their customer-centric approach and leverage the capabilities of the AWS Cloud to effectively engage with customers, capture feedback, and respond quickly, enabling organizational transformation and improved responsiveness to customer inquiries and feedback.
------------------
**You:**


Organize your teams around bureaucratic design principles

Create new analytical insights with existing products and services

Organize your teams around products and value streams

Leverage legacy infrastructure for cost efficiencies

Leverage agile methods to rapidly iterate and evolve
------------------
**ChatGPT:**


When planning to migrate to the AWS Cloud and aiming to become more responsive to customer inquiries and feedback as part of an organizational transformation, the following two tasks align with the principles of the AWS Cloud Adoption Framework (AWS CAF):

Organize your teams around products and value streams: This task focuses on adopting a product-oriented approach to organizing teams. Instead of traditional siloed departments or functional areas, teams are structured around specific products or value streams. This enables cross-functional collaboration and empowers teams to take end-to-end ownership of delivering value to customers. By organizing teams in this manner, the company can improve responsiveness, agility, and the ability to align with customer needs.

Leverage agile methods to rapidly iterate and evolve: Agile methodologies, such as Scrum or Kanban, promote iterative and incremental development, fostering faster feedback loops and continuous improvement. By embracing agile methods, teams can respond more quickly to customer inquiries and feedback, adapt to changing requirements, and deliver value in shorter cycles. Agile practices encourage transparency, collaboration, and continuous learning, enabling teams to iterate on their products and services based on customer insights.

These tasks align with the AWS CAF's focus on organizational readiness and agility. By organizing teams around products and value streams and leveraging agile methods, the company can foster a customer-centric culture, enhance responsiveness, and drive continuous improvement in their cloud migration and organizational transformation journey.
------------------
**You:**


Which AWS Route 53 routing policy would you use to route traffic to multiple resources and also choose how much traffic is routed to each resource?
------------------
**ChatGPT:**


The AWS Route 53 routing policy that allows you to route traffic to multiple resources and control the distribution of traffic among them is called "Weighted Routing."

With Weighted Routing, you can assign weights (or percentages) to different resources (such as EC2 instances or load balancers) and specify how much traffic should be routed to each resource. This allows you to distribute the traffic load across multiple resources based on your desired proportions.

Here's how it works:

Assign Weights: You assign a weight to each resource, indicating the proportion of traffic you want to direct to that resource. The weights are specified as numeric values, with higher values representing a higher proportion of traffic.

DNS Resolution: When a DNS query is made, Route 53 uses the weighted distribution algorithm to route traffic based on the assigned weights. For example, if you have two resources with weights of 70 and 30, Route 53 will route 70% of the traffic to the resource with the higher weight and 30% to the resource with the lower weight.

Proportional Traffic Distribution: The weighted routing policy ensures that the distribution of traffic matches the specified proportions. This allows you to control the traffic distribution among resources and implement various deployment strategies like blue/green deployments or A/B testing.

By using the Weighted Routing policy in Route 53, you can effectively manage and distribute traffic across multiple resources while maintaining control over the proportion of traffic directed to each resource.
------------------
**You:**


Which of the following AWS Support plans provide access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software? (Select two)
------------------
**ChatGPT:**


The AWS Support plans that provide access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software are as follows:

Business Support: The Business Support plan offers access to guidance, configuration, and troubleshooting for AWS interoperability with third-party software. It provides technical support for AWS services and products, including assistance with integrating and optimizing third-party software within the AWS environment.

Enterprise Support: The Enterprise Support plan also provides access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software. It offers personalized support, architectural reviews, and hands-on guidance to help optimize the use of AWS services in conjunction with third-party software solutions.

Both the Business Support and Enterprise Support plans offer comprehensive technical support, including assistance with interoperability challenges and ensuring the smooth integration of third-party software with AWS services. These plans provide access to AWS Support engineers who can provide guidance, configuration advice, and troubleshooting assistance to address any issues related to third-party software in the AWS ecosystem.
------------------
**You:**


3:48

↑

38/65

59:23

Finish test

Question 38:

Which of the following are correct statements regarding the AWS Global Infrastructure? (Select two)

Each Availability Zone (AZ) consists of one or more discrete data centers

Each AWS Region consists of a minimum of three Availability Zones (AZ)

Each Availability Zone (AZ) consists of two or more discrete data centers

Each AWS Region consists of a minimum of two Availability Zones (AZ)

Each AWS Region consists of two or more Edge Locations
------------------
**ChatGPT:**


The correct statements regarding the AWS Global Infrastructure are:

Each Availability Zone (AZ) consists of one or more discrete data centers.
Each AWS Region consists of a minimum of three Availability Zones (AZ).

Explanation:

An Availability Zone (AZ) is a distinct location within a region, typically comprising one or more data centers with redundant power, networking, and cooling.
AWS Regions are geographical areas around the world, each consisting of multiple Availability Zones.
To ensure high availability and fault tolerance, AWS recommends a minimum of three Availability Zones within each Region.
Edge Locations, on the other hand, are part of the AWS global network infrastructure and are used for content caching and distribution purposes. They are not directly related to the structure of Availability Zones or Regions.

Therefore, the correct statements are that each Availability Zone consists of one or more discrete data centers, and each AWS Region consists of a minimum of three Availability Zones.
------------------
**You:**


Which AWS Service can be used to mitigate a Distributed Denial of Service (DDoS) attack?
------------------
**ChatGPT:**


AWS provides several services to help mitigate Distributed Denial of Service (DDoS) attacks. One of the key services specifically designed for DDoS protection is AWS Shield.

AWS Shield is a managed DDoS protection service that safeguards applications running on AWS against various types of DDoS attacks. There are two tiers of AWS Shield:

AWS Shield Standard: This is the base level of protection that is automatically provided to all AWS customers at no additional cost. It offers protection against common and most frequently observed DDoS attacks. AWS Shield Standard is built into many AWS services, including Amazon CloudFront, Elastic Load Balancing, and Amazon Route 53.

AWS Shield Advanced: This is an additional, premium service that provides more advanced DDoS protection features and greater customization options. AWS Shield Advanced offers increased protection against larger and more sophisticated DDoS attacks. It provides real-time monitoring, attack mitigation, and access to the AWS DDoS Response Team (DRT) for assistance during attacks.

Both AWS Shield Standard and AWS Shield Advanced work by automatically detecting and mitigating DDoS attacks, helping to maintain the availability of your applications and protect your infrastructure.

In addition to AWS Shield, other AWS services such as Amazon CloudFront, AWS WAF (Web Application Firewall), and AWS Global Accelerator also contribute to DDoS protection by offering features like traffic filtering, anomaly detection, and scalable edge infrastructure.

By utilizing AWS Shield, along with other complementary services, you can enhance the resilience of your applications and infrastructure against DDoS attacks in the AWS environment.
------------------
**You:**


3:49

↓

40/65

58:07

Finish test

Question 40:

The DevOps team at an IT company is moving 500 GB of data from an EC2 instance to an S3 bucket in the same region. Which of the following scenario captures the correct charges for this data transfer?

The company would be charged for both the outbound data transfer from EC2 instance as well as the inbound data transfer into the S3 bucket

The company would only be charged for the inbound data transfer into the S3 bucket

The company would not be charged for this data transfer

The company would only be charged for the outbound data transfer from EC2 instance
------------------
**ChatGPT:**


In the given scenario of moving 500 GB of data from an EC2 instance to an S3 bucket in the same region, the correct charges for this data transfer would be:

The company would be charged for both the outbound data transfer from the EC2 instance as well as the inbound data transfer into the S3 bucket.

Explanation:

AWS data transfer charges are applied for data moving across different AWS services, even within the same region.
In this case, when data is transferred from the EC2 instance to the S3 bucket, it is considered outbound data transfer from the EC2 instance and inbound data transfer into the S3 bucket.
AWS charges for both outbound and inbound data transfer separately based on the amount of data transferred.
Therefore, the company would incur charges for both the outbound data transfer from the EC2 instance and the inbound data transfer into the S3 bucket.

So, the correct answer is: The company would be charged for both the outbound data transfer from the EC2 instance as well as the inbound data transfer into the S3 bucket.
------------------
**You:**


Compared to the on-demand instance prices, what is the highest possible discount offered for spot instances?
------------------
**ChatGPT:**


The highest possible discount offered for Amazon EC2 Spot Instances compared to on-demand instance prices can vary depending on factors such as supply and demand dynamics in the Spot Instance market. However, historically, Spot Instances have been known to offer discounts of up to 90% off the on-demand prices.

Spot Instances are a cost-effective option for workloads that are flexible with regard to their start and end times. The pricing of Spot Instances is determined by the Spot market, where prices fluctuate based on supply and demand. Customers bid on the maximum price they are willing to pay for a Spot Instance, and if their bid exceeds the current Spot price, their instance will be provisioned. The Spot price is determined by AWS and fluctuates over time.

The discount offered for Spot Instances can be significantly higher than on-demand prices due to the flexible nature of Spot pricing. Spot Instances allow users to take advantage of spare EC2 capacity in the AWS infrastructure at discounted rates, making it an attractive option for cost optimization.

It's important to note that while Spot Instances can provide significant cost savings, they are subject to potential interruptions. If the Spot price exceeds the customer's bid, the instance may be terminated. Therefore, Spot Instances are best
------------------
**You:**


3:52

↓

42/65

55:02

Finish test

Question 42:

Which of the following are the advantages of cloud computing? (Select three)

Trade capital expense for variable expense

Allocate a few months of planning for your infrastructure capacity needs

Spend money on building and maintaining data centers

Trade variable expense for capital expense

Benefit from massive economies of scale

Go global in minutes and deploy applications in multiple regions around the world with just a few clicks
------------------
**ChatGPT:**


The advantages of cloud computing are as follows:

Trade capital expense for variable expense: Cloud computing allows organizations to pay for IT resources on a pay-as-you-go basis. Instead of upfront capital expenditures for hardware and infrastructure, businesses can incur variable expenses based on their actual usage. This flexibility helps in cost optimization and aligning expenses with actual needs.

Benefit from massive economies of scale: Cloud service providers, such as AWS, operate on a large scale, enabling them to achieve economies of scale. This results in lower infrastructure costs, which are passed on to customers. Organizations can benefit from this cost advantage by leveraging cloud services rather than building and maintaining their own costly infrastructure.

Go global in minutes and deploy applications in multiple regions around the world with just a few clicks: Cloud computing enables organizations to expand their reach globally quickly and easily. Cloud service providers have a global infrastructure footprint, allowing businesses to deploy applications in multiple regions with minimal effort. This provides scalability, low-latency access to customers in different geographic locations, and the ability to meet regulatory and compliance requirements in specific regions.

The options that correctly capture the advantages of cloud computing are:

Trade capital expense for variable expense
Benefit from massive economies of scale
Go global in minutes and deploy applications in multiple regions around the world with just a few clicks.
------------------
**You:**


3:53

↑

43/65

53:45

Finish test

Question 43:

A silicon valley based healthcare startup stores anonymized patient health data on Amazon S3. The CTO further wants to ensure that any sensitive data on S3 is discovered and identified to prevent any sensitive data leaks. As a Cloud Practitioner, which AWS service would you recommend addressing this use-case?

Amazon Polly

Amazon Macie

AWS Glue

AWS Secrets Manager
------------------
**ChatGPT:**


To address the use-case of discovering and identifying sensitive data stored on Amazon S3 to prevent data leaks, the recommended AWS service would be Amazon Macie.

Amazon Macie is a fully managed service that uses machine learning and pattern matching techniques to automatically discover, classify, and protect sensitive data stored in AWS. It helps organizations identify and understand sensitive data like personally identifiable information (PII), financial information, healthcare records, and more.

In the given scenario, the healthcare startup wants to ensure that any sensitive data on Amazon S3, such as patient health data, is discovered and identified to prevent any potential leaks. Amazon Macie can analyze the content of S3 objects, identify sensitive data using pre-configured or custom-defined data types, and generate alerts or take remediation actions based on policies.

By utilizing Amazon Macie, the healthcare startup can enhance their data security posture and comply with relevant regulations and privacy requirements. It provides automated data discovery and classification, reducing the risk of data exposure and helping to prevent unauthorized access or breaches of sensitive information.
------------------
**You:**


3:54

↓

44/65

53:03 Finish test

Question 44:

A company runs an application on a fleet of EC2 instances. The company wants to automate the traditional maintenance job of running timely assessments and checking for OS vulnerabilities. As a Cloud Practitioner, which service will you suggest for this use case?

Amazon Inspector

AWS Shield

Amazon Macie

Amazon GuardDuty
------------------
**ChatGPT:**


For automating timely assessments and checking for OS vulnerabilities on a fleet of EC2 instances, the recommended AWS service is Amazon Inspector.

Amazon Inspector is an automated security assessment service that helps identify security vulnerabilities and deviations from best practices in applications deployed on Amazon EC2 instances. It analyzes the network, file system, and process activity of EC2 instances to provide a comprehensive security assessment.

In the given scenario, the company wants to automate the maintenance task of running assessments and checking for OS vulnerabilities. Amazon Inspector can help achieve this by providing automated security assessments and vulnerability scanning for the EC2 instances in their fleet.

By utilizing Amazon Inspector, the company can schedule recurring assessments, receive detailed findings reports, and gain insights into potential security vulnerabilities or misconfigurations in their EC2 instances. This automation simplifies the process of identifying and addressing security issues, ensuring that the fleet of EC2 instances remains secure and protected against common vulnerabilities.
------------------
**You:**


3:55

↑

45/65

52:10

Finish test

Question 45:

Which type of cloud computing does Amazon Elastic Compute Cloud (EC2) represent?

Infrastructure as a Service (IaaS)

Network as a Service (NaaS)

Platform as a Service (PaaS)

Software as a Service (SaaS)
------------------
**ChatGPT:**


Amazon Elastic Compute Cloud (EC2) represents Infrastructure as a Service (IaaS) in the context of cloud computing.

Infrastructure as a Service (IaaS) is a cloud computing model that provides virtualized computing resources over the internet. With IaaS, users can provision and manage virtual machines (VMs) or instances, storage, networks, and other fundamental computing resources. The cloud service provider, in this case, Amazon Web Services (AWS), is responsible for the underlying infrastructure, including servers, networking, and data centers, while the user has control over the operating systems, applications, and configurations within the virtual machines.

Amazon EC2 is a core service of AWS that offers resizable compute capacity in the form of virtual machines or instances. It allows users to launch, manage, and terminate instances as needed, providing them with full control over their computing resources in the cloud. Users can choose from a variety of instance types, operating systems, and configurations to meet their specific requirements.

Therefore, Amazon EC2 is an example of Infrastructure as a Service (IaaS) within the AWS cloud computing portfolio.
------------------
**You:**


4:02

↓

46/65

45:08

Finish test

Question 46:

A big data analytics company is moving its IT infrastructure from an on-premises data center to AWS Cloud. The company has some server-bound software licenses that it wants to use on AWS. As a Cloud Practitioner, which of the following EC2 instance types would you recommend to the company?

Dedicated Host

On-Demand Instance

Dedicated Instance

Reserved Instance (RI)
------------------
**ChatGPT:**


If a big data analytics company wants to use server-bound software licenses on AWS, I would recommend using Dedicated Instances or Dedicated Hosts, depending on their specific requirements.

Dedicated Instances are EC2 instances that run on hardware dedicated to a single AWS account. They provide the benefits of EC2 instances, such as scalability and flexibility, while ensuring that the instances run on hardware exclusively dedicated to the company's use. Dedicated Instances can be launched using On-Demand pricing, allowing the company to pay for compute capacity on an as-needed basis.

Dedicated Hosts, on the other hand, are physical servers dedicated to a single AWS account. The company can have more control over the underlying host infrastructure, including the ability to bring your own licenses (BYOL) for server-bound software. By using Dedicated Hosts, the company can place EC2 instances on dedicated physical servers and leverage their existing licenses.

The choice between Dedicated Instances and Dedicated Hosts depends on factors such as license mobility requirements, cost considerations, and the level of control desired over the underlying hardware.

It's important to note that while Reserved Instances (RI) offer cost savings for long-term commitments, they are not specifically designed to address the requirement of using server-bound software licenses. RIs provide capacity reservations but do not offer the same level of dedicated hardware isolation as Dedicated Instances or Dedicated Hosts.

Therefore, for using server-bound software licenses on AWS, I would recommend either Dedicated Instances or Dedicated Hosts, depending on the specific needs and preferences of the big data analytics company.
------------------
**You:**


4:06

47/65

41:49

Finish test

Question 47:

A multi-national corporation wants to get expert professional advice on migrating to AWS and managing their applications on AWS Cloud. Which of the following entities would you recommend for this engagement?

Concierge Support Team

APN Technology Partner

AWS Trusted Advisor

APN Consulting Partner
------------------
**ChatGPT:**


For expert professional advice on migrating to AWS and managing applications on the AWS Cloud, I would recommend engaging with an APN Consulting Partner.

APN stands for Amazon Partner Network, which is a global partner program by AWS. APN Consulting Partners are professional services firms that have demonstrated expertise in helping customers design, architect, build, migrate, and manage workloads on AWS. They possess a deep understanding of AWS services and best practices and can provide guidance and support throughout the entire cloud adoption journey.

By engaging with an APN Consulting Partner, the multi-national corporation can leverage their expertise and experience to plan and execute a successful migration to AWS. These partners offer a wide range of services, including architecture design, workload assessment, cost optimization, security implementation, and ongoing management of applications on the AWS Cloud.

While AWS Trusted Advisor provides automated best practice checks and recommendations, it is not specifically focused on providing expert professional advice for migrations or application management. The Concierge Support Team primarily assists with general guidance and support related to billing and account management.

APN Technology Partners, on the other hand, are independent software vendors (ISVs) that develop and offer software solutions that are integrated with AWS services. While they can provide valuable technology solutions, they may not be the ideal choice for comprehensive migration and application management advice.

Therefore, for the engagement requiring expert professional advice on migrating to AWS and managing applications, I would recommend partnering with an APN Consulting Partner.
------------------
**You:**


4:07

48/65

41:07

Finish test

Question 48:

A company wants to improve the resiliency of its flagship application so it wants to move from its traditional database system to a managed AWS database service to support active-active configuration in both the East and West US AWS regions. The active-active configuration with cross- region support is the prime criteria for any database solution that the company considers.

Which AWS database service is the right fit for this requirement?

Amazon Relational Database Service (Amazon RDS) for MYSQL

Amazon DynamoDB with DynamoDB Accelerator

Amazon DynamoDB with global tables

Amazon Aurora with multi-master clusters
------------------
**ChatGPT:**


For achieving an active-active configuration with cross-region support, the AWS database service that would be the right fit for this requirement is Amazon Aurora with multi-master clusters.

Amazon Aurora is a relational database service offered by AWS that is compatible with MySQL and PostgreSQL. It is designed for high availability, durability, and performance. Aurora supports a multi-master replication feature that allows for read and write operations to be distributed across multiple database instances.

By utilizing Aurora's multi-master clusters, the company can set up active-active configurations in both the East and West US AWS regions. The multi-master feature enables read and write access to be distributed across multiple instances in different regions, providing resiliency and ensuring that the application remains operational even if one region faces an outage.

Amazon RDS for MySQL is a managed relational database service, but it does not offer native multi-master capabilities for active-active configurations across regions.

Amazon DynamoDB with DynamoDB Accelerator (DAX) is a fully managed NoSQL database service, but it does not provide native support for multi-master configurations across regions.

Amazon DynamoDB with global tables, on the other hand, is a suitable option for global-scale applications that require multi-region replication, but it does not provide full active-active capabilities as it focuses on eventual consistency rather than immediate consistency.

Therefore, for the company's requirement of an active-active configuration with cross-region support, the recommended AWS database service would be Amazon Aurora with multi-master clusters.
------------------
**You:**


4:07

49/65

40:24 Finish test

Question 49:

According to the AWS Shared Responsibility Model, which of the following are responsibilities of AWS? (Select two)

Creating S3 bucket policies for appropriate user access

Replacing faulty hardware of Amazon EC2 instances

Creating IAM role for accessing Amazon EC2 instances

Enabling Multi Factor Authentication on AWS accounts in your organization

Maintaining Amazon S3 data in different availability zones to keep it durable
------------------
**ChatGPT:**


According to the AWS Shared Responsibility Model, the responsibilities of AWS include:

Replacing faulty hardware of Amazon EC2 instances: AWS is responsible for the underlying infrastructure, including the physical hardware of EC2 instances. If there is a hardware failure, AWS takes care of replacing the faulty hardware to ensure the availability of the service.

Maintaining Amazon S3 data in different availability zones to keep it durable: AWS ensures the durability of data stored in Amazon S3 by automatically replicating it across multiple availability zones within a region. This redundancy helps protect against data loss in the event of hardware or facility failures.

The other options mentioned in the question are the responsibilities of the customer or user of AWS services:

Creating S3 bucket policies for appropriate user access: This is the responsibility of the customer to configure and manage access controls, including bucket policies, to control user access to S3 buckets.

Creating IAM role for accessing Amazon EC2 instances: Customers are responsible for managing IAM (Identity and Access Management) roles and policies to control access to EC2 instances.

Enabling Multi-Factor Authentication (MFA) on AWS accounts in your organization: Customers are responsible for enabling and managing MFA for their AWS accounts to provide an additional layer of security.

Therefore, the correct options based on the AWS Shared Responsibility Model are:

Replacing faulty hardware of Amazon EC2 instances (AWS responsibility)
Maintaining Amazon S3 data in different availability zones to keep it durable (AWS responsibility)
------------------
**You:**


4:08

↓

50/65

39:47 Finish test

Question 50:

Which of the following Amazon S3 storage classes takes the most time to retrieve data (also known as first byte latency)?

Amazon S3 Intelligent-Tiering

Amazon S3 Standard

Amazon S3 Glacier Deep Archive

Amazon S3 Glacier Flexible Retrieval
------------------
**ChatGPT:**


Among the given options, the Amazon S3 storage class that takes the most time to retrieve data (also known as first byte latency) is Amazon S3 Glacier Deep Archive.

Amazon S3 Glacier Deep Archive is designed for long-term archival storage of data with infrequent access. It offers the lowest cost per gigabyte but has a longer retrieval time compared to other storage classes. Retrieving data from Amazon S3 Glacier Deep Archive can take several hours, as it involves a retrieval process that needs to be initiated before the data becomes accessible.

Amazon S3 Intelligent-Tiering and Amazon S3 Standard have lower retrieval times compared to Amazon S3 Glacier Deep Archive. They provide faster access to data, with Amazon S3 Intelligent-Tiering automatically moving data between two access tiers based on usage patterns, and Amazon S3 Standard offering immediate access to data.

Amazon S3 Glacier Flexible Retrieval is a retrieval option within the Amazon S3 Glacier storage class. It allows for expedited or standard retrievals, depending on the urgency of data access requirements. Expedited retrievals offer faster access than standard retrievals but have higher costs associated with them.

Therefore, among the given options, Amazon S3 Glacier Deep Archive has the longest retrieval time (first byte latency) when compared to the other Amazon S3 storage classes.
------------------
**You:**


4:09

↓

51/65

38:58

Finish test

Question 51:

A web application stores all of its data on Amazon S3 buckets. A client has mandated that data be encrypted before sending it to Amazon S3.

Which of the following is the right technique for

encrypting data as needed by the customer?

Enable server-side encryption with Amazon S3 Managed Keys (SSE-S3)

Enable client-side encryption using AWS encryption SDK

Enable server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS)

Encryption is enabled by default for all the objects written to Amazon S3. Additional configuration is not required
------------------
**ChatGPT:**


To encrypt data as needed by the customer before sending it to Amazon S3, the right technique would be to enable client-side encryption using the AWS Encryption SDK.

Client-side encryption involves encrypting the data on the client-side before it is uploaded to Amazon S3. The AWS Encryption SDK provides a set of libraries and APIs that enable developers to easily encrypt and decrypt data using strong encryption algorithms. With client-side encryption, the customer has full control over the encryption process, including key management and encryption algorithms.

The other options mentioned in the question are related to server-side encryption options in Amazon S3:

Enable server-side encryption with Amazon S3 Managed Keys (SSE-S3): With this option, Amazon S3 manages the encryption keys used to encrypt and decrypt the data. The keys are stored and managed by AWS, providing a convenient encryption solution. However, the encryption and decryption process happens on the server-side, not the client-side.

Enable server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS): This option allows you to use AWS KMS to manage the encryption keys used by Amazon S3. With SSE-KMS, the encryption and decryption process also happens on the server-side.

Encryption is enabled by default for all the objects written to Amazon S3. Additional configuration is not required: This statement is not entirely accurate. While Amazon S3 provides default encryption options, such as SSE-S3 and SSE-KMS, they need to be explicitly enabled for each S3 bucket or object. By default, encryption is not applied to objects unless the customer enables it.

Therefore, for encrypting data as needed by the customer before sending it to Amazon S3, the recommended technique is to enable client-side encryption using the AWS Encryption SDK.
------------------
**You:**


4:10

↓

52/65

38:05 Finish test

Question 52:

Which of the following are the storage services offered by the AWS Cloud? (Select two)

Amazon Elastic File System (Amazon EFS)

Amazon Elastic Compute Cloud (Amazon EC2)

Amazon Simple Queue Service (SQS)

Amazon Simple Storage Service (Amazon S3)

Amazon Simple Notification Service (SNS)
------------------
**ChatGPT:**


The storage services offered by the AWS Cloud are:

Amazon Simple Storage Service (Amazon S3): Amazon S3 is an object storage service that provides secure, durable, and scalable storage for various types of data. It is commonly used for storing and retrieving large amounts of unstructured data, such as images, videos, documents, backups, and log files.

Amazon Elastic File System (Amazon EFS): Amazon EFS is a scalable and fully managed file storage service that supports the Network File System (NFS) protocol. It provides shared file storage that can be accessed concurrently from multiple EC2 instances, making it suitable for workloads that require shared file access.

The other options mentioned in the question are not storage services:

Amazon Elastic Compute Cloud (Amazon EC2): Amazon EC2 is a virtual server infrastructure service that provides resizable compute capacity in the cloud. It allows users to launch and manage virtual machines (EC2 instances) to run their applications.

Amazon Simple Queue Service (SQS): SQS is a fully managed message queuing service that enables decoupling and asynchronous communication between distributed components of an application. It is primarily used for building distributed systems and facilitating communication between different services.

Amazon Simple Notification Service (SNS): SNS is a fully managed messaging service that enables the publishing and delivery of messages to subscribers or endpoints. It is used for sending notifications, alerts, and other event-driven communications to various subscribers, such as email, SMS, mobile push, and more.

Therefore, the correct options for the storage services offered by the AWS Cloud are:

Amazon Simple Storage Service (Amazon S3)
Amazon Elastic File System (Amazon EFS)
------------------
**You:**


4:10

↑

53/65

37:27

Finish test

A Project Manager, working on AWS for the first time, is confused about how credits are used in AWS. There are two credits available in the manager's account. Credit one is for $100, expires July 2022, and can be used for either Amazon S3 or Amazon EC2. Credit two is for $50, expires December 2022, and can be used only for Amazon EC2. The manager's AWS account has incurred two charges: $1000 for Amazon EC2 and $500 for Amazon S3.

What will be the outcome on the overall bill once the credits are used? (Select two)

Then, credit two is applied to $500 for Amazon S3 usage

Then, credit two is applied to the

remaining $900 of Amazon EC2 usage

Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge

<

။။
------------------
**ChatGPT:**


Based on the provided information, the outcome on the overall bill once the credits are used will be:

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge.

Credit one can be used for either Amazon S3 or Amazon EC2, and since it has a higher value of $100, it will be applied to the Amazon EC2 charge of $1000. After applying credit one, the remaining balance for Amazon EC2 will be $900.

Then, credit two is applied to the remaining $900 of Amazon EC2 usage.

Credit two is specifically for Amazon EC2 and has a value of $50. Since there is a remaining balance of $900 for Amazon EC2 after applying credit one, credit two can be applied to further reduce the cost. After applying credit two, the remaining balance for Amazon EC2 will be $850.

Therefore, the correct outcomes on the overall bill once the credits are used are:

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge.
Then, credit two is applied to the remaining $900 of Amazon EC2 usage.

The other options mentioned in the question are not correct:

Then, credit two is applied to $500 for Amazon S3 usage: Credit two cannot be applied to Amazon S3 as it is specifically for Amazon EC2.
Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones: Both credits can be used in the same billing cycle if they are applicable to the respective services.
------------------
**You:**


4:10

↑

53/65

37:27

Finish test

A Project Manager, working on AWS for the first time, is confused about how credits are used in AWS. There are two credits available in the manager's account. Credit one is for $100, expires July 2022, and can be used for either Amazon S3 or Amazon EC2. Credit two is for $50, expires December 2022, and can be used only for Amazon EC2. The manager's AWS account has incurred two charges: $1000 for Amazon EC2 and $500 for Amazon S3.

What will be the outcome on the overall bill once the credits are used? (Select two)

Then, credit two is applied to $500 for Amazon S3 usage

Then, credit two is applied to the

remaining $900 of Amazon EC2 usage

Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge

<

။။
------------------
**ChatGPT:**


I apologize for the confusion. The correct outcomes on the overall bill once the credits are used are:

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge.

Credit one can be used for either Amazon S3 or Amazon EC2, and since it has a higher value of $100, it will be applied to the Amazon EC2 charge of $1000. After applying credit one, the remaining balance for Amazon EC2 will be $900.

Only one credit can be used in one billing cycle, and the customer has a choice to choose from the available ones.

Since credit two is specifically for Amazon EC2 and cannot be used for Amazon S3, it cannot be applied to the $500 charge for Amazon S3 usage. Therefore, credit two will not be used in this case.

Therefore, the correct outcomes on the overall bill once the credits are used are:

Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge.
Only one credit can be used in one billing cycle, and the customer has a choice to choose from the available ones.

Apologies for the previous incorrect response.
------------------
**You:**


4:13

↓

54/65

34:33

Finish test

Question 54:

Which of the following AWS services has encryption enabled by default?

Amazon Elastic File System (Amazon EFS)

Amazon Elastic Block Store (Amazon EBS)

AWS CloudTrail Logs

Amazon Relational Database Service (Amazon RDS)
------------------
**ChatGPT:**


The correct answer is:

AWS CloudTrail Logs

AWS CloudTrail Logs have encryption enabled by default. CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. When you create a trail in CloudTrail, the log files generated by the service are automatically encrypted using AWS Key Management Service (AWS KMS). This ensures that the log files are encrypted at rest and provides an additional layer of security for your audit trail.

The other services mentioned, namely Amazon Elastic File System (Amazon EFS), Amazon Elastic Block Store (Amazon EBS), and Amazon Relational Database Service (Amazon RDS), do not have encryption enabled by default. Encryption for these services needs to be explicitly configured by the user.
------------------
**You:**


4:14

55/65

33:44 Finish test

Question 55:

A company needs a storage solution for a project wherein the data is accessed less frequently but needs rapid access when required. Which S3 storage class is the MOST cost-effective for the given use- case?

Amazon S3 Glacier (S3 Glacier)

Amazon S3 Standard-Infrequent Access (S3 Standard-IA)

Amazon S3 Standard

Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)
------------------
**ChatGPT:**


The correct answer is:

Amazon S3 Glacier (S3 Glacier)

Amazon S3 Glacier is the most cost-effective storage class for data that is accessed less frequently but needs rapid access when required. It is designed for long-term data archival and offers the lowest storage costs among the S3 storage classes.

Amazon S3 Standard-Infrequent Access (S3 Standard-IA) is also suitable for data that is accessed less frequently, but it has higher storage costs compared to Amazon S3 Glacier. S3 Standard-IA is designed for data that requires less frequent access but still needs quick retrieval when requested.

Amazon S3 Standard and Amazon S3 Intelligent-Tiering are not the most cost-effective options for the given use-case. Amazon S3 Standard is the default storage class and provides immediate access to data but has higher costs. Amazon S3 Intelligent-Tiering automatically moves data between different storage tiers based on its access patterns, which may not be the most cost-effective option for data accessed less frequently.

Therefore, for the given use-case, Amazon S3 Glacier is the most cost-effective storage class.
------------------
**You:**


4:51

↑

57/65

27:31

Finish test

Question 57:

A startup wants to provision an EC2 instance for the lowest possible cost for a long-term duration but needs to make sure that the instance would never be interrupted. As a Cloud Practitioner, which of the following options would you recommend?

EC2 Spot Instance

EC2 Dedicated Host

EC2 On-Demand Instance

EC2 Reserved Instance (RI)
------------------
**ChatGPT:**


The correct answer is:

EC2 Reserved Instance (RI)

For the lowest possible cost for a long-term duration and the assurance of uninterrupted usage, EC2 Reserved Instances (RI) would be the recommended option. Reserved Instances provide a significant discount compared to On-Demand Instances in exchange for a commitment of usage over a specified term, typically one or three years. By reserving capacity in advance, the startup can optimize costs and ensure the instance availability without the risk of interruption.

EC2 Spot Instances offer the lowest cost among the EC2 instance types but come with the risk of interruption. Spot Instances are ideal for workloads that are flexible and can handle interruptions, such as batch processing, data analysis, or CI/CD pipelines.

EC2 Dedicated Hosts are physical servers dedicated to a specific AWS account and provide visibility and control over the underlying infrastructure but are typically more expensive compared to other instance types.

EC2 On-Demand Instances provide instances with no upfront commitments or long-term contracts, allowing for flexibility but at a higher cost compared to Reserved Instances.

Considering the requirement for the lowest cost, long-term duration, and the assurance of no interruption, EC2 Reserved Instances would be the recommended option.
------------------
**You:**


4:52

↓

58/65

26:18 Finish test

Question 58:

Which of the following entities applies patches to the underlying OS for Amazon Aurora?

The AWS customer by using AWS Systems Manager

The AWS customer by SSHing on the instances

The AWS Support after receiving a request from the customer

The AWS Product Team automatically
------------------
**ChatGPT:**


The correct answer is:

The AWS Product Team automatically

For Amazon Aurora, the AWS Product Team takes care of applying patches to the underlying operating system. Amazon Aurora is a managed database service provided by AWS, and the AWS Product Team is responsible for managing and maintaining the underlying infrastructure, including patching the operating system.

As a customer, you do not need to manually apply patches or SSH into the instances to perform OS-level maintenance. AWS handles these tasks transparently, allowing you to focus on managing your database and applications without worrying about the underlying infrastructure.

AWS Systems Manager is a service that provides centralized visibility and control over your AWS resources, including managing and automating operational tasks. While you can use AWS Systems Manager for various management tasks, such as automation, patch management, and configuration management, it is not necessary to use it specifically for patching the underlying OS of Amazon Aurora.

AWS Support assists customers with technical issues and provides guidance and recommendations. However, they do not directly apply patches to the underlying OS of Amazon Aurora.

In summary, the AWS Product Team automatically applies patches to the underlying OS for Amazon Aurora, relieving customers of that responsibility.
------------------
**You:**


4:53

↓

59/65

25:48

Finish test

Question 59:

A company wants to identify the optimal AWS resource configuration for its workloads so that the company can reduce costs and increase workload performance. Which of the following services can be used to meet this requirement?

AWS Cost Explorer

AWS Compute Optimizer

AWS Systems Manager

AWS Budgets
------------------
**ChatGPT:**


The correct answer is:

AWS Compute Optimizer

AWS Compute Optimizer is the service that can be used to identify the optimal AWS resource configuration for workloads. It uses machine learning algorithms to analyze historical resource utilization and provide recommendations for right-sizing your AWS resources.

By leveraging AWS Compute Optimizer, you can gain insights into your workload's performance and resource utilization patterns. The service will provide specific recommendations on which EC2 instance types and sizes, as well as Auto Scaling group configurations, are best suited for your workloads. This helps you optimize your resources to achieve a balance between cost and performance.

AWS Cost Explorer, on the other hand, is a service that provides comprehensive cost visibility and analysis of your AWS spending. It helps you understand your cost patterns, identify cost drivers, and forecast future costs. While AWS Cost Explorer provides valuable cost-related insights, it does not specifically focus on workload performance optimization.

AWS Systems Manager is a management service that provides a unified interface for managing your AWS resources. It offers features such as automation, parameter management, patch management, and more. While AWS Systems Manager can help with managing resources, it does not provide specific recommendations for optimizing resource configurations.

AWS Budgets is a service that allows you to set and track cost and usage budgets for your AWS accounts. It helps you monitor your spending and receive alerts when your costs or usage exceed predefined thresholds. While AWS Budgets helps with cost management and monitoring, it does not provide recommendations for optimizing resource configurations.

In summary, for identifying the optimal AWS resource configuration for workloads, AWS Compute Optimizer is the recommended service to use.
------------------
**You:**


4:53

↓

60/65

25:09 Finish test

Question 60:

Which of the following is the MOST cost-effective option to purchase an EC2 Reserved Instance (RI)?

No upfront payment option with standard 1-year term

All upfront payment option with the standard 1-year term

No upfront payment option with standard

3-years term

Partial upfront payment option with standard 3-years term
------------------
**ChatGPT:**


The correct answer is:

All upfront payment option with the standard 1-year term

When purchasing an EC2 Reserved Instance (RI), the most cost-effective option is to choose the all upfront payment option with the standard 1-year term.

Reserved Instances offer significant cost savings compared to On-Demand instances, as they provide a capacity reservation and a discounted hourly rate for the instance usage. RI pricing options include No upfront, Partial upfront, and All upfront payment options, and the term can be either 1 year or 3 years.

Among these options, choosing the all upfront payment option with the standard 1-year term provides the highest cost savings. By making an upfront payment for the entire 1-year term, you receive the maximum discount on the hourly rate for the instance.

The no upfront payment option with the standard 1-year term would have a slightly higher hourly rate compared to the all upfront payment option. The no upfront payment option with the standard 3-year term and the partial upfront payment option with the standard 3-year term offer longer-term commitments but do not provide the same level of cost savings as the all upfront payment option with the standard 1-year term.

It's important to note that the cost-effectiveness of the RI options may vary depending on your specific usage patterns and requirements. It's recommended to analyze your usage and financial goals before selecting the appropriate RI payment option.
------------------
**You:**


4:55

↓

61/65

23:27 Finish test

Question 61:

Which AWS services can be used to facilitate

organizational change management, part of the Reliability pillar of AWS Well-Architected Framework? (Select three)

Amazon Inspector

Amazon GuardDuty

AWS Config

Amazon CloudWatch

AWS CloudTrail

AWS Trusted Advisor
------------------
**ChatGPT:**


The correct answers are:

AWS Config
AWS CloudTrail
AWS Trusted Advisor

These three AWS services can be used to facilitate organizational change management as part of the Reliability pillar of the AWS Well-Architected Framework.

AWS Config: AWS Config provides a detailed inventory of your AWS resources and tracks changes to resource configurations over time. It helps you assess, audit, and evaluate the configurations of your resources, making it easier to manage and track changes in your environment.

AWS CloudTrail: AWS CloudTrail provides a record of actions taken by a user, role, or AWS service in your AWS account. It captures API calls and logs important information about those calls, such as the identity of the caller, the time of the call, and the request parameters. This helps with auditing, compliance, and troubleshooting.

AWS Trusted Advisor: AWS Trusted Advisor is an automated tool that analyzes your AWS environment and provides recommendations for optimizing security, performance, cost, and fault tolerance. It helps identify potential issues and suggests improvements to enhance the reliability of your infrastructure.

Amazon Inspector, Amazon GuardDuty, and Amazon CloudWatch are valuable services but are not specifically focused on facilitating organizational change management as described in the question.
------------------
**You:**


4:56

↓

62/65

22:37 Finish test

Question 62:

An IT company is planning to migrate from an on- premises environment to AWS Cloud. Which of the following expense areas would result in cost savings when the company moves to AWS Cloud? (Select two)

Project manager salary

Data center physical security expenditure

Data center hardware infrastructure expenditure

SaaS application license fee

Developer salary
------------------
**ChatGPT:**


The correct answers are:

Data center hardware infrastructure expenditure
SaaS application license fee

When an IT company migrates from an on-premises environment to the AWS Cloud, it can realize cost savings in several areas. However, in the context of the given options, the two expense areas that would result in cost savings are:

Data center hardware infrastructure expenditure: By migrating to the AWS Cloud, the company no longer needs to invest in and maintain its own hardware infrastructure. AWS provides a scalable and flexible infrastructure as a service (IaaS) model, allowing companies to leverage cloud resources instead of purchasing and maintaining physical hardware.

SaaS application license fee: In the AWS Cloud, companies can take advantage of various software as a service (SaaS) offerings provided by AWS and its partners. These SaaS applications are typically available on a pay-as-you-go or subscription basis, eliminating the need for upfront license fees or long-term commitments associated with traditional software licensing.

While there may be other areas where cost savings can be achieved, such as reduced maintenance and management costs, the given options specifically highlight the areas where cost savings are most likely to be realized.
------------------
**You:**


4:57

↓

63/65

21:53

Finish test

Question 63:

What are the advantages that AWS Cloud offers over a traditional on-premises IT infrastructure? (Select two)

Trade capital expense for variable expense

Eliminate guessing on your infrastructure capacity needs

Increase speed and agility by keeping servers and other required resources ready before time in your data centers

Make a capacity decision before deploying an application, to reduce costs

Provide lower latency to applications by maintaining servers on-premises
------------------
**ChatGPT:**


The correct answers are:

Trade capital expense for variable expense
Eliminate guessing on your infrastructure capacity needs

The advantages that AWS Cloud offers over a traditional on-premises IT infrastructure include:

Trade capital expense for variable expense: With AWS Cloud, companies can pay for the resources and services they use on a variable expense model, rather than making upfront investments in hardware and infrastructure. This allows for greater flexibility and cost optimization, as companies can scale their resources up or down based on their actual needs.

Eliminate guessing on your infrastructure capacity needs: AWS Cloud provides the ability to scale resources on-demand, allowing companies to dynamically adjust their infrastructure capacity based on changing requirements. This eliminates the need for upfront capacity planning and reduces the risk of overprovisioning or underutilization of resources.

The other options mentioned in the question ("Increase speed and agility by keeping servers and other required resources ready before time in your data centers" and "Make a capacity decision before deploying an application, to reduce costs") are not advantages of AWS Cloud over a traditional on-premises IT infrastructure. These statements do not accurately represent the benefits of using AWS Cloud and may lead to confusion. Additionally, the statement "Provide lower latency to applications by maintaining servers on-premises" is incorrect, as AWS Cloud's global infrastructure and content delivery network (CDN) can provide low-latency access to applications and content from multiple locations around the world.
------------------
**You:**


5:00

↓

64/65

18:33

Finish test

Question 64:

An e-commerce company has deployed an RDS database in a single Availability Zone (AZ). The engineering team wants to ensure that in case of an AZ outage, the database should continue working on the same endpoint without any manual administrative intervention. Which of the following solutions can address this use-case?

Configure the database in RDS read replica mode with automatic failover to the standby

Deploy the database via AWS Elastic Beanstalk

Provision the database via AWS CloudFormation

Configure the database in RDS Multi-AZ deployment with automatic failover to the standby
------------------
**ChatGPT:**


The solution that can address the use-case described is:

Configure the database in RDS Multi-AZ deployment with automatic failover to the standby.

By configuring the RDS database in a Multi-AZ deployment, AWS automatically provisions and maintains a synchronous standby replica of the database in a different Availability Zone (AZ). In the event of an AZ outage, AWS automatically fails over to the standby replica, promoting it to the primary database instance. This failover process is handled by AWS without the need for manual administrative intervention. By using Multi-AZ deployment with automatic failover, the e-commerce company can ensure high availability and continuity of their database operations even in the event of an AZ outage.

The other options mentioned in the question ("Configure the database in RDS read replica mode with automatic failover to the standby" and "Deploy the database via AWS Elastic Beanstalk" and "Provision the database via AWS CloudFormation") do not specifically address the requirement of maintaining the database on the same endpoint without manual intervention during an AZ outage. RDS read replicas, AWS Elastic Beanstalk, and AWS CloudFormation have other purposes and functionalities, but they do not provide the same level of automated failover and high availability as the Multi-AZ deployment with automatic failover option.
------------------
**You:**


5:01

↑

65/65

17:56 Finish test

Question 65:

Which of the following AWS services can be used to connect a company's on-premises environment to a VPC without using the public internet?

Internet Gateway

AWS Direct Connect

VPC Endpoint

AWS Site-to-Site VPN
------------------
**ChatGPT:**


The AWS service that can be used to connect a company's on-premises environment to a Virtual Private Cloud (VPC) without using the public internet is:

AWS Direct Connect

AWS Direct Connect establishes a dedicated network connection between an on-premises data center and an AWS Direct Connect location. This dedicated connection bypasses the public internet, providing a more reliable and consistent network experience. With AWS Direct Connect, you can establish private connectivity between your on-premises environment and your VPC, allowing you to access AWS resources securely and directly.

The other options mentioned in the question ("Internet Gateway," "VPC Endpoint," and "AWS Site-to-Site VPN") have different purposes:

An Internet Gateway is used to connect a VPC to the internet, allowing communication between resources in the VPC and the public internet.
A VPC Endpoint enables private connectivity between a VPC and other AWS services without traversing the internet. However, it does not establish connectivity with an on-premises environment.
AWS Site-to-Site VPN is used to create an encrypted tunnel between an on-premises network and an AWS VPC over the public internet, providing secure communication.
------------------
**You:**


5:06

↓

1/65

1:29:58

Finish test

Question 1:

Which tool will help you review your workloads against current AWS best practices for cost optimization, security, and performance improvement and then obtain advice to architect them better?

Amazon CloudWatch

AWS Cost Explorer

AWS Trusted Advisor

Amazon Inspector
------------------
**ChatGPT:**


The tool that will help you review your workloads against current AWS best practices for cost optimization, security, and performance improvement and provide advice to architect them better is:

AWS Trusted Advisor

AWS Trusted Advisor is a service that provides real-time guidance to help you optimize your AWS resources, improve security and performance, and reduce costs. It evaluates your AWS environment based on AWS best practices and provides recommendations across various categories, including cost optimization, security, performance, and fault tolerance. By using AWS Trusted Advisor, you can identify areas for improvement and implement changes to optimize your workloads based on industry best practices.
------------------
**You:**


5:07

↓

2/65

1:29:02

Finish test

Question 2:

Which of the following options can be used to access and manage all AWS services (Select three)?

AWS Software Development Kit (SDK)

AWS Management Console

AWS Systems Manager

AWS Secrets Manager

Amazon API Gateway

AWS Command Line Interface (AWS CLI)
------------------
**ChatGPT:**


The options that can be used to access and manage all AWS services are:

AWS Management Console: The AWS Management Console is a web-based interface that allows you to access and manage all of your AWS services. It provides a graphical user interface (GUI) to interact with various AWS resources, configure settings, and monitor your applications.

AWS Command Line Interface (AWS CLI): The AWS CLI is a command-line tool that allows you to interact with AWS services through the command line. It provides a set of commands for managing AWS resources, automating tasks, and scripting. The AWS CLI is available for Windows, macOS, and Linux.

AWS Software Development Kit (SDK): The AWS SDKs are software development kits that provide libraries, code samples, and documentation for various programming languages. The SDKs allow you to programmatically access and manage AWS services in your applications. AWS SDKs are available for popular programming languages such as Java, Python, .NET, and more.

Note: While AWS Systems Manager and AWS Secrets Manager are powerful services for managing and securing your AWS resources, they are not directly used to access and manage all AWS services like the three options mentioned above.
------------------
**You:**


5:08

↓

3/65

1:28:20

Finish test

Question 3:

The engineering team at an IT company wants to monitor the CPU utilization for its fleet of Amazon Elastic Compute Cloud (Amazon EC2) instances and send an email to the administrator if the utilization exceeds 80%. As a Cloud Practitioner, which AWS services would you recommend to build this solution? (Select two)

Amazon Simple Notification Service (SNS)

Amazon CloudWatch

Amazon Simple Queue Service (SOS)

AWS Lambda

AWS CloudTrail
------------------
**ChatGPT:**


To build the solution for monitoring CPU utilization of Amazon EC2 instances and sending an email notification if the utilization exceeds 80%, the recommended AWS services are:

Amazon CloudWatch: Amazon CloudWatch is a monitoring and observability service provided by AWS. It allows you to collect and track metrics, logs, and events from various AWS resources, including Amazon EC2 instances. You can configure CloudWatch to collect CPU utilization metrics for the EC2 instances and set up alarms to trigger actions when certain thresholds are met, such as when the CPU utilization exceeds 80%.

Amazon Simple Notification Service (SNS): Amazon SNS is a fully managed messaging service that enables you to send notifications to various endpoints, including email, SMS, mobile push, and more. Once you have configured the CloudWatch alarm to trigger when CPU utilization exceeds 80%, you can configure an SNS topic as the action for the alarm. When the alarm is triggered, an email notification can be sent to the administrator via SNS.

Note: AWS Lambda and AWS CloudTrail are not directly related to building this specific solution. AWS Lambda is a serverless compute service used for running code in response to events, and AWS CloudTrail is a service for auditing and monitoring API calls made within your AWS account.
------------------
**You:**


5:09

↓

4/65

1:27:12

Finish test

Question 4:

Which of the following are examples of Horizontal Scalability (aka Elasticity)? (Select two)

Modify an EC2 instance type from t2.nano to u-12tb1.metal

Elastic Load Balancing (ELB)

Read Replicas in Amazon Relational Database Service (Amazon RDS)

Modify a Database instance to higher CPU and RAM

Add a bigger CPU to a computer
------------------
**ChatGPT:**


The examples of Horizontal Scalability, also known as Elasticity, are:

Elastic Load Balancing (ELB): Elastic Load Balancing is a service provided by AWS that automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, and IP addresses. It helps in achieving horizontal scalability by allowing you to add or remove instances based on the demand, thus scaling the application horizontally.

Read Replicas in Amazon RDS: Amazon RDS provides a managed database service, and it allows you to create read replicas of your primary database. Read replicas are copies of the primary database that can handle read traffic, thereby distributing the load and improving performance. By adding read replicas, you can horizontally scale the read capacity of your database system.

Note: The other options mentioned, such as modifying an EC2 instance type, modifying a database instance to higher CPU and RAM, and adding a bigger CPU to a computer, are related to vertical scalability (scaling up), where you increase the resources of a single instance to handle more load.
------------------
**You:**


5:11

↑

5/65

1:25:35

Finish test

Question 5:

Which AWS service can be used to store, manage, and deploy Docker container images?

AWS Lambda

Amazon Elastic Container Registry (Amazon ECR)

Amazon Elastic Container Service (Amazon ECS)

Amazon Elastic Compute Cloud (Amazon

EC2)
------------------
**ChatGPT:**


The AWS service that can be used to store, manage, and deploy Docker container images is Amazon Elastic Container Registry (Amazon ECR). Amazon ECR is a fully managed container registry service that makes it easy to store, manage, and deploy Docker container images. It provides a secure and scalable repository for storing Docker images, allowing you to easily share and distribute container images within your organization or with other AWS accounts. Amazon ECR integrates seamlessly with other AWS services like Amazon ECS (Elastic Container Service) and AWS Fargate, making it a convenient choice for container image management in the AWS ecosystem.
------------------
**You:**


5:12

↓

6/65

1:24:29

Finish test

Question 6:

A company's flagship application runs on a fleet of Amazon Elastic Compute Cloud (Amazon EC2) instances. As per the new policies, the system administrators are looking for the best way to provide secure shell access to Amazon Elastic Compute Cloud (Amazon EC2) instances without opening new ports or using public IP addresses.

Which tool/service will help you achieve this requirement?

AWS Systems Manager Session Manager

Amazon Inspector

Amazon Elastic Compute Cloud (Amazon EC2) Instance Connect

Amazon Route 53
------------------
**ChatGPT:**


The tool/service that will help achieve the requirement of providing secure shell access to Amazon EC2 instances without opening new ports or using public IP addresses is AWS Systems Manager Session Manager.

AWS Systems Manager Session Manager is a fully managed service that allows you to establish secure shell (SSH) connections to your Amazon EC2 instances directly from the AWS Management Console, without the need for bastion hosts, open ports, or public IP addresses. It provides a secure and auditable method for accessing your instances using the AWS Systems Manager console or the AWS CLI. With Session Manager, you can centrally manage access permissions, log session data, and control the level of access to your instances. It eliminates the need to manage SSH keys and simplifies the process of accessing your EC2 instances securely.
------------------
**You:**


5:13

↓

7/65

1:23:35

Finish test

Question 7:

What is the primary benefit of deploying an Amazon RDS Multi-AZ database with one standby?

Amazon RDS Multi-AZ reduces database usage costs

Amazon RDS Multi-AZ improves database performance for read-heavy workloads

Amazon RDS Multi-AZ protects the database from a regional failure

Amazon RDS Multi-AZ enhances database availability
------------------
**ChatGPT:**


The primary benefit of deploying an Amazon RDS Multi-AZ database with one standby is that it enhances database availability.

When you deploy an Amazon RDS Multi-AZ database, a standby replica is automatically created in a different Availability Zone (AZ) within the same AWS Region. The standby replica synchronously replicates data from the primary database instance. In the event of a planned or unplanned outage affecting the primary instance or its AZ, Amazon RDS automatically fails over to the standby replica, promoting it as the new primary instance.

By deploying a Multi-AZ database, you improve the availability of your database because in the event of a failure of the primary instance or its AZ, Amazon RDS automatically switches to the standby replica, minimizing downtime and providing continuous availability of your database. This enhances the reliability and resilience of your application by ensuring that the database remains accessible even during infrastructure failures or maintenance activities.
------------------
**You:**


5:13

↓

8/65

1:22:50

Finish test

Question 8:

Due to regulatory and compliance reasons, an organization is supposed to use a hardware device for any data encryption operations in the cloud. Which AWS service can be used to meet this compliance requirement?

AWS Trusted Advisor

AWS Key Management Service (AWS KMS)

AWS CloudHSM

AWS Secrets Manager
------------------
**ChatGPT:**


To meet the compliance requirement of using a hardware device for data encryption operations in the cloud, the organization can utilize AWS CloudHSM (Hardware Security Module).

AWS CloudHSM is a service that provides dedicated hardware security modules in the AWS Cloud. It enables you to generate and use encryption keys securely within the hardware modules. CloudHSMs are tamper-resistant devices that provide secure key storage and cryptographic operations. They help organizations meet regulatory and compliance requirements that mandate the use of hardware-based key management and encryption.

By using AWS CloudHSM, the organization can have a dedicated hardware device for encryption operations, ensuring the desired level of security and compliance. The sensitive data can be encrypted and decrypted using the keys stored in the CloudHSM, providing an additional layer of protection and meeting regulatory requirements.
------------------
**You:**


5:14

9/65

1:21:59

Finish test

Question 9:

Which of the following statements are true about AWS Lambda? (Select two)

AWS Lambda allows you to orchestrate and manage Docker containers to facilitate complex containerized applications on AWS

AWS Lambda lets you run code without provisioning or managing servers

You pay for the compute time you consume for AWS Lambda

AWS Lambda allows you to install databases on the underlying serverless Operating System

AWS Lambda provides access to the underlying operating system to control its behavior through code
------------------
**ChatGPT:**


The correct statements about AWS Lambda are:

AWS Lambda lets you run code without provisioning or managing servers. With Lambda, you can focus on writing and uploading your code, and AWS takes care of the underlying infrastructure, automatically scaling and managing the compute resources required to run your code.

You pay for the compute time you consume for AWS Lambda. AWS Lambda follows a pay-per-use pricing model where you are billed based on the number of requests and the duration of your code execution. You are not charged for idle time or when your code is not running.

The incorrect statements are:

AWS Lambda allows you to orchestrate and manage Docker containers to facilitate complex containerized applications on AWS. This statement is incorrect. While AWS provides services like Amazon Elastic Container Service (ECS) and AWS Fargate for managing Docker containers, Lambda itself is a serverless compute service and does not directly orchestrate or manage Docker containers.

AWS Lambda allows you to install databases on the underlying serverless Operating System. This statement is incorrect. AWS Lambda is primarily focused on running stateless code functions and does not provide direct access to the underlying operating system or support for installing and managing databases. For databases, AWS offers services like Amazon RDS, Amazon DynamoDB, and others.
------------------
**You:**


5:15

↓

10/65

1:21:03

Finish test

Question 10:

Which of the following AWS services is essential for implementing security of resources in AWS Cloud?

AWS Identity and Access Management (IAM)

AWS Shield

Amazon CloudWatch

AWS Web Application Firewall (AWS WAF)
------------------
**ChatGPT:**


The correct answer is: AWS Identity and Access Management (IAM).

AWS Identity and Access Management (IAM) is an essential service for implementing security of resources in AWS Cloud. IAM enables you to manage user identities and their access to AWS resources. With IAM, you can create and manage IAM users, groups, and roles, and define fine-grained permissions to control access to AWS services and resources.

While AWS Shield, Amazon CloudWatch, and AWS Web Application Firewall (WAF) are important services for enhancing security in AWS, they focus on specific aspects of security:

AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that helps safeguard web applications running on AWS.
Amazon CloudWatch is a monitoring service that collects and tracks metrics, logs, and events from various AWS resources, providing visibility into the operational health and performance of your infrastructure.
AWS Web Application Firewall (WAF) is a web application firewall that helps protect web applications from common web exploits and attacks.

However, when it comes to implementing security for resources in AWS, AWS Identity and Access Management (IAM) plays a fundamental role in managing user access and permissions.
------------------
**You:**


5:16

↓

11/65

1:20:23

Finish test

Question 11:

Which AWS service can be used to provision resources to run big data workloads on Hadoop clusters?

AWS Batch

Amazon EMR

AWS Step Functions

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


The correct answer is: Amazon EMR.

Amazon EMR (Elastic MapReduce) is the AWS service that can be used to provision resources to run big data workloads on Hadoop clusters. Amazon EMR simplifies the process of setting up, managing, and scaling Hadoop clusters by providing a managed platform that includes popular frameworks like Apache Hadoop, Apache Spark, and Presto.

With Amazon EMR, you can easily launch clusters of EC2 instances preconfigured with the necessary software for running big data applications. It handles the provisioning and management of the underlying infrastructure, allowing you to focus on analyzing and processing your data.

AWS Batch is a different service that is focused on running batch computing workloads, which may or may not be specific to big data processing.

AWS Step Functions is a serverless workflow orchestration service that helps you coordinate multiple AWS services to build complex applications or workflows.

Amazon Elastic Compute Cloud (Amazon EC2) is a foundational AWS service that provides resizable compute capacity in the cloud, but it is not specifically designed for provisioning resources to run big data workloads on Hadoop clusters.
------------------
**You:**


5:17

↓

12/65

1:19:28

| Finish test

Question 12:

A data analytics company stores its data on Amazon Simple Storage Service (Amazon S3) and wants to do SQL based analysis on this data with minimum effort. As a Cloud Practitioner, which of the following AWS services will you suggest for this use case?

Amazon Athena

Amazon Aurora

Amazon DynamoDB

Amazon Redshift
------------------
**ChatGPT:**


For the given use case of performing SQL-based analysis on data stored in Amazon S3 with minimum effort, the recommended AWS service is Amazon Athena.

Amazon Athena is an interactive query service that allows you to analyze data directly from Amazon S3 using standard SQL queries. It does not require any infrastructure setup or data loading as it directly integrates with the data stored in S3. You can simply define a schema for your data using Athena, and then run SQL queries to extract insights and perform analysis on the data.

Amazon Aurora is a MySQL and PostgreSQL compatible relational database service. While it is suitable for running SQL-based analysis, it is typically used for transactional workloads and may involve more setup and management overhead compared to Amazon Athena for analyzing data stored in S3.

Amazon DynamoDB is a fully managed NoSQL database service and may not be the best choice for performing SQL-based analysis. It is optimized for low-latency, high-scale applications, and its query capabilities are focused on NoSQL operations rather than traditional SQL queries.

Amazon Redshift is a fully managed data warehousing service that is specifically designed for analytics and reporting. It is a powerful solution for running SQL-based analysis on large datasets, but it requires data to be loaded into the Redshift cluster before analysis. In this case, since the data is already stored in Amazon S3, using Amazon Athena would be a more convenient and efficient choice.

Therefore, for the given use case, the recommended AWS service is Amazon Athena.
------------------
**You:**


5:18

↓

13/65

1:18:30

Finish test

Question 13:

Multi-AZ deployment is an example of which of the

following?

High Availability

Scale out

Scale up

Performance Efficiency
------------------
**ChatGPT:**


Multi-AZ deployment is an example of High Availability.

High Availability refers to the ability of a system or service to remain operational and accessible even in the event of component failures or disruptions. In the case of Amazon Web Services (AWS), Multi-AZ deployment is a feature available for certain services, such as Amazon RDS (Relational Database Service) and Amazon Elasticache, that provides automatic replication of resources across multiple Availability Zones (AZs).

In a Multi-AZ deployment, the primary resource is replicated to a standby resource in a different AZ. This standby resource can quickly take over if the primary resource becomes unavailable due to a failure or planned maintenance. This redundancy ensures that the service remains highly available and minimizes downtime.

Therefore, Multi-AZ deployment is an example of High Availability in AWS.
------------------
**You:**


5:18

↓

14/65

1:18:04

Finish test

Question 14:

Which Amazon Route 53 routing policy would you use to improve the performance for your customers by routing the requests to the AWS endpoint that provides the fastest experience?

Weighted routing

Failover routing

Latency-based routing

Simple routing
------------------
**ChatGPT:**


The Amazon Route 53 routing policy that you would use to improve the performance for your customers by routing requests to the AWS endpoint that provides the fastest experience is Latency-based routing.

Latency-based routing allows you to route traffic based on the lowest network latency to provide the best user experience. With this routing policy, Route 53 measures the latency between the end user and each available endpoint and directs the traffic to the endpoint with the lowest latency.

By using latency-based routing, you can ensure that your customers are directed to the AWS endpoint that can provide the fastest response time based on their geographical location. This helps to minimize latency and improve the overall performance of your application or service.

Therefore, the correct answer is Latency-based routing.
------------------
**You:**


5:19

↓

15/65

1:17:35

Finish test

Question 15:

A company wants a fully managed, flexible, and scalable file storage system, with low latency access, for its Windows-based applications. Which AWS service is the right choice for the company?

Amazon Elastic File System (Amazon EFS)

Amazon Elastic Block Storage (Amazon EBS)

Amazon FSX for Windows File Server

Amazon FSX for Lustre
------------------
**ChatGPT:**


The right choice for a fully managed, flexible, and scalable file storage system with low latency access for Windows-based applications in AWS would be Amazon FSx for Windows File Server.

Amazon FSx for Windows File Server is a fully managed native Windows file system that is built on Windows Server and integrated with other AWS services. It provides shared file storage that is accessible from multiple Amazon EC2 instances and supports the SMB protocol, making it suitable for Windows-based applications.

With Amazon FSx for Windows File Server, you can achieve low latency access to your file data, as it uses SSD storage and is optimized for high performance. It also offers features such as automatic backups, data deduplication, and integration with AWS Directory Service for managing user access and authentication.

Therefore, the correct answer is Amazon FSx for Windows File Server.
------------------
**You:**


5:20

↓

16/65

1:16:31

Finish test

Question 16:

Which of the following use-cases is NOT supported by Amazon Rekognition?

Detect text in a photo

Quickly resize photos to create thumbnails

Identify person in a photo

Label objects in a photo
------------------
**ChatGPT:**


The use-case that is NOT supported by Amazon Rekognition is "Quickly resize photos to create thumbnails."

Amazon Rekognition is a deep learning-based image and video analysis service provided by AWS. It offers a wide range of capabilities for image and video analysis, including object and scene detection, facial analysis, text detection, and celebrity recognition. However, resizing photos to create thumbnails is not a supported feature of Amazon Rekognition.

To resize photos and create thumbnails, you would typically use image processing libraries or services specifically designed for that purpose, such as AWS Lambda with image processing libraries or Amazon S3 image resizing capabilities.

Therefore, the correct answer is "Quickly resize photos to create thumbnails."
------------------
**You:**


5:20

17/65

1:15:58 Finish test

Which of the following statements are correct about the AWS root user account? (Select two)

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies

Root user credentials should only be shared with managers requiring administrative responsibilities to complete their jobs

Root user access credentials are the email address and password used to create the AWS account

Root user account password cannot be changed once it is set

It is highly recommended to enable Multi- Factor Authentication (MFA) for root user account
------------------
**ChatGPT:**


The correct statements about the AWS root user account are:

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies.
It is highly recommended to enable Multi-Factor Authentication (MFA) for the root user account.

Explanation:

When you create an AWS account, the email address and password used during the account creation process become the root user access credentials. The root user has full administrative privileges by default, including access to all AWS resources and services. However, it is recommended to avoid using the root user account for everyday tasks and instead create individual IAM users with appropriate permissions.

It is crucial to secure the root user account since it has full control over the AWS account. One way to enhance security is by enabling Multi-Factor Authentication (MFA) for the root user. MFA adds an extra layer of protection by requiring an additional verification method, such as a one-time password generated by a virtual or hardware MFA device, in addition to the password.

Therefore, the correct statements are:

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies.
It is highly recommended to enable Multi-Factor Authentication (MFA) for the root user account.
------------------
**You:**


5:21

↓

18/65

1:15:13

Finish test

Question 18:

An online gaming company wants to block users from certain geographies from accessing its content. Which AWS service can be used to accomplish this task?

AWS Shield

Amazon CloudWatch

Security group

AWS Web Application Firewall (AWS WAF)
------------------
**ChatGPT:**


To block users from certain geographies from accessing its content, the online gaming company can use AWS WAF (Web Application Firewall).

AWS WAF is a web application firewall that helps protect web applications from common web exploits. It allows you to define customizable rules to filter and block specific traffic based on various criteria, including geographic location. By configuring AWS WAF with geolocation-based rules, the company can block access to its content from specific geographies.

Therefore, the correct answer is:

AWS Web Application Firewall (AWS WAF)
------------------
**You:**


5:22

↓

19/65

1:14:37

Finish test

Question 19:

A retail company has multiple AWS accounts for each of its departments. Which of the following AWS services can be used to set up consolidated billing and a single payment method for these AWS accounts?

AWS Budgets

AWS Organizations

AWS Secrets Manager

AWS Cost Explorer
------------------
**ChatGPT:**


To set up consolidated billing and a single payment method for multiple AWS accounts, the retail company can use AWS Organizations.

AWS Organizations is a service that enables the central management of multiple AWS accounts. It allows you to create an organization that can contain multiple accounts, and provides features such as consolidated billing, fine-grained access control, and centralized policy management. With AWS Organizations, you can consolidate the billing for all the accounts in your organization, making it easier to manage and track costs.

Therefore, the correct answer is:

AWS Organizations
------------------
**You:**


5:23

↑

20/65

1:13:37

Finish test

Question 20:

An organization has a complex IT architecture involving a lot of system dependencies and it wants to track the history of changes to each resource. Which AWS service will help the organization track the history of configuration changes for all the resources?

AWS CloudFormation

AWS Config

AWS Service Catalog

AWS CloudTrail
------------------
**ChatGPT:**


To track the history of configuration changes for all resources in an organization's complex IT architecture, the appropriate AWS service is AWS Config.

AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources over time. It keeps track of the configuration changes and provides a detailed view of the configuration history, including who made the changes, when they were made, and what the changes were. AWS Config also allows you to set up rules and notifications to ensure compliance and detect any configuration drift.

Therefore, the correct answer is:

AWS Config
------------------
**You:**


5:24

↑

21/65

1:12:37

Finish test

Question 21:

As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?

Customer Data

Identity and Access Management

Server-side Encryption (SSE)

Edge Location Management
------------------
**ChatGPT:**


According to the AWS Shared Responsibility Model, AWS takes responsibility for the security and compliance of the underlying infrastructure and services, while the customer is responsible for certain aspects related to their usage of AWS services.

Out of the options provided, "Server-side Encryption (SSE)" is the responsibility of AWS from a security and compliance point of view. AWS ensures the implementation and management of server-side encryption for its services. This means that AWS is responsible for encrypting the data at rest within its services, providing mechanisms for key management, and ensuring compliance with relevant security standards.

The other options, "Customer Data," "Identity and Access Management," and "Edge Location Management," are the responsibilities of the customer.

Therefore, the correct answer is:

Server-side Encryption (SSE)
------------------
**You:**


5:25

↑

22/65

1:11:56

Finish test

Question 22:

Which AWS compute service provides the EASIEST way to access resizable compute capacity in the cloud with support for per-second billing and access to the underlying OS?

Amazon Elastic Container Service (Amazon ECS)

Amazon Elastic Compute Cloud (Amazon EC2)

Amazon Lightsail

AWS Lambda
------------------
**ChatGPT:**


The AWS compute service that provides the easiest way to access resizable compute capacity in the cloud, with support for per-second billing and access to the underlying operating system (OS), is Amazon Elastic Compute Cloud (Amazon EC2).

Amazon EC2 offers virtual servers in the cloud, allowing users to choose from various instance types with different compute, memory, storage, and networking capabilities. It provides flexibility and control over the underlying infrastructure, including the choice of operating system, configuration, and management of the instances.

With per-second billing, users are billed for the exact number of seconds that their instances are running, providing cost savings for short-lived workloads. Additionally, users have administrative access to the underlying OS, allowing them to configure and manage the instances as needed.

Therefore, the correct answer is:

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**You:**


5:26

↑

23/65

1:10:49

Finish test

Question 23:

An IT company wants to run a log backup process every Monday at 2 AM. The usual runtime of the process is 5 minutes. As a Cloud Practitioner, which AWS services would you recommend to build a serverless solution for this use-case? (Select two)

Amazon Elastic Compute Cloud (Amazon EC2)

Amazon CloudWatch

AWS Lambda

AWS Systems Manager

AWS Step Function
------------------
**ChatGPT:**


As a Cloud Practitioner, I would recommend using the following AWS services to build a serverless solution for the specified use case:

AWS Lambda: AWS Lambda allows you to run code without provisioning or managing servers. You can create a Lambda function that contains the log backup process and schedule it to run at the desired time using AWS CloudWatch Events. Lambda functions are event-driven, so you can configure them to execute on a schedule, such as every Monday at 2 AM.

Amazon CloudWatch: Amazon CloudWatch is a monitoring and observability service that can be used to schedule and trigger AWS Lambda functions. You can create a CloudWatch Events rule that triggers the Lambda function at the specified time and day. CloudWatch Events provides a cron expression syntax that allows you to define the schedule for recurring events.

By using AWS Lambda and Amazon CloudWatch together, you can build a serverless solution to run the log backup process every Monday at 2 AM without the need to provision or manage servers.

Therefore, the correct answers are:

AWS Lambda
Amazon CloudWatch
------------------
**You:**


5:27

24/65

1:09:42

Finish test

Question 24:

Which AWS technology/service helps you to scale your resources to match supply with demand while still keeping your cloud solution cost-effective?

AWS Cost Explorer

AWS Auto Scaling

O AWS OpsWorks

AWS CloudFormation
------------------
**ChatGPT:**


The AWS technology/service that helps you scale your resources to match supply with demand while keeping your cloud solution cost-effective is AWS Auto Scaling.

AWS Auto Scaling allows you to automatically adjust the number of Amazon EC2 instances in your application based on predefined conditions. It helps you maintain optimal performance and cost efficiency by scaling resources up or down as needed. You can define scaling policies that are based on metrics such as CPU utilization, network traffic, or custom metrics, and Auto Scaling will automatically add or remove instances to meet the desired capacity.

By using AWS Auto Scaling, you can ensure that your application can handle varying levels of traffic and workload without overprovisioning resources, thus optimizing costs.

Therefore, the correct answer is:

AWS Auto Scaling
------------------
**You:**


5:27

24/65

1:09:42

Finish test

Question 24:

Which AWS technology/service helps you to scale your resources to match supply with demand while still keeping your cloud solution cost-effective?

AWS Cost Explorer

AWS Auto Scaling

O AWS OpsWorks

AWS CloudFormation
------------------
**ChatGPT:**


The AWS technology/service that helps you scale your resources to match supply with demand while keeping your cloud solution cost-effective is AWS Auto Scaling.

AWS Auto Scaling allows you to automatically adjust the number of Amazon EC2 instances in your application based on predefined conditions. It helps you maintain optimal performance and cost efficiency by scaling resources up or down as needed. You can define scaling policies that are based on metrics such as CPU utilization, network traffic, or custom metrics, and Auto Scaling will automatically add or remove instances to meet the desired capacity.

By using AWS Auto Scaling, you can ensure that your application can handle varying levels of traffic and workload without overprovisioning resources, thus optimizing costs.

Therefore, the correct answer is:

AWS Auto Scaling
------------------
**You:**


5:27

25/65

1:09:09

Finish test

Question 25:

Which AWS service would you use to send alerts

when the costs for your AWS account exceed your budgeted amount?

AWS Pricing Calculator

AWS Organizations

AWS Budgets

AWS Cost Explorer
------------------
**ChatGPT:**


The AWS service you would use to send alerts when the costs for your AWS account exceed your budgeted amount is AWS Budgets.

AWS Budgets allows you to set custom budget thresholds for your AWS costs and usage. You can specify a budgeted amount and define the desired time period for the budget. When the actual costs exceed the budgeted amount, AWS Budgets can send alerts to specified recipients via email or Amazon Simple Notification Service (SNS).

By using AWS Budgets, you can closely monitor your AWS spending and receive timely notifications when your costs exceed the defined budget, enabling you to take necessary actions to control your expenses.

Therefore, the correct answer is:

AWS Budgets
------------------
**You:**


5:29

↑

26/65

1:07:59

Finish test

Question 26:

AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Elastic File System (Amazon EFS)

Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions

AWS Lambda functions, Amazon Simple Storage Service (Amazon S3)

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EC2 Auto Scaling groups

Amazon Elastic File System (Amazon EFS), AWS Lambda functions
------------------
**ChatGPT:**


AWS Compute Optimizer delivers recommendations for the following AWS resources:

Amazon Elastic Compute Cloud (Amazon EC2) instances
Amazon EC2 Auto Scaling groups

AWS Compute Optimizer analyzes the configuration and utilization of these resources to provide recommendations for optimizing their performance and cost-efficiency. It uses machine learning algorithms to analyze historical resource utilization patterns and compare them to AWS's best practices to identify areas for improvement.

Therefore, the correct answer is:

Amazon Elastic Compute Cloud (Amazon EC2) instances
Amazon EC2 Auto Scaling groups
------------------
**You:**


5:30

↑

27/65

1:06:48

| Finish test

Question 27:

Which of the following AWS services can be used to prevent Distributed Denial-of-Service (DDoS) attack? (Select three)

AWS Web Application Firewall (AWS WAF)

AWS Trusted Advisor

Amazon Inspector

AWS Shield

Amazon CloudFront with Amazon Route 53

AWS CloudHSM
------------------
**ChatGPT:**


The following AWS services can be used to prevent Distributed Denial-of-Service (DDoS) attacks:

AWS Web Application Firewall (AWS WAF): AWS WAF helps protect web applications from common web exploits and DDoS attacks by allowing you to define customizable security rules that control access to your applications.

AWS Shield: AWS Shield is a managed Distributed Denial-of-Service (DDoS) protection service that safeguards applications running on AWS against the most common and frequently observed DDoS attack patterns.

Amazon CloudFront with Amazon Route 53: Amazon CloudFront is a content delivery network (CDN) service that can be used to improve the performance and availability of web applications. It includes DDoS protection capabilities. Amazon Route 53 is a scalable domain name system (DNS) web service that can be used in conjunction with CloudFront to provide DDoS protection and load balancing.

Therefore, the correct answer is:

AWS Web Application Firewall (AWS WAF)
AWS Shield
Amazon CloudFront with Amazon Route 53
------------------
**You:**


10:24

5G

↓

28/65

1:04:15

Finish test

Question 28:

An organization is planning to move its infrastructure from the on-premises datacenter to AWS Cloud. As a Cloud Practioner, which options would you recommend so that the organization can identify the right AWS services to build solutions on AWS Cloud (Select two)?

AWS Partner Network (APN)

AWS Organizations

AWS CloudTrail

AWS Service Catalog

Amazon CloudWatch
------------------
**ChatGPT:**


As a Cloud Practitioner, I would recommend the following options for the organization to identify the right AWS services to build solutions on AWS Cloud:

AWS Partner Network (APN): The AWS Partner Network provides access to a vast ecosystem of AWS partners who can offer expertise and guidance in selecting and implementing the right AWS services for specific use cases. They can help with solution architecture, best practices, and implementation support.

AWS Service Catalog: AWS Service Catalog allows organizations to create and manage curated catalogs of approved AWS services that are pre-configured with recommended settings and configurations. It helps in standardizing the selection and provisioning of AWS services within an organization, ensuring compliance and best practices.

Therefore, the correct options are:

AWS Partner Network (APN)
AWS Service Catalog
------------------
**You:**


10:24

5G

↓

29/65

1:03:26

Finish test

Question 29:

Which characteristic of Cloud Computing imparts the ability to acquire resources as you need and release when you no longer need them?

Reliability

Resiliency

Durability

Elasticity
------------------
**ChatGPT:**


The characteristic of Cloud Computing that imparts the ability to acquire resources as you need and release them when you no longer need them is Elasticity. Elasticity allows users to scale their resource usage up or down based on demand, enabling efficient resource allocation and cost optimization. It provides the flexibility to quickly and easily add or remove resources as required, ensuring that you only pay for the resources you actually use.
------------------
**You:**


10:26

5G

↓

30/65

1:01:32

Finish test

Question 30:

Which AWS service should be used when you want to run container applications, but want to avoid the operational overhead of scaling, patching, securing, and managing servers?

Amazon Elastic Container Service (Amazon ECS) - Fargate launch type

Amazon Elastic Container Service

(Amazon ECS) - EC2 launch type

AWS Lambda

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


The AWS service that should be used when you want to run container applications without the operational overhead of scaling, patching, securing, and managing servers is Amazon Elastic Container Service (Amazon ECS) - Fargate launch type. With Amazon ECS using the Fargate launch type, you can focus on running and managing your containers without the need to provision or manage the underlying infrastructure. Fargate handles the scaling, patching, and management of the underlying infrastructure, allowing you to run containers in a serverless manner.
------------------
**You:**


10:27

5G

↓

31/65

1:01:02

Finish test

Question 31:

Which of the following statement is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?

Both inbound data transfer and outbound data transfer are charged

Only outbound data transfer is charged

Only inbound data transfer is charged

Neither inbound nor outbound data transfer are charged
------------------
**ChatGPT:**


The correct statement regarding the AWS pricing policy for data transfer charges into or out of an AWS Region is:

Both inbound data transfer and outbound data transfer are charged.

AWS charges for both inbound and outbound data transfer when data is transferred between your resources in an AWS Region and the internet or between AWS Regions. The pricing varies based on the amount of data transferred and the transfer type (e.g., data transfer between EC2 instances and the internet, or between AWS services within the same Region).
------------------
**You:**


10:28

5G

↓

32/65

59:54

Finish test

Question 32:

A developer has written a simple web application in PHP and he wants to just upload his code to AWS Cloud and have AWS handle the deployment automatically but still wants access to the underlying operating system for further enhancements. As a Cloud Practioner, which of the following AWS services would you recommend for this use-case?

AWS CloudFormation

AWS Elastic Beanstalk

Amazon Elastic Container Service (Amazon ECS)

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


For the given use case, as a Cloud Practitioner, I would recommend using AWS Elastic Beanstalk.

AWS Elastic Beanstalk is a fully managed service that makes it easy to deploy and run applications in multiple languages, including PHP. It abstracts away the underlying infrastructure and handles the deployment and scaling automatically based on the application's needs. With Elastic Beanstalk, the developer can simply upload their code and AWS will handle the deployment, including provisioning the necessary resources such as EC2 instances and load balancers.

Elastic Beanstalk also provides access to the underlying operating system if further enhancements or customization are required. It allows you to customize and configure the underlying infrastructure, including setting environment variables, scaling options, and more. This gives the developer the flexibility to make OS-level changes while still benefiting from the managed deployment and scaling capabilities provided by Elastic Beanstalk.
------------------
**You:**


10:29

5G

↓

33/65

59:15

Finish test

Question 33:

An organization deploys its IT infrastructure in a combination of its on-premises data center along with AWS Cloud. How would you categorize this deployment model?

Cloud deployment

Mixed deployment

Private deployment

Hybrid deployment
------------------
**ChatGPT:**


The deployment model described, where an organization deploys its IT infrastructure in a combination of its on-premises data center and AWS Cloud, is categorized as a hybrid deployment.

In a hybrid deployment model, an organization leverages both on-premises infrastructure and cloud services to meet its IT needs. This allows for a combination of resources, applications, and services to be hosted both in the organization's own data center and in the cloud. The hybrid deployment model offers flexibility and enables organizations to leverage the benefits of both on-premises infrastructure and cloud services, while also maintaining control over certain resources and data that may need to remain on-premises due to specific requirements or regulations.

In this scenario, the organization can utilize AWS Cloud services for certain workloads, while keeping other workloads on-premises in their own data center. The hybrid deployment model allows for seamless integration and communication between the on-premises infrastructure and the cloud, enabling organizations to leverage the scalability, agility, and cost-efficiency of the cloud while also leveraging their existing investments in on-premises infrastructure.
------------------
**You:**


10:30

5G

↓

34/65

58:28

Finish test

Question 34:

A fleet of Amazon EC2 instances spread across different Availability Zones (AZ) needs to access, edit and share file-based data stored centrally on a system. As a Cloud Practitioner, which AWS service would you recommend for this use-case?

Amazon Simple Storage Service (Amazon S3)

Amazon Elastic Block Store (Amazon

EBS)

Amazon Elastic File System (Amazon EFS)

EC2 Instance Store
------------------
**ChatGPT:**


For the given use case, where a fleet of Amazon EC2 instances spread across different Availability Zones (AZ) needs to access, edit, and share file-based data stored centrally on a system, the recommended AWS service would be Amazon Elastic File System (Amazon EFS).

Amazon EFS provides a scalable and fully managed file storage service that is designed to be highly available and durable. It offers a file system that can be mounted on multiple EC2 instances concurrently, allowing them to access and share the same data. It is well-suited for scenarios where multiple instances need to collaborate and share file-based data.

Key features of Amazon EFS include:

Elastic Scalability: Amazon EFS automatically scales storage capacity as per demand, so you don't need to worry about managing storage limits or performance.

Multi-AZ Durability: Data stored in Amazon EFS is automatically replicated across multiple Availability Zones, providing high durability and availability.

Shared Access: Multiple EC2 instances across different AZs can simultaneously access and modify files within the same Amazon EFS file system.

Compatibility: Amazon EFS supports the Network File System version 4 (NFSv4) protocol, which is compatible with most Linux-based applications and EC2 instances.

By using Amazon EFS, the fleet of EC2 instances can access and share the centrally stored file-based data, allowing for collaboration and efficient data management across multiple instances and Availability Zones.
------------------
**You:**


10:31

5G

↑

35/65

57:23

Finish test

Question 35:

Which AWS service publishes up-to-the-minute information on the general status and availability of all AWS services in all the Regions of AWS Cloud?

Amazon CloudWatch

AWS CloudFormation

AWS Health Dashboard - service health

AWS Health Dashboard - Your account

health
------------------
**ChatGPT:**


The AWS service that publishes up-to-the-minute information on the general status and availability of all AWS services in all the Regions of AWS Cloud is AWS Health Dashboard - service health.

The AWS Health Dashboard provides real-time visibility into the status of AWS services. It offers information on service disruptions, outages, and other events that may affect the availability and performance of AWS services. The dashboard provides a centralized view of the health of various AWS services across different regions.

By monitoring the AWS Health Dashboard - service health, users can stay informed about any ongoing issues or disruptions in AWS services and take necessary actions to mitigate the impact on their applications or infrastructure. It helps users stay updated on the overall health and availability of AWS services and plan their operations accordingly.
------------------
**You:**


10:31

5G

↑

36/65

56:47

Finish test

Question 36:

Which of the following AWS services are global in scope? (Select two)

Amazon Simple Storage Service (Amazon S3)

Amazon Relational Database Service (Amazon RDS)

AWS Identity and Access Management (AWS IAM)

Amazon CloudFront

Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


The two AWS services that are global in scope are:

AWS Identity and Access Management (AWS IAM): AWS IAM is a global service that enables you to manage access to your AWS resources. It allows you to create and manage users, groups, and roles to control who can access your AWS resources and what actions they can perform.

Amazon CloudFront: Amazon CloudFront is a global content delivery network (CDN) service that delivers static and dynamic web content, including images, videos, and application data, to end-users with low latency and high transfer speeds. CloudFront has edge locations distributed worldwide, making it a global service.

Both AWS IAM and Amazon CloudFront operate across multiple AWS Regions and are designed to provide global functionality and scalability.
------------------
**You:**


10:32

5G

↑

37/65

56:08

Finish test

Which of the following is the correct statement regarding the AWS Storage services?

Amazon Simple Storage Service (Amazon S3) is block based storage, Amazon Elastic Block Store (Amazon EBS) is object based storage and Amazon Elastic File System (Amazon EFS) is file based storage

Amazon Simple Storage Service (Amazon S3) is object based storage, Amazon Elastic Block Store (Amazon EBS) is block based storage and Amazon Elastic File System (Amazon EFS) is file based storage

Amazon Simple Storage Service (Amazon S3) is file based storage, Amazon Elastic Block Store (Amazon EBS) is block based storage and Amazon Elastic File System (Amazon EFS) is object based storage

Amazon Simple Storage Service (Amazon S3) is object based storage, Amazon Elastic Block Store (Amazon EBS) is file based storage and Amazon Elastic File System (Amazon EFS) is block based storage
------------------
**ChatGPT:**


The correct statement regarding the AWS Storage services is:

Amazon Simple Storage Service (Amazon S3) is object-based storage, Amazon Elastic Block Store (Amazon EBS) is block-based storage, and Amazon Elastic File System (Amazon EFS) is file-based storage.

Amazon Simple Storage Service (Amazon S3) is a scalable object storage service that allows you to store and retrieve data, such as files and documents, in the form of objects. It provides durability, high availability, and supports various storage classes for different use cases.

Amazon Elastic Block Store (Amazon EBS) is a block-level storage service that provides persistent block storage volumes for use with Amazon EC2 instances. It is designed for applications that require low-latency, high-performance storage, and provides features like snapshotting and replication.

Amazon Elastic File System (Amazon EFS) is a file storage service that provides scalable and fully managed file systems for use with Amazon EC2 instances. It allows multiple instances to access the same file system concurrently and provides features like automatic scaling and high availability.

Therefore, the correct statement is that Amazon S3 is object-based storage, Amazon EBS is block-based storage, and Amazon EFS is file-based storage.
------------------
**You:**


10:33

5G

↓

38/65

55:09 Finish test

Question 38:

A customer has created a VPC and a subnet within AWS Cloud. Which of the following statements is correct?

A subnet spans all of the Availability Zones (AZ) in the Region whereas an Amazon Virtual Private Cloud (Amazon VPC) spans only one Availability Zone (AZ) in the Region

Both the Amazon Virtual Private Cloud (Amazon VPC) and the subnet span only one Availability Zone (AZ) in the Region

Both the Amazon Virtual Private Cloud (Amazon VPC) and the subnet span all of the Availability Zones (AZ) in the Region

An Amazon Virtual Private Cloud (Amazon VPC) spans all of the Availability Zones (AZ) in the Region whereas a subnet spans only one Availability Zone (AZ) in the Region
------------------
**ChatGPT:**


The correct statement regarding a customer creating a VPC and a subnet within AWS Cloud is:

An Amazon Virtual Private Cloud (Amazon VPC) spans all of the Availability Zones (AZ) in the Region, whereas a subnet spans only one Availability Zone (AZ) in the Region.

An Amazon Virtual Private Cloud (Amazon VPC) is a logically isolated section of the AWS Cloud where you can launch AWS resources. It can span multiple Availability Zones within a Region, allowing you to distribute your resources across multiple data centers for high availability and fault tolerance.

A subnet, on the other hand, is a range of IP addresses in your VPC. It is a subdivision of a VPC and is associated with a specific Availability Zone. Each subnet resides in a single Availability Zone and can span multiple Availability Zones if you create subnets in each one.

Therefore, the correct statement is that an Amazon VPC spans all of the Availability Zones (AZ) in the Region, whereas a subnet spans only one Availability Zone (AZ) in the Region.
------------------
**You:**


10:34

↓

39/65

54:19

Finish test

Question 39:

According to the AWS Shared Responsibility Model, which of the following are responsibilities of the customer for Amazon RDS?

Applying patches to the Amazon Relational Database Service (Amazon RDS) database

Database encryption

Managing the underlying server hardware on which Amazon Relational Database Service (Amazon RDS) runs

Applying patches to the underlying OS
------------------
**ChatGPT:**


According to the AWS Shared Responsibility Model, the following are responsibilities of the customer for Amazon RDS:

Applying patches to the underlying OS: The customer is responsible for applying patches to the underlying operating system of the Amazon RDS instances. This includes installing security updates and patches provided by the operating system vendor.

Database encryption: The customer is responsible for managing and configuring encryption of their data in Amazon RDS. This includes enabling and managing encryption at rest and encryption in transit for the database.

On the other hand, the following responsibility is not the customer's responsibility for Amazon RDS:

Applying patches to the Amazon RDS database: AWS takes care of applying patches to the Amazon RDS database engine. AWS manages the maintenance and patching of the database engine to ensure it remains up-to-date and secure.

As for the responsibility of managing the underlying server hardware on which Amazon RDS runs, it is the responsibility of AWS, not the customer.

Therefore, the correct options are:

Applying patches to the underlying OS
Database encryption
------------------
**You:**


10:36

↓

40/65

52:18

Finish test

Question 40:

A startup is looking for 24x7 phone based technical support for its AWS account. Which of the following is the MOST cost-effective AWS support plan for this use-case?

AWS Enterprise On-Ramp Support

AWS Business Support

AWS Enterprise Support

AWS Developer Support
------------------
**ChatGPT:**


For the given use case of a startup looking for 24x7 phone-based technical support, the most cost-effective AWS support plan would be AWS Business Support.

AWS Business Support provides 24x7 access to customer service and technical support via email, chat, and phone. It offers a broad range of support for AWS services and includes general guidance, best practices, and assistance with service-specific inquiries. It is designed to meet the needs of businesses at a lower cost compared to higher-tier support plans.

AWS Enterprise On-Ramp Support is a limited-time plan available for new AWS customers that provides guidance and support during the initial onboarding and migration phase.

AWS Enterprise Support is a comprehensive support plan designed for enterprise customers with mission-critical workloads. It offers a higher level of support, including a Technical Account Manager (TAM) and architectural guidance, but it may be more costly for a startup.

AWS Developer Support is a plan designed for individual developers or small teams and provides technical support during business hours. It may not offer the level of coverage required for 24x7 phone-based support.

Therefore, for a startup seeking cost-effective 24x7 phone-based technical support, AWS Business Support would be the most suitable option.
------------------
**You:**


10:37

↑

41/65

51:31

Finish test

Question 41:

A social media company wants to protect its web application from common web exploits such as SQL injection and cross-site scripting. Which of the following AWS services can be used to address this use-case?

Amazon Inspector

AWS Web Application Firewall (AWS WAF)

AWS CloudWatch

Amazon GuardDuty
------------------
**ChatGPT:**


To protect a web application from common web exploits such as SQL injection and cross-site scripting, the appropriate AWS service to use is AWS Web Application Firewall (AWS WAF).

AWS WAF helps protect web applications from common attack patterns by allowing you to create rules that control the traffic to your application. It enables you to define customizable web security rules to filter out malicious traffic and block common attack patterns. With AWS WAF, you can mitigate SQL injection, cross-site scripting, and other web-based attacks.

Amazon Inspector is a security assessment service that helps identify vulnerabilities and security issues in your application deployments. While it can provide insights into potential security weaknesses, it does not specifically focus on protecting against web exploits like SQL injection or cross-site scripting.

AWS CloudWatch is a monitoring and observability service that collects and tracks metrics, logs, and events. While it can help detect unusual behavior and provide insights into your application's performance, it is not specifically designed for protecting against web exploits.

Amazon GuardDuty is a threat detection service that analyzes data sources across AWS accounts and services to identify potential malicious activity. While it can help detect and alert on various types of threats, it does not provide specific protection against web exploits.

Therefore, the most appropriate AWS service to address the use-case of protecting a web application from common web exploits is AWS Web Application Firewall (AWS WAF).
------------------
**You:**


10:37

↑

42/65

50:46

Finish test

Question 42:

Which Amazon Elastic Compute Cloud (Amazon EC2) pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that instance would not be interrupted?

Dedicated Host

On-demand Instance

Spot Instance

Reserved Instance (RI)
------------------
**ChatGPT:**


The most cost-effective and flexible pricing model for Amazon Elastic Compute Cloud (Amazon EC2) instances, without a long-term commitment or upfront payment, is the Spot Instance pricing model.

Spot Instances allow you to bid on spare EC2 instances' capacity, which can result in significant cost savings compared to On-Demand or Reserved Instances. With Spot Instances, you specify the maximum price you are willing to pay per hour, and if the current Spot price is below your bid price, your instance will run. However, it's important to note that the availability of Spot Instances is subject to fluctuation based on supply and demand. If the Spot price exceeds your bid price, your instance may be interrupted and terminated.

While Spot Instances offer great cost savings, they are not suitable for applications that require continuous, uninterrupted availability. If your instance is terminated due to changes in Spot prices, you may need to handle the interruption gracefully or have mechanisms in place to recover and continue processing.

Dedicated Hosts provide you with dedicated physical servers for your EC2 instances, but they are not the most cost-effective option, as they involve additional costs for the dedicated hardware.

On-Demand Instances provide you with instances that are billed per hour or per second, with no upfront commitment. They offer flexibility but are generally more expensive compared to Spot Instances or Reserved Instances.

Reserved Instances (RI) allow you to make a capacity reservation for a specific instance type in a specific region. They require a commitment for a term of 1 or 3 years, offering discounted pricing compared to On-Demand Instances. However, they do involve upfront payments and are not as flexible as Spot Instances.

Therefore, for a cost-effective and flexible pricing model with no long-term commitment or upfront payment, the most suitable option is the Spot Instance pricing model.
------------------
**You:**


10:38

↓

43/65

50:07 Finish test

Question 43:

Which of the following solutions can you use to connect your on-premises network with AWS Cloud (Select two)?

Amazon Route 53

AWS Virtual Private Network (VPN)

Amazon Virtual Private Cloud (Amazon VPC)

AWS Direct Connect

Internet Gateway
------------------
**ChatGPT:**


To connect your on-premises network with AWS Cloud, you can use the following solutions:

AWS Virtual Private Network (VPN): AWS VPN allows you to establish a secure and encrypted connection between your on-premises network and your Amazon Virtual Private Cloud (Amazon VPC). It uses the Internet as the transport medium and provides secure access to your resources in the AWS Cloud.

AWS Direct Connect: AWS Direct Connect enables you to establish a dedicated network connection between your on-premises network and AWS. With Direct Connect, you can bypass the public Internet and achieve a more reliable and consistent network performance. It provides a private and dedicated connection to AWS services, which is particularly beneficial for data-intensive workloads or sensitive data transfer.

Amazon Route 53 is a scalable domain name system (DNS) web service that translates domain names into IP addresses. While it is not directly used for connecting on-premises networks to AWS Cloud, it is commonly used for DNS routing and traffic management within AWS.

Amazon Virtual Private Cloud (Amazon VPC) is the networking layer for your AWS resources. It allows you to create isolated virtual networks in the AWS Cloud. While it provides network isolation and control within the AWS environment, it does not directly connect your on-premises network to AWS. However, you can use VPN or Direct Connect in combination with Amazon VPC to establish connectivity.

Internet Gateway is a horizontally scalable, redundant, and highly available VPC component that allows communication between your VPC and the Internet. It is used for Internet connectivity within the AWS environment but does not provide direct connectivity between on-premises networks and AWS Cloud.

Therefore, the correct options for connecting your on-premises network with AWS Cloud are AWS Virtual Private Network (VPN) and AWS Direct Connect.
------------------
**You:**


10:39

↓

44/65

49:26

Finish test

Question 44:

Which of the following AWS services are always free to use (Select two)?

AWS Auto Scaling

Amazon Simple Storage Service (Amazon S3)

Amazon Elastic Compute Cloud (Amazon

EC2)

Amazon DynamoDB

AWS Identity and Access Management (AWS IAM)
------------------
**ChatGPT:**


Among the given options, the following AWS services are always free to use:

AWS Identity and Access Management (AWS IAM): AWS IAM is the service used for managing user identities and access to AWS resources. The core features of IAM, such as creating and managing users, groups, and permissions, are available for free. However, there may be charges for certain advanced features or specific usage scenarios.

Amazon Simple Storage Service (Amazon S3): Amazon S3 is a scalable object storage service that allows you to store and retrieve data. There is a free tier available for Amazon S3, which includes a certain amount of storage, data transfer, and requests each month. As long as you stay within the free tier limits, you can use Amazon S3 for free.

Please note that while the core services of AWS Auto Scaling, Amazon Elastic Compute Cloud (Amazon EC2), and Amazon DynamoDB are not always free, there may be free usage tiers or specific usage scenarios where limited usage is available for free. However, these services typically incur charges based on usage beyond the free tier or specific service limits.

Therefore, the correct options for AWS services that are always free to use are AWS Identity and Access Management (AWS IAM) and Amazon Simple Storage Service (Amazon S3).
------------------
**You:**


10:40

↑

45/65

48:36

Finish test

Question 45:

What foundational capability under the operations perspective is part of the AWS Cloud Adoption Framework (AWS CAF)?

Vulnerability management

Application portfolio management

Platfrom engineering

Performance and capacity management
------------------
**ChatGPT:**


Among the given options, the foundational capability under the operations perspective that is part of the AWS Cloud Adoption Framework (AWS CAF) is Performance and capacity management.

The AWS Cloud Adoption Framework (CAF) is a framework designed to help organizations adopt the cloud and define their cloud strategy. It provides a structured approach for planning and implementing cloud adoption, covering various perspectives including business, people, governance, platform, security, and operations.

Performance and capacity management is an essential aspect of operating in the cloud. It involves monitoring and optimizing the performance of cloud resources and ensuring that sufficient capacity is available to meet the demands of the applications and services running in the cloud. This includes activities such as monitoring resource utilization, scaling resources as needed, and optimizing performance for cost-efficiency.

Therefore, the correct option for the foundational capability under the operations perspective in the AWS Cloud Adoption Framework (AWS CAF) is Performance and capacity management.
------------------
**You:**


10:41

↓

46/65

47:47

Finish test

Question 46:

Which of the following AWS services allows a database to have flexible schema and supports document data models?

Amazon Redshift

Amazon Aurora

Amazon Relational Database Service (Amazon RDS)

Amazon DynamoDB
------------------
**ChatGPT:**


Among the given options, the AWS service that allows a database to have a flexible schema and supports document data models is Amazon DynamoDB.

Amazon DynamoDB is a fully managed NoSQL database service provided by AWS. It is designed to provide fast and predictable performance with seamless scalability. DynamoDB allows you to store and retrieve data using flexible document data models, which means you can have a dynamic schema and store data in the form of JSON-like documents.

With DynamoDB, you can create tables with different attributes for each item, providing flexibility in defining the structure of your data. This allows you to adapt to changing requirements without needing to modify the entire database schema.

Therefore, the correct option for an AWS service that supports flexible schema and document data models is Amazon DynamoDB.
------------------
**You:**


10:41

↓

47/65

47:04

Finish test

Question 47:

Which of the following statements is INCORRECT about AWS Auto Scaling?

You can automatically remove unhealthy instances

You can automatically register new instances to a load balancer

You can scale out and add more Amazon Elastic Compute Cloud (Amazon EC2) instances to match an increase in demand as well as scale in and remove Amazon Elastic Compute Cloud (Amazon EC2) instances to match a reduced demand

You can automatically deploy AWS Shield when a DDoS attack is detected
------------------
**ChatGPT:**


The incorrect statement about AWS Auto Scaling is:

"You can automatically deploy AWS Shield when a DDoS attack is detected."

AWS Auto Scaling is a service that allows you to automatically adjust the number of Amazon EC2 instances in a scalable manner based on predefined conditions or metrics. It helps you maintain the desired application availability and performance by dynamically scaling your resources.

While AWS Shield is a DDoS (Distributed Denial-of-Service) protection service provided by AWS, it is not directly related to AWS Auto Scaling. AWS Shield is designed to protect your applications and infrastructure against DDoS attacks by providing automatic mitigation and protection. It operates independently of AWS Auto Scaling.

Therefore, the statement that is incorrect about AWS Auto Scaling is that it can automatically deploy AWS Shield when a DDoS attack is detected.
------------------
**You:**


10:42

↑

48/65

46:22

Finish test

Question 48:

What are the different gateway types supported by

AWS Storage Gateway service?

Tape Gateway, File Gateway and Block Gateway

Tape Gateway, Object Gateway and Volume Gateway

Tape Gateway, File Gateway and Volume Gateway

Object Gateway, File Gateway and Block Gateway
------------------
**ChatGPT:**


The different gateway types supported by the AWS Storage Gateway service are:

Tape Gateway: It provides a virtual tape library (VTL) interface for backup and archival workloads. It allows you to store data in Amazon S3 and Glacier using industry-standard backup applications.

File Gateway: It provides a file interface to store and retrieve objects in Amazon S3. It supports Network File System (NFS) and Server Message Block (SMB) protocols, allowing you to seamlessly integrate it with existing applications and on-premises file-based workloads.

Volume Gateway: It provides block storage volumes that can be mounted as iSCSI devices by your on-premises or EC2-based applications. It offers two configurations:

a. Stored Volumes: It stores your data locally and asynchronously backs up point-in-time snapshots to Amazon S3 for durability. This configuration is suitable for primary storage, where low-latency access to frequently accessed data is required.

b. Cached Volumes: It stores only frequently accessed data locally and stores the entire dataset in Amazon S3. This configuration optimizes storage costs while still providing low-latency access to frequently accessed data.

Therefore, the correct answer is: Tape Gateway, File Gateway, and Volume Gateway.
------------------
**You:**


10:43

↑

49/65

45:44

Finish test

Question 49:

The AWS Well-Architected Framework provides guidance on building cloud based applications using AWS best practices. Which of the following options are the pillars mentioned in the AWS Well- Architected Framework? (Select two)

Reliability

Elasticity

Scalability

Availability

Cost Optimization
------------------
**ChatGPT:**


The pillars mentioned in the AWS Well-Architected Framework are:

Reliability: This pillar focuses on the ability of a system to recover from failures and continue to function as expected. It includes aspects such as fault tolerance, high availability, and disaster recovery.

Cost Optimization: This pillar focuses on optimizing costs by making efficient use of resources and eliminating unnecessary expenses. It includes aspects such as choosing the right pricing models, monitoring resource usage, and optimizing for cost-effective solutions.

Therefore, the correct options are Reliability and Cost Optimization.
------------------
**You:**


10:43

↑

50/65

45:16

Finish test

Question 50:

Which service gives a personalized view of the status of the AWS services that are part of your Cloud architecture so that you can quickly assess the impact on your business when AWS service(s) are experiencing issues?

AWS Health - Service Health Dashboard

Amazon Inspector

Amazon CloudWatch

AWS Health - Your Account Health Dashboard
------------------
**ChatGPT:**


The service that gives a personalized view of the status of the AWS services that are part of your Cloud architecture is "AWS Health - Your Account Health Dashboard." It provides real-time information and notifications about the health of your AWS resources, services, and accounts, allowing you to assess the impact on your business when AWS services are experiencing issues.
------------------
**You:**


10:44

51/65

44:39

Finish test

Question 51:

Which of the following is correct about AWS Developer Support plan?

Allows unlimited contacts to open unlimited cases

Allows unlimited contacts to open a limited number of cases per month

Allows one contact to open a limited number of cases per month

Allows one contact to open unlimited cases

<

>
------------------
**ChatGPT:**


The correct statement about the AWS Developer Support plan is that it allows one contact to open a limited number of cases per month. The specific number of cases allowed may vary depending on the terms of the support plan.
------------------
**You:**


10:44

52/65

44:05 Finish test

Question 52:

Which AWS service helps with global application availability and performance using the AWS global network?

Elastic Load Balancing (ELB)

Amazon CloudFront

AWS Global Accelerator

Amazon Route 53
------------------
**ChatGPT:**


The AWS service that helps with global application availability and performance using the AWS global network is AWS Global Accelerator.
------------------
**You:**


10:45

↑

53/65

43:37

Finish test

Question 53:

Which of the following statement is correct for a Security Group and a Network Access Control List (Network ACL)?

Security Group acts as a firewall at the instance level whereas Network Access Control List (Network ACL) acts as a firewall at the subnet level

Security Group acts as a firewall at the Availability Zone (AZ) level whereas Network Access Control List (Network ACL) acts as a firewall at the VPC level

Security Group acts as a firewall at the subnet level whereas Network Access Control List (Network ACL) acts as a firewall at the instance level

Security Group acts as a firewall at the VPC level whereas Network Access Control List (Network ACL) acts as a firewall at the Availability Zone (AZ) level
------------------
**ChatGPT:**


The correct statement is: Security Group acts as a firewall at the instance level whereas Network Access Control List (Network ACL) acts as a firewall at the subnet level.
------------------
**You:**


10:46

↑

54/65

42:52

Finish test

Question 54:

Access Key ID and Secret Access Key are tied to which of the following AWS Identity and Access Management (AWS IAM) entities?

IAM User Group

IAM User

IAM Role

IAM Policy
------------------
**ChatGPT:**


Access Key ID and Secret Access Key are tied to an IAM User in AWS Identity and Access Management (AWS IAM).
------------------
**You:**


10:46

↓

55/65

42:27

Finish test

Question 55:

What are the fundamental drivers of cost with AWS Cloud?

Compute, Storage and Outbound Data Transfer

Compute, Storage and Inbound Data Transfer

Compute, Databases and Inbound Data Transfer

Compute, Databases and Outbound Data Transfer
------------------
**ChatGPT:**


The fundamental drivers of cost with AWS Cloud are Compute, Storage, and Outbound Data Transfer.
------------------
**You:**


10:47

↑

56/65

41:32

Finish test

Question 56:

Which AWS service enables users to find, buy, and immediately start using software solutions in their AWS environment?

AWS Systems Manager

AWS Marketplace

AWS Config

AWS OpsWorks
------------------
**ChatGPT:**


The AWS service that enables users to find, buy, and immediately start using software solutions in their AWS environment is called AWS Marketplace.
------------------
**You:**


10:47

↑

57/65

41:03 Finish test

Question 57:

As per the AWS Shared Responsibility Model, which of the following is a responsibility of the customer from a security and compliance point of view?

Configuration management for AWS global infrastructure

Patching/fixing flaws within the AWS infrastructure

Availability Zone (AZ) infrastructure management

Managing patches of the guest operating system on Amazon Elastic Compute Cloud (Amazon EC2)
------------------
**ChatGPT:**


As per the AWS Shared Responsibility Model, managing patches of the guest operating system on Amazon Elastic Compute Cloud (Amazon EC2) is a responsibility of the customer from a security and compliance point of view.
------------------
**You:**


10:48

↑

58/65

40:24

Finish test

Question 58:

An e-commerce company wants to assess its applications deployed on Amazon Elastic Compute Cloud (Amazon EC2) instances for vulnerabilities and deviations from AWS best practices. Which AWS service can be used to facilitate this?

Amazon Inspector

AWS CloudHSM

AWS Secrets Manager

AWS Trusted Advisor
------------------
**ChatGPT:**


To assess applications deployed on Amazon EC2 instances for vulnerabilities and deviations from AWS best practices, the e-commerce company can use Amazon Inspector.
------------------
**You:**


10:49

↑

59/65

39:49 Finish test

Question 59:

Which of the following AWS services comes under the Software as a Service (SaaS) Cloud Computing Type?

Elastic Load Balancing (ELB)

Amazon Elastic Compute Cloud (Amazon EC2)

Amazon Rekognition

AWS Elastic Beanstalk
------------------
**ChatGPT:**


Amazon Rekognition is the AWS service that falls under the Software as a Service (SaaS) Cloud Computing Type.
------------------
**You:**


10:49

↓

60/65

39:19

Finish test

Question 60:

A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?

AWS Direct Connect

AWS Wavelength

AWS Local Zones

AWS Edge Locations
------------------
**ChatGPT:**


To provide low-latency access to end-users in various locations, the gaming company can leverage the AWS CloudFront service with its global network of AWS Edge Locations. AWS CloudFront is a content delivery network (CDN) that helps deliver content with low latency and high data transfer speeds. It caches content at Edge Locations closest to end-users, reducing the distance and time taken to access the content, thereby improving the user experience.
------------------
**You:**


10:50

↓

61/65

38:15 Finish test

Question 61:

Which of the following AWS services are part of the

AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)

Amazon CloudWatch

AWS CloudTrail

AWS CloudFormation

AWS Trusted Advisor

Service Quotas
------------------
**ChatGPT:**


The AWS services that are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework are:

Amazon CloudWatch: It provides monitoring and observability for AWS resources and applications, helping detect and respond to operational issues.

AWS Trusted Advisor: It provides guidance on best practices and helps optimize AWS resources for reliability, security, performance, and cost.

These services contribute to ensuring the reliability of applications and systems deployed in the AWS Cloud.
------------------
**You:**


10:52

↓

62/65

37:06 Finish test

Question 62:

A photo sharing web application wants to store thumbnails of user-uploaded images on Amazon Simple Storage Service (Amazon S3). The thumbnails are rarely used but need to be immediately accessible from the web application. The thumbnails can be regenerated easily if they are lost. Which is the most cost-effective way to store these thumbnails on Amazon Simple Storage Service (Amazon S3)?

Use Amazon S3 Standard to store the thumbnails

Use Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) to store the thumbnails

Use Amazon S3 Glacier Flexible Retrieval to store the thumbnails

Use Amazon S3 Standard-Infrequent Access (S3 Standard-IA) to store the thumbnails
------------------
**ChatGPT:**


The most cost-effective way to store the thumbnails on Amazon Simple Storage Service (Amazon S3) in this scenario would be to use Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA).

Amazon S3 One Zone-IA is designed for data that can be easily re-created or is non-critical, and it offers a lower storage cost compared to Amazon S3 Standard. It stores data in a single availability zone, which reduces the cost but also means that the data is not replicated across multiple availability zones for higher durability.

Since the thumbnails can be easily regenerated if they are lost, and immediate accessibility is required from the web application, using Amazon S3 One Zone-IA provides a cost-effective solution while still meeting the requirements of the application.
------------------
**You:**


10:52

↓

63/65

36:24

Finish test

Question 63:

A company is using a message broker service on its on-premises application and wants to move this messaging functionality to AWS Cloud. Which of the following AWS services is the right choice to move the existing functionality easily?

Amazon Kinesis Data Streams

Amazon Simple Notification Service (Amazon SNS)

Amazon MQ

Amazon Simple Queue Service (Amazon sas)
------------------
**ChatGPT:**


To move the existing messaging functionality from an on-premises application to AWS Cloud, the right choice of AWS service would be Amazon MQ.

Amazon MQ is a managed message broker service that supports multiple messaging protocols and provides compatibility with existing applications. It supports industry-standard messaging protocols such as AMQP, MQTT, and STOMP, making it easier to migrate existing messaging functionality to AWS without making significant changes to the application code.

By using Amazon MQ, the company can seamlessly transition its message broker service to the cloud while maintaining compatibility with its on-premises application.
------------------
**You:**


10:53

↓

64/65

35:54 Finish test

Question 64:

Which policy describes prohibited uses of the web services offered by Amazon Web Services?

AWS Applicable Use Policy

AWS Fair Use Policy

AWS Trusted Advisor

AWS Acceptable Use Policy
------------------
**ChatGPT:**


The policy that describes prohibited uses of the web services offered by Amazon Web Services (AWS) is the AWS Acceptable Use Policy.

The AWS Acceptable Use Policy outlines the terms and conditions that govern the usage of AWS services. It specifies the activities that are prohibited and not allowed when using AWS services. This policy sets the guidelines for acceptable behavior and usage of AWS resources to ensure the security, reliability, and integrity of the services for all users.

It is important for users of AWS services to adhere to the AWS Acceptable Use Policy to maintain a safe and secure environment for themselves and other users of the platform.
------------------
**You:**


10:53

↑

65/65

35:27

Finish test

Question 65:

Which AWS support plan provides access to a designated Technical Account Manager (TAM)?

AWS Enterprise Support

AWS Developer Support

AWS Business Support

AWS Enterprise On-Ramp Support
------------------
**ChatGPT:**


The AWS support plan that provides access to a designated Technical Account Manager (TAM) is the AWS Enterprise Support plan.

The AWS Enterprise Support plan is a comprehensive support offering designed for enterprise customers. It includes a range of benefits and features to assist customers in operating and scaling their AWS environments. One of the key features of the AWS Enterprise Support plan is access to a designated Technical Account Manager (TAM).

A Technical Account Manager (TAM) is an AWS expert who works closely with the customer to understand their business goals and technical requirements. The TAM provides personalized guidance, architectural reviews, and best practices recommendations to help optimize the customer's use of AWS services. The TAM serves as a single point of contact within AWS, offering proactive assistance and support to address the customer's specific needs.

Overall, the AWS Enterprise Support plan with access to a designated Technical Account Manager (TAM) is ideal for customers who require a higher level of personalized support and guidance for their AWS deployments.
------------------
**You:**


Question 17: Incorrect
Which of the following statements are correct about the AWS root user account? (Select two)






Explanation
Correct options:

Root user access credentials are the email address and password used to create the AWS account

It is highly recommended to enable Multi Factor Authentication (MFA) for root user account

The Email address and the password used for signing up for AWS services are the AWS root user account credentials. Root user account, therefore, has full permissions on all AWS resources under that account. Restricting root user account access is not possible. As a best practice, Multi-Factor Authentication (MFA) should be set on the root user account. The root user account password can be changed after account creation. For all employees performing various administrative jobs, create individual user accounts using AWS IAM, and give administrative permissions as needed.

AWS Root User Account Security Best Practices:

 via - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

 via - https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials

Incorrect options:

Root user account password cannot be changed once it is set - This is incorrect. Like any other user credentials, the root user password can be changed after creation.

Root user credentials should only be shared with managers requiring administrative responsibilities to complete their jobs - This is a dangerous practice. Root user credentials should only be used only for some limited account-specific activity and root user credentials should be never be shared with anyone.

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies - Root user account permissions cannot be restricted, whoever has access to these credentials can perform any operation for that AWS account. The root user credentials should be kept safely.

References:

https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html

Question 21: Incorrect
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?





Explanation
Correct option:

Edge Location Management

Security and Compliance is a shared responsibility between AWS and the customer. The AWS Shared Responsibility Model can help relieve the customer’s operational burden as AWS operates, manages, and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates.

AWS is responsible for security "of" the cloud. This covers their global infrastructure elements including Regions, Availability Zones (AZ), and Edge Locations.

Incorrect options:

Customer Data

Identity and Access Management

Server-side Encryption (SSE)

The customer is responsible for security "in" the cloud. Customers are responsible for managing their data including encryption options and using Identity and Access Management tools for implementing appropriate access control policies as per their organization requirements. For abstracted services, such as Amazon S3 and Amazon DynamoDB, AWS operates the infrastructure layer, the operating system, and platforms, and customers access the endpoints to store and retrieve data. Therefore, these three options fall under the responsibility of the customer according to the AWS shared responsibility model.

Exam Alert:

Please review the AWS Shared Responsibility Model in detail as you can expect multiple questions on this topic in the exam:  via - https://aws.amazon.com/compliance/shared-responsibility-model/

Reference:

https://aws.amazon.com/compliance/shared-responsibility-model/

Question 26: Incorrect
AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)






Explanation
Correct options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EC2 Auto Scaling groups

Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions

AWS Compute Optimizer helps you identify the optimal AWS resource configurations, such as Amazon EC2 instance types, Amazon EBS volume configurations, and AWS Lambda function memory sizes, using machine learning to analyze historical utilization metrics. AWS Compute Optimizer delivers recommendations for selected types of EC2 instances, EC2 Auto Scaling groups, Amazon EBS volumes, and AWS Lambda functions.

AWS Compute Optimizer calculates an individual performance risk score for each resource dimension of the recommended instance, including CPU, memory, EBS throughput, EBS IOPS, disk throughput, disk throughput, network throughput, and network packets per second (PPS).

AWS Compute Optimizer provides EC2 instance type and size recommendations for EC2 Auto Scaling groups with a fixed group size, meaning desired, minimum, and maximum are all set to the same value and have no scaling policy attached.

AWS Compute Optimizer supports IOPS and throughput recommendations for General Purpose (SSD) (gp3) volumes and IOPS recommendations for Provisioned IOPS (io1 and io2) volumes.

AWS Compute Optimizer helps you optimize two categories of Lambda functions. The first category includes Lambda functions that may be over-provisioned in memory sizes. The second category includes compute-intensive Lambda functions that may benefit from additional CPU power.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Elastic File System (Amazon EFS)

Amazon Elastic File System (Amazon EFS), AWS Lambda functions

AWS Lambda functions, Amazon Simple Storage Service (Amazon S3)

AWS Compute Optimizer does not provide optimization recommendations for S3 and EFS, so these options are incorrect.

Reference:

https://aws.amazon.com/compute-optimizer/faqs/

Question 31: Incorrect
Which of the following statement is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?





Explanation
Correct option:

Only outbound data transfer is charged

One of the main benefits of cloud services is the ability it gives you to optimize costs to match your needs, even as those needs change. AWS services do not have complex dependencies or licensing requirements, so you can get exactly what you need to build innovative, cost-effective solutions using the latest technology.

There are three fundamental drivers of cost with AWS: compute, storage, and outbound data transfer. These characteristics vary somewhat, depending on the AWS product and pricing model you choose. Outbound data to the internet from all AWS regions is billed at region-specific, tiered data transfer rates. Inbound data transfer into all AWS regions from the internet is free.

Incorrect options:

Only inbound data transfer is charged

Both inbound data transfer and outbound data transfer are charged

Neither inbound nor outbound data transfer are charged

These three options contradict the explanation provided above, so these options are incorrect.

Reference:

https://d0.awsstatic.com/whitepapers/aws_pricing_overview.pdf

Question 42: Incorrect
Which Amazon Elastic Compute Cloud (Amazon EC2) pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that instance would not be interrupted?





Explanation
Correct option:

On-Demand Instance - An On-Demand Instance is an instance that you use on-demand. You have full control over its lifecycle — you decide when to launch, stop, hibernate, start, reboot, or terminate it. There is no long-term commitment required when you purchase On-Demand Instances. There is no upfront payment and you pay only for the seconds that your On-Demand Instances are running. The price per second for running an On-Demand Instance is fixed. On-demand instances cannot be interrupted.

EC2 Pricing Options Overview:  via - https://aws.amazon.com/ec2/pricing/

Incorrect options:

Reserved Instance (RI) - Reserved Instance (RI) provides you with significant savings on your Amazon EC2 costs compared to On-Demand Instance pricing. Reserved Instances (RI) are not physical instances, but rather a billing discount applied to the use of On-Demand Instances in your account. You can purchase a Reserved Instance (RI) for a one-year or three-year commitment, with the three-year commitment offering a bigger discount. You will be charged for the entire duration, irrespective of your usage. So this option is not correct for the given use-case.

Spot Instance - A Spot Instance is an unused EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. Spot Instances are well-suited for data analysis, batch jobs, background processing, and optional tasks. These can be terminated at short notice, so these are not suitable for critical workloads that need to run at a specific point in time. So this option is not correct for the given use-case.

Dedicated Host - Amazon EC2 Dedicated Host allows you to use your eligible software licenses from vendors such as Microsoft and Oracle on Amazon EC2 so that you get the flexibility and cost-effectiveness of using your licenses, but with the resiliency, simplicity, and elasticity of AWS. An Amazon EC2 Dedicated Host is a physical server fully dedicated for your use, so you can help address corporate compliance requirement. A Dedicated Host is not cost-efficient compared to an On-Demand instance. So this option is not correct.

Reference:

https://aws.amazon.com/ec2/pricing/

Question 44: Incorrect
Which of the following AWS services are always free to use (Select two)?






Explanation
Correct options:

AWS Identity and Access Management (AWS IAM) - AWS Identity and Access Management (AWS IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. IAM is a feature of your AWS account offered at no additional charge.

AWS Auto Scaling - AWS Auto Scaling monitors your applications and automatically adjusts the capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes. AWS Auto Scaling is available at no additional charge. You pay only for the AWS resources needed to run your applications and Amazon CloudWatch monitoring fees.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) - Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. This is not a free service. You pay for what you use or depending on the plan you choose.

Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. S3 service is not free and you pay to depend on the storage class you choose for your data.

Amazon DynamoDB - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB is not free and you are charged for reading, writing, and storing data in your DynamoDB tables, along with any optional features you choose to enable.

References:

https://aws.amazon.com/iam/

https://aws.amazon.com/autoscaling/

Question 51: Incorrect
Which of the following is correct about AWS Developer Support plan?





Explanation
Correct option:

Allows one contact to open unlimited cases

AWS Developer Support plan allows one primary contact to open unlimited cases.

Incorrect options:

Allows one contact to open a limited number of cases per month - As mentioned earlier, the AWS Developer Support plan allows one primary contact to open unlimited cases. So this option is incorrect.

Allows unlimited contacts to open unlimited cases - This is true for AWS Business Support, AWS Enterprise On-Ramp Support and AWS Enterprise Support plans. So this is incorrect for AWS Developer Support plan.

Allows unlimited contacts to open a limited number of cases per month - This is a made-up option and has been added as a distractor.

Reference:

https://aws.amazon.com/premiumsupport/plans/

Question 60: Incorrect
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?





Explanation
Correct option:

AWS Local Zones

AWS Local Zones allow you to use select AWS services, like compute and storage services, closer to more end-users, providing them very low latency access to the applications running locally. AWS Local Zones are also connected to the parent region via Amazon’s redundant and very high bandwidth private network, giving applications running in AWS Local Zones fast, secure, and seamless access to the rest of AWS services.

You should use AWS Local Zones to deploy workloads closer to your end-users for low-latency requirements. AWS Local Zones have their connection to the internet and support AWS Direct Connect, so resources created in the Local Zone can serve local end-users with very low-latency communications.

Various AWS services such as Amazon Elastic Compute Cloud (EC2), Amazon Virtual Private Cloud (VPC), Amazon Elastic Block Store (EBS), Amazon FSx, Amazon Elastic Load Balancing, Amazon EMR, Amazon ElastiCache, and Amazon Relational Database Service (RDS) are available locally in the AWS Local Zones. You can also use services that orchestrate or work with local services such as Amazon EC2 Auto Scaling, Amazon EKS clusters, Amazon ECS clusters, Amazon EC2 Systems Manager, Amazon CloudWatch, AWS CloudTrail, and AWS CloudFormation. AWS Local Zones also provide a high-bandwidth, secure connection to the AWS Region, allowing you to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

Incorrect options:

AWS Edge Locations - An AWS Edge location is a site that CloudFront uses to cache copies of the content for faster delivery to users at any location.

AWS Wavelength - AWS Wavelength extends the AWS cloud to a global network of 5G edge locations to enable developers to innovate and build a whole new class of applications that require ultra-low latency. Wavelength Zones provide a high-bandwidth, secure connection to the parent AWS Region, allowing developers to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

AWS Direct Connect - AWS Direct Connect is a cloud service that links your network directly to AWS, bypassing the internet to deliver more consistent, lower-latency performance. When creating a new connection, you can choose a hosted connection provided by an AWS Direct Connect Delivery Partner, or choose a dedicated connection from AWS—and deploy at over 100 AWS Direct Connect locations around the world. AWS Direct Connect provides consistently high bandwidth, low-latency access and it is generally used between on-premises data centers and AWS network. Direct Connect is overkill for the given requirement.

Reference:

https://aws.amazon.com/about-aws/global-infrastructure/localzones/

Question 61: Incorrect
Which of the following AWS services are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)






Explanation
Correct options:

AWS Trusted Advisor

Service Quotas

Foundations are part of the Reliability pillar of the AWS Well-Architected Framework. AWS states that before architecting any system, foundational requirements that influence reliability should be in place. The services that are part of foundations are: Amazon VPC, AWS Trusted Advisor, AWS Service Quotas (formerly called AWS Service Limits).

AWS Trusted Advisor is an online tool that provides you real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement. Whether establishing new workflows, developing applications, or as part of ongoing improvement, recommendations provided by Trusted Advisor regularly help keep your solutions provisioned optimally.

Service Quotas enables you to view and manage your quotas for AWS services from a central location. Quotas, also referred to as limits in AWS, are the maximum values for the resources, actions, and items in your AWS account. Each AWS service defines its quotas and establishes default values for those quotas.

Incorrect options:

AWS CloudTrail - AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides the event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command-line tools, and other AWS services. Think account-specific activity and audit; think CloudTrail.

AWS CloudFormation - AWS CloudFormation provides a common language to model and provision AWS and third-party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all Regions and accounts. Think infrastructure as code; think CloudFormation.

Amazon CloudWatch - Amazon CloudWatch is a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers. CloudWatch provides data and actionable insights to monitor applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health. This is an excellent service for building Resilient systems. Think resource performance monitoring, events, and alerts; think CloudWatch.

Reference:

https://wa.aws.amazon.com/wat.pillar.reliability.en.html
------------------
**ChatGPT:**


Apologies for the incorrect answers provided in my previous responses. Here are the correct answers for the questions you pointed out:

Question 17: Incorrect
Which of the following statements are correct about the AWS root user account? (Select two)

Correct options:

Root user access credentials are the email address and password used to create the AWS account.
It is highly recommended to enable Multi-Factor Authentication (MFA) for the root user account.

Explanation:
The root user account credentials are the email address and password used to create the AWS account. The root user has full permissions on all AWS resources and cannot have its access restricted. However, it is highly recommended to enable Multi-Factor Authentication (MFA) for the root user account to enhance security and protect against unauthorized access.

References:

AWS Identity and Access Management User Guide - Root user
AWS Identity and Access Management User Guide - Best Practices for Managing AWS Access Keys

Question 21: Incorrect
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?

Correct option:

Edge Location Management

Explanation:
According to the AWS Shared Responsibility Model, AWS is responsible for the security "of" the cloud, which includes managing and securing the underlying infrastructure, global network, and edge locations. Edge locations are part of AWS's infrastructure and are responsible for caching and delivering content to end-users, making their management a responsibility of AWS.

References:

AWS Shared Responsibility Model

Question 26: Incorrect
AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)

Correct options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EC2 Auto Scaling groups
Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions

Explanation:
AWS Compute Optimizer provides recommendations for optimizing resource configurations using machine learning. It delivers recommendations for Amazon EC2 instances, EC2 Auto Scaling groups, Amazon EBS volumes, and AWS Lambda functions. It helps identify optimal instance types, volume configurations, and memory sizes for Lambda functions based on historical utilization metrics.

References:

AWS Compute Optimizer FAQs

Question 31: Incorrect
Which of the following statements is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?

Correct option:

Only outbound data transfer is charged

Explanation:
According to AWS pricing policy, outbound data transfer from all AWS regions to the internet is billed at region-specific, tiered data transfer rates. However, inbound data transfer into all AWS regions from the internet is free.

References:

AWS Pricing Overview

Question 42: Incorrect
Which Amazon Elastic Compute Cloud (Amazon EC2) pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that the instance would not be interrupted?

Correct option:

On-Demand Instance

Explanation:
The On-Demand Instance pricing model in Amazon EC2 is the most cost-effective and flexible option. It does not require a long-term resource commitment or upfront payment. You pay only for the seconds that your On-Demand Instances are running. On-Demand Instances guarantee that the instance will not be interrupted.

References:

Amazon EC2 Pricing

Question 44: Incorrect
Which of the following AWS services are.
------------------
**You:**


Question 44: Incorrect
Which of the following AWS services are always free to use (Select two)?






Explanation
Correct options:

AWS Identity and Access Management (AWS IAM) - AWS Identity and Access Management (AWS IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. IAM is a feature of your AWS account offered at no additional charge.

AWS Auto Scaling - AWS Auto Scaling monitors your applications and automatically adjusts the capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes. AWS Auto Scaling is available at no additional charge. You pay only for the AWS resources needed to run your applications and Amazon CloudWatch monitoring fees.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) - Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. This is not a free service. You pay for what you use or depending on the plan you choose.

Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. S3 service is not free and you pay to depend on the storage class you choose for your data.

Amazon DynamoDB - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB is not free and you are charged for reading, writing, and storing data in your DynamoDB tables, along with any optional features you choose to enable.

References:

https://aws.amazon.com/iam/

https://aws.amazon.com/autoscaling/

Question 51: Incorrect
Which of the following is correct about AWS Developer Support plan?





Explanation
Correct option:

Allows one contact to open unlimited cases

AWS Developer Support plan allows one primary contact to open unlimited cases.

Incorrect options:

Allows one contact to open a limited number of cases per month - As mentioned earlier, the AWS Developer Support plan allows one primary contact to open unlimited cases. So this option is incorrect.

Allows unlimited contacts to open unlimited cases - This is true for AWS Business Support, AWS Enterprise On-Ramp Support and AWS Enterprise Support plans. So this is incorrect for AWS Developer Support plan.

Allows unlimited contacts to open a limited number of cases per month - This is a made-up option and has been added as a distractor.

Reference:

https://aws.amazon.com/premiumsupport/plans/

Question 60: Incorrect
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?





Explanation
Correct option:

AWS Local Zones

AWS Local Zones allow you to use select AWS services, like compute and storage services, closer to more end-users, providing them very low latency access to the applications running locally. AWS Local Zones are also connected to the parent region via Amazon’s redundant and very high bandwidth private network, giving applications running in AWS Local Zones fast, secure, and seamless access to the rest of AWS services.

You should use AWS Local Zones to deploy workloads closer to your end-users for low-latency requirements. AWS Local Zones have their connection to the internet and support AWS Direct Connect, so resources created in the Local Zone can serve local end-users with very low-latency communications.

Various AWS services such as Amazon Elastic Compute Cloud (EC2), Amazon Virtual Private Cloud (VPC), Amazon Elastic Block Store (EBS), Amazon FSx, Amazon Elastic Load Balancing, Amazon EMR, Amazon ElastiCache, and Amazon Relational Database Service (RDS) are available locally in the AWS Local Zones. You can also use services that orchestrate or work with local services such as Amazon EC2 Auto Scaling, Amazon EKS clusters, Amazon ECS clusters, Amazon EC2 Systems Manager, Amazon CloudWatch, AWS CloudTrail, and AWS CloudFormation. AWS Local Zones also provide a high-bandwidth, secure connection to the AWS Region, allowing you to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

Incorrect options:

AWS Edge Locations - An AWS Edge location is a site that CloudFront uses to cache copies of the content for faster delivery to users at any location.

AWS Wavelength - AWS Wavelength extends the AWS cloud to a global network of 5G edge locations to enable developers to innovate and build a whole new class of applications that require ultra-low latency. Wavelength Zones provide a high-bandwidth, secure connection to the parent AWS Region, allowing developers to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

AWS Direct Connect - AWS Direct Connect is a cloud service that links your network directly to AWS, bypassing the internet to deliver more consistent, lower-latency performance. When creating a new connection, you can choose a hosted connection provided by an AWS Direct Connect Delivery Partner, or choose a dedicated connection from AWS—and deploy at over 100 AWS Direct Connect locations around the world. AWS Direct Connect provides consistently high bandwidth, low-latency access and it is generally used between on-premises data centers and AWS network. Direct Connect is overkill for the given requirement.

Reference:

https://aws.amazon.com/about-aws/global-infrastructure/localzones/

Question 61: Incorrect
Which of the following AWS services are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)






Explanation
Correct options:

AWS Trusted Advisor

Service Quotas

Foundations are part of the Reliability pillar of the AWS Well-Architected Framework. AWS states that before architecting any system, foundational requirements that influence reliability should be in place. The services that are part of foundations are: Amazon VPC, AWS Trusted Advisor, AWS Service Quotas (formerly called AWS Service Limits).

AWS Trusted Advisor is an online tool that provides you real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement. Whether establishing new workflows, developing applications, or as part of ongoing improvement, recommendations provided by Trusted Advisor regularly help keep your solutions provisioned optimally.

Service Quotas enables you to view and manage your quotas for AWS services from a central location. Quotas, also referred to as limits in AWS, are the maximum values for the resources, actions, and items in your AWS account. Each AWS service defines its quotas and establishes default values for those quotas.

Incorrect options:

AWS CloudTrail - AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides the event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command-line tools, and other AWS services. Think account-specific activity and audit; think CloudTrail.

AWS CloudFormation - AWS CloudFormation provides a common language to model and provision AWS and third-party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all Regions and accounts. Think infrastructure as code; think CloudFormation.

Amazon CloudWatch - Amazon CloudWatch is a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers. CloudWatch provides data and actionable insights to monitor applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health. This is an excellent service for building Resilient systems. Think resource performance monitoring, events, and alerts; think CloudWatch.

Reference:

https://wa.aws.amazon.com/wat.pillar.reliability.en.html
------------------
**ChatGPT:**


Apologies for the incorrect answers provided in my previous responses. Here are the correct answers for the questions you pointed out:

Question 44: Incorrect
Which of the following AWS services are always free to use (Select two)?

Correct options:

AWS Identity and Access Management (AWS IAM)
AWS Auto Scaling

Explanation:
AWS Identity and Access Management (AWS IAM) is a service that enables you to manage access to AWS services and resources securely. It is available at no additional charge. AWS IAM allows you to create and manage AWS users, groups, and permissions.

AWS Auto Scaling is a service that automatically adjusts the capacity of your applications based on predefined scaling policies. The AWS Auto Scaling service itself is available at no additional charge. However, you still pay for the AWS resources (e.g., EC2 instances) that are launched as part of the scaling activities.

References:

AWS IAM Pricing
AWS Auto Scaling Pricing

Question 51: Incorrect
Which of the following is correct about AWS Developer Support plan?

Correct option:

Allows one primary contact to open unlimited cases

Explanation:
The AWS Developer Support plan allows one primary contact to open unlimited cases. It provides technical support for developers and is suitable for non-production environments and early-stage startups.

References:

AWS Support Plans

Question 60: Incorrect
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?

Correct option:

AWS Wavelength

Explanation:
AWS Wavelength is the AWS service that provides the necessary low-latency access to end-users. It extends the AWS cloud to the edge of 5G networks, allowing developers to deploy their applications in close proximity to mobile network operators' 5G infrastructure. This enables ultra-low-latency communication between the application and end-users, resulting in a great user experience for gaming and other latency-sensitive applications.

References:

AWS Wavelength

Question 61: Incorrect
Which of the following AWS services are part of the AWS Foundation services for the Reliability pillar of the Well-Architected Framework in AWS Cloud? (Select two)

Correct options:

AWS Trusted Advisor
Service Quotas

Explanation:
AWS Trusted Advisor is a service that provides real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement. It is part of the AWS Foundation services for the Reliability pillar.

Service Quotas (formerly called AWS Service Limits) is a service that enables you to view and manage your quotas for AWS services from a central location. Quotas define the maximum values for resources, actions, and items in your AWS account. It is also part of the AWS Foundation services for the Reliability pillar.

References:

AWS Trusted Advisor
Service Quotas
------------------
**You:**


6 Practice Exams | AWS Certified Cloud Practitioner CLF-C01
Start
Practice Test 1: Practice Test #1 - AWS Certified Cloud Practitioner
Start
Practice Test 2: Practice Test #2 - AWS Certified Cloud Practitioner
Start
Practice Test 3: Practice Test #3 - AWS Certified Cloud Practitioner
Start
Practice Test 4: Practice Test #4 - AWS Certified Cloud Practitioner
Start
Practice Test 5: Practice Test #5 - AWS Certified Cloud Practitioner
Start
Practice Test 6: Practice Test #6 - AWS Certified Cloud Practitioner
Practice Test 2: Practice Test #2 - AWS Certified Cloud Practitioner
Practice Test #2 - AWS Certified Cloud Practitioner - Results
Chart
Pie chart with 4 slices.
End of interactive chart.
Attempt 1
Question 17: Incorrect
Which of the following statements are correct about the AWS root user account? (Select two)






Explanation
Correct options:

Root user access credentials are the email address and password used to create the AWS account

It is highly recommended to enable Multi Factor Authentication (MFA) for root user account

The Email address and the password used for signing up for AWS services are the AWS root user account credentials. Root user account, therefore, has full permissions on all AWS resources under that account. Restricting root user account access is not possible. As a best practice, Multi-Factor Authentication (MFA) should be set on the root user account. The root user account password can be changed after account creation. For all employees performing various administrative jobs, create individual user accounts using AWS IAM, and give administrative permissions as needed.

AWS Root User Account Security Best Practices:

 via - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

 via - https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials

Incorrect options:

Root user account password cannot be changed once it is set - This is incorrect. Like any other user credentials, the root user password can be changed after creation.

Root user credentials should only be shared with managers requiring administrative responsibilities to complete their jobs - This is a dangerous practice. Root user credentials should only be used only for some limited account-specific activity and root user credentials should be never be shared with anyone.

Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies - Root user account permissions cannot be restricted, whoever has access to these credentials can perform any operation for that AWS account. The root user credentials should be kept safely.

References:

https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html

Question 21: Incorrect
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?





Explanation
Correct option:

Edge Location Management

Security and Compliance is a shared responsibility between AWS and the customer. The AWS Shared Responsibility Model can help relieve the customer’s operational burden as AWS operates, manages, and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates.

AWS is responsible for security "of" the cloud. This covers their global infrastructure elements including Regions, Availability Zones (AZ), and Edge Locations.

Incorrect options:

Customer Data

Identity and Access Management

Server-side Encryption (SSE)

The customer is responsible for security "in" the cloud. Customers are responsible for managing their data including encryption options and using Identity and Access Management tools for implementing appropriate access control policies as per their organization requirements. For abstracted services, such as Amazon S3 and Amazon DynamoDB, AWS operates the infrastructure layer, the operating system, and platforms, and customers access the endpoints to store and retrieve data. Therefore, these three options fall under the responsibility of the customer according to the AWS shared responsibility model.

Exam Alert:

Please review the AWS Shared Responsibility Model in detail as you can expect multiple questions on this topic in the exam:  via - https://aws.amazon.com/compliance/shared-responsibility-model/

Reference:

https://aws.amazon.com/compliance/shared-responsibility-model/

Question 26: Incorrect
AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)






Explanation
Correct options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EC2 Auto Scaling groups

Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions

AWS Compute Optimizer helps you identify the optimal AWS resource configurations, such as Amazon EC2 instance types, Amazon EBS volume configurations, and AWS Lambda function memory sizes, using machine learning to analyze historical utilization metrics. AWS Compute Optimizer delivers recommendations for selected types of EC2 instances, EC2 Auto Scaling groups, Amazon EBS volumes, and AWS Lambda functions.

AWS Compute Optimizer calculates an individual performance risk score for each resource dimension of the recommended instance, including CPU, memory, EBS throughput, EBS IOPS, disk throughput, disk throughput, network throughput, and network packets per second (PPS).

AWS Compute Optimizer provides EC2 instance type and size recommendations for EC2 Auto Scaling groups with a fixed group size, meaning desired, minimum, and maximum are all set to the same value and have no scaling policy attached.

AWS Compute Optimizer supports IOPS and throughput recommendations for General Purpose (SSD) (gp3) volumes and IOPS recommendations for Provisioned IOPS (io1 and io2) volumes.

AWS Compute Optimizer helps you optimize two categories of Lambda functions. The first category includes Lambda functions that may be over-provisioned in memory sizes. The second category includes compute-intensive Lambda functions that may benefit from additional CPU power.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Elastic File System (Amazon EFS)

Amazon Elastic File System (Amazon EFS), AWS Lambda functions

AWS Lambda functions, Amazon Simple Storage Service (Amazon S3)

AWS Compute Optimizer does not provide optimization recommendations for S3 and EFS, so these options are incorrect.

Reference:

https://aws.amazon.com/compute-optimizer/faqs/

Question 31: Incorrect
Which of the following statement is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?





Explanation
Correct option:

Only outbound data transfer is charged

One of the main benefits of cloud services is the ability it gives you to optimize costs to match your needs, even as those needs change. AWS services do not have complex dependencies or licensing requirements, so you can get exactly what you need to build innovative, cost-effective solutions using the latest technology.

There are three fundamental drivers of cost with AWS: compute, storage, and outbound data transfer. These characteristics vary somewhat, depending on the AWS product and pricing model you choose. Outbound data to the internet from all AWS regions is billed at region-specific, tiered data transfer rates. Inbound data transfer into all AWS regions from the internet is free.

Incorrect options:

Only inbound data transfer is charged

Both inbound data transfer and outbound data transfer are charged

Neither inbound nor outbound data transfer are charged

These three options contradict the explanation provided above, so these options are incorrect.

Reference:

https://d0.awsstatic.com/whitepapers/aws_pricing_overview.pdf

Question 42: Incorrect
Which Amazon Elastic Compute Cloud (Amazon EC2) pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that instance would not be interrupted?





Explanation
Correct option:

On-Demand Instance - An On-Demand Instance is an instance that you use on-demand. You have full control over its lifecycle — you decide when to launch, stop, hibernate, start, reboot, or terminate it. There is no long-term commitment required when you purchase On-Demand Instances. There is no upfront payment and you pay only for the seconds that your On-Demand Instances are running. The price per second for running an On-Demand Instance is fixed. On-demand instances cannot be interrupted.

EC2 Pricing Options Overview:  via - https://aws.amazon.com/ec2/pricing/

Incorrect options:

Reserved Instance (RI) - Reserved Instance (RI) provides you with significant savings on your Amazon EC2 costs compared to On-Demand Instance pricing. Reserved Instances (RI) are not physical instances, but rather a billing discount applied to the use of On-Demand Instances in your account. You can purchase a Reserved Instance (RI) for a one-year or three-year commitment, with the three-year commitment offering a bigger discount. You will be charged for the entire duration, irrespective of your usage. So this option is not correct for the given use-case.

Spot Instance - A Spot Instance is an unused EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. Spot Instances are well-suited for data analysis, batch jobs, background processing, and optional tasks. These can be terminated at short notice, so these are not suitable for critical workloads that need to run at a specific point in time. So this option is not correct for the given use-case.

Dedicated Host - Amazon EC2 Dedicated Host allows you to use your eligible software licenses from vendors such as Microsoft and Oracle on Amazon EC2 so that you get the flexibility and cost-effectiveness of using your licenses, but with the resiliency, simplicity, and elasticity of AWS. An Amazon EC2 Dedicated Host is a physical server fully dedicated for your use, so you can help address corporate compliance requirement. A Dedicated Host is not cost-efficient compared to an On-Demand instance. So this option is not correct.

Reference:

https://aws.amazon.com/ec2/pricing/

Question 44: Incorrect
Which of the following AWS services are always free to use (Select two)?






Explanation
Correct options:

AWS Identity and Access Management (AWS IAM) - AWS Identity and Access Management (AWS IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. IAM is a feature of your AWS account offered at no additional charge.

AWS Auto Scaling - AWS Auto Scaling monitors your applications and automatically adjusts the capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes. AWS Auto Scaling is available at no additional charge. You pay only for the AWS resources needed to run your applications and Amazon CloudWatch monitoring fees.

Incorrect options:

Amazon Elastic Compute Cloud (Amazon EC2) - Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. This is not a free service. You pay for what you use or depending on the plan you choose.

Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. S3 service is not free and you pay to depend on the storage class you choose for your data.

Amazon DynamoDB - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB is not free and you are charged for reading, writing, and storing data in your DynamoDB tables, along with any optional features you choose to enable.

References:

https://aws.amazon.com/iam/

https://aws.amazon.com/autoscaling/

Question 51: Incorrect
Which of the following is correct about AWS Developer Support plan?





Explanation
Correct option:

Allows one contact to open unlimited cases

AWS Developer Support plan allows one primary contact to open unlimited cases.

Incorrect options:

Allows one contact to open a limited number of cases per month - As mentioned earlier, the AWS Developer Support plan allows one primary contact to open unlimited cases. So this option is incorrect.

Allows unlimited contacts to open unlimited cases - This is true for AWS Business Support, AWS Enterprise On-Ramp Support and AWS Enterprise Support plans. So this is incorrect for AWS Developer Support plan.

Allows unlimited contacts to open a limited number of cases per month - This is a made-up option and has been added as a distractor.

Reference:

https://aws.amazon.com/premiumsupport/plans/

Question 60: Incorrect
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations.

Which AWS technology/service will provide the necessary low-latency access to the end-users?





Explanation
Correct option:

AWS Local Zones

AWS Local Zones allow you to use select AWS services, like compute and storage services, closer to more end-users, providing them very low latency access to the applications running locally. AWS Local Zones are also connected to the parent region via Amazon’s redundant and very high bandwidth private network, giving applications running in AWS Local Zones fast, secure, and seamless access to the rest of AWS services.

You should use AWS Local Zones to deploy workloads closer to your end-users for low-latency requirements. AWS Local Zones have their connection to the internet and support AWS Direct Connect, so resources created in the Local Zone can serve local end-users with very low-latency communications.

Various AWS services such as Amazon Elastic Compute Cloud (EC2), Amazon Virtual Private Cloud (VPC), Amazon Elastic Block Store (EBS), Amazon FSx, Amazon Elastic Load Balancing, Amazon EMR, Amazon ElastiCache, and Amazon Relational Database Service (RDS) are available locally in the AWS Local Zones. You can also use services that orchestrate or work with local services such as Amazon EC2 Auto Scaling, Amazon EKS clusters, Amazon ECS clusters, Amazon EC2 Systems Manager, Amazon CloudWatch, AWS CloudTrail, and AWS CloudFormation. AWS Local Zones also provide a high-bandwidth, secure connection to the AWS Region, allowing you to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.
------------------
**ChatGPT:**


Incorrect options:

AWS Snowball - AWS Snowball is a petabyte-scale data transport solution that uses secure appliances to transfer large amounts of data into and out of AWS. It is not specifically designed for low-latency access to end-users.

Amazon Elastic File System (Amazon EFS) - Amazon EFS is a fully managed file system service that provides scalable and highly available file storage for use with Amazon EC2 instances. It is not specifically designed to deliver low-latency gameplay to end-users.

Amazon RDS Multi-AZ - Amazon RDS Multi-AZ is a high-availability feature of Amazon RDS that provides automatic failover capability for database instances. While it helps ensure high availability, it does not specifically address low-latency access for gaming applications.

Reference:

https://aws.amazon.com/about-aws/global-infrastructure/localzones/
------------------
**You:**


11:09

↑

1/65

1:29:49

Finish test

Question 1:

Which AWS service can be used to automate code deployment to Amazon Elastic Compute Cloud (Amazon EC2) instances as well as on-premises instances?

AWS CloudFormation

AWS CodeCommit

AWS CodeDeploy

AWS CodePipeline
------------------
**ChatGPT:**


The correct answer is:

AWS CodeDeploy

AWS CodeDeploy is the AWS service that can be used to automate code deployment to Amazon EC2 instances as well as on-premises instances. It is a fully managed deployment service that automates software deployments to a variety of compute services, including Amazon EC2, Lambda, and on-premises servers. With AWS CodeDeploy, you can deploy your applications in a consistent and reliable manner, allowing you to rapidly release new features and updates.

AWS CloudFormation is a service that provides infrastructure as code and allows you to create and manage AWS resources using templates. It is used for provisioning and managing resources, but it does not directly handle code deployment.

AWS CodeCommit is a fully managed source control service that hosts private Git repositories. It provides a secure and scalable platform for storing and version-controlling your code, but it does not handle code deployment.

AWS CodePipeline is a fully managed continuous delivery service that helps you automate the release pipelines for your applications. It provides a workflow for building, testing, and deploying your code changes, but it does not directly deploy code to instances.

So, the correct answer is:

AWS CodeDeploy
------------------
**You:**


11:10

↑

2/65

1:28:23

Finish test

Question 2:

AWS Identity and Access Management (AWS IAM) policies are written as JSON documents. Which of the following are mandatory elements of an IAM policy?

Effect, Action

Effect, Sid

Action, Condition

Sid, Principal
------------------
**ChatGPT:**


The correct answer is:

Effect, Action

In AWS Identity and Access Management (IAM), policies are written as JSON documents. The mandatory elements of an IAM policy are the "Effect" and "Action" elements.

"Effect" specifies whether the policy statement allows or denies access. It can have two possible values: "Allow" or "Deny".

"Action" specifies the actions or operations that are allowed or denied. Actions are defined as a combination of a service namespace and an action name, such as "s3:GetObject" or "ec2:RunInstances".

The "Sid" element is optional and stands for "Statement ID". It is used to provide a unique identifier for the policy statement. It can be useful when you want to refer to a specific statement within a policy for management or troubleshooting purposes.

The "Principal" element is also optional and defines the AWS identities (users, groups, or roles) to which the policy applies. It specifies the entity that is allowed or denied access to the specified resources. If not specified, the policy applies to all principals.

So, in summary, the mandatory elements of an IAM policy are "Effect" and "Action".
------------------
**You:**


←

3/65

1:27:25

| Finish test

Question 3:

Which AWS service will you use if you have to move large volumes of on-premises data to AWS Cloud from a remote location with limited bandwidth?

AWS Snowball

AWS Direct Connect

AWS Virtual Private Network (VPN)

AWS Transit Gateway

<

>
------------------
**ChatGPT:**


The correct answer is:

AWS Snowball

If you need to move large volumes of on-premises data to AWS Cloud from a remote location with limited bandwidth, you can use AWS Snowball. AWS Snowball is a service that allows you to transfer large amounts of data to and from AWS using physical storage devices.

Here's how AWS Snowball works:

You request a Snowball device from the AWS Management Console.
AWS ships the Snowball device to your location.
You connect the Snowball device to your on-premises environment and transfer your data onto the device.
Once the data transfer is complete, you ship the Snowball device back to AWS.
AWS imports the data from the Snowball device into your designated S3 bucket.
You can then access and use your data in AWS Cloud.

AWS Snowball helps overcome limitations of limited bandwidth and high network costs by providing a physical device for data transfer. It ensures secure data transfer and minimizes the time required to move large volumes of data to AWS Cloud.

AWS Direct Connect, AWS Virtual Private Network (VPN), and AWS Transit Gateway are different services used for establishing network connectivity between your on-premises environment and AWS Cloud, but they are not specifically designed for moving large volumes of data like AWS Snowball.
------------------
**You:**


11:12

↑

4/65

1:26:43

| Finish test

Question 4:

Which of the following are correct statements regarding the AWS Shared Responsibility Model? (Select two)

Configuration Management is the responsibility of the customer

AWS is responsible for training AWS and customer employees on AWS products and services

For a service like Amazon EC2, that falls under Infrastructure as a Service (IaaS), AWS is responsible for maintaining guest operating system

For abstracted services like Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms

AWS is responsible for Security 'of' the Cloud
------------------
**ChatGPT:**


The correct statements regarding the AWS Shared Responsibility Model are:

Configuration Management is the responsibility of the customer.
AWS is responsible for Security 'of' the Cloud.

In the AWS Shared Responsibility Model:

AWS is responsible for the security 'of' the cloud, which means they are responsible for securing the underlying infrastructure that supports the AWS services. This includes aspects such as the physical security of data centers, network infrastructure, and hardware maintenance.

The customer is responsible for security 'in' the cloud, which means they are responsible for configuring and securing their applications, data, and operating systems that are deployed on AWS. This includes tasks such as configuring access controls, implementing security patches, and managing user access.

Regarding the other statements:

AWS is not responsible for training AWS and customer employees on AWS products and services. Training and education on AWS products and services are typically the responsibility of the customer or can be obtained through AWS training resources.

For a service like Amazon EC2, which falls under Infrastructure as a Service (IaaS), AWS is responsible for maintaining the underlying infrastructure, including the physical host, virtualization layer, and network connectivity. However, the responsibility for maintaining the guest operating system, including patching and updates, lies with the customer.

For abstracted services like Amazon S3, AWS operates the infrastructure layer, which includes the physical storage and network connectivity, but the responsibility for the operating system and platforms used by the customer applications lies with the customer.

Therefore, the correct statements are the ones mentioned at the beginning.
------------------
**You:**


11:14

↑

5/65

1:25:03

Finish test

Question 5:

Which of the following are recommended best practices for AWS Identity and Access Management (AWS IAM) service? (Select two)

Grant maximum privileges to avoid assigning privileges again

Rotate credentials regularly

Share AWS account root user access keys with other administrators

Create a minimum number of accounts and share these account credentials among employees

Enable multi-factor authentication (MFA) for all users
------------------
**ChatGPT:**


The recommended best practices for AWS Identity and Access Management (AWS IAM) service are:

Rotate credentials regularly: It is a good practice to rotate access keys and passwords for IAM users on a regular basis. This helps mitigate the risk of unauthorized access if credentials are compromised.

Enable multi-factor authentication (MFA) for all users: Enabling MFA adds an extra layer of security to user accounts by requiring users to provide an additional authentication factor, such as a time-based one-time password (TOTP) generated by a virtual MFA device or a hardware MFA token, in addition to their regular password.

The other options mentioned are not recommended best practices:

Granting maximum privileges to avoid assigning privileges again is not a recommended practice. Instead, the principle of least privilege should be followed, where users are given only the minimum privileges necessary to perform their tasks. This helps reduce the potential impact of compromised credentials.

Sharing AWS account root user access keys with other administrators is not recommended. It is best to create individual IAM users for administrators and grant them appropriate permissions. Sharing root user access keys increases the risk of unauthorized access and makes it difficult to track actions performed by individual administrators.

Creating a minimum number of accounts and sharing account credentials among employees is also not recommended. Each employee should have their own individual IAM account to ensure accountability and traceability of actions. Sharing account credentials can lead to security vulnerabilities and difficulties in managing access control.

Therefore, the correct answers are rotating credentials regularly and enabling multi-factor authentication (MFA) for all users.
------------------
**You:**


11:15

↑

6/65

1:24:14

Finish test

Question 6:

Which of the following statements is correct regarding the Amazon Elastic File System (Amazon EFS) storage service?

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system only in one Availability Zone (AZ)

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ) but not across VPCs and Regions

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ) and VPCs but not across Regions

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ), Regions and VPCs
------------------
**ChatGPT:**


The correct statement regarding the Amazon Elastic File System (Amazon EFS) storage service is:

EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ), Regions, and VPCs.

Amazon EFS provides a scalable and fully managed file storage service for use with Amazon EC2 instances. It is designed to provide shared file storage that can be accessed by multiple EC2 instances simultaneously. Amazon EFS file systems are accessible across multiple Availability Zones within a region, allowing high availability and durability. Additionally, EC2 instances in different VPCs and even different AWS regions can access the same Amazon EFS file system, making it a versatile and flexible storage option.

Therefore, the correct option is "EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ), Regions, and VPCs."
------------------
**You:**


11:16

↑

7/65

1:22:48

| Finish test

Question 7:

Which of the following AWS entities provides the information required to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance?

Amazon Elastic Block Store (Amazon EBS)

Amazon Machine Image (AMI)

AWS Lambda

Amazon Elastic File System (Amazon EFS)
------------------
**ChatGPT:**


The entity that provides the information required to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance is an Amazon Machine Image (AMI).

An Amazon Machine Image (AMI) is a template that contains the necessary information to launch an EC2 instance. It includes the root file system, launch permissions, and any other data required to start an instance. AMIs can be created and customized by users or obtained from the AWS Marketplace.

When launching an EC2 instance, you typically select an AMI that suits your needs, such as a specific operating system and software configuration. The AMI provides the base image from which the instance is created.

Therefore, the correct option is "Amazon Machine Image (AMI)."
------------------
**You:**


11:17

↑

8/65

1:21:30

Finish test

Question 8:

Which feature of AWS Cloud offers the ability to

innovate faster and rapidly develop, test and launch software applications?

Cost savings

Ability to deploy globally in minutes

Elasticity

Agility
------------------
**ChatGPT:**


The feature of AWS Cloud that offers the ability to innovate faster and rapidly develop, test, and launch software applications is "Agility."

Agility refers to the capability of quickly and easily adapting to changing business needs and requirements. AWS provides a wide range of services and tools that enable developers to rapidly develop, test, and deploy applications. With AWS, developers can leverage managed services, automation, and scalable infrastructure to speed up the development and deployment process.

By using AWS services like AWS Lambda for serverless computing, AWS CodeCommit and AWS CodePipeline for continuous integration and continuous delivery (CI/CD), and AWS Elastic Beanstalk for application deployment and management, developers can achieve greater agility in their software development lifecycle.

Therefore, the correct option is "Agility."
------------------
**You:**


11:18

↑

9/65

1:20:58

| Finish test

Question 9:

AWS Lambda pricing is based on which of the following criteria? (Select two)

The number of lines of code for the AWS

Lambda function

The size of the deployment package for the AWS Lambda function

The time it takes for the AWS Lambda function to execute

Number of requests for the AWS Lambda function

The language runtime of the AWS Lambda function
------------------
**ChatGPT:**


AWS Lambda pricing is based on the following criteria:

The time it takes for the AWS Lambda function to execute: AWS Lambda pricing is based on the duration of the function's execution, measured in increments of 100 milliseconds. You are billed for the actual time it takes for your function to run.

Number of requests for the AWS Lambda function: AWS Lambda pricing is also based on the number of requests made to your function. You are charged for each request made to your function, regardless of the amount of compute time used.

Therefore, the correct options are:

The time it takes for the AWS Lambda function to execute
Number of requests for the AWS Lambda function
------------------
**You:**


11:19

↑

10/65

1:20:13

Finish test

Question 10:

Which AWS service protects your AWS account by monitoring malicious activity and detecting threats?

Amazon GuardDuty

Amazon CloudWatch

AWS CloudTrail

AWS Trusted Advisor
------------------
**ChatGPT:**


The AWS service that protects your AWS account by monitoring malicious activity and detecting threats is Amazon GuardDuty. Amazon GuardDuty is a threat detection service that continuously monitors for malicious activity and unauthorized behavior within your AWS environment. It analyzes events, such as API calls and network traffic, to identify potential threats and security vulnerabilities.
------------------
**You:**


11:20

↑

11/65

1:19:17

Finish test

Question 11:

Which of the following Cloud Computing models does the 'gmail' service represent?

Infrastructure as a Service (IaaS)

Software as a Service (SaaS)

Function as a Service (FaaS)

Platform as a Service (PaaS)
------------------
**ChatGPT:**


The 'gmail' service represents the Software as a Service (SaaS) cloud computing model. Software as a Service (SaaS) provides users with access to software applications over the internet without the need for installation and management of the underlying infrastructure or software. Gmail is a web-based email service provided by Google, and users can access it through a web browser without needing to manage any infrastructure or software components.
------------------
**You:**


11:20

↓

12/65

1:18:45

Finish test

Question 12:

Which AWS service can help you create data-driven

business cases for transitioning your business from on-premises to AWS Cloud?

AWS Trusted Advisor

AWS Migration Evaluator

AWS Billing and Cost Management

AWS Budgets
------------------
**ChatGPT:**


The AWS service that can help you create data-driven business cases for transitioning your business from on-premises to AWS Cloud is AWS Migration Evaluator. AWS Migration Evaluator provides a comprehensive view of your on-premises environment and helps you assess the cost savings and other benefits of migrating to the AWS Cloud. It analyzes your on-premises infrastructure, applications, and data to provide insights and recommendations for migration. By using AWS Migration Evaluator, you can gather data and insights to build a business case for transitioning your business to the AWS Cloud.
------------------
**You:**


11:21

↑

13/65

1:18:08

Finish test

Question 13:

An AWS user is trying to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance in a given region. What is the region-specific constraint that the Amazon Machine Image (AMI) must meet so that it can be used for this Amazon Elastic Compute Cloud (Amazon EC2) instance?

You can use an Amazon Machine Image (AMI) from a different region, but it degrades the performance of the Amazon EC2 instance

You should use an Amazon Machine Image (AMI) from the same region, as it improves the performance of the Amazon EC2 instance

You must use an Amazon Machine Image (AMI) from the same region as that of the Amazon EC2 instance. The region of the Amazon Machine Image (AMI) has no bearing on the performance of the Amazon EC2 instance

An Amazon Machine Image (AMI) is a

<
------------------
**ChatGPT:**


An AWS user trying to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance in a given region must use an Amazon Machine Image (AMI) from the same region as that of the instance. The region-specific constraint requires the AMI and the EC2 instance to be in the same region. The region of the AMI has no direct impact on the performance of the EC2 instance, but it is necessary for compatibility and availability within the chosen region. Therefore, to ensure proper functionality and compatibility, it is recommended to use an AMI from the same region as the EC2 instance.
------------------
**You:**


11:22

↓

14/65

1:16:53

Finish test

Question 14:

A startup wants to set up its IT infrastructure on AWS Cloud. The CTO would like to receive detailed reports that break down the startup's AWS costs by the hour in an Amazon Simple Storage Service (Amazon S3) bucket. As a Cloud Practitioner, which AWS service would you recommend for this use-case?

AWS Budgets

AWS Cost Explorer

AWS Pricing Calculator

AWS Cost & Usage Report (AWS CUR)
------------------
**ChatGPT:**


As a Cloud Practitioner, I would recommend using the AWS Cost & Usage Report (AWS CUR) for the given use-case. The AWS Cost & Usage Report provides detailed information about your AWS costs and usage. It can break down costs by the hour and provide comprehensive reports on cost allocation, usage patterns, and resource utilization. You can configure the report to be delivered to an Amazon Simple Storage Service (Amazon S3) bucket, allowing you to store and analyze the data at your convenience. The AWS CUR offers flexibility and customization options to meet your specific reporting needs and provides valuable insights into your AWS cost management.
------------------
**You:**


11:24

↓

15/65

1:15:29

Finish test

Question 15:

Which of the following use cases is best suited for Amazon EFS Standard-Infrequent Access (EFS Standard-IA) storage class?

Object storage for workloads that need sub-second latency speeds for accessing the data

Use as boot volume for highly available Amazon Elastic Compute Cloud (Amazon EC2) instances

Storing data in a single AWS Availability Zone (AZ)

Storing files in an accessible location to satisfy audit requirements
------------------
**ChatGPT:**


The use case that is best suited for Amazon EFS Standard-Infrequent Access (EFS Standard-IA) storage class is "Storing files in an accessible location to satisfy audit requirements."

Amazon EFS Standard-IA is designed for workloads that require infrequent access to data but still need the ability to quickly retrieve it when necessary. It provides a lower-cost storage option compared to Amazon EFS Standard, while still offering the same level of durability and scalability. This storage class is ideal for storing files that need to be readily accessible to meet audit requirements, ensuring that data can be retrieved efficiently when needed.
------------------
**You:**


Which Amazon EC2 pricing model provides is the most cost-effective for an always-up, right-sized database server running a project that will last 1 year?
------------------
**ChatGPT:**


For an always-up, right-sized database server running a project that will last 1 year, the most cost-effective Amazon EC2 pricing model would typically be the Reserved Instances (RI) pricing model.

Reserved Instances allow you to reserve capacity for your Amazon EC2 instances in advance, offering significant cost savings compared to On-Demand instances. By committing to a specific instance type and term length (such as 1 year), you can receive a discounted hourly rate for your instances. This pricing model is well-suited for workloads that require long-term usage and have predictable utilization patterns.

By utilizing Reserved Instances, you can optimize your costs for the entire duration of your project while ensuring that your database server is always up and running at the right size. It's important to analyze your usage requirements and workload patterns to determine the appropriate instance type and the number of Reserved Instances needed to meet your specific needs.
------------------
**You:**


Which of the options below are recommendations in the performance efficiency pillar of the well-architected framework? (choose 2)
------------------
**ChatGPT:**


In the Performance Efficiency pillar of the AWS Well-Architected Framework, the following options are recommendations:

Selecting the Right Resource Types: Choose the appropriate AWS resource types that align with the needs of your workload. This involves considering factors such as compute, storage, database, and network resources. By selecting the right resource types, you can optimize performance and cost-effectiveness.

Designing for Elasticity: Design your architecture to scale horizontally or vertically based on workload demands. Elasticity allows your system to automatically handle varying levels of traffic or load by adding or removing resources dynamically. This ensures that your application can efficiently handle peak loads without over-provisioning and incurring unnecessary costs during low-demand periods.

These recommendations aim to optimize the performance of your workload while ensuring efficient resource utilization and cost-effectiveness.
------------------
**You:**


Which of the options are recommendations in the performance efficiency pillar of the well-architected framework?
------------------
**ChatGPT:**


Apologies for the confusion in my previous response. In the Performance Efficiency pillar of the AWS Well-Architected Framework, the following are recommendations:

Selection of Right Compute Resource: Choose the appropriate compute resource types based on the workload requirements. Consider factors such as CPU, memory, and network performance to ensure the selected compute resource can handle the expected workload efficiently.

Scalable and Elastic Architecture: Design your architecture to be scalable and elastic, allowing it to automatically adjust resources based on workload demands. This enables your application to handle varying levels of traffic and load without performance degradation.

Efficient Storage Management: Optimize storage usage by selecting the appropriate storage types and configurations. Use techniques like data compression, deduplication, and tiered storage to reduce costs and improve performance.

Caching: Implement caching mechanisms to reduce latency and improve performance. Use services like Amazon ElastiCache or Amazon CloudFront to cache frequently accessed data and reduce the load on backend resources.

Performance Monitoring and Analysis: Implement monitoring and analysis tools to gain insights into system performance. Use services like Amazon CloudWatch to monitor key metrics and identify performance bottlenecks or areas for optimization.

These recommendations focus on optimizing the performance of your architecture, ensuring efficient resource utilization, scalability, and monitoring to deliver a high-performing and cost-effective solution.
------------------
**You:**


Which of the options below are recommendations in the performance efficiency
pillar of the well-architected framework? (choose 2)

D Democratize advanced technologies

I: Go global in days

Use serverless architectures

[:I Rarely experiment
------------------
**ChatGPT:**


In the Performance Efficiency pillar of the well-architected framework, the recommendations are:

Use serverless architectures: Serverless architectures, such as AWS Lambda, can improve performance efficiency by abstracting the underlying infrastructure management. They automatically scale based on demand, allowing you to focus on writing code and optimizing the application logic rather than managing servers.

Democratize advanced technologies: This recommendation suggests making advanced technologies accessible to all teams within your organization. By democratizing advanced technologies, you can empower teams to leverage tools, services, and best practices that can enhance performance efficiency and innovation.

The options "Go global in days" and "Rarely experiment" are not specific recommendations in the Performance Efficiency pillar of the well-architected framework.
------------------
**You:**


Vhich feature enables fast, easy, and secure transfers of files over long distances
tetween a client and an Amazon 83 bucket?
O 53 Static Websites |
O 53 Copy |
Q Multipart Upload |
O 53 Transfer Acceleration |
------------------
**ChatGPT:**


The feature that enables fast, easy, and secure transfers of files over long distances between a client and an Amazon S3 bucket is "Transfer Acceleration." Transfer Acceleration is an Amazon S3 feature that utilizes Amazon CloudFront's globally distributed edge locations to accelerate file uploads to and downloads from S3 buckets. It improves transfer speeds by optimizing the network path between the client and the S3 bucket, making it ideal for scenarios where data needs to be transferred over long distances.
------------------
**You:**


Question 10:
Which of the following represent economic advantages of moving to the AWS cloud? (Select TWO.)
I:| Reduce the need to manage applications
El Increase efficiencies through automation
|:| Reduce the rate of change
[:I Reduce the need to manage infrastructure
[:I Increase time to market for new applications'
------------------
**ChatGPT:**


The economic advantages of moving to the AWS cloud include:

Reduce the need to manage applications: By leveraging AWS cloud services, organizations can offload the responsibility of managing applications to AWS, reducing the overhead and cost associated with maintaining and supporting complex applications.

Increase efficiencies through automation: AWS provides a wide range of automation tools and services that can streamline and optimize various operational tasks, leading to increased efficiencies and cost savings.

Therefore, the correct options are:

Reduce the need to manage applications
Increase efficiencies through automation
------------------
**You:**


Question 11:

Which of the options below are recommendations in the security pillar of the well-architected
framework? (Select TWO.)

I:I Enable traceability

|:| Apply security at the application layer

B Automate security best practices

[:I Protect data when it is at rest only

[:I Expect to be secure
------------------
**ChatGPT:**


In the security pillar of the well-architected framework, the following are recommendations:

Enable traceability: Implement mechanisms to track and monitor user activities and API calls, enabling auditing and investigation in case of security incidents.

Apply security at the application layer: Implement security measures and best practices directly within the application code and architecture to protect against common security vulnerabilities.

Therefore, the correct options are:

Enable traceability
Apply security at the application layer
------------------
**You:**


Question 12:
Which pricing options are available when using Amazon EC2 Reserved Instances? (Select TWO.)
El Capacity upfront
I] All upfront
I] Mainly upfront
El Partial upfront
El Enterprise upfront
------------------
**ChatGPT:**


When using Amazon EC2 Reserved Instances, the following pricing options are available:

All upfront: Pay for the entire reservation term upfront and receive the highest discount compared to other options.

Partial upfront: Make a partial upfront payment and pay the remaining balance in monthly installments over the reservation term.

Therefore, the correct options are:

All upfront
Partial upfront
------------------
**You:**


El Physical security of the data center |
[:I Replacement and disposal of disk drives |
El Configuration of security groups |
[:I Patch management of operating systems |
[:I Encryption of customer data |
------------------
**ChatGPT:**


In the security pillar of the well-architected framework, the following options are recommendations:

Physical security of the data center: Implement measures to ensure the physical security of the data center where the infrastructure is hosted.

Replacement and disposal of disk drives: Establish processes for secure replacement and disposal of disk drives to prevent unauthorized access to data.

Configuration of security groups: Properly configure security groups to control inbound and outbound traffic to resources.

Patch management of operating systems: Implement regular patch management practices to keep operating systems up to date and address security vulnerabilities.

Encryption of customer data: Implement encryption mechanisms to protect customer data at rest and in transit.

Therefore, the correct options are:

Physical security of the data center
Replacement and disposal of disk drives
------------------
**You:**


Under the AWS shared responsibility model what is AWS responsible for? (Select TWO.)
------------------
**ChatGPT:**


Under the AWS shared responsibility model, AWS is responsible for the following:

Security "of" the Cloud: AWS is responsible for protecting the infrastructure that runs the cloud services, including hardware, software, and networking components. This includes measures such as data center security, network security, and infrastructure-level security.

Compliance with regulations and standards: AWS ensures that its infrastructure meets industry-specific compliance requirements and regulatory standards, such as HIPAA for healthcare data, PCI DSS for payment card data, and GDPR for personal data protection.

Therefore, the correct options are:

Security "of" the Cloud
Compliance with regulations and standards
------------------
**You:**


Question 13:
Under the AWS shared responsibility model what is AWS responsible for? (Select TWO.)
I] Physical security of the data center
I] Replacement and disposal of disk drives
I] Configuration of security groups
I] Patch management of operating systems
I] Encryption of customer data
------------------
**ChatGPT:**


Under the AWS shared responsibility model, AWS is responsible for the following:

Physical security of the data center: AWS is responsible for securing the physical infrastructure of its data centers, including access controls, monitoring, and environmental safeguards.

Replacement and disposal of disk drives: AWS is responsible for managing the replacement and disposal of disk drives used within its infrastructure to ensure data security.

Therefore, the correct options are:

Physical security of the data center
Replacement and disposal of disk drives
------------------
**You:**


Question 16:
Which service provides a way to convert video and audio files from their source format into versions
that will playback on devices like smartphones, tablets and PCs?
0 Amazon Elastic Transcoder
Q Aws Glue
0 Amazon Rekognition
0 Amazon Comprehend
------------------
**ChatGPT:**


The service that provides a way to convert video and audio files into versions that can be played back on devices like smartphones, tablets, and PCs is Amazon Elastic Transcoder.

Therefore, the correct option is:

Amazon Elastic Transcoder
------------------
**You:**


When using AWS Organizations with consolidated billing what are two valid best practices? (Select
TWO.)

I] Always enable multi-factor authentication (MFA) on the root account

|:| Always use a straightforward password on the root account

I] The paying account should be used for billing purposes only

|:| Use the paying account for deploying resources

|:| Never exceed the limit of 20 linked accounts
------------------
**ChatGPT:**


When using AWS Organizations with consolidated billing, two valid best practices are:

The paying account should be used for billing purposes only: It is recommended to designate one AWS account as the paying account and use it solely for managing billing and payment. This helps in centralizing the billing process and simplifying cost management.

Use the paying account for deploying resources: It is common practice to use the paying account for deploying resources, as it provides better visibility and control over the overall AWS usage and costs. By deploying resources from the paying account, you can easily track and manage the expenses associated with those resources.

The other options mentioned:

Always enable multi-factor authentication (MFA) on the root account: While enabling MFA is a good security practice, it is not specifically related to AWS Organizations with consolidated billing.

Always use a straightforward password on the root account: Using a straightforward password is not a recommended security practice, and it is generally advised to use strong, complex passwords.

Never exceed the limit of 20 linked accounts: AWS Organizations allows you to have more than 20 linked accounts, so this option is not a valid best practice.

Therefore, the correct options are:

The paying account should be used for billing purposes only
Use the paying account for deploying resources
------------------
**You:**


Which of the options below are recommendations in the reliability pillar of the well-architected
framework? (Select TWO.)

I:| Use ad-hoc recovery procedures

El Automatically recover from failure

|:| Scale vertically to increase aggregate system availability

[:I Attempt to accurately estimate capacity requirements

[:I Manage change in automation
------------------
**ChatGPT:**


In the reliability pillar of the well-architected framework, the following options are recommendations:

Automatically recover from failure: It is recommended to design your system in a way that allows for automatic recovery from failures. This can involve implementing mechanisms such as automated scaling, fault tolerance, and automated healing of resources.

Manage change in automation: Automating change management processes helps to reduce the risk of errors and increases the reliability of the system. By using automation tools and processes, you can ensure that changes are applied consistently and reliably across your infrastructure.

The other options mentioned:

Use ad-hoc recovery procedures: Ad-hoc recovery procedures are not recommended as they can be error-prone and lack consistency.

Scale vertically to increase aggregate system availability: Scaling vertically (increasing the size or capacity of individual resources) may improve performance but does not directly address system availability or reliability.

Attempt to accurately estimate capacity requirements: While estimating capacity requirements is important, it is not a specific recommendation in the reliability pillar of the well-architected framework.

Therefore, the correct options are:

Automatically recover from failure
Manage change in automation
------------------
**You:**


Question 19:
Which AWS support plan comes with a Technical Account Manager (TAM)?
0 Developer
0 Enterprise
------------------
**ChatGPT:**


The AWS support plan that comes with a Technical Account Manager (TAM) is the "Enterprise" support plan. The Technical Account Manager provides personalized support and acts as a single point of contact for the customer, helping them with their AWS environment, architectural guidance, and proactive assistance.
------------------
**You:**


Question 20:
Which service provides the ability to simply upload applications and have AWS handle the deployment
details of capacity provisioning, load balancing, auto-scaling, and application health monitoring?
0 Amazon EC2
Q AWS Elastic Beanstalk
0 Amazon EC2 Auto Scaling
O AWS OpsWorks
------------------
**ChatGPT:**


The service that provides the ability to simply upload applications and have AWS handle the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring is "AWS Elastic Beanstalk". AWS Elastic Beanstalk is a fully managed service that makes it easy to deploy, run, and scale applications quickly by abstracting the underlying infrastructure complexities. It allows you to focus on your application code while AWS takes care of the deployment and management tasks.
------------------
**You:**


You are concerned that you may be getting close to some of the default service limits for several AWS
services. What AWS tool can be used to display current usage and limits?

0 AWS CloudWatch

O AWS Personal Health Dashboard

O AWS Trusted Advisor

0 AWS Systems Manager
------------------
**ChatGPT:**


The AWS tool that can be used to display current usage and limits, and provide recommendations for optimizing your AWS resources, is "AWS Trusted Advisor". AWS Trusted Advisor is a service that helps you optimize your AWS infrastructure, security, and cost by providing real-time guidance. It provides checks and recommendations in various categories, including service limits, to ensure you are utilizing AWS resources efficiently and staying within the prescribed limits.
------------------
**You:**


Question 22:

You need to run a production process that will use several EC2 instances and run constantly on an
ongoing basis. The process cannot be interrupted or restarted without issue. What EC2 pricing model
would be best for this workload?

0 Reserved instances

0 Spot instances

0 On-demand instances

0 Flexible instances
------------------
**ChatGPT:**


For a production process that requires uninterrupted and continuous usage of EC2 instances, the best EC2 pricing model would be "Reserved Instances". Reserved Instances allow you to reserve capacity for a specified duration, providing a significant discount compared to On-Demand instances. Reserved Instances are well-suited for workloads that require continuous, long-term usage, such as production processes that run constantly without interruption. By reserving the capacity, you ensure that the instances will be available for your workload, and you can optimize costs by committing to a specific term and payment option.
------------------
**You:**


ec2 pricing model most cost effective
------------------
**ChatGPT:**


When it comes to choosing the most cost-effective pricing model for Amazon Elastic Compute Cloud (EC2), it depends on your specific usage patterns and requirements. Amazon EC2 offers several pricing options, and the best choice for you will depend on factors such as workload characteristics, duration, and predictability. Here are some of the pricing models available for EC2:

On-Demand Instances: With on-demand instances, you pay for compute capacity by the hour or by the second, without any long-term commitments or upfront payments. This model is ideal if you have unpredictable workloads or short-term requirements.

Reserved Instances (RI): Reserved Instances involve a commitment for a specific instance type in a particular availability zone for a term of one or three years. In exchange for the commitment, you receive a significant discount compared to on-demand rates. Reserved Instances are recommended if you have steady-state workloads or predictable usage.

Spot Instances: Spot Instances allow you to bid on unused EC2 capacity, and you only pay the current spot price. Spot Instances can be significantly cheaper than on-demand instances but are subject to interruptions if the spot price exceeds your bid. They are suitable for fault-tolerant and flexible workloads that can handle interruptions.

Savings Plans: Savings Plans provide flexibility across EC2 instance families, sizes, operating systems, and regions, allowing you to reduce your costs by committing to a consistent amount of compute usage (measured in dollars per hour) over a one- or three-year term. Savings Plans offer potential savings compared to on-demand rates.

To determine the most cost-effective pricing model, you should analyze your workload patterns, usage requirements, and budgetary constraints. It's often recommended to use a combination of pricing models to optimize costs, such as using Reserved Instances for baseline workloads and Spot Instances for burstable or non-critical workloads.

Keep in mind that EC2 pricing can change over time, so it's essential to regularly review your usage and adjust your instance types and pricing models accordingly to ensure cost-effectiveness.
------------------
**You:**


right sized database server one year
------------------
**ChatGPT:**


To determine the right-sized database server for a one-year period, you need to consider the following factors:

Workload: Analyze the workload requirements of your database, including the number of concurrent users, transactions per second, data volume, and growth rate. Understand the read and write patterns, query complexity, and expected response times.

Database Management System (DBMS): Different DBMSs have varying resource requirements. Consider the specific DBMS you're using and its recommended hardware specifications.

Performance Metrics: Look at performance metrics such as CPU utilization, memory usage, disk I/O, and network bandwidth. Monitor these metrics on your existing database server or use database profiling tools to gather information on resource utilization.

Scalability: Anticipate future growth and scalability needs. Consider if your workload is likely to increase or change significantly over the one-year period. Evaluate the ability to scale up (vertical scaling) or scale out (horizontal scaling) based on your workload projections.

High Availability and Redundancy: Determine if you require high availability and redundancy. This may involve setting up a failover server or implementing database replication for data redundancy and disaster recovery.

Cloud or On-Premises: Decide whether you will be running your database server on the cloud or on-premises. Cloud providers offer a wide range of instance types and sizes, allowing you to choose the appropriate resources.

Once you have gathered this information, you can consider the following steps:

a. Estimate your resource requirements based on workload analysis, performance metrics, and scalability needs.

b. Consult the documentation and recommendations provided
------------------
**You:**


Which Amazon EC2 pricing model provides is the most cost-effective for an always-up, right-sized database server running a project that will last 1 year?
------------------
**ChatGPT:**


For an always-up, right-sized database server
------------------
**You:**


3:48

Ô

ẤY

5G

↑

1/65

1:29:50

Finish test

Question 1:

Which AWS services can be used as infrastructure automation tools? (Select TWO.)

AWS CloudFormation

Amazon CloudFront

AWS Batch

AWS OpsWorks

Amazon QuickSight
------------------
**ChatGPT:**


The two AWS services that can be used as infrastructure automation tools are:

AWS CloudFormation: AWS CloudFormation is a service that enables you to model and provision AWS infrastructure resources in a declarative manner. It allows you to create templates to define the desired configuration of your infrastructure and then automatically provisions and manages those resources for you.

AWS OpsWorks: AWS OpsWorks is a configuration management service that uses Chef, an automation platform, to manage and automate infrastructure deployments. It provides a flexible way to define and manage the infrastructure and applications, including automation of tasks like software configuration, package installation, and server scaling.

Please note that while Amazon CloudFront and Amazon QuickSight are AWS services, they are not primarily used as infrastructure automation tools. Amazon CloudFront is a content delivery network (CDN) service, and Amazon QuickSight is a business intelligence and data visualization service.
------------------
**You:**


3:49

Ô ẤY 5G

2/65

1:28:54

| Finish test

Question 2:

What technology enables compute capacity to adjust as loads change?

Load balancing

Automatic failover

Round robin

Auto Scaling
------------------
**ChatGPT:**


The technology that enables compute capacity to adjust as loads change is Auto Scaling. Auto Scaling is a feature provided by various cloud platforms, including AWS, that automatically adjusts the number of instances in a compute group based on the current demand. It dynamically scales the compute capacity up or down to match the changing workload.

Load balancing is a mechanism that distributes incoming network traffic across multiple servers or resources to ensure efficient utilization and high availability. It helps evenly distribute the workload and prevent any single resource from being overwhelmed.

Automatic failover is a feature that allows for the automatic switching to a backup or secondary system in the event of a failure or outage in the primary system. It is typically used to ensure continuous availability and minimize downtime.

Round robin is a simple load balancing algorithm that distributes requests or connections evenly across a set of resources in a rotational manner. It does not directly enable compute capacity to adjust as loads change but rather provides a basic load distribution mechanism.

Therefore, the correct answer to the question is Auto Scaling.
------------------
**You:**


3:50

Ô ẤY 5G

↓

3/65

1:27:59

Finish test

Question 3:

How can a company separate costs for storage, Amazon EC2, Amazon S3, and other AWS services by department?

Add department-specific tags to each

resource

Create a separate VPC for each department

Create a separate AWS account for each department

Use AWS Organizations
------------------
**ChatGPT:**


To separate costs for storage, Amazon EC2, Amazon S3, and other AWS services by department, the recommended approach is to use AWS Organizations. AWS Organizations is a service that allows you to centrally manage multiple AWS accounts within your organization. It provides features for creating and managing a hierarchy of AWS accounts, enabling you to set up separate accounts
------------------
**You:**


3:51

Ô ẤY 5G

←

4/65

1:27:22

Finish test

Question 4:

Which AWS Support plan provides access to architectural and operational reviews, as well as 24/7 access to Cloud Support Engineers through email, online chat, and phone?

Basic

Business

Developer

Enterprise
------------------
**ChatGPT:**


The AWS Support plan that provides access to architectural and operational reviews, as well as 24/7 access to Cloud Support Engineers through email, online chat, and phone is the "Enterprise" plan. The Enterprise Support plan is the highest tier of support offered by AWS and provides a comprehensive set of benefits to customers.

The Enterprise Support plan includes features such as:

Access to AWS Trusted Advisor, which provides best practices and recommendations for optimizing your AWS infrastructure.

Access to AWS Support Concierge, a service that offers guidance and support for architectural and operational best practices.

24/7 access to Cloud Support Engineers through multiple channels like email, online chat, and phone.

Assistance with architectural reviews to help optimize
------------------
**You:**


3:52

Ô ẤY 5G

↓

5/65

1:26:44

| Finish test

Question 5:

Under the AWS shared responsibility model, which of the following is an example of security in the AWS Cloud?

Managing edge locations

Physical security

Firewall configuration

Global infrastructure
------------------
**ChatGPT:**


Under the AWS shared responsibility model, security in the AWS Cloud is a shared responsibility between AWS and the customer. AWS is responsible for the security "of" the cloud, which means they are responsible for securing the infrastructure and services that make up the AWS Cloud. On the other hand, the customer is responsible for security "in" the cloud, which involves properly configuring and securing the resources they deploy on AWS.

Among the options provided, an example of security in the AWS Cloud that falls under the customer's responsibility is "Firewall configuration." Customers are responsible for properly configuring and managing the security groups and network access control lists (ACLs) in order to control traffic to and from their resources on AWS.

The other options mentioned are the responsibilities of AWS:

"Managing edge locations" is the responsibility of AWS. Edge locations are part of the AWS global infrastructure and are used for content delivery and low-latency access to services like Amazon CloudFront.

"Physical security" is also the responsibility of AWS. They are responsible for securing their data centers, facilities, and physical infrastructure.

"Global infrastructure" is the responsibility of AWS, as they are responsible for building and maintaining the global infrastructure that supports their cloud services.

Therefore, the correct example of security in the AWS Cloud under the shared responsibility model is "Firewall configuration."
------------------
**You:**


3:54

↓

Ô ẤY 5G

7/65

1:24:41

Finish test

Question 7:

Which Amazon EC2 pricing model provides is the most cost-effective for an always-up, right-sized database server running a project that will last 1 year?

On-Demand Instances

Convertible Reserved Instances

Spot Instances

Standard Reserved Instances
------------------
