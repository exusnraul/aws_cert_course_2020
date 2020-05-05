
Udemy  AWS Certified Cloud Practitioner Ultimate Exam Training Course 2020


Course : https://capitalsolutionsgroup.udemy.com/course/aws-certified-cloud-practitioner-training-course/learn/lecture/18549168#overview
         - Neal Davis, UK, AUStralia
Google : search for "AWS certified cloud practitioner guide" 
  - https://aws.amazon.com/certification/certified-cloud-practitioner/

exam 65 questions
====
multiple choice / multiple answer
  - if 4 answers - only 1
  - if 5+, 1 or more

$100

90 minutes

test center or online proctored
  - online proctored can stay at home

recommends NOT taking other "practice exams"
  - thinks this course is good enough to pass

White papers - get at 
  - Overview of Amazon Web Services
  - Architecting for the Cloud : AWS Best Practices
  - How AWS Pricing Works
  - Cost Management in the AWS Cloud


Start with Section 4. IAM Users -> START HERE FOR ADDITIONAL NOTES TO THE SLIDES - OTHERWISE JUST READ SLIDES


==========================================================================================

Exam Guide : 
4 domains 
1. Cloud Concepts  - 26%
  1.1 Define the AWS Cloud and its value proposition
      - why would people want to use it
  1.2 Identify aspects of AWS Cloud economics
      - why it makes economical sense
  1.3 List the different cloud architecture design principles
2. Security  25%
  2.1 Define the AWS Shared Responsibility model
      - who's responsibility for what, eg AWS vs customer
  2.2 Define AWS Cloud Security and compliance concepts
  2.3 Identify AWS access management capabilities
  2.4 Identify resources for security support
3. Technology  - 33%
  3.1 Define methods of deploying and operating in the AWS Cloud
  3.2 Define the AWS global infrastructure
      - what makes up the data centers and the systems that are in them
  3.3 Identify the core AWS services
      - large part of course
      - basics
  3.4 Identify resources for technology support
4. Billing and pricing  - 16%
  4.1 Compare and contrast the various pricing models
      - understand how they price for each service & understand differences
  4.2 Recognize the various account structures in relation to AWS billing and pricing
  4.3 Identify resources available for support

1. Cloud Concepts - 26%
2. Security - 25%
3. Technology - 33%
4. Billing & Pricing - 16%

Downloads : https://digitalcloud.training/aws-ccp-exam-training-course-downloads/

==========================================================================================
==========================================================================================

Section 2. Overview of Cloud Computing

What is Cloud Computing ?

- gmail
- facebook
- dropbox

Cloud Computing : 
- the on-demand delivery of IT services from a third-party provider over the Internet

Cloud Service : 
- The IT capability that is being provided by the cloud provider
- gmail : email
- facebook : social networking
- dropbox : storage

"pay as you go" : typical, only pay for what you use


Enterprise Organization Examples
================================
- website
  - website & storage up in the cloud
  - cloud takes care of scaling storage and/or servers to handle customer demand

- order system
  - order system ui
  - db to hold orders
    - perform analytics to 'plan' future business
    - do on the cloud only when analytics are needed
  - scaling handled by cloud

Cloud Characteristics {technical}
=====================
- on-demand, self-service
  - cmds consume resources on a remote site
- broad network access
  - connect to the service, eg internet {eg, AWS}, WANs
- resource pooling
  - resources used by multiple users
- rapid elasticity
  - scaling - resources to handle more users, storage
  - elasticity - scale up / down
- measure service
  - monitored so you pay for what you use

Service Models
==============
- On-premises / private cloud
  - all managed by you
- IaaS - Infrastructure
  - AWS EC2 - request a virtual server
  - but once AWS gives it to you - you have to manage it, eg the OS, runtime libraries, data & code
- PaaS - Platform
  - developer uploads code to AWS Elastic Beanstalk
  - but once AWS gives it to you - you have to manage just data & code
- SaaS - Software
  - Sales Team logs sales data into Salesforce.com
  - all managed by provider
    - users just consume the service, eg gmail, facebook, dropbox


Deployment Models
=================
- where are your resources deployed
- private cloud
  - dedicated environment but it's all yours - eg VMWare, RedHat, OpenStack
  - benefits :
    - complete control, eg data security reasons
- public cloud
  - AWS, MS Azure, Google Cloud Platform
  - these companies need LOTS of resources 
    - so they buy all that which allows them to charge lower costs than if private company had to buy that much
  - benefits :
    - variable expense
    - scaling, elasticity
- hybrid cloud
  - combination of private / public
  - benefits :
    - allow companies to use private for certain proprietary components and public for 'common'
- multicloud
  - use multiple clouds, eg Azure, AWS
  - why ? different services, price points, etc


