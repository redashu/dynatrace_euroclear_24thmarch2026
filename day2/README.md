# Info about Grail

![Grail overview](grail1.png)

## Creating custom buckets using Dynatrace REST API

![REST API example](api1.png)

## Dynatrace Architecture

![Dynatrace architecture diagram](arch1.png)

## Dynatrace Grail Storage options and locations in Cloud

![Storage options](st1.png)


## checking status of agents 

```
systemctl status oneagent
   36  systemctl status dynatracegateway.service 
```

### dynatrace native command

```bash
./oneagentctl --version 
1.333.55.20260317-092136
[root@ip-172-31-36-243 tools]# ./oneagentctl --get-server  
{*https://ip-172-31-36-243.ec2.internal:9999/communication;https://172.31.36.243:9999/communication}{https://prod-ap-southeast-5-sydney-ap-southeast-2a.live.dynatrace.com/communication;https://prod-ap-southeast-5-sydney-ap-southeast-2b.live.dynatrace.com/communication;https://prod-ap-southeast-5-sydney-ap-southeast-2c.live.dynatrace.com/communication}{https://sg-ap-southeast-2-52-62-137-27-prod-ap-southeast-5-sydney.live.dynatrace.com/communication;https://sg-ap-southeast-2-13-55-162-49-prod-ap-southeast-5-sydney.live.dynatrace.com/communication;https://sg-ap-southeast-2-52-63-8-98-prod-ap-southeast-5-sydney.live.dynatrace.com/communication;https://sg-ap-southeast-2-13-55-101-144-prod-ap-southeast-5-sydney.live.dynatrace.com/communication;https://sg-ap-southeast-2-13-54-211-156-prod-ap-southeast-5-sydney.live.dynatrace.com/communication}{https://blg71138.live.dynatrace.com:443/communication}
[root@ip-172-31-36-243 tools]# ./oneagentctl --get-monitoring-mode
fullstack
```

#### History

```bash
cd /opt/dynatrace/
ls
cd oneagent/
ls
cd agent/
ls
cd tools/
ls
./oneagentctl --help
./oneagentctl --version 
./oneagentctl --get-server  
./oneagentctl --get-monitoring-mode
```
