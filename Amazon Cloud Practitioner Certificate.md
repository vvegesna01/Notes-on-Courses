Date: 12-22-2024
Tags: [[Courses]] [[Cloud Computing]] [[Computer Science]] 
Status: #active 
Link: https://www.youtube.com/watch?v=NhDYbskXRgc&pp=ygUvZnJlZWNvZGUgY2FtcCBhd3MgY2xvdWQgcHJhY3RpdGlvbmVyIGNlcnRpZmljYXQ%3D

---
### Resources
- freecodecamp 14 hour course: https://www.youtube.com/watch?v=NhDYbskXRgc&pp=ygUvZnJlZWNvZGUgY2FtcCBhd3MgY2xvdWQgcHJhY3RpdGlvbmVyIGNlcnRpZmljYXQ%3D
- practice tests: https://skillcertpro.com/
- to schedule the exam: https://aws.amazon.com/certification/certified-cloud-practitioner/

### Study Plan
- around 30 hours for complete beginner
- maybe 10 hours for me
- 1-2 hours for 2 weeks
- knowledge based exam
- do labs and practice exams (free practice exam here: https://exampro.co/clf-c02)

## What is the AWS Cloud Practitioner Exam? (CCP)
- Cloud Concepts, Cloud Architecture, Cloud Deployment Models
- AWS Core Services - compute, storage, networking
	- billing, pricing, identity, security, governance of cloud
### Exam Structure
- 65 Questions
	- 50 scored questions
	- 15 unscored questions
- You can get a total of 30 questions wrong and pass
- No penalty for wrong qs
- multiple choice
- Passing Grade: 70%
- Exam Time: 90 mins/ Seat Time: 120 mins/ 1.5 mins per question
- Valid for 36 months - 3 years before recertification **azure is apparently forever certification**

- [ ] Domain 1: [[#^028cc7 |Cloud Concepts]](24%) 15-16 Questions
- [ ] Domain 2: Security and Compliance (30%) 19-20 Questions
- [ ] 🔺 Domain 3: Cloud Technology and Services (34%) 22 Questions
- [ ]  Domain 4: Billing, Pricing and Support (12%) 8 questions

## What is Cloud Computing?
[Cloud Concepts FreeCodeCamp Video](https://www.youtube.com/watch?v=NhDYbskXRgc&t=2762s) ^028cc7

> [!question] What is Cloud Computing?
> Using network of remote servers hosted on the internet to store, manage, and process data and not on a local computer

### Evolution of Cloud Computing
- Dedicated server
	- one physical machine -> single business
	- pros: high security
	- cons: expensive, high maintenance
- VPS Virtual Private Server
	- one machine -> virtualized into sub-machines
	- pros: runs multiple web-apps, better utilization and isolation of resources
	- cons: 
- Shared Hosting
	- one physical machine -> shared by many businesses
	- pros: super cheap, maintainance costs are delegated
	- cons: relies on most people under-utilizing resources, limited to machines functionality, poor isolation
- Cloud Hosting
	- *multiple* physical machines -> act as one system
	- sys is abstracted into multiple cloud services
	- pros: flexible, scalable, secure, add more services as needed, virtualised isolation, shared costs so it's cheap, high configurability

| Name           | Define                                                                                                  | Pros                                                                                                                                                                                         | Cons                                                                                                                                                                             |
| -------------- | ------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Dedicated**  | - single tenant<br>- control of virtualization                                                          | - guarantee of security, privacy<br>- BUT up to you to define security<br>- full utility of resources                                                                                        | - guess capacity upfront<br>- low utilization and overpaying<br>- not easy to scale, manual migration<br>- limited by Host OS<br>- multiple apps - conflict in resources sharing |
| **VMs**        | - machine within a machine<br>- multi-tenant<br>- Hypervisor - software layer that lets you run the VMs | - paying for a fraction of the server<br>- easy to vertically and horizontally scale                                                                                                         | - still some underutlization<br>- limited by Guest OS<br>- multiple apps - conflict in resource sharing<br>- might still overpay for an underutilized machine                    |
| **Containers** | - virtual machine running containers<br>- Docker Deamon - software layer like hypervisor<br>            | - maximise the capacity - cost-effective<br>- can add and resize containers<br>- containers share OS but more efficient than VMs<br>- no conflicts during resource sharing for multiple apps | - more maintanence                                                                                                                                                               |
| **Functions**  | - serverless compute<br>- upload code, choose mem and duration                                          | - less maintanence<br>- cost-effective<br>                                                                                                                                                   | - side effect is cold-starts, sometimes requests can be slow                                                                                                                     |

### AWS - Amazon Web Services - fun facts
- launched in 2006, leading cloud service provider (CSP)
- Simple Queue Service - 2004 - first service launched for public use
- Simple Storage Service (S3) - 2006
- Elastic Compute Cloud (EC2) - 2006 - most used right now

### What is a CSP?

> [!info] What classifies as a Cloud Service Platform
> essentially a company that provides the following
> 	- multiple cloud services
> 	- chained together to create cloud architecture
> 	- unified and accessible via a **Single Unified API** - eg: AWS API
> 	- utilize metered billing based on usage
> 	- rich monitoring built in - eg: AWS CloudTrail
> 	- infrastructure as a service (IaaS)
> 	- offer automation via IaC
> 

### Landscape of CSPs
- Tier 1 - Top Tier - AWS, Azure, GCP, Alibaba Cloud
- Tier 2 - Mid Tier - IBM Cloud, Oracle Cloud, Huawei Cloud, Tencent Cloud
- Tier 3 - Light Tier - Vultr, Digital Ocean, Akamai (offer more core Iaas, cost-effective, mostly VPS)
- Tier 4 - Private Tier - OpenStack, Apache CloudStack, VMWare vSphere (Iaas but on your own private data center)

### Common Cloud Services - 4 Core Services
- Compute - virtual computer that runs apps, programs and code
- Networking - virtual network defining internet connections or isolations between services 
- Storage - virtual hard drive - stores files
- Databases - virtual DB - storing reporting data, db for general web app purposes

#### AWS Tech
- Compute - EC2 Virtual Machines
- Networking - VPC Private Cloud Network
- Storage - EBS Virtual Hard Drives
- Databases - RDS SQL databases
outside of the core:
	- analytics, app integration, ML, IoT, Blockchain, Media Services, Robotics, Satellites, Billing

### Types of Cloud Computing
- Saas - for customers
	- run and managed by service provider
	- Salesforce , GMail, Office365
	- designed for customers
- PaaS - platform - for devlopers
	- focus on deployment and management of your apps
	- Heroku
- IaaS - Infrastructure - for admins

### Cloud Computing Models
Public Cloud
- everything built on the CSP
- a.k.a Cloud First
Private Cloud
- built on company's datacenters
- a.k.a On-Premise
Hybrid Cloud
- both on-Premise and CSP together
Cross-Cloud/Multi-Cloud
- using multiple CSPs
- eg: using Azure Arc for GCP Kubernetes within Amazon EKS

### Deployment Model Use Cases

| Cloud                                                                                        | Hybrid                                                                                       | On-Premise                                                                            |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| fully cloud                                                                                  | both cloud and on-premise                                                                    | - deploying resources on premises<br>- private cloud                                  |
| Startups, small enough to go from VSP to CSP<br>SaaS offerings<br>New Projects and companies | orgs that started with own datacenter<br>can't easily move to cloud without enough resources | - orgs that cannot run on cloud due to regulatory compliance<br>- have sensitive data |
| DropBox, Basecamp, SquareSpace                                                               | Deloitte, CIBC, Fintech, Investment Management, Legacy On-Premise                            | hospitals, government, AIG                                                            |

---
[[AWS Account for Practice (IAM User Credentials)]]

### Regions in AWS
- reccomend using us-east-1
	- billing only shows up in us-east-1
- some services are "global" services - S3 and CloudFront (does not require region selection)
- some services have a region dependancy

### Billing
 