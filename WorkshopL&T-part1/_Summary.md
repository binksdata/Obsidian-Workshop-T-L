
This is a summary file, that sources information from [[Log]] and [[Committee1]] notes.


```dataview
table remind as "Remind"
where contains(remind, "")
```


### Ideas
```dataview
table idea as "idea"
where contains(idea, "")
```


### Tasks
```tasks
not done
description includes remind
```

### Action to take
```tasks 
not done
starts after today
tags include #action
```


### Events
```dataview
TABLE WITHOUT ID L.date as Date, L.event as Event
FROM ""
FLATTEN file.lists as L
WHERE L.date > date(today)
WHERE L.event != blank
SORT L.date
```

### Events extended
```dataview
TABLE L.date as Date, L.event as Event, L.note as Note
FROM ""
FLATTEN file.lists as L
WHERE L.date > date(today)
WHERE L.event != blank
SORT L.date
```



