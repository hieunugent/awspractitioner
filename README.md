# AWS Practitioner
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
- What is an EBS volume?
  - An EBS (Elastic Block STore) Volume is a network drive you can attach to your instances while they run 
  - It allows your instances to persist data, even after their termination 
  - They can only be mounted to one instance at a time (at the CCP level) , CCP: Certified Cloud Practitioner - onw EBS can be only mounted to one EC2 instance Associate level (Solutions Architect, DEveloper, SysOps ):"Multi-attach" Feature for some EBS
  - they are bound to a specific availability Zone
  - Analogy : Think of them as a Network USB stick
  - free tier: 30 GB of free EBS Storage of type General Purpose (SSD) or  Magnetic per MOnth
- EBS Volume:
  - It's a network drive:
    - it uses the network to communicate the instance, which means there might be a bit of latency 
    - it can be detached from an EC2 instance and attached to another one quickly 
  - It's Locked to an Availability Zone (AZ)
    - An EBS volume in Us-east-1 a cannot be attached to us-east-1b
    - to move a volume across, you first need to snapshot it
  - Have a provisioned capacity(size in GbS, and IOPS)
    - you get billed for all the provisioned capacity
    - you can increase the capacity of the drive over time
  - EBS delete on termination attribute
    - controls the EBS behaviour when an EC2 instace terminates
      - by default, the root EBs volume is delleted (attribute enabled)
      - by default, any other attached EBS volume is not Deleled ( Attribute Disable)
    - this can be controlled by The AWS console/ AWS CLI
    - use case : preserve root volume when instance is terminated
