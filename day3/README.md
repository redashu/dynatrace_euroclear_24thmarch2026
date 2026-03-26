# dynatrace_euroclear_24thmarch2026

### Install & configure info of Oneagent 

```
2-user@ip-172-31-36-243 ~]$ sudo -i
[root@ip-172-31-36-243 ~]# cd /opt/dynatrace/
[root@ip-172-31-36-243 dynatrace]# ls
autoupdater  gateway  oneagent  remotepluginmodule
[root@ip-172-31-36-243 dynatrace]# cd oneagent/
[root@ip-172-31-36-243 oneagent]# ls
agent
[root@ip-172-31-36-243 oneagent]# cd agent/
[root@ip-172-31-36-243 agent]# ls
SELinuxPolicy                          authorizedkeys  datasources            installer.version  libmusl64  tools
THIRDPARTYLICENSEREADME.txt            bin             dt_fips_disabled.flag  lib                rdp        uninstall.sh
agentinstaller-sbom-external.cdx.json  conf            initscripts            lib64              res
[root@ip-172-31-36-243 agent]# cd conf/
[root@ip-172-31-36-243 conf]# ls
dt-extensibility-root.cert.pem  loganalytics.schema.json  ruxitagentnetwork.conf  ruxitserverfull.pem             watchdog.conf
extensions.conf                 oneagent.conf             ruxitserver.pem         securityRulesLoganalytics.json
[root@ip-172-31-36-243 conf]# vim oneagent.conf 
[root@ip-172-31-36-243 conf]# cd /var/lib/dynatrace/
[root@ip-172-31-36-243 dynatrace]# ls
enrichment  gateway  oneagent  packages  remotepluginmodule
[root@ip-172-31-36-243 dynatrace]# 
[root@ip-172-31-36-243 dynatrace]# 
[root@ip-172-31-36-243 dynatrace]# cd oneagent/
[root@ip-172-31-36-243 oneagent]# ls
agent  datastorage
[root@ip-172-31-36-243 oneagent]# ls agent/
backup  config  customkeys  downloads  installer_tmp  runtime  watchdog
[root@ip-172-31-36-243 oneagent]# ls datastorage/
crashreports  loganalytics  memorydump  supportalerts
[root@ip-172-31-36-243 oneagent]# 
[root@ip-172-31-36-243 oneagent]# ls /var/log/dynatrace/
autoupdater  gateway  oneagent  supportarchive

```

### AI in dynatrace with Internal components 

<img src="aic.png">

### AI model types 

<img src="aic1.png">

### Installing Docker 

```
yum install docker -y

systemctl enable --now docker 

===> deploying webapp as container 


docker run -itd --name ashuc1 -p 1234:80 nginx

docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS                                   NAMES
df4f2720b16b   nginx     "/docker-entrypoint.…"   7 minutes ago   Up 7 minutes   0.0.0.0:1234->80/tcp, :::1234->80/tcp   ashuc1

```

