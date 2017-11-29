# **xmr-stack-cpu-installer**
## **installer for ubuntu 16.04/16.10 server.**

###THIS SCRIPT DOWNLOAD, COMPILE, INSTALL AND MAKE SETTING OF XMR-STACK-CPU AND INSTALL CPULIMIT FOR LIMIT CPU USAGE FOR A SIMPLE VPS RUNNING UBUNTU 16.04 SERVER





#### **USAGE**:
> _:~# ./installminingserver {WALLET} {PASSWORD} {+NAMEOFWORKER} {POOL} {PERCENTAGEOFCPULIMIT}"_





#### **this script run and tested with xmrpool.eu, it's for 2 core vps.**


#### **For use more core edit /root/xmr-stack-cpu/bin/config.txt and comment # or delete this line:**
  
 _[
     { "lowpowermode" : false, "noprefetch" : true, "affinetocpu" : 0 },
      { "lowpowermode" : false, "noprefetch" : true, "affinetocpu" : 1 },
    ],_

###### **Change with:**
 _null,_


###### **Run manually the miner:**

_./root/miner_

###### copy the suggestion and write in config.txt like this:
"cpu_threads_conf" :

_[
    { "lowpowermode" : false, "noprefetch" : true, "affinetocpu" : false },
],_






#### KNOWED ISSUE:
POOL name_of_worker:
- check if pool have sign like "wallet.nameofworker", 
    -yes? put it in NAMEOFWORKER field.
    -no? for other pool leave blank "" the NAMEOFWORKER field.
