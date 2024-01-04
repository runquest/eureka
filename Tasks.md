-----
##### TO DO from journal
```dataview
TASK 
FROM "000 - 📝 journal"
WHERE !completed
```
---
#### Ideas

tasks can be mine specific to a project and they can come up from meetings, journaling or be reoccurring.
tasks can be the ones that others committed on doing and I want to keep an eye on. 

----
##### TO DO from MY
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
