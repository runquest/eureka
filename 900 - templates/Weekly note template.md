# <%moment(tp.file.title).startOf('isoWeek').format("MMM DD") %> - <%moment(tp.file.title).endOf('isoWeek').format("MMM DD") %>

[[journal/_weekly/<%moment(tp.file.title).subtract(1,'week').format("gggg-[W]ww")%>|<- Previous week]] | [[journal/week/<%moment(tp.file.title).add(1,'week').format("gggg-[W]ww")%>|Next week ->]]


# Days





# Overview
```dataview
table without id
from "journal/_daily"
where week = "<% moment(tp.file.title).format("gggg-[W]ww") %>"
```
 