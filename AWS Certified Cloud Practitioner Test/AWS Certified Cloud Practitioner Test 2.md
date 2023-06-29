AWS Certified Cloud Practitioner: Test 2 - Results
--------------------------------------------------

Return to review

Chart

Pie chart with 4 slices.

Created with Highcharts 9.2.2

End of interactive chart.

Attempt 1

All knowledge areas

*   All knowledge areas
    
*   AWS Shared Responsibility Model
    
*   AWS Cost Management
    
*   AWS Management & Governance
    
*   AWS Cloud Architecture & Design
    
*   AWS Networking & Content Delivery
    
*   AWS Compute
    
*   AWS Security, Identity, & Compliance
    
*   AWS Developer Tools
    
*   AWS Migration & Transfer
    
*   AWS Storage
    
*   AWS Cloud Benefits
    
*   AWS Analytics
    
*   AWS Application Integration
    
*   AWS Database
    

All questions

*   All questions
    
*   Correct
    
*   Incorrect
    
*   Skipped
    
*   Marked for review
    

Question 1:
According to the AWS shared responsibility model, which task is the customer's responsibility?

*   Maintaining the infrastructure needed to run Amazon DynamoDB.
    
*   Maintaining Amazon API Gateway infrastructure.
    
*   Updating the guest operating system on Amazon EC2 instances.
    
    (Correct)
    
*   Updating the operating system of AWS Lambda instances.
    

#### Explanation

According to the AWS Shared Responsibility Model updating Amazon EC2 guest operating systems falls under the area of security “in” the cloud which is a customer responsibility. With EC2, AWS manage the underlying platform on which EC2 runs but you must launch and manage your operating systems.

**CORRECT:** "Updating the guest operating system on Amazon EC2 instances" is the correct answer.

**INCORRECT:** "Maintaining the infrastructure needed to run Amazon DynamoDB" is incorrect. This is a responsibility of AWS.

**INCORRECT:** "Updating the operating system of AWS Lambda instances" is incorrect. This is a responsibility of AWS.

**INCORRECT:** "Maintaining Amazon API Gateway infrastructure" is incorrect. This is a responsibility of AWS.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 2:
Which service can a Cloud Practitioner use to configure custom cost and usage limits and enable alerts for when defined thresholds are exceeded?

*   AWS Trusted Advisor
    
*   Consolidated billing
    
*   Cost Explorer
    
*   AWS Budgets
    
    (Correct)
    

#### Explanation

AWS Budgets allows you to set custom budgets to track your cost and usage. With AWS Budgets, you can choose to be alerted by email or SNS notification when actual or forecasted cost and usage exceed your budget threshold, or when your actual RI and Savings Plans' utilization or coverage drops below your desired threshold.

**CORRECT:** "AWS Budgets" is the correct answer.

**INCORRECT:** "Consolidated billing" is incorrect. This is associated with AWS Organizations and provides a single bill across multiple member accounts.

**INCORRECT:** "AWS Trusted Advisor" is incorrect. This service provides guidance on AWS best practices.

**INCORRECT:** "Cost Explorer" is incorrect. This service is used for exploring the costs incurred within your account.

**References:**

