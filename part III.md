#### Currently, you have a NAT Gateway defined for your private instances. You need to make the NAT Gateway highly available. How can this be accomplished?
  * Create a NAT Gateway in Another Availability Zone
#### A company wants to have a fully managed data store in AWS. It should be a compatible MySQL database, which is an application requirement. Which of the following database can be used for this purpose?
  * Amazon Aurora
    * is a fully managed, MySQL and PostgreSQL compatible, relational database engine
#### A Solution Architect is designing an online shopping application running in a VPC on EC2 instances behind an ELB Application. The instances run in a Auto Scaling group across multiple Availability Zones. The application tier must read and write data to a customer database cluster. There should be no access to the database from the Internet, but the cluster must be able to obtain software patches from the Internet. Which VPC design meets these requirements?
  * Public subnets for the application tier and NAT Gateway, and private subnets for the database cluster.
#### A company has an application that stores images and thumbnails for images on S3. While the thumbnail images need to be available for download immediately, the images themselves are not accessed that frequently. Which is the most cost-efficient storage option to store images that meets these requirements?
  * Amazon S3 standard Infrequent Access 
#### You have an application hosted on AWS consisting of EC2 Instances launched via an AutoScaling Group. You notice that the EC2 Instances are not scaling up on demand. What checks can be done to ensure that the scaling occurs as expected?
  * Ensure that the right metrics are being used to trigger the scale out.
    * If your scaling events are not based on the right metrics and donot have the right threshold defined, then the scaling will not occur as you want it to happen.
#### You have an application hosted in AWS that writes images to an S3 bucket. The concurrent number of users on the application is expected to reach around 10,000 with approximately 500 reads and writes expected per second. How should the architecture maximize Amazon S3 performance?
  * Prefix each object name with a random string
    * If the request rate is high, you can use hash keys or random string to prefix the object name. 
#### A company has a set of EBS Volumes that need to be catered to in case of a disaster. How can one achieve this in an efficient manner using the existing AWS services?
  * Use EBS Snapshots to create the volume in another region.
#### Your company currently has a web distribution hosted using the AWS CloudFront service. The IT Security department has confirmed that the application using the web distribution now falls under the scope of PCI compliance. Which of the following steps needs to be carried out to ensure that the compliance objectives are met? 
  * Ensure CloudFront access logs
  * Capture requests that are sent to the CloudFront API
    * If you run PCI or HIPPA compliant workloads on AWS shared responsibility model, it is recommended that you log your CLoudFront usage data for the last 365 days for future audition process. To log usage data, follow above 2 options.
#### Your company has a set of EC2 instances hosted in AWS. There is a mandate to prepare for disaster and come up with the necessary disaster recovery procedures. Which of the following would help in mitigating the effects of a disaster for the EC2 Instances?
  * Use AMIs to recreate the EC2 Instances in another region.
    * You can create an AMI from the EC2 instances and then copy them to another region. In case of a disaster, an EC2 instance can be created from the AMI. 
#### A company currently hosts a Redshift cluster in AWS. For security regions, it should be ensured that all traffic from and to the Redshift cluster doesn't go through the Internet. Which of the following features can be used to fulfill this requirement in an efficient manner?
  * Enable Amazon Redshift Enhanced VPC Routing.
    * When you use Amazon Redshift Enhanced VPC Routing, Amazon Redshift forces all **Copy** and **Unload** traffic between your cluster and your data repositories throught your Amazon VPC.
    * If Enhanced VPC is not enabled, Amazon Redshift routes traffic through the internet, including traffic to other services within the AWS network. 
#### A company has a set of Hyper-V machines and VMware virtual machine. They are now planning on migrating these instances to the AWS cloud. Which of the following can be used to move this resources to AWS Cloud?
  * Use the VM Import Tools
    * You can import Windows and Linux VMs that use VMware ESX or Workstation, Microsoft Hyper-V, and Citrix Xen virtualization formats.
