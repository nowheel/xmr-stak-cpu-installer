# xmr-stack-cpu-installer
# installer for ubuntu 16.04/16.10 server.

THIS SCRIPT DOWNLOAD, COMPILE, INSTALL AND MAKE SETTING OF XMR-STACK-CPU AND INSTALL CPULIMIT FOR LIMIT CPU USAGE FOR A SIMPLE VPS RUNNING UBUNTU 16.04 SERVER

DONATE XMR:
48zHnevytL2Rbhf38Ma5msRtDeXvJ8d8pHCAw3NMdNd9iEGhnnnSZC1cfxdtVx32xN6BMDdfgDZHaaianRA831PyLPcy5tk

USAGE:
:~# ./install_mining_server {WALLET} {PASSWORD} {+NAMEOFWORKER} {POOL} {PERCENTAGEOFCPULIMIT}"

this script run and tested with xmrpool.eu, it's for 2 core vps.

For use more core edit /root/xmr-stack-cpu/bin/config.txt and comment # or delete this line:
  
  [
     { "low_power_mode" : false, "no_prefetch" : true, "affine_to_cpu" : 0 },
      { "low_power_mode" : false, "no_prefetch" : true, "affine_to_cpu" : 1 },
    ],

Change with:
  null,

Run manually the miner:
./root/miner
copy the suggestion and write in config.txt like this:
"cpu_threads_conf" :
[
    { "low_power_mode" : false, "no_prefetch" : true, "affine_to_cpu" : false },
],




KNOWED ISSUE:
POOL name_of_worker:
- check if pool have sign like "wallet.nameofworker", 
    -yes? put it in NAMEOFWORKER field.
    -no? for other pool leave blank "" the NAMEOFWORKER field.