Legacy IT
=========
- old way of doing things
- companies need :
  - data centers, power, computing equipment, software licenses, maintenance, staff wages, etc
- requires lots of 
  - capital
  - operational overhead {maintenance, wages}
  - limited scalability


6 Advantages of Cloud {as told by AWS}
=====================
- https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html
- Trade capital expense for variable expense
  - no need for $$ for data centers
- benefits from massive economies of scale
- stop guessing about capacity
  - cloud takes care of knowing storage capacity, num of users, etc - consumer doesn't need to
- increase speed & agility
- stop spending $$$ running & maintaining data centers
- go global in minutes



==========================================================================================
==========================================================================================

Section 3: AWS Cloud Overview

AWS Cloud History
=================
- internal launch 2002
- vision 2003
- public launch 2004
- re-launch S3, SQS {Simple Queue Service}, EC2 2006
- amazon.com retail sites migrated 2010
- $1.57 B 2015
- $25 B 2018

- 165 services, eg computing. machine learning, storage, analytics, etc
- 22 geographical regions


AWS Global Infrastructure
=========================
- region
  - 22 regions around the world
  - different geographical areas
  - w/2 or more AZs, 
  - each AZ isolated from other AWS regions
- availability zones {AZ}
  - actual locations into which you launch your resources, eg an EC2 AMI instance
  - 1 or more data centers that are physically separate from other AZs
  - AZs span 1 or more data centers and have direct, low-latency, high throughput & redundant network connections between each other
  - each AZ is designed as an independent failure zone
    - app deployed in multiple AZs, if 1 fails, the other is just fine
  - physically separated w/in a region but not in same building, use discrete power sources
- edge locations
  - location w/a cache of content that can be delivered at low latency to users
  - used by CloudFront
- regional edge cache
  - part of CloudFront
  - larger caches that sit between AWS services & Edge locations
- global network
  - highly available, low latency private global network
  - interconnecting every data center, AZ & AWS region


AWS Services in Scope for Exam
==============================
- Identity & Access Management {IAM}
  - users, groups, policies
- AWS Compute
- check out the slides & the course summary


AWS Global vs Regional Services
===============================
- check the PDF for the ones that pertain to the exam
- global
  - AWS IAM
  - Amazon S3 {storage}
  - AWS Direct Connect {networking}
  - Content Delivery & DNS
    - Amazon Toute 53
    - Amazon CloudFront
  - Cloud Governance & Security
    - AWS WAF & Shield
    - AWS Artifact
    - AWS Trusted Advisor
    - AWS Personal Health Dashboard
- regional
  - the rest


- IAM - user accounts
  - just one
  - global account
    - different permissions


- EC2 web server , Amazon RDS DB
  - regional
  - stood up in 1 region / AZ
  - S3 Buckets
    - regional
    - stood up in another region/AZ
    - copy data from above to here


AWS Billing & Pricing Overview
==============================
- 3 fundamentals
  - compute
    - pay for compute / running time, eg EC2
  - storage
    - pay for amount of data stored
    - eg S3, EBS, EFS
  - Data Outbound
    - charged outbound data transfer rate
    - aggregated across the services, combined amount is charged

- on-demand
  - user for compute & database capacity
  - no long-term commitments
  - beauty of the cloud
    - not tied to IPs

- dedicated instances {more expensive}
  - available for Amazon EC2
  - hardware dedicated to a single customer

- spot instances
  - purchase spare capacity w/no commitments
  - great discounts
  - but subject to disappearing at any time

- reservations
  - up to 75% discount in exchange for a term commitment
    - 1 or 3 year term
  - options to pay
    - no upfront
    - partial upfront 
    - all upfront
  - available for
    - EC2 Reserved instances
    - DynamoDB Reserved capacity
    - ElastiCache Reserved nodes
    - RDS Reserved instances
    - RedShift Reserved nodes {data warehouse}


AWS Acceptable Use Policy
=========================
- check the white paper
- describes prohibited uses of AWS
- common sense
- AWS monitors


AWS Exam Cram
=============
- check the downloaded pdf
- 100%, 6/6


==========================================================================================
==========================================================================================

Section 4: Identity & Access Management {IAM Roles}

IAM Overview
============
Creating users {U}, groups {G}, policies {P}, roles {R}
Controls access.
Identity Federation
- integrate an external entity to check for access, eg MicroSoft Active Directory
- {U} create individual accounts to grant access 
- {U} can also assign to a service
- {P} defines permissions; apply to a user, group or role
- {G} collections of users w/policies attached to them, or,
- {G,P} add a bunch of users to a group & then apply 1 policy for that group
- {R} security identity, similar to a user account, that can be assumed by other entities
  - eg, launch an EC2 server, assign a role to that server, role would have a policy attached to it,
    - allowing it to access S3 and store data there;


