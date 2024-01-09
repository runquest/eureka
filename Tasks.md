##### TO DO from journal
```dataview
TASK 
FROM "000 - 📝 journal/_daily"
WHERE !completed
WHERE !contains(text, "#daily")
```
---
#### Ideas

tasks can be mine specific to a project and they can come up from meetings, journaling or be reoccurring.
tasks can be the ones that others committed on doing and I want to keep an eye on.
how to publish documentation for everyone to see?

----
##### TO DO from MY

- [ ] Mobile application changes 
- [ ] Summarize proposal to Gene
- [ ] Mobile application 
- [x] Archive JIRA boards
- [ ] Prepare for HIPAA project 
- [ ] Set up question of the day
- [x] Make SequalAce work
```dataview
TASK 
FROM "002 - 📍 my"
WHERE !completed
WHERE contains(text, "#my #aiste")
```
##### TO DO from VTA
```dataview
TASK 
FROM "003 - 🎾 vta"
WHERE !completed
```
### TO DO from SBOARD
```dataview
TASK 
FROM "001 - ⭕️ sboard"
WHERE !completed
```