#### An architecture consists of following:
  * a. primary and secondary infrastructure hosted in AWS.
  * b. Both infrastructure comprise ELB, AutoScaling and EC2 resources.
  **

  How should Route 53 be configured to ensure proper failover in case the primary infrastructure were to go down?
  * Configure a failover routing policy.
    * You can create an active-passive failover configuration by using failover records. Create a primary and a secondary failover record that have the same name and type, and associate a health check with each. 
#### A company requires to provision test environment in a short duration. Also required is an ability to tear them down easily for cost optimization. How can this be achieved.
  * Use CloudFormation templates to provision the resources accordingly. 
    * AWS CLoudFormation provides templates that you can use to create AWS resources and provision them in an orderly and predictable fashion. This can be useful for creating short-lived environments, such as test environments.
#### A company stores its log data in S3 bucket. There is current need to have search capabilities available for the data in S3. How can this be achieved in an efficient and ongoing manner?
  * Use an AWS Lambda function which gets triggered whenever the data is added to the S3 bucket.
  * Load the data into Amazon ElasticSearch.
    * AWS ELasticSearch provides full search capabilities and can be used to log files stored in S3 buckets. 
#### A company wants to self-manage a database environment. Which of the following should be adopted to fulfill this requirement?
  * Create an EC2 Instance and install the database service accordingly. 
#### A company wants to have a 50Mbps dedicated connection to its AWS resources. Which of the below services can help fulfill this requirement?
  * Direct Connect
    * AWS Direct Connect makes it easy to establish a dedicated network connection from your premises to AWS. Using AWS DirectConnect, you can establish private connectivity between AWS and your datacenter, office, or colocation environment, which in many cases can reduce your network costs, increase bandwidth throughput, and provide a more consistent network experience than Internet-based connections.
#### A company is building a Two-Tier web application to serve dynamic transaction-based content. The Data Tier uses an Online Transactional Processing (OLTP) database. What should you leverage to enable an elastic and scalable Web Tier?
  * ELastic Load Balancing, Amazon EC2, and AutoScaling
#### A customer planning on hosting an AWS RDS instance, needs to ensure that the underlying data is encrypted. How can this be achieved? 
  * Ensure that the right instance class is chosen for the underlying instance. 
  * Encrypt the database during creation 
    * Encryption for the database can be done during the creation of the database. Also, you need to ensure that the underlying instance type supports DB encryption.
#### Your Operations department is using an incident based application hosted on a set of EC2 instances. These instances are placed behind an Auto Scaling Group to ensure the right number of instances are in place to support the application. The operations department has expressed dissatisfaction with regard to poor application performance at 9:00 AM each day. However, it is also noticed that the system performance returns to optimal at 9:45 AM. What can be done to ensure that this issue gets fixed?
  * Add a Scheduled Scaling Policy at 8:30 AM.
    * Scaling based on a schedule allows you to scale your application in response to predictable load changes. 
#### Your company currently has data hosted in an Amazon Aurora MySQL DB. Since this data is critical, there is a need to ensure that it can be made available in another region in case of a disaster. How can this be achieved?
  * Create a Read Replica for the database.
    * You can create an Amazon Aurora MySQL DB cluster as a Read Replica in a different AWS Region than the source DB cluster. Taking this approach can improve your disaster recovery capabilities, let you scale read operations into a region that is closer to your users, and make it easier to migrate from one region to another. 
#### A company has a set of EC2 Linux based instances hosted in AWS. There is a need to have a standard file interface for files to be used across all Linux based instances. Which of the following can be used for this purpose?
  * Consider using AWS EFS
#### Your company is planning on using Route 53 as the DNS provider. There is a need to ensure that the company's domain name points to an existing CloudFront distribution. How can this be achieved?
  * Create an Alias record which points to the CloudFront distribution.
#### A company needs to extend their storage infrastructure to the AWS Cloud. The storage needs to be available as iSCSI devices for on-premises application servers. Which of the following would be able to fulfill this requirement?
  * Use the AWS Storage Gateway-cached volumes service.
    * By using cached volumes, you can use Amazon S3 as your primary data storage, while retaining frequently accessed data locally in your storage gateway. 
