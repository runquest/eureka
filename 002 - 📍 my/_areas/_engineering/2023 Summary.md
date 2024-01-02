---
tags:
---

### OKRs of 2023

| Area | Jan - March | April - June | July - September | October  - December
| --- | --- | --- | --- | --- | --- |



#### Q1
##### **Objective: Summarize resource optimization opportunities**
###### KR #1: On weekly basis report on resource performance / utilization metrics || ==90%==
March 6: Dashboard is reviewed weekly, but it is not relevant to report on it for the entire team at the moment.
###### KR #1: Have benchmarks for the key metrics (CPU, memory management, failed requests, errors, etc.) || ==75%==
March 6: Missing memory management for webapp but coming; 
Dashboard on AWS is built out for application performance tracking & benchmarking.|
#### Q2
##### **Improve Developer Experience** 
###### KR #1: Reduce build times from 20 minute to 5 minutes || ==40%==
Added caching & reduced code build times from 7 to 2 min.
###### KR #2: Ability to run development environment on local machine from A to Z || ==90%==
Testing period with developers.

#### Q3 Nothing.

#### Q4
##### **Get lean & mean** 
###### KR #1: Maintain 0 Common Vulnerability & Exposure (CVE) Issues - Security || ==100%==
With rails upgrade & Ben's work we are at 0. 
###### KR #3: Improve test coverage on MYhi from 28% to 70% || ==60%==
We are at 53% test coverage on MYhi as of December 21.
###### KR #3: Remove Asset Pipeline from application build pipeline: Removed, Updated & Unified frontend || ==60%==

###### KR #4: Enable Science Portal MVP: Science team curate existing biomarkers without engineering team involvement || ==75%==
We deployed Nova to POC and attached it to MYhi. Consensus on Science team is that tool Nova is correct tool, however we should be plugging into MYnd database. There was no expectation to have it deployed to production.
###### KR #5: Ability to launch environment-on-demand || ==40%==
We have an ability to spin it up. However technologically it was not what was intended with this ticket. 

| Repo | # releases / year | Repo |# releases / year | Repo |# releases / year |
|---- | ---- | ---- |---- | ---- | ---- |
| #MYhi | 45 | #MYnd | 23 | #Mobile | 12
#### Commit history for 2023 #myhi 
![[Screenshot 2023-12-21 at 1.27.44 PM.png]]

[[productivity]] how do we track individuals & project productivity
### Biggest projects
* Created API v2
* Vendor QC Automation
* One Signal integration
* Localstack
* Build your own action plan
* Batch QC
* Front end in react
* Provider portal
* Code deletion
* Test coverage
* Explored BlueButton

| date | erick | carin | vlad | syed | sitender | alther | skyler | ben |aiste|
|--|--|--|--|--|--|--|--|--|--|
|jan 30|--|Finishing Vendor Uploads, QC Items when Vlad & Alther back|--|Auto renewals on penguin; Next: Lambda|CIS Framework|--|--|--|--|
|feb 6|Build serializer, API Keys extraction|QC Automation|ASI, QC Automation, Certificate automation|Renaming, Next: Lambda|CIS Framework, Vanta|QC Automation|Onboarding|--|--|
|feb 13|Serializer|QC Automation|QC Automation|Lambda pipeline|--|Vendor uploads|Vendor frontend|--|--|
|march 6|OneSignal|Testing QC Automation, Review portal for Vendors|Deploying QC Automation, ASI cost report, Looked into Pulumi, Next: Iac|Lambda automation, cert automated deploys, Pulumi POC|--|--|Wrapping React FE, Dockerize Local environments|--|away|
|april 17|Testing Build your own AP, Requisition form generated, drying out mailers|Addressing Review portal feedback, decomisioning MYnd FE|Lambda in localstack, DNS records|QC Automation deploy|--|--|--|--|--|
|april 24|Build your own AP Backend complete, Requisition form generated|Batch QC, Reviewer portal, Fixing plasma functionality|Lambda in localstack. Localstack A-Z. Pulumi IaC|--|--|--|Batch QC, Reviewer portal|--|--|
|may 1|Requisition form generate|Plasma only|Requisition Lambda & S3|QC Automation lambda deploy, automated certbot deploys, Threat modeling|--|--|Build your own AP, improve build & deploy times|--|--|
|may 8|--|plasma only|progress Localstack for A-Z tests|--|--|--|Action Plan screens|--|--|
|june 12|Action plans|--|Patching, Data team needs IaC Snowflake to S3|--|--|--|--|--|--|
|july 3|Provider portal flow & kitless workflow, Skinny controllers|Last week: imported new diets, foods, food categories - ready for deploy this week, This week: merging biofunctions + subcategories|Review Lambda documentation by Syed, Reviewed Staging deploy failures, All processes is taking ½ longer, Current week: Unified Dockerfile ticket|Last week: Observing deploys: troubleshooting deploys failures, This week: MariaDB upgrade working on LocalStack first|--|--|Last week: all biomarkers + biomarkers, Kitless onboarding, Inertia, gem to put assets to s3 - needs DevOps, figure out how to manage package.lock better|--|--|
|july 10|--|merge biofunctions & subcategories|Database upgrade 10.3 -> 10.6, Fixed QC pipeline, Xuruken logs into Mynd container is not working|--|--|--|--|--|--|
|august 14|Bluebutton|Provider portal|Lambda memory errors, snowflake s3 integration, mariaDb upgrade|--|--|--|away|--|--|
|september 11|Wrapping data sharing|Provider portal|MariaDB upgrade deploy to prod, Vanta tasks|--|--|--|away|--|--|
|october 16|Code deletion|Product bundles|Nova, patching, Staging down|--|--|--|UI Consolidation|AppSignal, MYhi: Ruby 3.2, Rails 6.5, Coveralls.io|--|
|november 2|Code deletion|Product bundles|Patching, reclaiming pulumi stack|--|--|--|Sample management|PDF reports|--|
|november 27|Test coverage|Biofunction removal|--|--|--|--|Syncup DevOps pulumi basic|PDF reports|--|
|december 18|Seed data|Deployed Biofunction removal|PDF, Pulumi, Bricks|--|--|--|Deployed Sample management|PDF reports|--|
### Changes
**Team changes**
Left: Negin, Syed, Alther, Vlad, Sitender
Onboarded: Skyler, Ben
##### Current structure
```d2
gene <- aiste
aiste <-  skyler
aiste <-  ben
aiste <-  vlad
aiste <-  erick
aiste <-  carin
aiste <-  ravneet
skyler <-  ben
skyler <-  vlad
skyler <-  erick
skyler <-  carin
skyler <-  ravneet
ben <-  erick
ben <-  carin
```
![[Screenshot 2023-12-21 at 2.44.55 PM.png]]![[Screenshot 2023-12-21 at 2.45.29 PM.png]]![[Screenshot 2023-12-21 at 2.45.50 PM.png]]