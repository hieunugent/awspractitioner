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