#### Your company has a set of application that make use of Docker containers used by the Development team. There is a need to move these containers to AWS. Which of the following methods could be used to set up these Docker containers in a seperate environment in AWS?
  * Create an Elastic Beanstalk environment with the necessary Docker containers. 
    * Elastic Beanstalk supports the deployment of web applications from Docker containers. 
#### A company currently hosts their architecture in the US region. They now need to duplicate this architecture to the Europe region and extend the application hosted on this architecture to the new region. In order to ensure that users across the globe get the same seamless experience from either setups, what among the following needs to be done?
  * Create a Geolocation Route 53 Policy to route the policy based on the location.
    * Geolocation routing lets you choose the resources that serve your traffic based on the geographic location of your users, meaning the location that DNS queries originate from. 
#### A customer has an instance hosted in the AWS Public Cloud. The VPC and subnet used to host the instance have been created with the default settings for the Network Access Control Lists. An IT Administrator needs to be provided secure access to the underlying instance. How can this be accomplished?
  * Ensure that the security group allows Inbound SSH traffic from the IT Administrator's Workstation
    * Since, security group are stateful, we do not have to configure outbound traffic. What enters the inbound traffic is allowed in the outbound traffic too. 
    * The default network ACL is configured to allow all traffic to flow in and out of the subnets to which it is associated. Since the question does not mention that it is a custom VPC we would assume it be the default one. 
#### A company has an on-premises infrastructure which they want to extend to the AWS Cloud. There is a need to ensure that communication across both environments is possible over the Internet. What would you create in this case to fulfill this requirement?
  * Create a VPN connection between the on-premises and the AWS Environment
    * AWS Direct connection between the on-premises and AWS Environment is not a better option because the question says **"Over the internet"** Direct connect does not involve the Internet.
    * VPN connection can be configured in minutes and are good solution if you have an immediate need, have low to modest bandwidth requirement, and can tolerate the inherent variability in Internet-based connectivity. 
#### A company wants to build a brand new application on the AWS Cloud. They want to ensure that this application follows the Microservices architecture. Which of the following services can be used to build this sort of architecture?
  * AWS Lambda
  * AWS ECS (Elastic Container Service)
  * AWS API Gateway: Serverless component for managing access to APIs.
#### A CloudFront distribution is being used to distribute content from an S3 bucket. It is required that only a particular set of users get access to certain content. How can this be accomplished?
  * Create CloudFront signed URLs and then distribute these URLs to these users. 
#### Your Development team wants to start making use of EC2 Instances to host their Application and Web servers. In the space of automation, they want the Instances to always download the latest version of the Web and Application servers when they are launched. As an architect, what would you recommend for this scenario?
  * Ask the Development team to create scripts which can be added to the Users Data section when the instance is launched. 
#### Your company has an application that takes care of uploading, processing and publishing videos posted by users. The current architecture for this application includes the following:
* a. A set of EC2 instances to transfer user uploaded videos to S3 buckets
* b. A set of EC2 worker processes to process and publish the videos.
* c. An Auto Scaling Group for the EC2 worker processes.
Which of the following can be added to the architecture to make it more reliable?
  * Amazon SQS
    * is used to decouple systems. It can store requests to process videos to be picked up by the worker processes.
#### You have a business-critical two-tier web application currently deployed in 2 Availability Zones in a single region, using Elastic Load Balancing and Auto Scaling. The app depends on synchronous replication at the database layer. The application needs to remain fully available even if one application AZ goes offline and if Auto Scaling cannot launch new instances in the remaining AZ. How can the current architecture be enhanced to ensure this?
  * Deploy in 3 AZ with Auto Scaling minimum set to handle 50 per cent peak load per zone. 
    * Bcoz, we need to maintain 100% availability. 
#### You have the following architecture deployed in AWS:
* a. A set of EC2 instances which sit behind an ELB
* b. A database hosted in AWS RDS.
**** 
Of late, the performance on the database has been slacking due to a high number of read requests. Which of the following can be added to the architecture to alleviate the performance issue?
  * Use ElastiCache in front of the database.
    * ElastiCache is an in-memory-cache which can be used to cache common read requests.
