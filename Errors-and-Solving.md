#### can not start docker daemon, because of docker0 has exists.
**error info:**
```
INFO[0000] Default bridge (docker0) is assigned with an IP address 172.17.0.0/16. Daemon option --bip 
can be used to set a preferred IP address
FATA[0000] Error starting daemon: Error initializing network controller: Error creating default "bridge" 
network: cannot create network docker0 (9553b18c05db5f513bdd6198b6f79009719537511c337f53bc534fa514c89cda): 
conflicts with network 29dea97c02f2296703ea9ca303ad6f68c7f7c99408c3094117ed7039044eba62 (docker0): 
networks have same bridge name
```
#### solve
```
yum install bridge-utils
ip link  set docker0 down
brctl delbr docker0

```

#### remove docker
```
rm docker/bins
rm -rf /var/lib/docker
```
