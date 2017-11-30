# **xmr-stack-cpu-installer**
## **installer for ubuntu 16.04/16.10 server.**



### THIS SCRIPT DOWNLOAD, COMPILE, INSTALL AND MAKE SETTING OF XMR-STACK-CPU AND INSTALL CPULIMIT FOR LIMIT CPU USAGE FOR A SIMPLE VPS RUNNING UBUNTU 16.04 SERVER

#### What it do:
- Upgrade your ubuntu.
- Install dependencies:
	- libmicrohttpd-dev
	- libssl-dev
	- cmake
	- build-essential
	- libhwloc-dev
	- screen
	- git
- Download, compile and install xmr-stack-cpu (compile with 2% fee to dev).
- Configure xmr-stack-cpu (2core, for more core -> )
- Install cpulimit
- create executable file on /root
- crontab for running every reboot


#### **INSTALL**:
	 :~# cd /root/
	 :~# wget https://raw.githubusercontent.com/nowheel/xmr-stak-cpu-installer/master/xmr-stak-cpu_ubuntu
	 :~# chmod +x xmr-stak-cpu_ubuntu
	 :~# ./xmr-stak-cpu_ubuntu {WALLET/USER} {PASSWORD} {+NAMEOFWORKER} {POOL} {PERCENTAGEOFCPULIMIT}"

##### **Like this**:
	 :~# ./xmr-stak-cpu_ubuntu 48zHnevytL2Rbhf38Ma5msRtDeXvJ8d8pHCAw3NMdNd9iEGhnnnSZC1cfxdtVx32xN6BMDdfgDZHaaianRA831PyLPcy5tk x +vps5 xmrpool.eu 3333 3





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
- Check if pool have sign like "wallet.nameofworker",

	Yes? put it in NAMEOFWORKER field.

    No? for other pool leave blank "" the NAMEOFWORKER field

WRONG SETTING AT INSTALL:
- remove all file and folder created by script in /root folder, after reinstall.



#### Next Goals:
- add service instead of crontab
- add parameters for change setting without reinstall it
- change installation folder in opt/
- enable/disable xmr-stak-cpu web interface
- compile new version of xmr-stak instead of xmr-stak-cpu, the new version is ALL IN ONE (xmr-stak-cpu and xmr-stak-gpu in one software).



#### file and folder created in root folder:
		./cpulimit-miner
        ./miner
        ./xmr-stack-cpu_ubuntu
        ./xmr-stak-cpu
        ./xmr-stak-cpu/bin
        ./xmr-stak-cpu/bin/config.txt
        ./xmr-stak-cpu/bin/config.txt.old
        ./xmr-stak-cpu/bin/xmr-stak-cpu
	
	
## Don't forget to buy me a beer:
> _XMR = 48zHnevytL2Rbhf38Ma5msRtDeXvJ8d8pHCAw3NMdNd9iEGhnnnSZC1cfxdtVx32xN6BMDdfgDZHaaianRA831PyLPcy5tk_
