### DQL examples 

```
fetch dt.system.events
| fields timestamp , bucket

===> renaming field

fetch dt.system.events
| fieldsRename timestamp,mytime

===>
fetch dt.system.events
| filter contains(event.type ,"GET")

===>
fetch dt.system.events
| filter contains(event.type ,"GET")
| limit 10
```

### Timeseries data -- core metrics 

```
timeseries avg(dt.host.cpu.usage) , by:{dt.entity.host} , interval:5m
```