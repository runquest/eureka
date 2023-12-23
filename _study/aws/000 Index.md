
### What to pay attention to?

- Application architects require storage solution
- Make the architecture highly available and more cost effective - autoscaling, load balancers, availability zones
- Access limitation - security groups, network access levels, firewalls, cloudfront



##### Test domain 1: Design **Resillient** Architectures

Understand various *block*, *file*, *object* storage technologies and their usecases: 
[ ] [[Amazon EBS]]
[ ] [[Instance Store]]
[ ] [[Amazon EFS]]
[ ] [[Amazon S3]]
[ ] [[Amazon FSx]]

Architecture need to be highly available and fault tolerant:
[ ] [[Amazon Elastic Load Balancing]]
[ ] [[Amazon Route 53]]
[ ] [[Amazon TDS Read Replicas]]
[ ] [[Multi-AZ]]

Understand [ ] [[AWS Global Infrastructure]] in order to determine how to design application stacks to best use the underlying infrastructure architecture.

##### Test domain 2: Design **High-Performing** Architectures

- [ ] Able to select best storage and database services to use for a given scenario based on performance
- [ ] Able to implement elasticity and scalability to architecture effectively at *application, storage, & database layers*:
	[ ] [[AWS Auto Scaling]]
	[ ] [[EC2 Auto Scaling]]

##### Test domain 3: Design **Secure** Applications and Architectures

- [ ] Understand how to configure security controls for *authentication, authorization, access and encryption to data*
- [ ] Know how to design isolation and separation
	[ ] AWS service architecture
	[ ] Amazon [[0011 - EC2]] instance deployment options
	[ ] Amazon VPC configurations
- [ ] Best practices
	[ ] implementing services in the most secure manner
	[ ] creating users, groups and roles using [[AWS IAM]]
	[ ]  [[AWS Directory Servises]]
	[ ] Technologies that include DDoS mitigation: 
		[ ] [[AWS Auto Scaling]]
		[ ] [[Cloudfront]]
		[ ] [[Amazon Route 53]]
- [ ] Monitoring & logging
	[ ] [[Amazon CloudWatch]]
	[ ] [[AWS CloudTrail]]
	[ ] when and what penetration testing you are allowed to perform within AWS cloud
	[ ] compliance programs AWS complies with
- [ ] Technologies
	[ ] [[Amazon VPC]]
	[ ] [[AWS KMS]]
	[ ] [[AWS CloudHSM]]
	[ ] [[AWS IAM]]
	[ ] [[Amazon Cognito]]
	[ ] [[AWS Directory Servises]]

##### Test domain 4: Design **Cost-Optimized** Architectures
- [ ] Undnerstand the various cost models of compute and storage services

-----
[[0010 - Compute]]
	[[0011 - EC2]]
	[[0012 - Amazon EBS]]
	[[0013 - Elastic Load Balancer]]
	[[0014 - AWS Auto Scaling]]
	[[0015 - Amazon ECS]]
	[[0016 - AWS Lambda]]
[[0020 - Storage]]
[[0030 - AWS Database]]
[[0040 - Migration]]
[[0050 - Networking and Content Delivery]]
[[0060 - Management Tools]]
[[0070 - Analytics]]
[[0080 - AWS Security, Identity & Compliance]]
[[0090 - Application Integration]]
[[0100 - AWS Desktop & App Strea]]