#### An application is currently hosted on an EC2 Instances which has attached EBS Volumes. The data on these volumes is frequently accessed. But after a duration of a week, the documents needs to be moved to infrequent access storage. Which of the following EBS volume type provides cost efficiency for the moved documents?
  * EBS Cold HDD(sc1)
    * Most cost efficient
#### A company is running three production web server reserved EC2 instances with EBS-backed root volumes. These instances have a consistent CPU load of 80%. Traffic is being distributed to these instances by an Elastic Load Balancer. They also have production and development Multi-AZ RDS MySQL databases. What recommendation would you make to reduce cost in this environment without affecting availabilty of mission-critical systems?
  * Consider not using a Multi-AZ RDS deployment for the development database. 
    * Multi-AZ databases are better for production environments rather than for development environments, so you can reduce costs by not using these for development environments.
#### An application consists of a couple of EC2 Instances. One EC2 Instance hosts a web application and the other Instance hosts the database server. Which of the following changes can be made to ensure high availability of the database layer?
  * Have another EC2 instances in the another Availability Zone with replication configured.
    * To ensure high availability, have the EC2 instances in another Availability Zone, so even if one goes down, the other one will still be available. 
#### You are designing an architecture on AWS with disaster recovery in mind. Currently the architecture consists of an ELB and underlying EC2 Instances in a primary and secondary region. How can you establish a switchover in case of failure in the primary region?
  * Use Route 53 Health Checks and then do a failover.
    * If you have multiple resources that perform the same function, you can configure DNS failover so that Route 53 will route your traffic from an unhealthy resources to a healthy resource. 
#### Your company currently has an infrastructure hosted On-premises. You have been requested to devise an architecture on AWS for migrating some of the On-premise components. A current concern is the data storage layer. Minimum administrative overheads are also required for the underlying infrastructure in AWS. Which of the following would be included in your proposed architecture?
  * Use DynamoDB to store data in tables
  * Use the Simple Storage Service to store data
#### Currently, you're helping design and architect a highly available application. After building the initial environment, you discover that a part of your application doesnot work correctly until port 443 is added to the security group. After adding port 443 to the appropriate security group, how much time will it take before the changes are applied and the application begins working correctly?
  * Changes apply instantly to the security group, and the application should be able to respond to 443 requests.
    * Some systems for setting up firewalls let you filter on source ports. Security groups let you filter only on destination ports.
    * When you add or remove rules, they are automatically applied to all instances associated with the security group.
#### A customer has a single 3-TB volume on-premise that is used to hold a large repository of images and print layout files. This repository is growing at 500GB a year and must be presented as a single logical volume. The customer is becoming increasingly constrained with their local storage capacity and wants an offsite backup of this data, while maintaining low-latency access to their frequently accessed data. Which AWS Storage Gateway configuration meets the customer requirements?
  * Gateway-Cached Volumes with snapshots scheduled to Amazon S3
    * Gateway-cached volumes let you use Amazon S3 as your primary data storage while retaining frequently accessed data locally in your storage gateway. 
#### A company is planning to use the AWS ECS service to work with containers. There is a need for the least amount of administrative overhead while launching containers. How can this be achieved?
  * Use the Fargate launch type in AWS ECS
    * Fargate launch type allows you to run your containerized applications without the need to provision and manage the backend infrastructure. Just register your task definition and Fargate launches the container for you. 
#### You are responsible for deploying a critical application to AWS. It is required to ensure that the controls set for this application meet PCI compliance. Also, there is need to monitor web application logs to identify any malicious activity. Which of the following services can be used to fulfill this requirements.
  * Amazon CloudWatch Logs
  * Amazon CloudTrial