[https://aws.amazon.com/aws-cost-management/aws-budgets/](https://aws.amazon.com/aws-cost-management/aws-budgets/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 3:
What AWS service, tool, or feature can help companies identify underutilized Amazon EC2 instances and reduce their costs?

*   Amazon Inspector
    
*   Cost Explorer
    
*   Consolidated billing
    
*   AWS Trusted Advisor
    
    (Correct)
    

#### Explanation

AWS Trusted Advisor provides recommendations that help you follow AWS best practices. Trusted Advisor evaluates your account by using checks. These checks identify ways to optimize your AWS infrastructure, improve security and performance, reduce costs, and monitor service quotas. You can then follow the check recommendations to optimize your services and resources.

**CORRECT:** "AWS Trusted Advisor " is the correct answer (as explained above.)

**INCORRECT:** "Amazon Inspector" is incorrect as Inspector is a fully managed vulnerability assessment tool and does not monitor instance utilization.

**INCORRECT:** "Consolidated billing" is incorrect as this is a feature of AWS Organizations which provides one bill for all the AWS accounts under the master account.

**INCORRECT:** "Cost Explorer" is incorrect as this is a cost dashboard and doesn’t have insight into resource utilization.

**References:**

[https://aws.amazon.com/premiumsupport/technology/trusted-advisor/](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-management-services/](https://digitalcloud.training/aws-cloud-management-services/)

Question 4:
Which AWS service or feature allows a company to receive a single monthly AWS bill when using multiple AWS accounts?

*   Consolidated billing
    
    (Correct)
    
*   Amazon Cloud Directory
    
*   AWS Cost Explorer
    
*   AWS Cost and Usage report
    

#### Explanation

You can use the consolidated billing feature in AWS Organizations to consolidate billing and payment for multiple AWS accounts or multiple Amazon Internet Services Pvt. Ltd (AISPL) accounts. Every organization in AWS Organizations has a _master (payer) account_ that pays the charges of all the _member (linked) accounts_.

Consolidated billing has the following benefits:

• **One bill** – You get one bill for multiple accounts.

• **Easy tracking** – You can track the charges across multiple accounts and download the combined cost and usage data.

• **Combined usage** – You can combine the usage across all accounts in the organization to share the volume pricing discounts, Reserved Instance discounts, and Savings Plans. This can result in a lower charge for your project, department, or company than with individual standalone accounts.

• **No extra fee** – Consolidated billing is offered at no additional cost.

**CORRECT:** "Consolidated billing" is the correct answer.

**INCORRECT:** "Amazon Cloud Directory" is incorrect. Cloud Directory is used for creating cloud-native directories. This is not related to billing.

**INCORRECT:** "AWS Cost Explorer" is incorrect. AWS Cost Explorer has an easy-to-use interface that lets you visualize, understand, and manage your AWS costs and usage over time. It does not centralize billing.

**INCORRECT:** "AWS Cost and Usage report" is incorrect. The AWS Cost & Usage Report lists AWS usage for each service category used by an account and its IAM users in hourly or daily line items, as well as any tags that you have activated for cost allocation purposes.

**References:**

[https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 5:
What should a Cloud Practitioner ensure when designing a highly available architecture on AWS?

*   Servers have low-latency and high throughput network connectivity.
    
*   A single monolithic application component handles all operations.
    
*   There are enough servers to run at peak load available at all times.
    
*   The failure of a single component should not affect the application.
    
    (Correct)
    

#### Explanation

In a highly available system the failure of a single component should not affect the application. This means that if a single component such as an application server fails, there should be other applications servers available that can seamlessly take over operations and ensure the application continues to operate.

**CORRECT:** "The failure of a single component should not affect the application" is the correct answer.

**INCORRECT:** "Servers have low-latency and high throughput network connectivity" is incorrect. It is not necessary for all architectures to have low-latency and high throughput network connectivity and this does not ensure high availability.

**INCORRECT:** "There are enough servers to run at peak load available at all times" is incorrect. This would be wasteful in terms of resources and cost. There should be enough servers available to handle current load with adequate capacity to operate functionally in the event of a system failure. Additional servers can be launched automatically. as the application demand increases.

**INCORRECT:** "A single monolithic application component handles all operations" is incorrect. This is a bad design practice that reduces the availability of the system as the failure of update of any individual component can bring the whole system down.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/real-time-communication-on-aws/high-availability-and-scalability-on-aws.html](https://docs.aws.amazon.com/whitepapers/latest/real-time-communication-on-aws/high-availability-and-scalability-on-aws.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 6:
Which on-premises costs must be included in a Total Cost of Ownership (TCO) calculation when comparing against the AWS Cloud? (Select TWO.)

*   Project management services
    
*   Operating system administration
    
*   Database schema development
    
*   Physical compute hardware
    
    (Correct)
    
*   Network infrastructure in the data center
    
    (Correct)
    

#### Explanation

When performing a TCO analysis you must include all costs you are currently incurring in the on-premises environment that you will not pay for in the AWS Cloud. This should include labor costs for activities that will be reduced or eliminated. Labor costs that will continue to be incurred in the cloud need not be included.

**CORRECT:** "Physical compute hardware" is a correct answer.

**CORRECT:** "Network infrastructure in the data center" is also a correct answer.

**INCORRECT:** "Operating system administration" is incorrect. You don’t need to include these costs as you will continue to incur them in the AWS Cloud.

**INCORRECT:** "Project management services" is incorrect. You don’t need to include these costs as you will continue to incur them in the AWS Cloud.

**INCORRECT:** "Database schema development" is incorrect. You don’t need to include these costs as you will continue to incur them in the AWS Cloud.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/how-aws-pricing-works/aws-pricingtco-tools.html](https://docs.aws.amazon.com/whitepapers/latest/how-aws-pricing-works/aws-pricingtco-tools.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 7:
A company needs a consistent and dedicated connection between AWS resources and an on-premise system.

Which AWS service can fulﬁl this requirement?

*   AWS DataSync
    
*   AWS Direct Connect
    
    (Correct)
    
*   AWS Managed VPN
    
*   Amazon Connect
    

#### Explanation

An AWS Direct Connect connection is a private, dedicated link to AWS. As it does not use the internet, performance is consistent.

The following diagram shows how a corporate data center is connected to AWS using a Direct Connect link via an AWS Direct Connect location:

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-38-25-1ddda98895c9ab1ac808e9c06fa177f0.png)

**CORRECT:** "AWS Direct Connect" is the correct answer.

**INCORRECT:** "AWS Managed VPN" is incorrect. This services uses the public internet so it is not a dedicated link and performance will not be consistent.

**INCORRECT:** "Amazon Connect" is incorrect. Amazon Connect is an easy to use omnichannel cloud contact center that helps companies provide superior customer service at a lower cost

**INCORRECT:** "AWS DataSync" is incorrect. AWS DataSync makes it simple and fast to move large amounts of data online between on-premises storage and Amazon S3, Amazon Elastic File System (Amazon EFS), or Amazon FSx for Windows File Server.

**References:**

[https://aws.amazon.com/directconnect/](https://aws.amazon.com/directconnect/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 8:
A Service Control Policy (SCP) is used to manage the maximum available permissions and is associated with which of the following?

Service control policies (SCPs) manage permissions for which of the following?

*   Availability Zones
    
*   AWS Global Infrastructure
    
*   AWS Regions
    
*   AWS Organizations
    
    (Correct)
    

#### Explanation

Service control policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. SCPs are associated with AWS Organizations and help you to ensure your accounts stay within your organization’s access control guidelines. SCPs are available only in an organization that has all features enabled.

**CORRECT:** "AWS Organizations" is the correct answer.

**INCORRECT:** "AWS Global Infrastructure" is incorrect. SCPs are not associated with the AWS Global Infrastructure.

**INCORRECT:** "AWS Regions" is incorrect. SCPs are not associated with AWS Regions.

**INCORRECT:** "Availability Zones" is incorrect. SCPs are not associated with Availability Zones.

**References:**

[https://docs.aws.amazon.com/organizations/latest/userguide/orgs\_manage\_policies\_scps.html](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-management-services/](https://digitalcloud.training/aws-cloud-management-services/)

Question 9:
Which AWS services offer compute capabilities? (Select TWO.)

*   Amazon ECS
    
    (Correct)
    
*   Amazon CloudHSM
    
*   AWS Lambda
    
    (Correct)
    
*   Amazon DynamoDB
    
*   Amazon EFS
    

#### Explanation

The Amazon Elastic Container Service (ECS) is a compute service that allows you to run Docker containers as tasks on AWS. AWS Lambda is a function as a service offering that provides the ability to run compute functions in response to triggers.

**CORRECT:** "Amazon ECS" is a correct answer.

**CORRECT:** "AWS Lambda" is also a correct answer.

**INCORRECT:** "Amazon DynamoDB" is incorrect. DynamoDB is a database service.

**INCORRECT:** "Amazon EFS" is incorrect. The Elastic File System (EFS) is a file-based storage system.

**INCORRECT:** "Amazon CloudHSM" is incorrect. CloudHSM is a service that is used to securely store and manage encryption keys.

**References:**

[https://aws.amazon.com/lambda/features/](https://aws.amazon.com/lambda/features/)

[https://aws.amazon.com/ecs/](https://aws.amazon.com/ecs/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 10:
What can a Cloud Practitioner use the AWS Total Cost of Ownership (TCO) Calculator for?

*   Estimate a monthly bill for the AWS Cloud resources that will be used
    
*   Enable billing alerts to monitor actual AWS costs compared to estimated costs
    
*   Generate reports that break down AWS Cloud compute costs by duration, resource, or tags
    
*   Estimate savings when comparing the AWS Cloud to an on-premises environment
    
    (Correct)
    

#### Explanation

The TCO calculators allow you to estimate the cost savings when using AWS, compared to on-premises, and provide a detailed set of reports that can be used in executive presentations. The calculators also give you the option to modify assumptions that best meet your business needs.

**CORRECT:** "Estimate savings when comparing the AWS Cloud to an on-premises environment" is the correct answer.

**INCORRECT:** "Generate reports that break down AWS Cloud compute costs by duration, resource, or tags" is incorrect. This describes the AWS Cost & Usage Report.

**INCORRECT:** "Estimate a monthly bill for the AWS Cloud resources that will be used" is incorrect. This describes the AWS Pricing Calculator (or Simple Monthly Calculator).

**INCORRECT:** "Enable billing alerts to monitor actual AWS costs compared to estimated costs" is incorrect. Billing alerts can be enabled using Amazon CloudWatch.

**References:**

[https://aws.amazon.com/tco-calculator/](https://aws.amazon.com/tco-calculator/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 11:
Which combination of steps will enable multi-factor authentication (MFA) on an AWS account? (Select TWO.)

*   Activate the MFA device in the IAM console or by using the AWS CLI.
    
    (Correct)
    
*   Activate AWS Shield on an MFA-compatible device.
    
*   Activate the MFA device by using Amazon GuardDuty.
    
*   Acquire an MFA-compatible device.
    
    (Correct)
    
*   Contact AWS Support to initiate MFA activation.
    

#### Explanation

Multi-factor authentication (MFA) in AWS is a simple best practice that adds an extra layer of protection on top of your user name and password. With MFA enabled, when a user signs in to an AWS Management Console, they will be prompted for their user name and password (the first factor—what they know), as well as for an authentication code from their AWS MFA device (the second factor—what they have).

Taken together, these multiple factors provide increased security for your AWS account settings and resources. You can enable MFA for your AWS account and for individual IAM users you have created under your account. MFA can also be used to control access to AWS service APIs.

You will first need a device capable of providing an application which can support virtual MFA. There are several form factors to choose from:

![](https://img-b.udemycdn.com/redactor/raw/practice_test_question_explanation/2022-07-18_21-35-09-4a450fa9e6575c33f2d068f9c2cb31eb.jpg)

Once you have this device, you will need to register it to your AWS account through the AWS Identity and Access Management (IAM) service.

**CORRECT:** "Acquire an MFA-compatible device" is a correct answer (as explained above.)

**CORRECT:** "Activate the MFA device in the IAM console or by using the AWS CLI" is also a correct answer (as explained above.)

**INCORRECT:** "Contact AWS Support to initiate MFA activation" is incorrect. AWS Support cannot enable MFA for you regardless of which support tier you are using.

**INCORRECT:** "Activate AWS Shield on an MFA-compatible device" is incorrect. AWS Shield is a DDoS mitigation service and has nothing to do with MFA.

**INCORRECT:** "Activate the MFA device by using Amazon GuardDuty'' is incorrect. Amazon GuardDuty is an intelligent threat detection service which has nothing to do with MFA.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_mfa\_enable\_virtual.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_virtual.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 12:
Which AWS service is a fully-managed source control service that hosts secure Git-based repositories?

*   AWS CodePipeline
    
*   AWS CodeCommit
    
    (Correct)
    
*   AWS CodeBuild
    
*   AWS CodeDeploy
    

#### Explanation

AWS CodeCommit is a fully-managed [source control](https://aws.amazon.com/devops/source-control/) service that hosts secure Git-based repositories. It makes it easy for teams to collaborate on code in a secure and highly scalable ecosystem.

CodeCommit eliminates the need to operate your own source control system or worry about scaling its infrastructure. You can use CodeCommit to securely store anything from source code to binaries, and it works seamlessly with your existing Git tools.

**CORRECT:** "AWS CodeCommit" is the correct answer.

**INCORRECT:** "AWS CodeBuild" is incorrect. AWS CodeBuild is a fully managed continuous integration service that compiles source code, runs tests, and produces software packages that are ready to deploy.

**INCORRECT:** "AWS CodeDeploy" is incorrect. CodeDeploy is a deployment service that automates application deployments to Amazon EC2 instances, on-premises instances, serverless Lambda functions, or Amazon ECS services.

**INCORRECT:** "AWS CodePipeline" is incorrect. AWS CodePipeline is a fully managed [continuous delivery](https://aws.amazon.com/devops/continuous-delivery/) service that helps you automate your release pipelines for fast and reliable application and infrastructure updates.

**References:**

[https://aws.amazon.com/codecommit/features/](https://aws.amazon.com/codecommit/features/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 13:
How can an organization gain access to compliance reports natively through the AWS console?

*   AWS Certificate Manager (ACM)
    
*   AWS Identity and Access Management (IAM)
    
*   AWS Security Hub
    
*   AWS Artifact
    
    (Correct)
    

#### Explanation

AWS Artifact is your go-to, central resource for compliance-related information that matters to you. You can access the AWS Artifact console to use AWS Artifact to review, accept, and track the status of AWS agreements

**CORRECT:** "AWS Artifact" is the correct answer (as explained above.)

**INCORRECT:** "AWS Identity and Access Management (IAM)" is incorrect because IAM is related to administering permissions for Users, Groups and Roles within your account, and is not related to compliance.

**INCORRECT:** "AWS Security Hub" is incorrect. AWS Security Hub is not a compliance service. AWS Security Hub is a cloud security posture management service that automates best practice checks, aggregates alerts, and supports automated remediation.

**INCORRECT:** "AWS Certificate Manager (ACM)" is incorrect as ACM manages SSL certificates, not compliance.

**References:  
**[https://docs.aws.amazon.com/artifact/latest/ug/what-is-aws-artifact.html](https://docs.aws.amazon.com/artifact/latest/ug/what-is-aws-artifact.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 14:
A company needs an AWS service that can continuously monitor the company's AWS account. If there are any changes to the architecture, members of the team must be contacted.

Which service will meet these requirements?

*   AWS Trusted Advisor
    
*   AWS Config
    
    (Correct)
    
*   Amazon Macie
    
*   Amazon GuardDuty
    

#### Explanation

AWS Config keeps track of all changes to your resources by invoking the Describe or the List API call for each resource in your account. The service uses those same API calls to capture configuration details for all related resources.

AWS Config also tracks the configuration changes that were not initiated by the API. AWS Config examines the resource configurations periodically and generates configuration items for the configurations that have changed.

You can configure alerts to let team members know if resource configurations have changed. AWS Config can send notifications using Amazon SNS topics.

**CORRECT:** "AWS Config" is the correct answer (as explained above.)

**INCORRECT:** "Amazon Macie" is incorrect. Amazon Macie helps identify Personally identifiable information (PII) data within S3 Bucket and does not track configuration changes.

**INCORRECT:** "Amazon GuardDuty" is incorrect. Amazon GuardDuty is an intelligent threat detection service which has nothing to do with resource configuration.

**INCORRECT:** "AWS Trusted Advisor" is incorrect, as AWS Trusted Advisor provides recommendations that help you follow AWS best practices and does not track resource configuration.

**References:**

[https://docs.aws.amazon.com/config/latest/developerguide/how-does-config-work.htm](https://docs.aws.amazon.com/config/latest/developerguide/how-does-config-work.html)l

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-management-services/](https://digitalcloud.training/aws-cloud-management-services/)

Question 15:
Which benefit of AWS enables companies to replace upfront fixed expenses with variable expenses when using on-demand technology services?

*   High availability
    
*   Global reach
    
*   Pay-as-you-go pricing
    
    (Correct)
    
*   Economies of scale
    

#### Explanation

Pay-as-you-go-pricing is an example of the AWS advantage “Trade capital expense for variable expense**”**. This is documented in the [**Six Advantages of Cloud Computing**](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)**.**

Instead of having to invest heavily in data centers and servers before you know how you’re going to use them, you can pay only when you consume computing resources, and pay only for how much you consume.

**CORRECT:** "Pay-as-you-go pricing" is the correct answer.

**INCORRECT:** "Economies of scale" is incorrect. This is not an example of replacing fixed expenses with variable expenses. The benefit of economies of scale relates to achieving a lower variable cost than you can get on your own. Because usage from hundreds of thousands of customers is aggregated in the cloud, providers such as AWS can achieve higher economies of scale, which translates into lower pay as-you-go prices.

**INCORRECT:** "Global reach" is incorrect. This is most closely associated with the advantage “Go global in minutes”. With AWS you can easily deploy your application in multiple regions around the world with just a few clicks. This means you can provide lower latency and a better experience for your customers at minimal cost.

**INCORRECT:** "High availability" is incorrect. High availability is not related to pricing. Instead, it means you can design your applications to be available with minimum downtime even when disruptions occur.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 16:
A cloud practitioner needs to migrate a 70 TB of data from an on-premises data center into the AWS Cloud. The company has a slow and unreliable internet connection.

Which AWS service can the cloud practitioner leverage to transfer the data?

*   AWS DataSync
    
*   AWS Snowball
    
    (Correct)
    
*   AWS Storage Gateway
    
*   Amazon S3 Glacier
    

#### Explanation

AWS Snowball is a method of transferring the data using a physical device. A Snowball Edge device can hold up to 80 TB so a single device can be used. This transfer method completely avoids the slow and unreliable internet connection.

**CORRECT:** "AWS Snowball" is the correct answer.

**INCORRECT:** "Amazon S3 Glacier" is incorrect. Glacier is used for archiving data in the cloud.

**INCORRECT:** "AWS Storage Gateway" is incorrect. Storage Gateway is a service that offers options for connecting on-premises storage to the cloud.

**INCORRECT:** "AWS DataSync" is incorrect. DataSync uses the internet to transfer data You can utilize Snowcone but that only holds up to 8 TB per device.

**References:**

[https://docs.aws.amazon.com/snowball/latest/developer-guide/specifications.html#specs-v3s-optimized](https://docs.aws.amazon.com/snowball/latest/developer-guide/specifications.html#specs-v3s-optimized)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 17:
Which of the following can be used to identify a specific user who terminated an Amazon RDS DB instance?

*   AWS CloudTrail
    
    (Correct)
    
*   Amazon Inspector
    
*   AWS Trusted Advisor
    
*   Amazon CloudWatch
    

#### Explanation

AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure.

CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services.

This event history simplifies security analysis, resource change tracking, and troubleshooting. In addition, you can use CloudTrail to detect unusual activity in your AWS accounts. These capabilities help simplify operational analysis and troubleshooting.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-02-15_14-02-28-d02df2dc3c706d756e01e43b042724b3.jpg)

**CORRECT:** "AWS CloudTrail" is the correct answer.

**INCORRECT:** "Amazon Inspector" is incorrect. Inspector is used for running an automated security assessment service on cloud resources.

**INCORRECT:** "Amazon CloudWatch" is incorrect. CloudWatch is used for performance monitoring.

**INCORRECT:** "AWS Trusted Advisor" is incorrect. Trusted Advisor helps you to build your AWS resources in accordance with best practices.

**References:**

[https://aws.amazon.com/cloudtrail/](https://aws.amazon.com/cloudtrail/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-monitoring-and-logging-services/](https://digitalcloud.training/aws-monitoring-and-logging-services/)

Question 18:
AWS are able to continue to reduce their pricing due to:

*   The AWS global infrastructure
    
*   Reserved instance pricing
    
*   Pay-as-you go pricing
    
*   Economies of scale
    
    (Correct)
    

#### Explanation

By using cloud computing, you can achieve a lower variable cost than you can get on your own. Because usage from hundreds of thousands of customers is aggregated in the cloud, providers such as AWS can achieve higher economies of scale, which translates into lower pay as-you-go prices.

**CORRECT:** "Economies of scale" is the correct answer.

**INCORRECT:** "The AWS global infrastructure" is incorrect. The global infrastructure is the basis of the AWS platform but it is not the reason prices continue to reduce.

**INCORRECT:** "Pay-as-you go pricing" is incorrect. This pricing model is a benefit but not the reason unit prices are reducing.

**INCORRECT:** "Reserved instance pricing" is incorrect. This pricing model results in savings for customers in specific areas but not the reason for the overall reduction in prices.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 19:
Which of the following are valid best practices for using the AWS Identity and Access Management (IAM) service? (Select TWO.)

*   Use groups to assign permissions to IAM users.
    
    (Correct)
    
*   Create individual IAM users.
    
    (Correct)
    
*   Embed access keys in application code.
    
*   Grant maximum privileges to IAM users.
    
*   Use inline policies instead of customer managed policies.
    

#### Explanation

This is the list of valid IAM best practices:

• [Lock away your AWS account root user access keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials)

• [Create individual IAM users](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users)

• [Use groups to assign permissions to IAM users](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#use-groups-for-permissions)

• [Grant least privilege](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege)

• [Get started using permissions with AWS managed policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#bp-use-aws-defined-policies)

• [Use customer managed policies instead of inline policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#best-practice-managed-vs-inline)

• [Use access levels to review IAM permissions](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#use-access-levels-to-review-permissions)

• [Configure a strong password policy for your users](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#configure-strong-password-policy)

• [Enable MFA](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#enable-mfa-for-privileged-users)

• [Use roles for applications that run on Amazon EC2 instances](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#use-roles-with-ec2)

• [Use roles to delegate permissions](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#delegate-using-roles)

• [Do not share access keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#sharing-credentials)

• [Rotate credentials regularly](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#rotate-credentials)

• [Remove unnecessary credentials](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#remove-credentials)

• [Use policy conditions for extra security](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#use-policy-conditions)

• [Monitor activity in your AWS account](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#keep-a-log)

• [Video presentation about IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#top-practices-video)

**CORRECT:** "Create individual IAM users" is a correct answer.

**CORRECT:** "Use groups to assign permissions to IAM users" is also a correct answer.

**INCORRECT:** "Embed access keys in application code" is incorrect. This is not a best practice; you should always try and avoid embedding any secret credentials and access keys in application code. Instead, it is preferable to use IAM roles to delegate permission to applications.

**INCORRECT:** "Use inline policies instead of customer managed policies" is incorrect. This is not a best practice. You should use customer managed policies instead of inline policies.

**INCORRECT:** "Grant maximum privileges to IAM users" is incorrect. You should instead follow the principle of least privilege and grant the minimum permissions a user needs to perform their job role.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 20:
What is the function of Amazon EC2 Auto Scaling?

*   Automatically updates the EC2 pricing model, based on demand.
    
*   Scales the number of EC2 instances in or out automatically, based on demand.
    
    (Correct)
    
*   Automatically modifies the network throughput of EC2 instances, based on demand.
    
*   Scales the size of EC2 instances up or down automatically, based on demand.
    

#### Explanation

Amazon EC2 Auto Scaling helps you maintain application availability and allows you to automatically add or remove EC2 instances according to conditions you define. You can use the fleet management features of EC2 Auto Scaling to maintain the health and availability of your fleet. You can also use the dynamic and predictive scaling features of EC2 Auto Scaling to add or remove EC2 instances.

**CORRECT:** "Scales the number of EC2 instances in or out automatically, based on demand." is the correct answer.

**INCORRECT:** "Scales the size of EC2 instances up or down automatically, based on demand." is incorrect. Auto Scaling adjusts the number of EC2 instances, not the size of EC2 instances.

**INCORRECT:** "Automatically updates the EC2 pricing model, based on demand." is incorrect. Auto Scaling does not change pricing models

**INCORRECT:** "Automatically modifies the network throughput of EC2 instances, based on demand." is incorrect. Auto Scaling does not modify network throughput for instances.

**References:**

[https://aws.amazon.com/ec2/autoscaling/](https://aws.amazon.com/ec2/autoscaling/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 21:
Which AWS service does AWS Snowball Edge natively support?

*   Amazon EC2
    
    (Correct)
    
*   AWS Database Migration Service (AWS DMS)
    
*   AWS Trusted Advisor
    
*   AWS Server Migration Service (AWS SMS)
    

#### Explanation

You can run Amazon EC2 compute instances hosted on a Snowball Edge with the sbe1, sbe-c, and sbe-g instance types. The sbe1 instance type works on devices with the Snowball Edge Storage Optimized option. The sbe-c instance type works on devices with the Snowball Edge Compute Optimized option. Both the sbe-c and sbe-g instance types work on devices with the Snowball Edge Compute Optimized with GPU option.

**CORRECT:** "Amazon EC2" is the correct answer.

**INCORRECT:** "AWS Server Migration Service (AWS SMS)" is incorrect. AWS SMS does not integrate natively with Snowball Edge.

**INCORRECT:** "AWS Database Migration Service (AWS DMS)" is incorrect. AWS DMS does not integrate natively with Snowball Edge.

**INCORRECT:** "AWS Trusted Advisor" is incorrect. Trusted Advisor does not integrate natively with Snowball Edge.

**References:**

[https://docs.aws.amazon.com/snowball/latest/developer-guide/using-ec2.html#ec2-overview-edge](https://docs.aws.amazon.com/snowball/latest/developer-guide/using-ec2.html#ec2-overview-edge)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 22:
According to the shared responsibility model, which security-related task is the responsibility of the customer?

*   Maintaining physical networking configuration.
    
*   Securing servers and racks at AWS data centers.
    
*   Maintaining server-side encryption.
    
    (Correct)
    
*   Maintaining firewall configurations at a hardware level.
    

#### Explanation

All client-side and server-side encryption is a responsibility of the customer using the AWS Cloud. This can be clearly seen in the shared responsibility model infographic below:

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-02-15_14-11-36-2962b9aa4ba978d8fe6bc78ffa291ddf.jpg)

**CORRECT:** "Maintaining server-side encryption" is the correct answer.

**INCORRECT:** "Securing servers and racks at AWS data centers" is incorrect. This is an AWS responsibility.

**INCORRECT:** "Maintaining firewall configurations at a hardware level" is incorrect. This is an AWS responsibility.

**INCORRECT:** "Maintaining physical networking configuration" is incorrect. This is an AWS responsibility.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 23:
Which AWS hybrid storage service enables a user’s on-premises applications to seamlessly use AWS Cloud storage?

*   Amazon Connect
    
*   AWS Storage Gateway
    
    (Correct)
    
*   AWS Direct Connect
    
*   AWS Backup
    

#### Explanation

AWS Storage Gateway is a hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage. Customers use Storage Gateway to simplify storage management and reduce costs for key hybrid cloud storage use cases.

These include moving tape backups to the cloud, reducing on-premises storage with cloud-backed file shares, providing low latency access to data in AWS for on-premises applications, as well as various migration, archiving, processing, and disaster recovery use cases.

**CORRECT:** "AWS Storage Gateway" is the correct answer.

**INCORRECT:** "AWS Backup" is incorrect. AWS Backup is a fully managed backup service that makes it easy to centralize and automate the backup of data across AWS services. It is not used for connecting on-premises storage to cloud storage.

**INCORRECT:** "Amazon Connect" is incorrect. Amazon Connect is an easy to use omnichannel cloud contact center that helps companies provide superior customer service at a lower cost. It has nothing to do with storing data.

**INCORRECT:** "AWS Direct Connect" is incorrect. AWS Direct Connect is a cloud service solution that makes it easy to establish a dedicated network connection from your premises to AWS. It is not related to storage of data.

**References:**

[https://aws.amazon.com/storagegateway/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc](https://aws.amazon.com/storagegateway/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 24:
What can be used to allow an application running on an Amazon EC2 instance to securely store data in an Amazon S3 bucket without using long-term credentials?

*   Amazon Connect
    
*   AWS IAM role
    
    (Correct)
    
*   AWS IAM access key
    
*   AWS Systems Manager
    

#### Explanation

An IAM _role_ is an IAM identity that you can create in your account that has specific permissions. An IAM role is similar to an IAM user, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. However, instead of being uniquely associated with one person, a role is intended to be assumable by anyone who needs it.

Also, a role does not have standard long-term credentials such as a password or access keys associated with it. Instead, when you assume a role, it provides you with temporary security credentials for your role session.

**CORRECT:** "AWS IAM role" is the correct answer.

**INCORRECT:** "AWS Systems Manager" is incorrect. This service manages Amazon EC2 instances.

**INCORRECT:** "Amazon Connect" is incorrect. This is a contact center service.

**INCORRECT:** "AWS IAM access key" is incorrect. Access keys are considered long-term credentials and therefore should not be embedded on EC2 instances in code. Using a role is more secure

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_roles.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 25:
Which of the following is an advantage for a company running workloads in the AWS Cloud vs on-premises? (Select TWO.)

*   Increased productivity for application development teams.
    
    (Correct)
    
*   Increased time to market for new application features.
    
*   Higher acquisition costs to support elastic workloads.
    
*   Lower overall utilization of server and storage systems.
    
*   Less staff time is required to launch new workloads.
    
    (Correct)
    

#### Explanation

Using AWS cloud services can help development teams to be more productive as they spend less time working on the infrastructure layer as it is provided for them. This additionally means launching new workloads requires less time as you can automate the implementation of the application and there is no underlying hardware layer to configure.

**CORRECT:** "Less staff time is required to launch new workloads" is a correct answer.

**CORRECT:** "Increased productivity for application development teams" is also a correct answer.

**INCORRECT:** "Increased time to market for new application features" is incorrect. AWS services should decrease time to market, not increase time.

**INCORRECT:** "Higher acquisition costs to support elastic workloads" is incorrect. The acquisition costs should be lower, not higher.

**INCORRECT:** "Lower overall utilization of server and storage systems" is incorrect. This is not a benefit of moving to the cloud.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 26:
Which AWS dashboard displays relevant and timely information to help users manage events in progress, and provides proactive notifications to help plan for scheduled activities?

*   AWS Trusted Advisor dashboard
    
*   Amazon CloudWatch dashboard
    
*   AWS Service Health Dashboard
    
*   AWS Personal Health Dashboard
    
    (Correct)
    

#### Explanation

AWS Personal Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you. While the Service Health Dashboard displays the general status of AWS services, Personal Health Dashboard gives you a personalized view into the performance and availability of the AWS services underlying your AWS resources.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-41-44-6a31304d8a5267bea2164a82bceff92d.png)

The dashboard displays relevant and timely information to help you manage events in progress, and provides proactive notification to help you plan for scheduled activities. With Personal Health Dashboard, alerts are triggered by changes in the health of AWS resources, giving you event visibility, and guidance to help quickly diagnose and resolve issues.

**CORRECT:** "AWS Personal Health Dashboard" is the correct answer.

**INCORRECT:** "AWS Service Health Dashboard" is incorrect. This shows the current status of services across regions. However, it does not provide proactive notifications of scheduled activities or guidance of any kind.

**INCORRECT:** "AWS Trusted Advisor dashboard" is incorrect. AWS Trusted Advisor is an online tool that provides you real time guidance to help you provision your resources following AWS best practices.

**INCORRECT:** "Amazon CloudWatch dashboard" is incorrect as this service is used for monitoring performance related information for your infrastructure and resources, not the underlying AWS resources.

**References:**

[https://aws.amazon.com/premiumsupport/technology/personal-health-dashboard/](https://aws.amazon.com/premiumsupport/technology/personal-health-dashboard/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 27:
How should an organization deploy an application running on multiple EC2 instances to ensure that a power failure does not cause an application outage?

*   Launch the EC2 instances into different VPCs
    
*   Launch the EC2 instances into Edge Locations
    
*   Launch the EC2 instances into different Availability Zones
    
    (Correct)
    
*   Launch the EC2 instances in separate regions
    

#### Explanation

If you have multiple EC2 instances that are part of an application, you should deploy them into separate availability zones (AZs). Each AZ has redundant power and is also fed from a different grid. AZs also have low-latency network links which is often advantageous for most applications.

You do not need to deploy into separate regions to prevent a power outage bringing your application down. AZs have redundant power and grids so you are safe deploying your applications into multiple AZs. If you split your applications across regions you introduce latency which may impact your application. You may also run into data sovereignty issues in some cases.

Deploying your EC2 instances into different VPCs is not required and would complicate your application deployment. Also, bear in mind that VPCs within a region use the same underlying infrastructure so deploying into different VPCs may still result in your EC2 instances being deployed into the same AZs. It is a best practice to deploy into separate AZs.

**CORRECT:** "Launch the EC2 instances into different Availability Zones" is the correct answer.

**INCORRECT:** "Launch the EC2 instances in separate regions" is incorrect as described above.

**INCORRECT:** "Launch the EC2 instances into different VPCs" is incorrect as described above.

**INCORRECT:** "Launch the EC2 instances into Edge Locations" is incorrect. You cannot deploy EC2 instances into Edge Locations.

**References:**

[https://aws.amazon.com/about-aws/global-infrastructure/](https://aws.amazon.com/about-aws/global-infrastructure/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-global-infrastructure/](https://digitalcloud.training/aws-global-infrastructure/)

Question 28:
Which AWS service can be used to run Docker containers?

*   Amazon AMI
    
*   Amazon ECR
    
*   Amazon ECS
    
    (Correct)
    
*   AWS Lambda
    

#### Explanation

Amazon Elastic Container Service (ECS) is a highly scalable, high performance container management service that supports Docker containers and allows you to easily run applications on a managed cluster of Amazon EC2 instances.

**CORRECT:** "Amazon ECS" is the correct answer.

**INCORRECT:** "AWS Lambda" is incorrect. AWS Lambda is a serverless technology that lets you run code in response to events as functions

**INCORRECT:** "Amazon ECR" is incorrect. Amazon Elastic Container Registry (ECR) is a fully-managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images

**INCORRECT:** "Amazon AMI" is incorrect. Amazon Machine Images (AMI) store configuration information for Amazon EC2 instances.

**References:**

[https://aws.amazon.com/ecs/](https://aws.amazon.com/ecs/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 29:
According to the AWS Shared responsibility model, which two tasks are the responsibility of AWS? (Select TWO.)

*   Manage customer data.
    
*   Provide physical security for Availability Zones.
    
    (Correct)
    
*   Perform identity and access management.
    
*   Patch the operating system of Amazon S3.
    
    (Correct)
    
*   Encrypt client-side data and authenticate data integrity.
    

#### Explanation

As part of the AWS Shared Responsibility Model, the customer does not have any insight into how physical infrastructure is managed or maintained. The customer is responsible for security _in_ the cloud, whereas AWS are responsible for the security _of_ the cloud.

Also, AWS customers have no insight into how Amazon S3 works behind the scenes, as Amazon S3 is a fully managed object storage service. Users simply use Amazon S3, and AWS manage all the infrastructure, OS patching and maintenance etc. for you.

**CORRECT:** "Provide physical security for Availability Zones” is correct (as explained above.)

**CORRECT:** “Patch the operating system of Amazon S3" is also correct (as explained above.)

**INCORRECT:** "Encrypt client-side data and authenticate data integrity" is incorrect. Customers are responsible for the security of what is in the cloud, including encryption, and how data integrity is managed.

**INCORRECT:** "Perform identity and access management" is incorrect. Only AWS customers can use IAM to provision permissions to Users, Groups, and roles within AWS.

**INCORRECT:** "Manage customer data" is incorrect. AWS does not have an insight into customer data stored as part of AWS, and this is solely the responsibility of the AWS customer to manage their own data.

**References:  
**[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 30:
Which AWS service can act as a hybrid storage solution to connect on-premises workloads with the AWS cloud?

*   AWS Direct Connect
    
*   AWS Storage Gateway
    
    (Correct)
    
*   Amazon Connect
    
*   AWS Backup
    

#### Explanation

AWS Storage Gateway is a hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage. You can use Storage Gateway to simplify storage management and reduce costs for key hybrid cloud storage use cases.

These include moving backups to the cloud, using on-premises file shares backed by cloud storage, and providing low-latency access to data in AWS for on-premises applications.

To support these use cases, the service provides four different types of gateways – Tape Gateway, Amazon S3 File Gateway, Amazon FSx File Gateway, and Volume Gateway – that seamlessly connect on-premises applications to cloud storage, caching data locally for low-latency access.

**CORRECT:** "AWS Storage Gateway" is the correct answer (as explained above.)

**INCORRECT:** "Amazon Connect" is incorrect as Connect is a cloud-based telecommunications service providing managed cloud-based customer contact centers.

**INCORRECT:** "AWS Backup" is incorrect as this is a service which manages backups in a cost-effective, fully managed, policy-based manner.

**INCORRECT:** "AWS Direct Connect" is incorrect. Although Direct Connect is a service for creating hybrid connections to on-premises data centers, it is a direct physical cable connection and not a storage service.

**References:**

[https://aws.amazon.com/storagegateway/](https://aws.amazon.com/storagegateway/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 31:
Which of the following best describes an Availability Zone in the AWS Cloud?

*   One or more edge locations based around the world
    
*   A completely isolated geographic location
    
*   A subnet for deploying resources into
    
*   One or more physical data centers
    
    (Correct)
    

#### Explanation

An Availability Zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity in an AWS Region. AZ’s give customers the ability to operate production applications and databases that are more highly available, fault tolerant, and scalable than would be possible from a single data center.

The diagram below shows how AZs relate to AWS Regions:

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-34-04-aa33e389e016bdf374480fab750ff6d7.png)

**CORRECT:** "One or more physical data centers" is the correct answer.

**INCORRECT:** "A completely isolated geographic location" is incorrect. This is a description of an AWS Region.

**INCORRECT:** "One or more edge locations based around the world" is incorrect. Edge locations are used by Amazon CloudFront for caching content.

**INCORRECT:** "A subnet for deploying resources into" is incorrect. Subnets are created within AZs.

**References:**

[https://aws.amazon.com/about-aws/global-infrastructure/regions\_az/](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-global-infrastructure/](https://digitalcloud.training/aws-global-infrastructure/)

Question 32:
Which AWS service can be used to perform data extract, transform, and load (ETL) operations so you can prepare data for analytics?

*   Amazon S3 Select
    
*   Amazon Athena
    
*   Amazon QuickSight
    
*   AWS Glue
    
    (Correct)
    

#### Explanation

AWS Glue is a serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development. AWS Glue provides all of the capabilities needed for data integration so that you can start analyzing your data and putting it to use in minutes instead of months.

AWS Glue provides both visual and code-based interfaces to make data integration easier. Users can easily find and access data using the AWS Glue Data Catalog. Data engineers and ETL (extract, transform, and load) developers can visually create, run, and monitor ETL workflows with a few clicks in AWS Glue Studio.

See how AWS Glue works with ETL workloads:

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-02-15_14-05-14-0398c60c3f356928be4c67de7268f635.jpg)

**CORRECT:** "AWS Glue" is the correct answer.

**INCORRECT:** "Amazon QuickSight" is incorrect. Amazon QuickSight is a cloud-native, serverless, business intelligence service.

**INCORRECT:** "Amazon Athena" is incorrect. Amazon Athena is a serverless, interactive query service to query data and analyze big data in Amazon S3 using standard SQL

**INCORRECT:** "Amazon S3 Select" is incorrect. This service enables applications to retrieve only a subset of data from an object by using simple SQL expressions.

**References:**

[https://aws.amazon.com/glue/](https://aws.amazon.com/glue/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-analytics-services/](https://digitalcloud.training/aws-analytics-services/)

Question 33:
A Cloud Practitioner requires a simple method to identify if unrestricted access to resources has been allowed by security groups. Which service can the Cloud Practitioner use?

*   Amazon CloudWatch
    
*   AWS CloudTrail
    
*   AWS Trusted Advisor
    
    (Correct)
    
*   VPC Flow Logs
    

#### Explanation

AWS Trusted Advisor checks security groups for rules that allow unrestricted access (0.0.0.0/0) to specific ports. Unrestricted access increases opportunities for malicious activity (hacking, denial-of-service attacks, loss of data). The ports with highest risk are flagged red, and those with less risk are flagged yellow. Ports flagged green are typically used by applications that require unrestricted access, such as HTTP and SMTP.

The following image shows the results of the security group checks in an AWS account:

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2020-11-24_08-54-13-779777916b3890c0dc629727ac313c40.jpg)

**CORRECT:** "AWS Trusted Advisor" is the correct answer.

**INCORRECT:** "Amazon CloudWatch" is incorrect. CloudWatch is used for performance monitoring.

**INCORRECT:** "VPC Flow Logs" is incorrect. VPC Flow Logs are used to capture network traffic information, they will not easily identify unrestricted security groups.

**INCORRECT:** "AWS CloudTrail" is incorrect. This service is used for auditing API actions

**References:**

[https://aws.amazon.com/premiumsupport/technology/trusted-advisor/](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 34:
Which of the following statements are security principles within the AWS Well-Architected Framework? (Select TWO.)

*   Protect data in transit and at rest.
    
    (Correct)
    
*   Perform operations as code.
    
*   Analyze and attribute expenditures.
    
*   Deploy globally in minutes.
    
*   Monitor, alert, and audit actions and changes to AWS resources.
    
    (Correct)
    

#### Explanation

Ongoing monitoring with alerting and remediation actions is a critical part of a coherent security posture. With ongoing monitoring, you can make sure any potential threats or security concerns can be remediated as soon as possible.  
Secondly, protecting data both in transit and at rest is a vital part of a security procedure which ensures that no data is read by anyone who shouldn’t have access to it.

**CORRECT:** "Monitor, alert, and audit actions and changes to AWS resources" is the correct answer (as explained above.)

**CORRECT:** "Protect data in transit and at rest" is also a correct answer (as explained above.)

**INCORRECT:** "Analyze and attribute expenditures" is incorrect as this relates specifically to cost optimization

**INCORRECT:** "Deploy globally in minute" is incorrect. This advantage of the cloud can help with reliability, scalability, and performance efficiency however security is not affected by the ability to host globally distributed applications.

**INCORRECT:** "Perform operations as code" is incorrect. Operations as code can help tangentially with providing a strong security posture but performing operations as code is more associated with reliability.

**References:**

[https://aws.amazon.com/architecture/well-architected/](https://aws.amazon.com/architecture/well-architected/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 35:
A company plan to move the application development to AWS. Which benefits can they achieve when developing and running applications in the AWS Cloud compared to on-premises? (Select TWO.)

*   AWS takes care of application security patching.
    
*   AWS automatically replicates all data globally.
    
*   AWS will fully manage the entire application.
    
*   AWS can accommodate large changes in application demand.
    
    (Correct)
    
*   AWS makes it easy to implement high availability.
    
    (Correct)
    

#### Explanation

AWS provides many options for high availability including multiple availability zones within Regions and multiple Regions around the world. There are also many options to leverage durable data storage, message buses, databases.

AWS have a huge global infrastructure with massive amounts of capacity. It is therefore very easy to accommodate large changes in application demand and this can often be seamless to your application.

**CORRECT:** "AWS makes it easy to implement high availability" is a correct answer.

**CORRECT:** "AWS can accommodate large changes in application demand" is also a correct answer.

**INCORRECT:** "AWS automatically replicates all data globally" is incorrect. This is not true; data is not replicated globally unless you configure it do so.

**INCORRECT:** "AWS will fully manage the entire application" is incorrect. This is not true; AWS will not manage your application.

**INCORRECT:** "AWS takes care of application security patching" is incorrect. AWS take care of security patches for the underlying infrastructure but not your application.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 36:
A user needs an automated security assessment report that will identify unintended network access to Amazon EC2 instances and vulnerabilities on those instances.

Which AWS service will provide this assessment report?

*   EC2 security groups
    
*   AWS Conﬁg
    
*   Amazon Macie
    
*   Amazon Inspector
    
    (Correct)
    

#### Explanation

Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. Amazon Inspector automatically assesses applications for exposure, vulnerabilities, and deviations from best practices.

After performing an assessment, Amazon Inspector produces a detailed list of security findings prioritized by level of severity. These findings can be reviewed directly or as part of detailed assessment reports which are available via the Amazon Inspector console or API.

**CORRECT:** "Amazon Inspector" is the correct answer.

**INCORRECT:** "EC2 security groups" is incorrect. Security groups are instance-level firewalls used for controlling network traffic reaching and leaving EC2 instances.

**INCORRECT:** "AWS Conﬁg" is incorrect. AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources.

**INCORRECT:** "Amazon Macie" is incorrect. Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect sensitive data in AWS.

**References:**

[https://aws.amazon.com/inspector/](https://aws.amazon.com/inspector/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 37:
Which technology can automatically adjust compute capacity as demand for an application increases or decreases?

*   High availability
    
*   Load balancing
    
*   Auto Scaling
    
    (Correct)
    
*   Fault tolerance
    

#### Explanation

Amazon EC2 Auto Scaling helps you maintain application availability and allows you to automatically add or remove EC2 instances according to conditions you define. You can use the fleet management features of EC2 Auto Scaling to maintain the health and availability of your fleet.

You can also use the dynamic and predictive scaling features of EC2 Auto Scaling to add or remove EC2 instances. Dynamic scaling responds to changing demand and predictive scaling automatically schedules the right number of EC2 instances based on predicted demand. Dynamic scaling and predictive scaling can be used together to scale faster.

The image below shows an example where an Auto Scaling group is configured to ensure the average CPU of instances in the ASG does not exceed 60%. An additional instance is being launched as the actual load is 71.5%.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-02-15_14-38-39-26e362143fe4d040ca4ba3b1ed1bdc90.jpg)

**CORRECT:** "Auto Scaling" is the correct answer.

**INCORRECT:** "Load balancing" is incorrect. Load balancing is not about compute capacity but ensuring connections are distributed across multiple instances.

**INCORRECT:** "Fault tolerance" is incorrect. Fault tolerance is related to the architecture of an application that ensures that the failure of any single component does not affect the application.

**INCORRECT:** "High availability" is incorrect. High availability ensures the maximum uptime for your application by designing the system to recover from failure.

**References:**

[https://aws.amazon.com/ec2/autoscaling/](https://aws.amazon.com/ec2/autoscaling/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-compute-services/](https://digitalcloud.training/aws-compute-services/)

Question 38:
Which Amazon EC2 tool acts as a virtual firewall to control inbound and outbound traffic to an EC2 instance?

*   Security group
    
    (Correct)
    
*   Network access control list (ACL)
    
*   AWS WAF
    
*   AWS Shield
    

#### Explanation

A security group acts as a virtual firewall, controlling the traffic that is allowed to reach and leave the resources that it is associated with. For example, after you associate a security group with an EC2 instance, it controls the inbound and outbound traffic for the instance.

**CORRECT:** "Security Group" is the correct answer (as explained above.)

**INCORRECT:** "AWS Shield" is incorrect. AWS Shield is a managed Distributed Denial of Service (DDoS) protection service and does not control traffic.

**INCORRECT:** "AWS WAF" is incorrect, as the WAF is a Web Application Firewall - something that is placed in front of your web applications outside of your VPC - whereas security groups live within your VPC, controlled instance specific inbound and outbound traffic.

**INCORRECT:** "Network access control list (ACL)" is incorrect. Although Network ACLs are virtual firewalls which control access within a VPC, Network ACLs exist on the subnet level, not on the instance level.

**References:**

[https://docs.aws.amazon.com/vpc/latest/userguide/VPC\_SecurityGroups.html](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html)

Question 39:
Which AWS service should a Cloud Practitioner use to automate conﬁguration management using Puppet?

*   AWS OpsWorks
    
    (Correct)
    
*   AWS Conﬁg
    
*   AWS CloudFormation
    
*   AWS Systems Manager
    

#### Explanation

AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet. Chef and Puppet are automation platforms that allow you to use code to automate the configurations of your servers.

OpsWorks lets you use Chef and Puppet to automate how servers are configured, deployed, and managed across your [Amazon EC2](https://aws.amazon.com/ec2/) instances or on-premises compute environments,

**CORRECT:** "AWS OpsWorks" is the correct answer.

**INCORRECT:** "AWS Conﬁg" is incorrect. AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources.

**INCORRECT:** "AWS CloudFormation" is incorrect. AWS CloudFormation provides a common language for you to model and provision AWS and third party application resources in your cloud environment.

**INCORRECT:** "AWS Systems Manager" is incorrect. AWS Systems Manager gives you visibility and control of your infrastructure on AWS. Systems Manager provides a unified user interface so you can view operational data from multiple AWS services and allows you to automate operational tasks across your AWS resources.

**References:**

[https://aws.amazon.com/opsworks/](https://aws.amazon.com/opsworks/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 40:
A company is migrating virtual machines (VMs) from their data center to the AWS Cloud. The company plans to deploy these migrated machines on Amazon EC2.

Which cloud computing model will the company use for this operation?

*   Function as a Service (FaaS)
    
*   Software as a Service (SaaS)
    
*   Platform as a Service (PaaS)
    
*   Infrastructure as a Service (IaaS)
    
    (Correct)
    

#### Explanation

Infrastructure as a Service (IaaS) is a type of cloud computing service that offers essential compute, storage, and networking resources on demand, on a pay-as-you-go basis. IaaS is one of the four types of cloud services, along with software as a service (SaaS), platform as a service (PaaS), and Function as a Service (FaaS).

![](https://img-b.udemycdn.com/redactor/raw/practice_test_question_explanation/2022-07-18_21-49-33-af1bdb7cea9a476a079a0f84d99c8688.jpg)

**CORRECT:** "Infrastructure as a Service (IaaS)" is the correct answer (as explained above.)

**INCORRECT:** "Platform as a Service (PaaS)" is incorrect. Platform as a service (PaaS) is a cloud computing model where a third-party provider delivers hardware and software tools to users over the internet. Usually, these tools are needed for application development.

**INCORRECT:** "Function as a Service (FaaS)" is incorrect, FaaS (Function-as-a-Service) is a type of cloud-computing service that allows you to execute code in response to events i.e. Lambda functions within AWS.

**INCORRECT:** "Software as a Service (SaaS)" is incorrect. Software as a service is a software licensing and delivery model in which software is licensed on a subscription basis and is centrally hosted.

**References:**

[https://magenest.com/en/aws-iaas-paas-saas/](https://magenest.com/en/aws-iaas-paas-saas/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 41:
How can an organization take advantage of tiered pricing across multiple business units within an organization?

*   Cost Explorer utilization reports.
    
*   All Upfront Reserved Instances.
    
*   AWS Organizations consolidated billing.
    
    (Correct)
    
*   AWS Organizations service control policies (SCPs).
    

#### Explanation

You can use the consolidated billing feature in AWS Organizations to consolidate billing and payment for multiple AWS accounts. This can be used for multiple business units within an organization.

Consolidated billing has the following benefits:

*   **One bill** – You get one bill for multiple accounts.
    
*   **Easy tracking** – You can track the charges across multiple accounts and download the combined cost and usage data.
    
*   **Combined usage** – You can combine the usage across all accounts in the organization to share the volume pricing discounts, Reserved Instance discounts, and Savings Plans. This can result in a lower charge for your project, department, or company than with individual standalone accounts.
    
*   **No extra fee** – Consolidated billing is offered at no additional cost.
    

Consolidated billing includes:

· **Paying Account** – independent and cannot access resources of other accounts

· **Linked Accounts** – all linked accounts are independent

**CORRECT:** "AWS Organizations consolidated billing" is the correct answer (as explained above.)

**INCORRECT:** "AWS Organizations service control policies (SCPs)" is incorrect. Service Control Policies set a limit of the maximum amount of permissions within Organizational Units (OUs) within AWS Organizations.

**INCORRECT:** "All Upfront Reserved Instances" is incorrect, as Reserved Instances are an EC2 instance pricing option, which has nothing to do with billing an organization.

**INCORRECT:** "Cost Explorer utilization reports" is incorrect. Cost Explorer does not allocate a billing strategy, and only shows billing information.

**References:**

[https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-management-services/](https://digitalcloud.training/aws-cloud-management-services/)

Question 42:
Which Amazon EC2 pricing model should be avoided if a workload cannot accept interruption if capacity becomes temporarily unavailable?

*   Convertible Reserved Instances
    
*   On-Demand Instances
    
*   Spot Instances
    
    (Correct)
    
*   Standard Reserved Instances
    

#### Explanation

Amazon EC2 Spot Instances let you take advantage of unused EC2 capacity in the AWS cloud. Spot Instances are available at up to a 90% discount compared to On-Demand prices.

The downside is that if capacity becomes temporarily unavailable, your instances may be terminated.

**CORRECT:** "Spot Instances" is the correct answer.

**INCORRECT:** "On-Demand Instances" is incorrect. On-demand instances are not subject to interruption if capacity becomes temporarily unavailable.

**INCORRECT:** "Standard Reserved Instances" is incorrect. Reserved instances are not subject to interruption if capacity becomes temporarily unavailable

**INCORRECT:** "Convertible Reserved Instances" is incorrect. Reserved instances are not subject to interruption if capacity becomes temporarily unavailable.

**References:**

[https://aws.amazon.com/ec2/spot/](https://aws.amazon.com/ec2/spot/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 43:
A user has limited knowledge of AWS services, but wants to quickly deploy a scalable Node.js application in an Amazon VPC.

Which service should be used to deploy the application?

*   Amazon LightSail
    
*   AWS CloudFormation
    
*   Amazon EC2
    
*   AWS Elastic Beanstalk
    
    (Correct)
    

#### Explanation

AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

You can simply upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. At the same time, you retain full control over the AWS resources powering your application and can access the underlying resources at any time.

**CORRECT:** "AWS Elastic Beanstalk" is the correct answer.

**INCORRECT:** "Amazon LightSail" is incorrect. LightSail is a good service to use when you don’t have good knowledge of AWS. However, you cannot deploy a scalable node.js application into a VPC.

**INCORRECT:** "AWS CloudFormation" is incorrect. CloudFormation is used for automating the deployment of infrastructure resources in AWS.

**INCORRECT:** "Amazon EC2" is incorrect. This would require more expertise that using Elastic Beanstalk.

**References:**

[https://aws.amazon.com/elasticbeanstalk/](https://aws.amazon.com/elasticbeanstalk/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/additional-aws-services/](https://digitalcloud.training/additional-aws-services/)

Question 44:
A company needs to use third-party software for its workload on AWS.

Is there a feature or service of AWS that the company can use to purchase the software?

*   AWS Managed Services
    
*   AWS License Manager
    
*   AWS Marketplace
    
    (Correct)
    
*   AWS Resource Access Manager
    

#### Explanation

AWS Marketplace is a curated digital catalog that makes it easy for organizations to discover, procure, entitle, provision, and govern third-party software. You can find thousands of software listings from popular categories like security, business applications, and data & analytics, and across specific industries, such as healthcare, financial services, and public sector.

**CORRECT:** "AWS Marketplace" is the correct answer (as explained above.)

**INCORRECT:** "AWS Managed Service" is incorrect as this describes services in which AWS customers don’t have to provision their own infrastructure.

**INCORRECT:** "AWS License Manager" is incorrect as it is a service that makes it easier for you to manage Software Licenses.

**INCORRECT:** "AWS Resource Access Manager" is incorrect as it is a service that helps you to securely share your resources across AWS accounts, within your organization or organizational units (OUs) within AWS and has nothing to do with third party services.

**References:**

[https://aws.amazon.com/mp/marketplace-service/overview/](https://aws.amazon.com/mp/marketplace-service/overview/)

Question 45:
Which AWS service is used to send both text and email messages from distributed applications?

*   Amazon Simple Workflow Service (Amazon SWF)
    
*   Amazon Simple Queue Service (Amazon SQS)
    
*   Amazon Simple Notiﬁcation Service (Amazon SNS)
    
    (Correct)
    
*   Amazon Simple Email Service (Amazon SES)
    

#### Explanation

Amazon Simple Notification Service (SNS) is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-35-05-1deb0c82e6ddd66e2cf5bea59aeb3458.png)

Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging. Using Amazon SNS topics, your publisher systems can fan out messages to a large number of subscriber endpoints for parallel processing, including [Amazon SQS](https://aws.amazon.com/sqs/) queues, [AWS Lambda](https://aws.amazon.com/lambda/) functions, and HTTP/S webhooks.

Additionally, SNS can be used to fan out notifications to end users using mobile push, SMS, and email.

**CORRECT:** "Amazon Simple Notiﬁcation Service (Amazon SNS)" is the correct answer.

**INCORRECT:** "Amazon Simple Email Service (Amazon SES)" is incorrect. This service is used for sending email but not SMS text messages.

**INCORRECT:** "Amazon Simple Workflow Service (Amazon SWF)" is incorrect. Amazon SWF helps developers build, run, and scale background jobs that have parallel or sequential steps. You can think of Amazon SWF as a fully-managed state tracker and task coordinator in the Cloud.

**INCORRECT:** "Amazon Simple Queue Service (Amazon SQS)" is incorrect. Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

**References:**

[https://aws.amazon.com/sns/](https://aws.amazon.com/sns/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-application-integration/](https://digitalcloud.training/aws-application-integration/)

Question 46:
Which AWS service can be used to load data from Amazon S3, transform it, and move it to another destination?

*   Amazon Kinesis
    
*   Amazon RedShift
    
*   AWS Glue
    
    (Correct)
    
*   Amazon EMR
    

#### Explanation

AWS Glue is an Extract, Transform, and Load (ETL) service. You can use AWS Glue with data sources on Amazon S3, RedShift and other databases. With AWS Glue you transform and move the data to various destinations. It is used to prepare and load data for analytics.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-39-16-d3561ad49e055562cb4c1fa687dc8b64.png)

**CORRECT:** "AWS Glue" is the correct answer.

**INCORRECT:** "Amazon RedShift" is incorrect. Amazon RedShift is a data warehouse. With a data warehouse you load data from other databases such as transactional SQL databases and run analysis. You can analyze data using SQL and Business Intelligence tools.

**INCORRECT:** "Amazon EMR" is incorrect. Amazon EMR is a managed Hadoop framework running on EC2 and S3. It is used for analyzing data, not for ETL.

**INCORRECT:** "Amazon Kinesis" is incorrect. Amazon Kinesis is used for collecting, processing and analyzing real-time streaming data.

**References:**

[https://aws.amazon.com/glue/](https://aws.amazon.com/glue/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-analytics-services/](https://digitalcloud.training/aws-analytics-services/)

Question 47:
Which of the statements below is correct in relation to Consolidated Billing? (Select TWO.)

*   You receive a single bill for multiple accounts
    
    (Correct)
    
*   You receive one bill per AWS account
    
*   You can combine usage and share volume pricing discounts
    
    (Correct)
    
*   You pay a fee per linked account
    
*   You are charged a fee per user
    

#### Explanation

Consolidated billing has the following benefits:

One bill – You get one bill for multiple accounts.

Easy tracking – You can track the charges across multiple accounts and download the combined cost and usage data.

Combined usage – You can combine the usage across all accounts in the organization to share the volume pricing discounts and Reserved Instance discounts. This can result in a lower charge for your project, department, or company than with individual standalone accounts.

**CORRECT:** "You receive a single bill for multiple accounts" is a correct answer.

**CORRECT:** "You can combine usage and share volume pricing discounts" is also a correct answer.

**INCORRECT:** "You receive one bill per AWS account" is incorrect as you receive a single bill for multiple accounts.

**INCORRECT:** "You pay a fee per linked account" is incorrect as you do not pay a fee.

**INCORRECT:** "You are charged a fee per user" is incorrect as you do not pay a fee.

**References:**

[https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 48:
An application has highly dynamic usage patterns. Which characteristics of the AWS Cloud make it cost-effective for this type of workload? (Select TWO.)

*   Reliability
    
*   Strict security
    
*   Elasticity
    
    (Correct)
    
*   Pay-as-you-go pricing
    
    (Correct)
    
*   High availability
    

#### Explanation

AWS is a cost-effective for dynamic workloads because it is elastic, meaning your workload can scale based on demand. And because you only pay for what you use (pay-as-you-go pricing).

**CORRECT:** "Elasticity" is the correct answer.

**CORRECT:** "Pay-as-you-go pricing" is the correct answer.

**INCORRECT:** "High availability" is incorrect. This is not a characteristic that results in cost-effectiveness.

**INCORRECT:** "Strict security" is incorrect. This is not a characteristic that results in cost-effectiveness.

**INCORRECT:** "Reliability" is incorrect. This is not a characteristic that results in cost-effectiveness.

**References:**

[https://aws.amazon.com/architecture/](https://aws.amazon.com/architecture/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 49:
A Cloud Practitioner noticed that IP addresses that are owned by AWS are being used to attempt to flood ports on some of the company’s systems.

To whom should the issue be reported?

*   AWS Professional Services
    
*   AWS Trust & Safety team
    
    (Correct)
    
*   AWS Technical Account Manager (TAM)
    
*   AWS Partner Network (APN)
    

#### Explanation

If you suspect that AWS resources are used for abusive purposes, contact the AWS Trust & Safety team using the [Report Amazon AWS abuse form](https://aws.amazon.com/forms/report-abuse), or by contacting [abuse@amazonaws.com](mailto:abuse@amazonaws.com). Provide all the necessary information, including logs in plaintext, email headers, and so on, when you submit your request.

**CORRECT:** "AWS Trust & Safety team" is the correct answer.

**INCORRECT:** "AWS Professional Services" is incorrect. This is not the correct team.

**INCORRECT:** "AWS Partner Network (APN)" is incorrect. This is not the correct team.

**INCORRECT:** "AWS Technical Account Manager (TAM)" is incorrect. This is not the correct team.

**References:**

[https://aws.amazon.com/premiumsupport/knowledge-center/report-aws-abuse/](https://aws.amazon.com/premiumsupport/knowledge-center/report-aws-abuse/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 50:
Which AWS service helps customers meet corporate, contractual, and regulatory compliance requirements for data security by using dedicated hardware appliances within the AWS Cloud?

*   AWS CloudHSM
    
    (Correct)
    
*   AWS Key Management Service (AWS KMS)
    
*   AWS Secrets Manager
    
*   AWS Directory Service
    

#### Explanation

The AWS CloudHSM service helps you meet corporate, contractual, and regulatory compliance requirements for data security by using dedicated Hardware Security Module (HSM) instances within the AWS cloud. AWS CloudHSM enables you to easily generate and use your own encryption keys on the AWS Cloud.

**CORRECT:** "AWS CloudHSM" is the correct answer.

**INCORRECT:** "AWS Secrets Manager" is incorrect. AWS Secrets Manager enables you to easily rotate, manage, and retrieve database credentials, API keys, and other secrets throughout their lifecycle.

**INCORRECT:** "AWS Key Management Service (AWS KMS)" is incorrect. This service is also involved with creating and managing encryption keys but does not use dedicated hardware.

**INCORRECT:** "AWS Directory Service" is incorrect. AWS Directory Service for Microsoft Active Directory, also known as AWS Managed Microsoft AD, enables your directory-aware workloads and AWS resources to use managed Active Directory in the AWS Cloud.

**References:**

[https://aws.amazon.com/cloudhsm/features/](https://aws.amazon.com/cloudhsm/features/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 51:
Which cloud architecture design principle is supported by deploying workloads across multiple Availability Zones?

*   Design for failure.
    
    (Correct)
    
*   Design for agility.
    
*   Automate infrastructure.
    
*   Enable elasticity.
    

#### Explanation

Amazon EC2 instances can be deployed in an Amazon VPC across multiple Availability Zones. You would then typically use an Elastic Load Balancer (ELB) to distribute load between the available instances. This architecture enables high availability as if a single instance fails or if something fails that causes an outage in an entire Availability Zone, the application still has available instances to continue to service demand.

**CORRECT:** "Design for failure" is the correct answer.

**INCORRECT:** "Design for agility" is incorrect. This is not an example of agility; it is an example of high availability and fault tolerance.

**INCORRECT:** "Automate infrastructure" is incorrect. This is not an example of automating.

**INCORRECT:** "Enable elasticity" is incorrect. This is not an example of elasticity. Elasticity would be enabled by using Amazon EC2 Auto Scaling.

**References:**

[https://aws.amazon.com/architecture/well-architected/](https://aws.amazon.com/architecture/well-architected/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 52:
Which AWS-managed service can be used to process vast amounts of data using a hosted Hadoop framework?

*   Amazon EMR
    
    (Correct)
    
*   Amazon Redshift
    
*   Amazon Athena
    
*   Amazon DynamoDB
    

#### Explanation

Amazon Elastic Map Reduce (EMR) is a web service that enables businesses, researchers, data analysts, and developers to easily and cost-effectively process vast amounts of data. EMR utilizes a hosted Hadoop framework running on Amazon EC2 and Amazon S3.

**CORRECT:** "Amazon EMR" is the correct answer.

**INCORRECT:** "Amazon DynamoDB" is incorrect. DynamoDB is not a hosted Hadoop framework, it is a no-SQL database.

**INCORRECT:** "Amazon Athena" is incorrect. Amazon Athena is a serverless, interactive query service to query data and analyze big data in Amazon S3 using standard SQL

**INCORRECT:** "Amazon Redshift" is incorrect. Amazon Redshift is a fast, simple, cost-effective data warehousing service.

**References:**

[https://aws.amazon.com/emr/](https://aws.amazon.com/emr/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 53:
An eCommerce company plans to use the AWS Cloud to quickly deliver new functionality in an iterative manner, minimizing the time to market.

Which feature of the AWS Cloud provides this functionality?

*   Cost effectiveness
    
*   Fault tolerance
    
*   Elasticity
    
*   Agility
    
    (Correct)
    

#### Explanation

In a cloud computing environment, new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes.

This results in a dramatic increase in agility for the organization, since the cost and time it takes to experiment and develop is significantly lower.

**CORRECT:** "Agility" is the correct answer.

**INCORRECT:** "Elasticity" is incorrect. Elasticity enables infrastructure to scale based on demand and helps applications perform and be cost effective. It does not reduce time to market.

**INCORRECT:** "Fault tolerance" is incorrect as this is involved with ensuring applications stay available in the event of a fault.

**INCORRECT:** "Cost effectiveness" is incorrect. The AWS Cloud can be cost effective but this is not the benefit that allows faster time to market.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 54:
Which of the following should be used to improve the security of access to the AWS Management Console? (Select TWO.)

*   AWS Certiﬁcate Manager
    
*   Security group rules
    
*   AWS Multi-Factor Authentication (AWS MFA)
    
    (Correct)
    
*   AWS Secrets Manager
    
*   Strong password policies
    
    (Correct)
    

#### Explanation

For extra security, AWS recommends that you require multi-factor authentication (MFA) for all users in your account. With MFA, users have a device that generates a response to an authentication challenge.

Both the user's credentials (something you know) and the device-generated response (something you have) are required to complete the sign-in process. If a user's password or access keys are compromised, your account resources are still secure because of the additional authentication requirement.

![](https://img-b.udemycdn.com/redactor/raw/2020-06-13_05-37-33-c65dfc24318841c97e0722e4b5cef6aa.png)

Additionally, strong password policies should be used to enforce measures including minimum password length, complexity, and password reuse restrictions.

**CORRECT:** "AWS Multi-Factor Authentication (AWS MFA)" is a correct answer.

**CORRECT:** "Strong password policies" is also a correct answer.

**INCORRECT:** "AWS Secrets Manager" is incorrect. This service enables you to easily rotate, manage, and retrieve database credentials, API keys, and other secrets throughout their lifecycle.

**INCORRECT:** "AWS Certiﬁcate Manager" is incorrect. This service is used for creating SSL/TLS certificates for use with HTTPS connections.

**INCORRECT:** "Security group rules" is incorrect as these are used to restrict traffic to/from your EC2 instances.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 55:
Which of the following tasks can a user perform to optimize Amazon EC2 costs? (Select TWO.)

*   Set a budget to limit spending on Amazon EC2 instances using AWS Budgets.
    
*   Create users in a single Region to reduce the spread of EC2 instances globally.
    
*   Create a policy to restrict IAM users from accessing the Amazon EC2 console.
    
*   Purchase Amazon EC2 Reserved Instances.
    
    (Correct)
    
*   Implement Auto Scaling groups to add and remove instances based on demand.
    
    (Correct)
    

#### Explanation

Cost optimization can include using Auto Scaling groups to scale the number of EC2 instances according to actual demand. Also, using Amazon EC2 reserved instances for suitable workloads is a good way of optimizing costs over the longer term.

**CORRECT:** "Implement Auto Scaling groups to add and remove instances based on demand" is a correct answer.

**CORRECT:** "Purchase Amazon EC2 Reserved Instances" is also a correct answer.

**INCORRECT:** "Create a policy to restrict IAM users from accessing the Amazon EC2 console" is incorrect. This is not an optimization strategy; it will just prevent access completely which could be going too far.

**INCORRECT:** "Set a budget to limit spending on Amazon EC2 instances using AWS Budgets" is incorrect. You can use AWS Budgets to notify you of spend but not to actually limit spend.

**INCORRECT:** "Create users in a single Region to reduce the spread of EC2 instances globally" is incorrect. You cannot create users in a single Region, all IAM Users are global.

**References:**

[https://aws.amazon.com/aws-cost-management/aws-cost-optimization/](https://aws.amazon.com/aws-cost-management/aws-cost-optimization/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-billing-and-pricing/](https://digitalcloud.training/aws-billing-and-pricing/)

Question 56:
A Cloud Practitioner wants to configure the AWS CLI for programmatic access to AWS services. Which credential components are required? (Select TWO.)

*   A secret access key
    
    (Correct)
    
*   A public key
    
*   An access key ID
    
    (Correct)
    
*   A private key
    
*   An IAM Role
    

#### Explanation

Access keys are long-term credentials for an IAM user or the AWS account root user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API (directly or using the AWS SDK).

Access keys consist of two parts: an access key ID (for example, AKIAIOSFODNN7EXAMPLE) and a secret access key (for example, wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY).

Like a user name and password, you must use both the access key ID and secret access key together to authenticate your requests. Manage your access keys as securely as you do your user name and password.

**CORRECT:** "An access key ID" is a correct answer.

**CORRECT:** "A secret access key" is also a correct answer.

**INCORRECT:** "A public key" is incorrect. Public/private keys are used for encryption and are also associated with the key pairs used to authenticate to EC2 instances.

**INCORRECT:** "A private key" is incorrect. Public/private keys are used for encryption and are also associated with the key pairs used to authenticate to EC2 instances.

**INCORRECT:** "An IAM Role" is incorrect. IAM Roles are not used for configuring the CLI for programmatic access. They can be used for delegating access to AWS services and cross-account access.

**References:**

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_credentials\_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-identity-and-access-management/](https://digitalcloud.training/aws-identity-and-access-management/)

Question 57:
A Cloud Practitioner is re-architecting a monolithic application. Which design principles for cloud architecture do AWS recommend? (Select TWO.)

*   Use self-managed servers.
    
*   Implement manual scalability.
    
*   Design for scalability.
    
    (Correct)
    
*   Rely on individual components.
    
*   Implement loose coupling.
    
    (Correct)
    

#### Explanation

Dependencies such as queuing systems, streaming systems, workflows, and load balancers are loosely coupled. Loose coupling helps isolate behavior of a component from other components that depend on it, increasing resiliency and agility

AWS recommend that you architect applications that scale horizontally to increase aggregate workload availability. This scaling should be automatic where possible.

**CORRECT:** "Implement loose coupling" is a correct answer.

**CORRECT:** "Design for scalability" is also a correct answer.

**INCORRECT:** "Implement manual scalability" is incorrect. AWS do not recommend manual processes. Everything should be automated as much as possible.

**INCORRECT:** "Use self-managed servers" is incorrect. AWS do not recommend using self-managed servers. They do recommend using serverless services if you can.

**INCORRECT:** "Rely on individual components" is incorrect. This is not a best practice; you should never rely on individual components. It is better to build redundancy into the system so the failure of an individual component does not affect the functioning of the application.

**References:**

[https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/architecting-for-the-cloud/](https://digitalcloud.training/architecting-for-the-cloud/)

Question 58:
Amazon S3 is typically used for which of the following use cases? (Select TWO.)

*   Host a static website
    
    (Correct)
    
*   Media hosting
    
    (Correct)
    
*   Message queue
    
*   In-memory data cache
    
*   Install an operating system
    

#### Explanation

Amazon S3 is an object storage system. Typical use cases include: Backup and storage, application hosting, media hosting, software delivery and hosting a static website.

**CORRECT:** "Host a static website" is the correct answer.

**CORRECT:** "Media hosting" is the correct answer.

**INCORRECT:** "Install an operating system" is incorrect. You cannot install an operating system on an object-based storage system. Instead, you need a block-based storage system such as Amazon EBS.

**INCORRECT:** "In-memory data cache" is incorrect. You cannot use Amazon S3 as an in-memory data cache; for this you need a service such as Amazon ElastiCache.

**INCORRECT:** "Message queue" is incorrect. You cannot use Amazon S3 as a message queue (or at least it is not a typical use case). You should use a services such as Amazon SQS or Amazon MQ.

**References:**

[https://docs.aws.amazon.com/AmazonS3/latest/gsg/S3-gsg-CommonUseScenarios.html](https://docs.aws.amazon.com/AmazonS3/latest/gsg/S3-gsg-CommonUseScenarios.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-storage-services/](https://digitalcloud.training/aws-storage-services/)

Question 59:
A company requires a dashboard for reporting when using a business intelligence solution. Which AWS service can a Cloud Practitioner use?

Which AWS service can be used?

*   Amazon Redshift
    
*   Amazon Athena
    
*   Amazon QuickSight
    
    (Correct)
    
*   Amazon Kinesis
    

#### Explanation

Amazon QuickSight is a scalable, serverless, embeddable, machine learning-powered business intelligence (BI) service built for the cloud.

QuickSight lets you easily create and publish interactive BI dashboards that include Machine Learning-powered insights.

QuickSight dashboards can be accessed from any device, and seamlessly embedded into your applications, portals, and websites.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-02-15_14-42-48-95a67e88779316ede1aab52c984b5aa7.jpg)

**CORRECT:** "Amazon QuickSight" is the correct answer.

**INCORRECT:** "Amazon Redshift" is incorrect. RedShift is a data warehouse solution not a dashboard. You can use QuickSight with RedShift.

**INCORRECT:** "Amazon Kinesis" is incorrect. This is a service for collecting streaming data.

**INCORRECT:** "Amazon Athena" is incorrect. Athena is used for running SQL queries on data in Amazon S3.

**References:**

[https://aws.amazon.com/quicksight/](https://aws.amazon.com/quicksight/)

**Save time with our AWS cheat sheets:**

[https://quicksight.aws.amazon.com/](https://quicksight.aws.amazon.com/)

Question 60:
Which AWS service should a Cloud Practitioner use to establish a secure network connection between an on-premises network and AWS?

*   Virtual Private Network
    
    (Correct)
    
*   AWS Web Application Firewall (WAF)
    
*   AWS Mobile Hub
    
*   Amazon Virtual Private Cloud (VPC)
    

#### Explanation

AWS Virtual Private Network solutions establish secure connections between your on-premises networks, remote offices, client devices, and the AWS global network.

**CORRECT:** "Virtual Private Network" is the correct answer.

**INCORRECT:** "AWS Mobile Hub" is incorrect. This service is used for building, testing, and monitoring mobile applications that make use of one or more AWS services.

**INCORRECT:** "AWS Web Application Firewall (WAF)" is incorrect. This service is used for protecting against common web exploits.

**INCORRECT:** "Amazon Virtual Private Cloud (VPC)" is incorrect. This is a virtual network in the cloud. You connect your AWS VPN to your Amazon VPC.

**References:**

[https://aws.amazon.com/vpn/](https://aws.amazon.com/vpn/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Question 61:
Which benefits can a company immediately realize using the AWS Cloud? (Select TWO.)

*   User control of physical infrastructure
    
*   Increased agility
    
    (Correct)
    
*   No responsibility for security
    
*   Variable expenses are replaced with capital expenses
    
*   Capital expenses are replaced with variable expenses
    
    (Correct)
    

#### Explanation

A couple of the benefits that companies will realize immediately when using the AWS Cloud are increased agility and a change from capital expenditure to variable operational expenditure.

Agility is enabled through the flexibility of cloud services and the ease with which applications can be deployed, scaled, and managed. When using cloud services you pay for what you use and this is a variable, operational expense which can be beneficial to company cashflow.

**CORRECT:** "Capital expenses are replaced with variable expenses" is a correct answer.

**CORRECT:** "Increased agility" is also a correct answer.

**INCORRECT:** "Variable expenses are replaced with capital expenses" is incorrect. This is the wrong way around, capital expenses are replaced with variable expenses.

**INCORRECT:** "User control of physical infrastructure" is incorrect. This is not true, you do not get control of the physical infrastructure.

**INCORRECT:** "No responsibility for security" is incorrect. This is not true, you are still responsible for “security in the cloud”.

**References:**

[https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-cloud-computing-concepts/](https://digitalcloud.training/aws-cloud-computing-concepts/)

Question 62:
A Cloud practitioner wants to know if there are services which can protect from DDoS (Distributed Denial of Service) attacks directed at AWS services.

Which AWS service or tool will provide this protection?

*   Network access control list (ACL)
    
*   Amazon GuardDuty
    
*   AWS Shield
    
    (Correct)
    
*   Security group
    

#### Explanation

AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS. AWS Shield provides always-on detection and automatic inline mitigations that minimize application downtime and latency, so there is no need to engage AWS Support to benefit from DDoS protection.

There are two tiers of AWS Shield - Standard and Advanced.

**CORRECT:** "AWS Shield" is the correct answer (as explained above.)

**INCORRECT:** "Network access control list (ACL)" is incorrect. Network ACLs exist within a VPC, and act as a stateless firewall for network traffic in and out of your subnets.

**INCORRECT:** "Security group" is incorrect. A Security Group is a Stateful firewall which exists to prevent unwarranted access to any instances running within a VPC.

**INCORRECT:** Amazon GuardDuty" is incorrect. Amazon GuardDuty is an intelligent threat detection service which has nothing to do with Distributed Denial of Service (DDoS) protection.

**References:**

[https://aws.amazon.com/shield/features](https://aws.amazon.com/shield/features/)/

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-security-services/](https://digitalcloud.training/aws-security-services/)

Question 63:
According to the shared responsibility mode, which security and compliance task is AWS responsible for?

*   Updating operating systems
    
*   Granting permissions to users and services
    
*   Updating Amazon EC2 host firmware
    
    (Correct)
    
*   Encrypting data at rest
    

#### Explanation

According to the AWS shared responsibility model AWS are responsible for security “of” the cloud. This includes updating the firmware of the EC2 host servers on which instances run. All of the other answers are incorrect as they represent security “in” the cloud which is a customer responsibility.

![](https://img-b.udemycdn.com/redactor/raw/test_question_description/2021-02-15_13-40-29-3e028766622b1f8c65a2c73a9371674a.jpg)

**CORRECT:** "Updating Amazon EC2 host firmware" is the correct answer.

**INCORRECT:** "Granting permissions to users and services" is incorrect as this is a customer responsibility.

**INCORRECT:** "Encrypting data at rest" is incorrect as this is a customer responsibility.

**INCORRECT:** "Updating operating systems" is incorrect as this is a customer responsibility.

**References:**

[https://aws.amazon.com/compliance/shared-responsibility-model/](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-shared-responsibility-model/](https://digitalcloud.training/aws-shared-responsibility-model/)

Question 64:
A company is interested in moving its on-premises NoSQL database into the AWS Cloud.

Which AWS service should the company use to replace their existing database?

*   Amazon RDS for MySQL
    
*   Amazon Redshift
    
*   Amazon Quantum Ledger Database (Amazon QLDB)
    
*   Amazon DynamoDB
    
    (Correct)
    

#### Explanation

Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance applications at any scale. DynamoDB offers built-in security, continuous backups, automated multi-Region replication, in-memory caching, and data export tools. When you hear of AWS Managed NoSQL databases, DynamoDB is the only acceptable choice.

**CORRECT:** "Amazon DynamoDB" is the correct answer (as explained above.)

**INCORRECT:** "Amazon RDS for MySQL" is incorrect as RDS is a managed Relational (SQL) database service. The question calls for a NoSQL database.

**INCORRECT:** "Amazon Quantum Ledger Database (Amazon QLDB)" is incorrect. Amazon Quantum Ledger Database (QLDB) is a fully managed ledger database that provides transparent, immutable, and cryptographically verifiable transactions- and is not a suitable replacement for an on-premises NoSQL database.

**INCORRECT:** "Amazon Redshift" is incorrect, as it is an SQL-based data warehousing solution. It would not be a suitable replacement for an on-premises NoSQL database.

**References:**

[https://aws.amazon.com/dynamodb/](https://aws.amazon.com/dynamodb/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-database-services/](https://digitalcloud.training/aws-database-services/)

Question 65:
A company has a global user base and needs to deploy AWS services that can decrease network latency for their users. Which services may assist? (Select TWO.)

*   AWS Direct Connect
    
*   Amazon CloudFront
    
    (Correct)
    
*   AWS Global Accelerator
    
    (Correct)
    
*   Amazon VPC
    
*   Application Auto Scaling
    

#### Explanation

Amazon CloudFront is a content delivery network (CDN) that caches media assets such as files, photos, and videos in Edge locations around the world. This gets your content closer to the user base which decreases latency.

AWS Global Accelerator is a service that can direct users to the nearest AWS Region that contains and endpoint for an application. The service utilizes Edge locations to decrease latency and then forwards all traffic on the AWS global network which also decreases latency.

**CORRECT:** "Amazon CloudFront" is a correct answer.

**CORRECT:** "AWS Global Accelerator" is also a correct answer.

**INCORRECT:** "Amazon VPC" is incorrect as this service does not decrease latency for global users.

**INCORRECT:** "Application Auto Scaling" is incorrect as this is used to scale applications based on workload, it does not decrease latency.

**INCORRECT:** "AWS Direct Connect" is incorrect as this service does decrease latency but not for a global user base.

**References:**

[https://aws.amazon.com/global-accelerator/](https://aws.amazon.com/global-accelerator/)

[https://aws.amazon.com/cloudfront/](https://aws.amazon.com/cloudfront/)

**Save time with our AWS cheat sheets:**

[https://digitalcloud.training/aws-content-delivery-and-dns-services/](https://digitalcloud.training/aws-content-delivery-and-dns-services/)

[https://digitalcloud.training/aws-networking-services/](https://digitalcloud.training/aws-networking-services/)

Continue

Retake test

Settings

*   Report abuse
    

Fullscreen