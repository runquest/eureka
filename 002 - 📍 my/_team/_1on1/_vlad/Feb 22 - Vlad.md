---
aliases: 
tags:
  - 1on1
  - vlad
created at: 2024-02-22
JIRA Filter: "[Vlad's filter](https://molecularyou.atlassian.net/issues/?filter=10023)"
Topics:
---
----
### What is on Vlad's mind?

* On going
	* debugging certbot - prod is good 
		* penguin myhi will went down in 7 days - we got throttled
		* others will be updated automatically
		* 6 certificate renewals
	* shoryuken issues - graceful shutting it down
		* architectural problem
		* graceful shutdown script runs on redeploys, but it will not trigger if it is rolled back, and not triggered if instance to go down
		* shoryuken is running in the same container and 
			* risk based situation - happens not much
		* running experiment on how EB runs 2 containers
		* switching to multi containers platform
		* when rails receives graceful shutdown script send signal to shoryuken, rollbacks
		* how to fix if message is missed
	* nova - nothing focused on certbot which is complex
* Access review - Aiste asked to add POC account + sophos, review aws


## Marc's proposal - Vlad's thoughts
Agreed with most things and disagreed with some.

* Sharing resources (isolation) & co-locating for the cost sharing resources
	* we are saving: 1RDS, 1NAT, 1 Bastion (50 - 100 /month)
	* deploys would be slower, and rollback and slower
* Security + Deploys hard line to walk
* Environment optimization for speed

* Time & priority constraints
* started talking in April , started work in august
* Terraform vs. Pulumi
* ACM - breaks HIPAA, and that's why we are dealing with Certbot Lambda's. 
	* load balance to instance leg is unencrypted - maybe Fargate instance provides with certificates;
* Snowflake connects to Fivetran via bastion
	* VPC Peering
* Load balancer

Consider:
	* ECS (Container orchestrator) / EC2 
	* ECS/ Fargate




* Work is priority now that school is easy
* Rollback of Penguin - DB + App Deployment
	* We needed to rollback 5 days and Penguin images is not returned - investigating, but not a quick fix that was visible - no point in fixing pipeline for that at the moment
* Epheral environment
	* Seeds broke: working with Erick (2 fixes)
	- We should recreate environments once a month? #my #aiste
	- Local redirects were broken - fixed with kind of a patch
	- + added pretty domains - for future we will be using ticket numbers for it
* Primary focus: Infrastructure as Code
	* Low response rate from Ben & Skyler on Vlad's PRs
* Ben took back SQS Pulumi project
	* Vlad's surprised that Ben studied on his own time
### What is on Aiste's mind?

- Latest Infrastructure diagram
- AWS Inspector - enable
- VPN renewals - i do not want people coming and saying their internet is not working

### Projects
[Vlad's filter](https://molecularyou.atlassian.net/issues/?filter=10023)

**Epheral environments:**

Lambdas
SQS
EC2
IAMs

**Missing:**
Beanstalk
IAMs (granual permissions)

### Action points from last meeting

```dataview
TASK 
FROM "002 - 📍 my/_team/_1on1/_vlad"
WHERE !completed
```


### Action points today
