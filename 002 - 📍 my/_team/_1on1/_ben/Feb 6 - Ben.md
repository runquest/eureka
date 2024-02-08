---
aliases: 
tags:
  - 1on1
  - ben
created at: 2024-02-06
JIRA Filter: "[Ben JIRA](https://molecularyou.atlassian.net/issues/?filter=10015)"
Topics:
---
----
### What is on Ben's mind?

* We need consistent data at different stages
- read replica and then promote it
- we are at aws 
- writing scripts for testing
- TDD
- meet up is kicking off in march


* Hard to define what is dead or alive in code base
	* 
* Review: https://github.com/molecularyou/mynd/pull/208
* PDF hold report - remove state machine
* SQS complete - Active 

### What is on Aiste's mind - talked about

* Test: when report is on hold client shoudl not see it;
* Heavy Queries: Take a day next week to investigate AppSignal and find low hanging fruits to fix. https://molecularyou.atlassian.net/browse/EXP-146
* Professional Development program: Ben can only consider going to Rails conference
* 

* I see 8+ tickets in progress
	* where did motivation for this  came?
		* in preparation for doing changes in regards to reports on hold feature
	* Why is it taking so long
		* MYnd
			* 1-2 days on MYnd
			* 2.5 days of MYhi - higher complexity
			* 1 Planning - report hold
			* Tuesday unproductive

- PDF Hold feature - EOD Monday
- Schema - Vlad's tasks ✅
- PDF Report endpoint - blocking Aiste
- Test Shoryuken and merge
- NEXT: Sendgrid emails


### Projects
##### Database Migrations
Database schema - created two tickets one for MYhi and one for MYnd - schema's between production and staging completely off.
	* Decided: 
	1) Back up environment data; 
	2) Take schema from Production; 
	3) Load production schema 
	4) Load back data
#### Technical Debt
* Update Health Report model with Display + Unit object 

### Action points from last meeting
```dataview
TASK 
FROM "002 - 📍 my/_team/_1on1/_ben"
WHERE !completed
```

### Action points today
