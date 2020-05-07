
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

- CloudFormation {infrastructure}
  - template-driven
  - deploy infrastructure using code
  - services launched for you via JSON
  - Change Sets, Stacks, Templates

- ElasticBeanStalk  {applications}
  - builds containers
  - platform service
  - leverages CloudFormation
  - WAR / ZIP files w/code = environment built "for you"

exam cram
=========
5/6 - missed What sac can be used to automatically create an Amazon VPC & then launch
      an EC2 instance.... : Correct answer : CLoudWatch

==========================================================================================
==========================================================================================

Section 14: AWS Migration & Transfer Services

- migrate on-premises to Cloud
- {DMS} Database Migration Service
  - target : Amazon RDS, Aurora

- Snowball, SnowMobile
  - very large amounts of data into AWS

exam cram
=========
- 4/4

==========================================================================================
==========================================================================================

Section 15: AWS Billing & Pricing

- Need to know :
  - what you get for free
    - VPC
    - Elastic Beanstalk {just the resources}
    - CloudFormation  {just the resources}
    - IAM
    - Auto-Scaling
    - Consolidated Billing
    - data going into AWS {only outbound}
  - what you get charged for
    - compute
      - amount of time your instance is running  {based on instance type}
      - load balancing {Network, Balanced}
      - detailed monitoring {CloudWatch}
      - Elastic IP addresses {if allocated but not used}
      - AWS Lambda
      - ECS
      - FarGate
    - storage
      - amount of data being stored
      - S3
        - class type
        - quantity
        - # of requests
        - moving data between storage classes
      - S3 Glacier
      - EBS
        - amount provisioned
      - EFS
        - storage classes, amount used
    - network
      - VPN connections
      - PrivateLink
      - NAT Gateways, instances
      - AWS Direct Connect - # port hours
    - Database
      - RDS  {amount of time running}
        - clock time, instance type
    - outbound data transfer
  - how are you charged
    - models
      - on-demand
        - good for short term
      - dedicated
        - good for compliance, licensed software, ie software per workstation
      - spot instances {purchasing spare capacity}
        - up to 90% off on-demand
        - terminated when AWS needs capacity back
      - reservations  {all services will have 'reserved' in their name}
        - good if you predictable usage, @75% savings over on-demand
        - no upfront
        - partial upfront
        - all upfront
      - savings plan
  - special payment options


exam cram
=========
10/14 - try 1
14/14 - try 2


==========================================================================================
==========================================================================================

Section 16: AWS Cloud Security

- Shared Responsibility Model
  - what customer is responsible for
    - Security "IN" the cloud
  - what AWS is responsible for
    - Security "OF" the cloud

exam cram
=========
12/12

==========================================================================================
==========================================================================================

Section 17: AWS Architecting for the Cloud