- EBS Snapshots
    - make a backup of your EBS volume at a point in time
    - Nopt neccessary to detach volume to do snapshot, but recommended
    - can copy snapshots across AZ or REgions
    - ![snapshot](https://user-images.githubusercontent.com/22860697/122657067-f7179100-d114-11eb-9667-a2bbd07098ec.JPG)
- AMI Overview:
    - AMI = Amazon Machine Image
    - AMI are a customization of an EC2 instance
      - you add your own software, configuration, operation system, monitoring
      - Faster boot / configuration time because all your software is pre-packaged 
    - AMI are built for a specific region and can be copied across regions
    - you can launch EC2 instance from :
      - A public AMI: AWS provided
      - your own AMI: you make and maintain them yourself
      - An AWS Marketplace AMI: an AMI someone else made (and potentially sells)
- AMI Process (from an EC2 instance)
    - Start an EC2 instance and customize it 
    - Stop the instance for data integrity
    - Build an AMI - This will also create EBS snapshots 
    - launch instances from other AMIs
    - ![AMIprocess](https://user-images.githubusercontent.com/22860697/122663544-0a941d80-d150-11eb-9dfb-8ba212c05787.JPG)

- EC2 Image Builder
    - Used to automate the creation of Virtual Machines or container images
    - => Automate the creation , maintain , validate and test EC2 AMIs
    - can be run on a schedule (weekly, or whenever packages are updated, etc..)
    - free service (only pay for underlying resources )
    - ![buildimageAMI](https://user-images.githubusercontent.com/22860697/122663922-ceae8780-d152-11eb-8570-c7a923ee2fec.JPG)
- EC2 Instance Store
  - EBS volume are network drives with good but "limited" Performance
  - If you need a high-performance hardware disk , use EC2 Intance Store
  - Better I/O performance
  - Ec2 Instance Store lose theor storage if they are stopped (ephemeral)
  - Good for buffer/cache/scatch data/temporary content
  - risk of data loss if hardware fail
  - Backups and Replication are your RESPONSIBLE
- EFS -Elastic File SYstems
  - Managed NFS that can be mounted on 100s of EC2
  - EFS works with linux EC2 intances in multi-AZ
  - highly available , scalable expensice (3x gp2, pay per use, no capacity planning
  - ![efs](https://user-images.githubusercontent.com/22860697/124177256-d3354300-da64-11eb-9364-ba930e89edfd.JPG)
- EBS vs EFS
  - ![EBSvsEFS](https://user-images.githubusercontent.com/22860697/124200686-d3e0d000-da8a-11eb-9a2c-79a7f02ecb41.JPG)
- EFS infrequent Access (EFS-IA)
  - storage class that is cost optimized for file not accessed every day
  - up to 92% lower cost compared to EFS Standard
  - EFS will automatically move your files to EFS-IA base on the last time they were accessed
  - Enable EFS-IA with a lifeCycle Policy
  - Example: move files that are not accessed for 60 days to EFS-IA
  - Transparent to applications accessing EFS
  - ![EFS-IA](https://user-images.githubusercontent.com/22860697/124201735-97fb3a00-da8d-11eb-9b7d-d9db66406976.JPG)
- Share Responsibility Model for EC2 storage
   -  ![resposibleEC2Storage](https://user-images.githubusercontent.com/22860697/124215173-60e65200-daa8-11eb-8999-13227acd757c.JPG)
- Amazon Fsx for window file serve
  - a fully mananged highly reliable and scalable window native shared file system
  - built on windowe file server
  - supports SMB protocol andwindow NTFS
  - integrated with Microsoft Active Directory
  - Can be Accessed From AWS or your on premise infrastructure
  - ![fsxwin](https://user-images.githubusercontent.com/22860697/124216305-cdfae700-daaa-11eb-9f8c-9527b9ed8bbc.JPG)
- Amazpm FSx for Lustre
  - A fully managed high performance , scalable file storage for high Performance Computing (HPC)
  - the name Lustre is derived form Linux and cluster
  - Machine learning , Analytic video procesing , Finacial modeling, ...
  - Scale up to 100s GB/s, Millionss of IOPs, sub-ms Latencies
  - ![lustre](https://user-images.githubusercontent.com/22860697/124216905-12d34d80-daac-11eb-90ee-fe2acc4a4177.JPG)
- High Availability Scalability, Elasticity 
  - scalability means that an application / systems can handle greater loads by adapting 
  - there are two kinds of scalability:
    - Vertical Scalability
    - Horizontal Scalabity(+ elasticity)
  - Scalability is linked but differeant to high Availability
- Vertivcal Scalabil;ity:
  - vertical scalability means increasing the size of the instance
  - for example your application runs on a t2.micro
  - scaling that application vvertically means running ity on a t2.large
  - vertical scalability  is very common for non distributed systemsuch as a database
  - there usually a limmit to how much you can vertically scale
- horizontal scalability :
  - means increasing the number of instances / systems for your application  
  - horizontal scaling implies distributed systems
  - this is very common for web application modern application 
  - its is easy to horizontalliy scale thank teh cloud offering such as AMazon EC2
- high Availability 
  - high available usually goes hand in hand with horizontal scaling 
  - high available means running your application /system in at least 2 availability zones
  - the goal of the high availability is to survive a data center loss
- scalability : ability to accommodate a larger load by making the hardware stronger scale up or by adding nodes sacle out
- elasicity once a system is scalable elasticity means that there will be some autoscaling so that the system can scale beesase on the load. this is cloud friendly, pay per use , match demand , optimize costs
- Agility : not related to scalability - distractor new It resources are only a click away, which means that you reduce the time to make those resource available to your developers from weeks to just minute
- Elastic load balancing ELB Overview:
- what is load balancing?
  - load balanced ar3e servers that forward internet traffic to multiple server(EC2 instances) downstream
  - ![loadbalancer](https://user-images.githubusercontent.com/22860697/125679229-01ff265e-ae89-4432-8530-960cad864b26.JPG)
- why use a load balancer?
  - spread load across multiple downstream instances
  - expose a single point of access DNS to your application
  - seamlessly handle failures of downstream instances
  - do regular health checks to your instance
  - provide SSL termination (HTTPS) for your websites
  - high availability across zones
- why use a ELASTIC LOAD BALANCER?
  - An ELB is a managerd load balancer
    - AWS guarantees that it will be working 
    - AWS takes caer of upgrades , maintenance hih availabily
    - AWS provides only a few configuration knobs
  - it cost less to setup your ownn load balancer but it will be a lot more effeor on your end (maintenance , integrations)
  - 3 kinds of load balanceer offered by AWS 
    - Application load balancer ( HTTP/HTTPS only) layer 7
    - Network load Balancer ( ultra high performance allow for TCP) layer 4
    - Classic load Balancer ( SLowly retiring) layer 4 and 7
  
- Gateway load Balancer - How it work
  - Gateway Load Balancer combines a transparent network gateway (that is, a single entry and exit point for all traffic) and a load balancer that distributes traffic and scales your virtual appliances with the demand.
  - you can send traffic to GWLB by making simple configuration updates in your VPCs’ route tables. With GWLB, customers can scale their virtual appliances elastically by load balancing traffic across a fleet of virtual appliances. GWLB improves availability by routing traffic flows through healthy virtual appliances, and reroutes flows when an appliance becomes unhealthy.
  - With GWLB, you can use your own appliances of choice in AWS and rely on GWLB to manage their scale and availability needs, while retaining skillsets and existing processes. You can also scale your virtual appliances elastically by load balancing traffic across a fleet of virtual appliances. The scaling up and down of appliances reduces costs. GWLB sends both directions of the traffic flow to the same appliance, thereby allowing the appliance to perform stateful traffic processing.
  - GWLB and the virtual appliances exchange application traffic with each other using GENEVE encapsulation, which allows GWLB to preserve the content of the original traffic. GWLB uses Gateway Load Balancer Endpoint (GWLBe), a new type of VPC Endpoint powered by AWS PrivateLink, which can be a next-hop in the route table. This simplifies insertion of appliance services across VPC boundaries.
  - For example, you can make a Customer VPC where the customer workloads will sit, which will be the VPC where the GWLB Endpoint is deployed. AWS Partner’s appliances will be deployed in the Partner VPC.
  - ![GWLB](https://user-images.githubusercontent.com/22860697/125682151-2f3e5a79-7589-46fc-9ae1-8f60616d9c8f.JPG)
  - The appliance providers and consumers can reside in different AWS accounts and VPCs. GWLBe enables consolidation of appliances, consistency of security policies, reduction in operator errors, and seamless inspection of traffic without having to change the traffic source or destination and requiring NAT translations.
  - To ensure high availability, you can use the advanced routing capabilities of GWLB to direct traffic to only healthy appliances, and reroute traffic when an appliance becomes unhealthy due to faults. GWLB works across VPCs and user accounts, giving you the option to centralize virtual appliance fleets. The ability to use GWLB across user accounts enables partners to offer their virtual appliances as an AWS-hosted service that customers access from their VPCs. This reduces complexity and improves security.
  - ASG