#### One plans on using SQS queues and AWS Lambda to leverage the serverless aspects of the AWS Cloud. Each invocation to AWS Lambda will send message to an SQS queue. In order for message to be sent, which of the following must be in place?
  * An IAM Role with the required permissions.
    * While working with AWS Lambda functions, if there is a need to access other resources, ensure that an IAM role is in place. 
#### You have enabled CloudTrial logs for your company's AWS account. In addition, the IT Security department has mentioned that the logs needs to be encrypted. How can this be achieved?
  * There is no need to do anything since the logs will already be encrypted.
    * By default, CloudTrial log files are encrypted using Amazon S3 server-side encryption (SSE). You can also choose to encrypt your log files with an AWS Key Management Service (KMS).
#### A company has set up their data layer in the S3. There are a number of requests which include read/write and updates to objects in an S3 bucket. Users sometimes complain that updates to an object are not being reflacted. The reason is:
  * Updates are being made to the same key for the objects. 
    * Updates made to objects in S3 follow an eventual consistency model. Hence, for object updates made to the same key, there can be a single delay when the updated object is provided back to the user on the next read request. 
#### You plan on hosting a web application consisting of a web server and a database server. These servers are going to be hosted on different EC2 Instances in different subnets in a VPC. Which of the following can be used to ensure that the database server only allows traffic from the web server?
  * Make use of Security Group
    * helps to control traffic into an EC2 Instance
 #### A company has a redshift cluster defined in AWS. The IT Operations team have ensured that both automated and manual snapshots are in place. Since the cluster is going to be run for a long duration of a couple of years, reserved instances have been purchased. There has been a recent concern on the cost being incurred by the cluster. Which of the following steps can be carried out to minimize the costs being incurred by the cluster?
   * Delete the manual snapshots.
     * Regardless of whether you enable automated snapshots, you can take a manual snapshot whenever you want. Amazon Redshift will never automatically delete a manual snapshot. Manual snapshots are retained even after you delete your cluster.
#### You currently have a set of Lambda functions which have business logic embedded in them. You want customers to have the ability to call these functions via HTTPS. How can this be achieved?
  * Use the API Gateway and provide integration with the AWS Lambda function
#### A company wants to deploy docker containers to the AWS Cloud. They also want a highly scalable service which can help manage the orchestration of these containers. Which of the following would be ideal for such a requirement?
  * Use the Amazon Elastic Container Service for Kubernetes (EKS)
    * Amazon EKS is a managed service that makes it easy to run Kubernetes on AWS without needing to install and operate your own Kubernetes cluster.
    
#### You create an Auto Scaling Group  which is used to spin up instances On Demand. As an architect, you need to ensure that the instance are pre-installed with a software when they are launched. What are the ways in which you can achieve this?
  * Add the scripts for the installation in the User data section
  * Create a golden image and then create a launch configuration
    * The User data section of an instance launch can be used to pre-configure software after the instance is initially booted.
    * You can create AMI or Golden Image with the already installed software, then create a launch configuration which can be used by Auto Scaling Group. 
#### You need to ensure that data stored in S3 is encrypted but do not want to manage the encryption keys. Which of the following encryption mechanism can be used in this case?
  * SSE- S3
#### You have a requirement for deploying an existing Java based application to AWS. There is a need for automatic scaling for the underlying environment. Which of the following can be used to deploy this environment in the quickes way possible?
  * Use the Elastic Beanstalk service to provision the environment. 
    * AWS ELastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS. 
#### You have been tasked with architecting an application in AWS. The architecture would consist of EC2, the Classic Load Balancer, Auto Scaling and Route 53. There is a directive  to ensure that BLue-Green deployments are possible in this architecture. Which routing policy could you ideally use in Route 53 for achieving Blue-Green deployment?
  * Weighted
    * Weighted routing lets you associate multiple resourcese with a single domain name(example.com) or subdomain name(hello.example.com) and choose how many traffic is routed to each resource. This can be useful for a variety of purposes, including load balancing and testing new versions of software. 
    
 #### You need to have a Data storage layer in AWS. Following are the key requirements:
   * a. Storage of JSON documents
   * b. Availability of Indexes
   * c. Automatic scaling
   * Which of the following would be an ideal storage layer for the above requirements?
     * DynamoDB.
 #### Your company is planning on hosting their development, test and production applications on EC2 Instances in AWS. They are worried about how access control would be given to relevant IT Admins for each of the above environments. As an architect, what would you suggest for managing the relevant accesses?
   * Add tags to the instances marking each environment and then segregate access using IAM Policies. 
     * You can quickly identify the resource based on tags. Tag consist of a key and an optional value. 
