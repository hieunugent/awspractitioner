# awspractitioner
## what is cloud computing?
- what is cloud computing 
  - cloud computing is the on-demand delivery of compute power,database storage, application, and other IT resources.
  - pay as you go pricing 
  - provision exactly the type and size of computing
  -  almost istantly for your demand
  - simple way access server, storage, databases and a set of application service
  - AWS will maintains the network connected hardware required for these application 
- private cloud:
  - cloud service uses by a single org not exposed to the public 
  - complete control
  - security for sensitive app
  - meet specific business needs
- public cloud:(azure, AWS, Google cloud)
  - cloud resouces owned and operate by a third party cloud service provider delivered over the internet
  - six advantages of cloud computing 
- hybrid cloud:
  - keep some servers on premises and extend some capabilities to the cloud
  - control over sensitive asset in your private infrastructure
  - flexibility and cost effectiveness of the public cloud
- Five Characteristics of cloud Computing
  - On-demand self service
  - Broad network access
  - multi- tenancy and resourse pooling 
  - rapid elasticity and
  - measured service
- Six advantage of Cloud computing
  - Trade capial expense(CAPEX) for operational expense(OPEX): pay on demain, dont own hardware, reduce total cost of ouwnership TCO and Opreational Expense (OPEX)
  - benefit from massive economies of scale : price are reduced as AWS is more efficienent due to large scale
  - Stop guesing capacity 
  - increase speed and agility
  - stop spending money running and maintainging data center
  - go global in minutes: leverage the AWS globale infrastureture
- problem solver by cloud:
  - Flexibility: change resourse types when needed
  - cost effectiveness: pay ass you go
  - Scalability : accommodate larger loads by making hardware stronger or adding additional node
  - elasticity: ability to scale out and scale in when needed
  - high-availibility and fault-tolerance: build across data centers
  - Agility: rapidly develop, test and launch software application 
  
