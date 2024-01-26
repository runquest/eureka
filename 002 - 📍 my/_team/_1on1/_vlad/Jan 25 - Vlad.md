---
aliases: 
tags:
  - 1on1
  - vlad
created at: 2024-01-25
JIRA Filter: "[Vlad's filter](https://molecularyou.atlassian.net/issues/?filter=10023)"
Topics:
---
----
### What is on Vlad's mind?
* Work is priority now that school is easy
* Rollback of Penguin - DB + App Deployment
	* We needed to rollback 5 days and Penguin images is not returned - investigating, but not a quick fix that was visible - no point in fixing pipeline for that at the moment
* Epheral environment
	* Seeds broke: working with Erick (2 fixes)
	- [ ] We should recreate environments once a month? #my #aiste
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