#### You are performing a Load Testing exercise on your application hosted on AWS. While testing your Amazon RDS MySql DB instance, you notice that your application becomes non responsive when you reach 100% CPU utilization. Your application is read-heavy. What methods will help your data-tier to meet the application's needs? 
  * Add Amazon RDS DB Read Replicas, and have your application direct read queries to them.
  * Use ElastiCache in front of AWS RDS DB to cache common queries
  * Shard your data set among multiple Amazon RDS DB Instance. 
#### You work for a large company having multiple applications which are very different from each other. These are built using different programming languages. How can you deploy these applications as quickly as possible?
  * Develop each app in a separate Docker container and deploy using Elastic Beanstalk
    * With Docker containers you can define your own runtime environment, choose your own platform, programming language. 
#### You are designing a system which needs at minimum, 8 m4.large instances operating to service traffic. While designing a system for high availability in the us-east-1 region having 6 AZ, your company needs to be able to handle the death of a full AZ. How should you distribute the servers to save as much cost as possible, assuming all of the EC2 nodes are properly linked to an ELB? Your VPC account can utilize us-east-1's AZ a through f, inclusive 
  * 2 servers in each of AZ's a through e, inclusive
    * with this soln, you can have minimum of 8 servers even if one AZ goes down. 
#### An application currently consists of an EC2 Instances hosting a Web application. The Web application connects to an AWS RDS database. Which of the following can be used to ensure that database layer is highly available?
  * Enable Multi-AZ for the AWS RDS database.
#### An application currently accepts users to upload files to an S3 bucket. You want to ensure that the file name for each uploaded file is stored in DynamoDB table. How can this be achieved? 
  * Create a AWS Lambda function to insert the required entry for each uploaded file
  * Add an event with notification send to Lambda.
#### An application allows users to upload images to an S3 bucket. Initially these images will be downloaded quite frequently, but after some time, the images might only be accessed once a week and the retrieval time should be as minimal as possible. What could be done to ensure a cost effective solution?
  * Store the objects in S3-standard storage
  * Create a Lifecycle Policy to transfer the objects to S3- Infrequent Access storage after a certain duration of time.
#### A company hosts a popular web application that connects to an Amazon RDS MySQL DB instance running in a private VPC subnet created with default ACL settings. The IT Security department has identified a DDoS attack from a suspecting IP. How can you protect the subnets from this attack?
  * Change the Inbound NACL to deny access from the suspecting IP.
#### Videos are uploaded to an S3 bucket, and you need to provide access to users to view the same. What is the best way to do so, while maintaining a good user experience for all users regardless of the region in which they are located?
  * Use CloudFront with S3 bucket as a source. 
#### An organization has a requirement to store 10TB worth of scanned files. They are required to have a search application in place to search through the scanned files. Which of below mentioned options is ideal for implementing the search facility?
  * Use S3 with standard redundancy to store and serve the scanned files. Use CloudSearch for query processing, and use Elastic Beanstalk to host the website across multiple Availability Zones.
#### A concern raised in your company is that developers could potentially delete production baseed EC2 resources. As a Cloud Admin, which of the below options would you choose to help alleviate this concern?
  * Tag the production instances with a production-identifying tag and add resource-level permissions to the developers with an explicit deny on the terminal API call to instances with the production tag
  * Create a seperate AWS account and add developers to that account
#### You are an architect for a gaming application which is in the desing phase. Which of the following services can be used to ensure optimal performance and least latency for gaming users?
  * AWS ElastiCache
    * Amazon ElastiCache offers fully managed Redis and Memcached. Seamlessly deploy, operate, and scale popular open source compatible in-memory data stores. Popular choice for Gaming, IOT apps, Ad-Tech, Financial Services and Healthcare.