## The diff Types of Cloud Computing 
- type of cloud comp.
  - infrastructure as a service(IaaS)
    - provide building block for IT
    - Provides networking, computers data storage space
    - highest level of flexibity
    - easy parallel with traditional onpremise IT
  - Platform as a Service(PaaS)
    - remove the need fr your organation to manage the underlying infrastructure 
    - Focus on the deployment and management of your applications
  - Software as a service (SaaS)
     - completeed product that is run and manger by the service provider
 
   ![alt text](https://github.com/hieunugent/awspractitioner/blob/main/Capture.JPG?raw=true)
- example of CLoud Computing Types
  - infrastructure as a service: Amazon EC2, GCP, Azure, Rackspace, Linode
  - Platform as a service : Elastic Beanstalk(on AWS), Heroku, Google app Engine (GCP), Azure
  - Softwarea as a service : Many AWS service (ex: Rekognition for ML), Goole app. Gropbox, Zoom 
- Pricing of the cloud   
  - Compute
  - storage
  - data transfer Out of the cloud
- use cases includage
  - Enterprise IT, Backup store Big Data Analytics
  - website hosting Mobile and Social APPs, Gaming 
- AWS Global INfrastructure
    - regions: cluter of data centers, most AWS services are region-scoped
    - availability Zones:
      - each region has many availability zones ussualy 3 min 2 max 6 : ap-southeast-2a, ap-southest-2b
      - each available zone is one or more discrete data cneter with redundant power, networing and connectivity
      - they are separate form each other , so that they area isolate from disaster
      - they area connected with highbandwidth, ultra-low latency networking
    - Data Centers, Edge Locations, Points Of presense 
    - How to choose an AWS region:
        - Compliance with data governance and legal requirements : data never leaves a region without your explicit permission
        - proximity to customers: reduced latency 
        - Available services within a region: new services and new feature aren't available in every Region 
        - pricing varies region to region and is transparent in the service pricing page
- SHAre Responsebility:
   ![alt text](https://github.com/hieunugent/awspractitioner/blob/main/shareresponse.JPG?raw=true)
## IAM - Identity and Access Management
- IAM: USers & Groups
    - IAM = Identity and Access Management, Globoal service
    - Root Accountr created by default shouldn't e used or shared
    - users are people within your organization, and can be grouped
    - groups only contain users not other groups
    - users dont have to belong to a group, and user can belong to multiple groups
    ![alt text](https://github.com/hieunugent/awspractitioner/blob/main/groups.JPG?raw=true)

- IAM: Permissions
    - Users or groups can be assigned JSON documents called policies
    - these policies define the permission of the users
    - In AWS you apply the least privilege principle : dont give more permissions than a user needs
- IAM : policies:
    ![alt text](https://github.com/hieunugent/awspractitioner/blob/main/IAMpolicy.JPG?raw=true)
    ![alt text](https://github.com/hieunugent/awspractitioner/blob/main/policysStructure.JPG?raw=true)
- IAM - Password policy
   - Strong passwords = higher security for your account 
   - In AWS, you can setup a password policy 
      - set a munimum password length 
      - require specific character types
      - allow all IAM users to change their own password 
      - requires users to change their password 
      - require user change password after sometime
      - prevent password reuse
   - Multi Factor Authentication - MFA
      - user have access to your account and can change config or delete resource in your AWS 
      - you want to protect your root account and IAM user 
      - MFA = password + security device you own 
       ![alt text](https://github.com/hieunugent/awspractitioner/blob/main/MFA.JPG?raw=true)
      - main benefit of MFA: if password is stolen or hacked the account is not compromised
- HOw can users access AWS
  - three option to access AWS:
    - Aws Management console : protect by password and MFA
    - AWS command line interface (CLI) : protect by access keys
    - AWS software DEveloper kit (SDK) for code protected by access keys
  - Access keys are generated through the Aws Console
  - Users Manage theri own access keys
  - Access keys are secret, just like a password 
- what is AWS CLI ?
  - tool to interact with AWS serevice using commmands in command-line shell
  - direct access to the public APIs of AWS services
  - can develop scripts to manage your resources
- what is the SDK ?
  - AWS software development kit
  - language specific APIs
  - enable you to access and manage AWS sevices programmatically 
  - Embedded within your application 
  - supports :
    - SDKs(java , python , PHP, .Net, JS, Go , NOde.js, C++)
    - Mobile SDKs
    - IOT Devices SDKs (Embedded C,  Arduino, ...) 
- IAM roles for services
  - somw AWS service will need to perform actions on your befhalf
  - to do so we will assign permisssions to Aws service with IAM roles 
  - common roles : EC2 instance Role Lambda Function Roles, ROle For Clound Formation 
   ![alt text](https://github.com/hieunugent/awspractitioner/blob/main/IAMroles.JPG?raw=true)
- IAM Security Tools
  - Iam Credential Report (account level)
     - a repost taht lst all your accounts user and the status of their various credential 
  - Iam Access Advisor user level
    - access advisor show the service permissions granted to a user and when those serviece wre last access 
    - you can use this information to revise your policies
- Shared Resposibility MOdel For IAM
  ![alt text](https://github.com/hieunugent/awspractitioner/blob/main/ShareResIAM.JPG?raw=true)

## EC2 - Elastic Compute Cloud
- Amazopn EC2
  - EC2 is one of the most pouylar of AWS offering 
  - EC2 is Elastic compute cloud is infrastructure as a service
  - it mainly consists in the capability of :
    - renting virtual machines (EC2)
    - storing data virtual drive EBS
    - distributing load across machines ELB
    - Scaling the services using an auto scaling group
  - Knowing EC2 is fundamental to understand how the cloud works
 - EC2 sizing and configuration options
    - OS : linux win Mac
    - how much compute power and cores CPU
    - how much random access memory Ram
    - how much storage space :
      - Network attachhed (EBS and EFS)
      - hardware (Ec2 Instance store)
    - Network card speed of the card public IP Address
    - firewall rules security group
    - Bootraps Scipt( configure at first launch ) : EC2 User Data
 - EC2 Users Data
    - It is possible to bootstrap our instances using an EC2 USer data Script
    - Bootstrapping means launching acommands when a machine starts
    - that scropts is only run once at the instance first Start
    - EC2 user data is used to automate boot tasks such as:
      - installing updates 
      - installing software
      - downloading common files  from the internet
      - anything you can think of
    - it run with Root user
- EC2 INstance typ example
    ![EC2InstanceType](https://user-images.githubusercontent.com/22860697/121975134-c4951f00-cd35-11eb-8fcd-3152d1034869.JPG)
- EC2 Instance Types 
    - types of EC2 instance are used to optimised diff use cases
    - ![Ec2typesuse](https://user-images.githubusercontent.com/22860697/121979329-cc0cf600-cd3e-11eb-8602-f304355ae9c0.JPG)
    - General purpose:
      - great for diversity of workload such as web servers or code repo
      - balance between : compute, memory, networking
    - COmpute Optimized:
      - Great for Compute intensive task that require high performance processors
        - Batch Processing workloads
        - medias transcoding 
        - high performance web serves
        - high performance computing HPC
        - scientific modeling and machine learning
        - dedicated gaming servers
        - ![computeoptimize](https://user-images.githubusercontent.com/22860697/121980082-33777580-cd40-11eb-953e-cb444a287e66.JPG)

    - Memory Oprimized
        - fast performance for workload that process larger data sets in memory
        - Use cases :
          - high performance , relational / non relational databases
          - distribute web scale cahse stores
          - in memory data bases opimised for BI (business intelligent)
          - APplication performing realtime processing of big unstructure data 
          - ![memoryoptimise](https://user-images.githubusercontent.com/22860697/121980029-16db3d80-cd40-11eb-88cd-0ab667028076.JPG)
     - Storage Optimizes
        - Great for storage intensive tasks that require high sequential read and write access to large data sets on local storage 
        - use cases:
          - hihg frequency online transaction procesing (OLTP) systems
          - realtional and NOSQL databases
          - cache fpr in memory database 
          - Data warehouseing appilcations
          - distirbuted dile systems
          - ![storagoptimised](https://user-images.githubusercontent.com/22860697/121980403-bac4e900-cd40-11eb-87e9-b5ba3af38ad4.JPG)

- Introduction to security Groups
  - security groups are the fundamental of network security In AWS
  - they control how traddic is allowed into or out of our EC2 instances
  - ![securitygroup](https://user-images.githubusercontent.com/22860697/122133611-eb189000-cdf1-11eb-87f8-2d7acecb8d45.JPG)

  - only contain allow rules
  - rules can reference by IP or by Security Group
  - Security group acting as a firewall on EC2 instances
  - they regulate: 
      - access to ports
      - authoriesd IP ranges  - IPv4 and IPv6
      - control inbound network from other to the instance
      - control outbound network from instance to other
  - ![securitryDiagram](https://user-images.githubusercontent.com/22860697/122134037-b78a3580-cdf2-11eb-9fe1-fdcd1118112c.JPG)
  - good to know:
    - can be attached to multiple instance
    - locked down to a region /VPC combination
    - live outside the EC2 - if traffic is blocked the EC2 instance wont see it 
    - it good to maintain one separate security group for ssh access
    - if your application is not accessible (timeout), then it's a security group issue
    - if give a " connectio refused error, then it's an application error opr it's not lauched 
    - by default all inbound traffic is block 
    - all outbound traffic is authoried
    - ![securitygroupdiagram2](https://user-images.githubusercontent.com/22860697/122134584-c1606880-cdf3-11eb-9f6f-bec94db45f16.JPG)
  - classic Ports to know 
    - ![classicport](https://user-images.githubusercontent.com/22860697/122134776-2320d280-cdf4-11eb-83a6-d5ffb0f7c1c7.JPG)
- EC2 Instances Purchasing Options:
  - On-demand Instances : short workload, predictable pricing
  - ![ondemainprice](https://user-images.githubusercontent.com/22860697/122138926-a47c6300-cdfc-11eb-9a80-70f8b40bb97c.JPG)

  - reserved: (minimum 1 year)
    - reserved instances : long workloads 
    - convertible reserverd Instances : Long workloads with flexible instance
    - schedule reserved instances: example - every thursday between 3 adn 6pm 
    - ![resinstanceprice](https://user-images.githubusercontent.com/22860697/122139140-2a001300-cdfd-11eb-899e-98508e2f7f09.JPG)

  - spot instances: short wrkloads, cheap can lose instance (less reliable)
  - ![spotinstanceprice](https://user-images.githubusercontent.com/22860697/122139279-7e0af780-cdfd-11eb-8a0b-0312b53166e4.JPG)
  - dedicated Hosts: Book an entire Physical server, control instance placement
  - ![dedicateinstance](https://user-images.githubusercontent.com/22860697/122139460-e8bc3300-cdfd-11eb-85c4-793707e5436f.JPG)
  - dedicate  Instance:
    - instances running on hardware that dedicated to you 
    - may share hardware with other instances in same account 
    - no control over instance placement (can move hardware after STop/ Start)
    - ![comparededicate](https://user-images.githubusercontent.com/22860697/122139707-6d0eb600-cdfe-11eb-89c3-2f700872111c.JPG)
   - ![example](https://user-images.githubusercontent.com/22860697/122139869-cb3b9900-cdfe-11eb-8c25-1dc823f1e82f.JPG)
- Share REsponsibility Model for EC2
- ![compareresponse](https://user-images.githubusercontent.com/22860697/122140145-574dc080-cdff-11eb-906b-9f6419a92127.JPG)
 


        
    