- Best Practices section
- horizontal {increase #instances} over vertical scaling {manually increase instance stats, downtime}
- resources are reusable
- use automation
- loose coupling - reduce interdependencies
  - service discovery
- use existing AWS services - not building new servers
- use right db for workload
- remove single points of failure
  - introduce redundancy
- detect failure {health checks, alarms, automate detection & reaction}
- durable data storage
- optimize for cost
  - only build what you need
- caching
  - improve performance & cost efficiency	
  - Application Data Caching {AWS ElastiCache, Dynamo DB DAX}
- Security
  - use AWS
  - reduce privileged access
  - CloudFormation {build secure environments - template}
  - Auditing - {Trusted Advisor, Config, Inspector}

- 5 Pillars of Operational Excellence
  - Operational Excellence
  - Security
  - Reliability
  - Performance Efficiency
  - Cost Optimization

exam cram
=========
12/12

==========================================================================================
==========================================================================================

Section 18: AWS Additional Services Seen on the Exam

- AWS Rekognition - image analysis, objects, facial features, celebrities
  - videos as well
- AWS SNS - Simple Notification Service  {loose coupling} - a push service
  - application integration services
  - publish / subscribe
  - sending notifications from publishers to subscribers
    - eg, EC2, CloudWatch, S3 send a message into SNS topics - sends on to Simple Q Svc, emails, AWS Lambda
    - pushes msgs to subscribers
  - managed service, pay-as-you-go
- AWS SQS Simple Queue Service - pull-based service
  - message bus
  - create queues, msgs get placed into
    - eg, EC2s get info from customers, place info/orders into qs
      - back-end EC2 apps process msgs in qs
  - different types of qs
  - back-end keeps polling qs
- AWS SWF - Simple Workflow Service
  - order service
  - ideal for human-enabled workflows
- AWS Step Functions
  - replacing a lot of SWF use cases
  - uses JSON code
  - creates visual workflow - good for decision tree flows - yes/no, pass/fail - workflows
  - state machines

==========================================================================================
==========================================================================================

Section 19: AWS Full length practice exams

- test # 1 : 80%
- test # 2 : 86%

==========================================================================================
==========================================================================================

Section 20: Extra Labs, multiple EC2 instances w/ELB

==========================================================================================
==========================================================================================

Section 21: Final Exam Preparation + BONUS

- downloaded additional exams and cheat sheet
- checked everything into Git



===============================================================
===============================================================
===============================================================


CarahSoft - AWS Webinar - Cloud Practitioner Boot Camp
05/07/2020 - 12p-4p

- trade capital expense for variable/operational expense
- benefit from massive economies of scale
- stop guessing capacity
- increase speed & agility
- stop spending $$ running & maintaining data centers
- go global in minutes

AWS Global Infrastructure
-------------------------
- 24 Regions
- 76 Availability Zones
- 205+ Edge Locations

- US East 1 - 1st region made generally available
  - 50 mile radius around there - AZ

- infrastructure.aws - website showing global AWS infrastructure


Regions & AZs
-------------
- Regions - separate independent areas
- AZs connected by high-speed low-latency links

AZs
---
- multiple isolated locations within a region
- 1 AZ @= 1 data center
- independent failure zones
- physically separated
- on separate Low Risk Flood Plains

4 Popular Use cases
-------------------
- Dev & Test
  - eg, Elastic BeanStalk {no charge for service - service for the resources}
    - easily create copies of their environments
    - upload code - BeanStalk does resource allocation
  - resources only needed when used

- Storage
  - low cost data storage
  - object, block & file storage
  - S3 {11 9's security, Glacier {low-cost archival}

- Disaster Recovery
  - enables faster disaster recovery of they critical IT systems w/o
    incurring infrastructure expense for a 2nd site
  - Fast Performance
  - No Tapes
  - Compliance
  - Elasticity
    - add any amount of data quickly adapting to increase / decrease resources
  - Secure
    - Auditing, Certifications, etc
  - Partners
    - Solution Provider & Integration Assistance

- Big Data
  - Storage & Databases
    - Object Storage
    - NoSQL
    - Graph databases
    - HBase
    - Aurora
  - Analytic Frameworks
    - Hadoop & Spark
    - ElasticSearch
  - Data Warehousing
    - RedShift
  - Business Intelligence
  - Real-Time Analytics
  - Machine Learning

- AWS Storage Gateway - connect on-premises db to cloud-based AWS services


Shared Responsibility Model
---------------------------
- who is responsible for what
- Security & Compliance -> shared responsibility
- AWS - security "OF" the cloud
  - hardware, data centers, networking equipment & software
- Customer - security "IN" the cloud 
  - all application security
  - data encryption
  - OS security patches, IAM, network & firewall configurations


AWS Well-Architected Framework
------------------------------
- Pillars
- Design Principles
- Questions

5 Pillars
---------
- Operations Excellence
- Security
  - implement a strong identity foundation
  - enable traceability
  - apply security at all layers
  - automate best practices
  - encrypt data in transit & at rest
- Reliability
  - test recovery procedures
  - automatically recover
  - scale horizontally to increase aggregate system availability
  - stop guessing capacity
  - manage change using automation
- Performance
  - use advanced technologies
  - go global in minutes
  - use server less architectures
    - DynamoDB
    - Lambda
  - experiment more often
  - mechanical sympathy
- Cost Optimization
  - adopt a consumption model
  - measure overall efficiency
  - stop spending money on datacenter operations
  - analyze and attribute expenditure
  - use managed services to reduce cost of ownership


AWS Compute Services
--------------------
- EC2
  - Elastic Compute Cloud
  - resizable compute capacity
  - instance types
    - combines CPU, memory, storage & networking capacity
    - c4.large
      - 'c' : Instance Families, 'c' -> compute
      - '4' : Instance Generations
      - 'large' : Instance sizes

  - integrated with
    - EBS
    - CloudWatch
    - VPC
    - IAM
    - Batch
    - ECS - container service

  - Instance Types
    - On-Demand
      - pay only when used
    - Reserved
      - discounted price, up to 75% - NEED to make a time commitment, eg 1 - 3 years
    - Spot
      - discounted - uses "spare"/unused compute capacity
      - up to 90% 
      - good for no time commitment serverless applications, big data calls
      - auction / bid to obtain - can go away at any time {2 minute notice}


Data Storage Options
--------------------
- Instance Store
  - temporary - once instance stops - data goes away
  - physically attached to host
  - good for cache, scratch data
- EBS
  - persistent
  - data is independent of instance lifecycle


AMIs
----
- Composed of AMI - Machine Images
  - Amazon maintained
  - Community Built
  - Personally built ones  {can be public or private}


Auto-Scaling
------------
- Maintains EC2 Instance availability
  - detects bad ones
  - replaces w/good
- Automatically Scale Up / Down
  - based on cfg'd settings / rules

AWS Lambda
----------
- serverless Compute service  {DynamoDB - RDS}
- runs code in response to events 
  - automatically manages underlying resources


{1255p-105p : 10 minute break}


AWS Storage Services
--------------------
- S3 - Simple Storage Service
- can run AWS Analytic Services against S3
  - Athena, Redshift, EMR
- S3 Lake
  - stand up a Data Lake
- up to 10 object tags
  - use tags to perform operations
- can assign access policies against data
- ACLs - access control list
- 6 Classes - cost-based
- Glacier & Glacier Deep Archive
  - longer term storage
- can analyze data and move data between classes
- manage data at all levels at-scale
- cfg fine-tune access to data
- cost effectively store data across classes
- audit & report on data
  - develop rules against analysis
- 11 9s of durability
- scale data on-demand & in minutes
- ingest & store as much data as needed, eg good for Big Data

Classes
-------
- Standard
  - multi AZ
  - used for frequent access
- Intelligent-Tiering
  - uses deep learning to analyze
  - data w/changing access patterns
  - optimize storage costs
  - no management required  {cost optimized automatically}
  - no retrieval fees
  - supports all of the capabilities of the rest of the S3 storage classes
- Standard 1A - '1A' - Infrequent Access
- One Zone 1A {only 1 AZ}
  - infrequent access
  - multi AZ
  - easily recreatable data
  - mobile / enterprise backup data
- Glacier
- Glacier Deep Archive
  - cold storage
  - accessed infrequently
  - fee for retrieving
  - good for media archives, medical data
  - recover in 12 hours or less
  - fully managed


EBS - Elastic Block Storage
---------------------------
- durable high-performance
- simple to use
  - low latency, high throughput
- performant
  - elastic volumes
    - adjust size & tune performance w/NO disruption
- reliable
  - scaled across multi AZ
- snapshots 
  - incremental
  - users control encryption
- each EC2 has 1 EBS Boot Volume


EFS - Elastic File System
-------------------------
- NFS file System
- SIMple
  - fully managed
  - can mount multiple
  - secure
- elastic
  - grows automatically
  - stores data redundantly by default
- scalable


Data Transfer
-------------
- Direct Connect
  - private connection between on-premises & AWS
  - establish a quick on-premises to AWS connection
  - 1 GB, 10 GB
- SnowBall, Snowmobile
  - send data in bulk, ie Tera, Peta, Exa
  - data encrypted
  - hardware devices sent to you
- Storage Gateway
  - hybrid cloud data storage solution
  - simplify storage mgmt
  - 3 Types
    - simple 
    - Tape / File / ????
  - connects to other S3 storage services
- Transfer Acceleration
- Kinesis
- many others


IAM : Security & Access Control
===============================
-------------------------------
- IAM - identity & Access Management
- users, groups
  - Permissions assigned to Policies
  - Policies assign to Roles
  - Roles given to users, groups
- USERS
  - entity that interact w/AWS
  - person or service
  - access thru AWS Console {userid, password} / or CLI {Access Key & ID}
- eg, new employee
- use root user as little as possible
- best practice
  - use root user to create an IAM user w/Admin access

Users & Permissions
-------------------
- no permissions by default when created
- have to attach permissions
  - ie, who has access
  - what actions

Policies
--------
- Managed
  - attached to multiple users, groups and roles
- Inline
  - usually just for one-off causes

Groups
------
- reduces individual user management
- assign policy to a Group - then add users into groups

Roles
-----
- an identity w/permission policies that determine what the identity can / cannot do
- can be assumed by anyone
- give cross-account access
- access within an account
- NO credentials
- Federation : give access to identities defined outside AWS


{Lab & break : 145p-230p}
Lab log in : https://975060361121.signin.aws.amazon.com/console
Introduction to AWS Identity and Access Management



VPC
---
- default one every region
- can span Availability Zones
- own logically isolated area w/in a region
- ENI - elastic network interface
  - represents a virtual network card
- Subnet  {firewall for your EC2}
  - public
  - private
    - no route to an Internet gateway
- Internet Gateway
  - attached to VPC - allows access out to Internet
  - provides a target in your VPC route tables for internet
  - perform network access translation {NAT}
- NACL
  - firewall
- Route Table
  - directs where traffic from your VPC goes


VPC Peering
-----------
- networking connection between 2 VPCs
- enables you to route traffic between them using private IP addresses
- appear to be communicating as if in the same network 
- allows inter-region connections
- helps facilitate the transfer of data
  - eg, create a file-sharing network



AWS Database Services
---------------------
- relational
  - Aurora, RDS
- key-value
  - DynamoDB
- In-memory
  - ElastiCache
- Document
  - DocumentDB

Aurora {RDS}
------------
- MySQL, PostgreSQL compatible relational
- performance & scalable
- availability & durable
- highly secure
- fully managed by RDS
- 5 times faster MySQL / 3 times faster PostgreSQL
- read-replicas
- cost effectiveness - 1/10 the cost


RDS
---
- Aurora, MySQL, PostgreSQL, MariaDB, SQL Server, Oracle
- managed relational
- easy to administer
- highly scalable
- fast & secure
- available & durable
  - automatic multi-AZ
- DMS
  - Database Migration Service
    - migrates on-premises source dbs to AWS
  - source db remains fully operational

DynamoDB
--------
- NoSQL db service
- performance
- fully managed
  - scales up & down automatically
- serverless
  - good for modern apps
- comprehensive security
- global database for global users and apps
- encrypts all data by default
- integrates w/ IAM
- easily replicates tables across multiple AWS Regions


DocumentDB
----------
- mongodb-compatible
- fully managed, scalable
- performance at scale
- durable
  - 6 copies of data across 3 AZs
- highly available
- can be used w/AWS DMS


RedShift  {large data sets, analysis}
--------
- data warehouse service
- fast
  - paralel processing
- highly scalable
- virtually unlimited concurrency
  - dynamically scales based on data volumes
- extends your data lake
- 10x performance
- 1/10th cost
- uses machine learning to analyze data - peta, exabytes
- use KMS & HSM for security




Monitoring & Auditing
---------------------
- CloudWatch  {resource monitoring}
  - monitoring service
  - monitors cloud resources, applications
  - collects & tracks metrics
  - collect & monitor log files
  - set alarms
    - based upon analysis
    - high resolution
    - help w/cost
  - Logs
    - collect & store
    - Bended  {AWS logs}
    - AWS Service Logs
    - Custom {apps, on-premises}
      - install agent to collect on-premises logs
  - built-in Dashboards to display metrics
  - graph metrics & data for analysis
  - eg, CPU utilization, memory

- CloudTrail  {AUDITing user account actions, activity, console,}
  - enabled by default
  - compliance auditing 
  - operational troubleshooting
  - security analysis
  - automatic compliance remediation
  - actions taken by users, roles or AWS service are recorded
  - last 90 days kept around
  - Event History
  - Management Events - management operations
  - Data Events - resource operations performed



AWS CloudFormation  {SaaS}
==================
- InfraStructure As Code
- Templated resource provisioning
- create templates to describe the AWS Resources used to run your application
- no charge for service
  - charged for resource usage
- infrastructure as code
  - entire architecture described in a text file
  - Designer - usually design your architecture - saves to a text file
- automates provisioning of architecture



AWS CloudFront  {Content Delivery Service}
==============
- delivers content to customers
- global content delivery
- works w/WAF & Shield - protects DDoS


Edge Locations  {CDN}
--------------
- used w/CloudFront
- "instances" that contain user data close to end users


Route 53
--------
- DNS Web Service
- route end users to Internet applications by using a human readable URL


AWS Config   {Compliance}
----------
- monitors configuration and changes between cfgs
- simplify security configuration, management, troubleshooting
- fully managed
- inventory
- history
- change notifications
- discover existing resources
- assess overall compliance & risk status
- SNS - get notified via AWS Simple Notification Service of changes


Artifact
--------
- central resource for compliance documentation
- certifications, regulations, attestations, etc



Cost Optimization
-----------------
- on-demand
  - spiky demands
- reserved
  - for a known committed time period
- spot
  - time insensitive, goes away at any time
  - spare
- dedicated
  - highly sensitive
  - most expensive
  - dedicated resources
  - cause your own licenses


Support Plans
-------------
- Basic
  - long response times
  - not much support
- Developer
- Business
  -most popular
  - 24x7 access
- Enterprise
  - dedicated TAM - Tech Account Manager




AWS Organizations
================
- centrally govern your environment
- policy based management for multiple AWS accounts
- control AWS service use across accounts
- automate account creation
- consolidate billing & Usage reporting
- manage cross-account access


Service Control Policy - SCP
----------------------------
- control which AWS service actions are accessible to account principals - including root


- AWS Certified Cloud Practitioner Certification Exam Guide
- go thru AWS White papers  {"dense"}
- WhizLabs - free practice tests


