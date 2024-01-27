# Obsidian-workshop-part1
Obsidian cost-free text-oriented tool to enhance Teaching&amp;Leadership workflow

Obsidian's note-taking empowers academics: capturing fleeting ideas, building interconnected knowledge bases, organising research, creating mind maps, and tracking tasks, all while respecting busy schedules.
In a one-hour hands-on share-what-works-for-me workshop, we will become familiar with basic syntax on how to put it to work for work management. Bring your own laptop.

Please pre-install your Obsidian beforehand: https://help.obsidian.md/Getting+started/Download+and+install+Obsidian

## **Cheat-sheet for the final exercise:**

1. Dataview query
```dataview
table remind as "Remind"
where contains(remind, "")
```
_- example of information entry:_
- remind:: thing-to-remind

2. Dataview query
```dataview
TABLE WITHOUT ID L.date as Date, L.event as Event
FROM ""
FLATTEN file.lists as L
WHERE L.date > date(today)
WHERE L.event != blank
SORT L.date
```

_- example of information entry:_
- [date:: 2024-02-05], [event:: unit guides are due]

3. Tasks query
```tasks
not done
description includes remind
```

_- example of information entry:_
- [ ] - remind:: review conference paper


4. Tasks query
```tasks
not done
starts after today
tags include #action
```
_- example of information entry:_
- [ ] do-something #action 📅 2024-02-05
