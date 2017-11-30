# **xmr-stack-cpu-installer**
## **installer for ubuntu 16.04/16.10 server.**



### THIS SCRIPT DOWNLOAD, COMPILE, INSTALL AND MAKE SETTING OF XMR-STACK-CPU AND INSTALL CPULIMIT FOR LIMIT CPU USAGE FOR A SIMPLE VPS RUNNING UBUNTU 16.04 SERVER

#### **USAGE**:
	 :~# ./xmr-stack-cpu_ubuntu {WALLET} {PASSWORD} {+NAMEOFWORKER} {POOL} {PERCENTAGEOFCPULIMIT}"

##### **like this**: 
	 :~# ./xmr-stack-cpu_ubuntu 48zHnevytL2Rbhf38Ma5msRtDeXvJ8d8pHCAw3NMdNd9iEGhnnnSZC1cfxdtVx32xN6BMDdfgDZHaaianRA831PyLPcy5tk x +vps5 xmrpool.eu 3333 3





#### **this script run and tested with xmrpool.eu, it's for 2 core vps.**

##### --------------------------------------------------------------------------------------------
#### **For use more core edit /root/xmr-stack-cpu/bin/config.txt and comment # or delete this line:**
  
  [
     { "lowpowermode" : false, "noprefetch" : true, "affinetocpu" : 0 },
      { "lowpowermode" : false, "noprefetch" : true, "affinetocpu" : 1 },
    ],

###### **Change with:**
	 null,

###### **Run manually the miner:**

	 ./root/miner
###### copy the suggestion and write in config.txt like this:
	"cpu_threads_conf" :
		 [
		    { "lowpowermode" : false, "noprefetch" : true, "affinetocpu" : false },
		],




##### --------------------------------------------------------------------------------------------

#### KNOWED ISSUE:
POOL name_of_worker:
- check if pool have sign like "wallet.nameofworker",

	yes? put it in NAMEOFWORKER field.
	
    no? for other pool leave blank "" the NAMEOFWORKER field.