#### An organization planning to use AWS for their production roll out, wants to implement automation for deployment such that it will automatically create a LAMP stack, download the latest PHP installable from S3 and setup the ELB. Which of the below metioned AWS Service meets the requirement for making an orderly deployment of the software?
  * ElastiBeanstalk
    * We can simply upload code and Elasti Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, Auto-Scaling to application Health Monitoring. 
#### Your current log analysis application takes more than four hours to generate a report of a top 10 users of your web application. You have been asked to implement a system that can report this information in real time, ensure that the report is always up to date, and handle increases in the number of requests to your web application. Choose the option that is cost-effective and can fulfill the requirements.
  * Post your log data to Amazon Kinesis data stream, and subscribe your log-processing application so that is configured to process your logging data. 
#### There is a requirement to load a lot of data from your on-premise network on to AWS Redshift. Which of the below options can be used for this data transfer? 
  * Direct Connect
  * Snowball
#### As the cloud administrator of your company, you notice that one of EC2 instances is restarting frequently. There is a need to troubleshoot and analyse the system logs. What can be used in AWS to store and analyze the log files from the EC2 Instances?
  * AWS CLoudWatch Logs
#### Your company has migrated their production environment into AWS VPC 6 months ago. As a cloud architect, you are required to revise the infrastructure and ensure that it is cost-effective in the long term. There are more than 50 EC2 instances that are up and running all the time to support the business operation. What can you do to lower cost?
  * Reserved Instance
    * when you have instances that will be used continuously and throughout the year.
#### You have configured an Auto-scaling group for which the minimum running instance is 2 and maximum running instance is 10. For the past 30 minutes, all five instances have been running at 100 CPU utilization; however, the AutoScaling group has not added any more instances to the group. What is the most likely cause for this?
  * You already have 20 on-demand instances
  * The Auto Scaling group's scale up policy has not yet been reached
    * By default, you can run upto 20 on-demand EC2 instances. If you need more, you have to complete a requisition form and submit it to AWS. 
#### A company has an application hosted in AWS. This application consists of EC2 instances that sit behind ELB with EC2 instances. The following are requirements from an administrative perspective
  * a. Must be able to collect and analyze logs with regard to ELB's performance
  * b. Ensure that notifications are sent when the latency goes beyond 10 seconds.
  * Which of the following can be used to achieve this requirements?
    * Use CloudWatch for monitoring
    * Enable the logs on the ELB and then investigate the logs whenever there is an issue. 
 #### Your company would like to leverage the AWS storage option and integrate it with the current on-premise infrastructure. Besides, due to business requirements, low latency access to all the data is a must. Which of the following options would be best suited for this scenario?
  * Configure Storage Gateway Stored Volume
    If you need low-latency access to your database, first configure your on-premise gateway to store all your data locally. Then asynchronously back up point-in-time snapshots of this data to Amazon S3. This configuration provides durable and inexpensive offsite backups that you can recover to your local data center or Amazon EC2.
#### An IT company would like to secure their resources in their AWS Account. Which of the following options is able to secure data at rest and in transit in AWS?
  * Encrypt all EBS volumes attached to EC2 instances
  * Use Server-Side Encryption for S3
  * Use SSL/HTTPS when using the Elastic Load Balancer
#### Your company is hosting an appication in AWS. The application is read intensive and consists of a set of web servers and AWS RDS. It has been noticed that the response time of the application decreases due to the load on the AWS RDS instance. Which of the following measures can be taken to scale the data tier?
  * Create a Amazon DB read replica. Configure the application layer to query the Read Replicas for query needs.
  * Use ElastiCache in front of your Amazon RDS DB to cache common queries
    * RDS read replica provides enhanced performance and durability for database(DB) instances. This replication feature makes it easy to elastically scale out beyond the capacity constrants of a single DB Instance for read-heavy database workloads.
