### Installing oneagent in linux based machine 

### login to root user 

```
ec2-user@ip-172-31-36-243 ~]$ sudo -i
[root@ip-172-31-36-243 ~]# whoami
root
[root@ip-172-31-36-243 ~]# 

===>
Dowanload -->verify --> Install --{follow dynatrace website}

```

### after installation things to verify 

```
cd /opt/
[root@ip-172-31-36-243 opt]# ls
aws  dynatrace
[root@ip-172-31-36-243 opt]# cd dynatrace/
[root@ip-172-31-36-243 dynatrace]# ls
oneagent
[root@ip-172-31-36-243 dynatrace]# cd oneagent/
[root@ip-172-31-36-243 oneagent]# ls
agent
[root@ip-172-31-36-243 oneagent]# cd agent/
[root@ip-172-31-36-243 agent]# ls
SELinuxPolicy                agentinstaller-sbom-external.cdx.json  bin   datasources            initscripts        lib    libmusl64  res    uninstall.sh
THIRDPARTYLICENSEREADME.txt  authorizedkeys                         conf  dt_fips_disabled.flag  installer.version  lib64  rdp        tools

--->

 systemctl status oneagent

● oneagent.service - Dynatrace OneAgent
     Loaded: loaded (/etc/systemd/system/oneagent.service; enabled; preset: disabled)
     Active: active (running) since Tue 2026-03-24 09:31:30 UTC; 1min 34s ago
    Process: 15972 ExecStart=/opt/dynatrace/oneagent/agent/initscripts/oneagent start (code=exited, status=0/SUCCESS)
   Main PID: 16053 (oneagentwatchdo)
      Tasks: 50 (limit: 4666)
     Memory: 136.4M
        CPU: 1.953s
     CGroup: /system.slice/oneagent.service

```

### more systemctl options 

```
18  systemctl stop  oneagent
   19  systemctl status  oneagent
   20  systemctl start  oneagent
   21  systemctl status  oneagent
```