IAM Users   ****** START HERE FOR ADDITIONAL NOTES TO THE SLIDES - OTHERWISE JUST REFER TO THEM
=========
- user accounts assigned to individuals or a service
- eg, Ethan, Adrian


IAM Groups
==========
- eg, Developers, AWS Admins, Operations


IAM Roles
=========
- created & then "assumed" by another entity
- eg, create an EC2 instance - assign a 'role' that allows full access to S3 storage service
- roles bypass need for an explicit userid/password
- defined role permissions assumed by entities having that role


IAM Policies
============
- eg, "full access" to S3, "read only" to DynamoDB



IAM Authentication Methods
==========================
- external, eg, MS Active Directory
- API : need an access key id & secret access key, eg, command line, SDKs
- UI AWS Mgmt Console : need an IAM User account w/password
- some AWS Services : need a signing certificate


IAM Multi-Factor Authentication
===============================
- adding additional security
- 3 factors
  - 1. Something Only You Know, eg, password
  - 2. Something Only You Have, eg, Google Authenticator app, device - ie RSA ID
  - 3. Something Only You Are, eg, fingerprint
- in AWS
  - {You Know} IAM User password
  - {You Have} virtual {apt generate a code} or physical {RSA device} MFA device


IAM Security Token Service {STS}
================================
- see slides


IAM Best Practices
==================
- see slides


Exam Cram
=========
- 7/8
- ROLES are used to delegate permissions - choices were users, groups, policies, roles

==========================================================================================
==========================================================================================

Section 5: Create AWS Free Tier Account (optional)

Hands-on AWS online site
========================
- new user : rjzawis
- access key id :  create new ones
- secret access key : 

==========================================================================================
==========================================================================================

Section 6: AWS Compute

- EC2 - web service part of AWS Compute suite of products
- by default, 20 instances per region max
  - if need more, have to apply to AWS & ask - more $$$
- EC2 is a REGIONAL service -must select the region to launch the instance

- created an EC2 instance
- created an EC2 instance w/httpd & default :80/index.html installed

- ECS - FARGATE - run Docker containers quickly
  - handles cluster mgmt for you
  - created NGINX cluster

- LAMBDA
  - serverless
  - run code w/o provisioning or managing servers
  - "trigger" executed - eg, web page visited
  - don't pay until the code runs

- LIGHTSAIL
  - easily provision compute services
  - easily created a WordPress app


==========================================================================================
==========================================================================================

Section 7: AWS Storage

- Object, Block, and File Storage

- Object - S3
- Block - EBS
- File - File

S3
==
- object stored in buckets
- REST API to connect - get, put, post, delete
- referenced via URL

EBS
===
- only 1 that can be used as a boot
- appear as local disks
- volumes mounted over a network
- create partitions, etc
- can attach multiple EBS volumes to a single EC2 BUT
  - CANNOT attach the same EBS volume to multiple EC2 instances
- MUST be in same AvlZone
- 1 can be a boot partition, another data

EFS
===
- connect using a 'protocol', eg NFS
- mount file system to a mount point

S3
==
- upload objects {files, pix, etc} into buckets

exam cram
=========
8/8

==========================================================================================
==========================================================================================

Section 8: AWS NETWORKING

- VPC - Virtual Private Cloud
- own personal subnets

exam cram
=========
6/6 - 1 lookup

==========================================================================================
==========================================================================================

Section 9: AWS DATABASES

- relational vs non-relational
- RDS
- DynamiDB
- RedShift
- ElastiCache

exam cram
=========
8/8 - no lookups

==========================================================================================
==========================================================================================

Section 10: AWS Elastic Load Balancing & Auto-Scaling


exam cram
=========
8/8 - looked up 1

==========================================================================================
==========================================================================================

Section 11: AWS Content Delivery & DNS Services

- Route 53 - DNS across regions
- CloudFront - ContentDelivery - CDN


exam cram
=========
7/8 - missed "Which service has built-in DDOS protection ? - said Route 53, correct answer : CloudFront

==========================================================================================
==========================================================================================

Section 12: AWS Monitoring & Logging SErvices

- CloudWatch : performance
- CloudTrail : auditing


exam cram
=========
4/4

==========================================================================================
==========================================================================================

Section 13: AWS Automation & Platform Services

- 

exam cram
=========


==========================================================================================
==========================================================================================

Section 14: AWS Migration & Transfer Services

- 

exam cram
=========


==========================================================================================
==========================================================================================

Section 15: AWS AWS Billing & Pricing

- 

exam cram
=========


==========================================================================================
==========================================================================================

Section 16: AWS AWS Cloud Security

- 

exam cram
=========


==========================================================================================
==========================================================================================

Section 17: AWS Architecting for the Cloud

- 

