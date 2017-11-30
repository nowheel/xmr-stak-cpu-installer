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
	 :~# ./xmr-stack-cpu_ubuntu {WALLET/USER} {PASSWORD} {+NAMEOFWORKER} {POOL} {PERCENTAGEOFCPULIMIT}"

##### **Like this**: 
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
-
- Check if pool have sign like "wallet.nameofworker",

	Yes? put it in NAMEOFWORKER field.
	
    No? for other pool leave blank "" the NAMEOFWORKER field

WRONG SETTING AT INSTALL:
- remove all file and folder created by script in /root folder, after reinstall.



#### Next Goals:
- delete old precompiling files of xmr-stak-cpu
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
        ./xmr-stak-cpu/CMakeCache.txt
        ./xmr-stak-cpu/CMakeFiles
        ./xmr-stak-cpu/CMakeFiles/3.5.2
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CMakeCCompiler.cmake
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CMakeCXXCompiler.cmake
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CMakeDetermineCompilerABI_C.bin
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CMakeDetermineCompilerABI_CXX.bin
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CMakeSystem.cmake
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CompilerIdC
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CompilerIdC/CMakeCCompilerId.c
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CompilerIdC/a.out
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CompilerIdCXX
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CompilerIdCXX/CMakeCXXCompilerId.cpp
        ./xmr-stak-cpu/CMakeFiles/3.5.2/CompilerIdCXX/a.out
        ./xmr-stak-cpu/CMakeFiles/CMakeDirectoryInformation.cmake
        ./xmr-stak-cpu/CMakeFiles/CMakeError.log
        ./xmr-stak-cpu/CMakeFiles/CMakeOutput.log
        ./xmr-stak-cpu/CMakeFiles/CMakeTmp
        ./xmr-stak-cpu/CMakeFiles/Makefile.cmake
        ./xmr-stak-cpu/CMakeFiles/Makefile2
        ./xmr-stak-cpu/CMakeFiles/TargetDirectories.txt
        ./xmr-stak-cpu/CMakeFiles/cmake.check_cache
        ./xmr-stak-cpu/CMakeFiles/feature_tests.bin
        ./xmr-stak-cpu/CMakeFiles/feature_tests.c
        ./xmr-stak-cpu/CMakeFiles/feature_tests.cxx
        ./xmr-stak-cpu/CMakeFiles/progress.marks
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/C.includecache
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/DependInfo.cmake
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/build.make
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/cmake_clean.cmake
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/cmake_clean_target.cmake
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/crypto
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/crypto/c_blake256.c.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/crypto/c_groestl.c.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/crypto/c_jh.c.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/crypto/c_keccak.c.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/crypto/c_skein.c.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/crypto/soft_aes.c.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/depend.internal
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/depend.make
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/flags.make
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/link.txt
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-c.dir/progress.make
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/CXX.includecache
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/DependInfo.cmake
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/build.make
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/cli-miner.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/cmake_clean.cmake
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/console.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/crypto
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/crypto/cryptonight_common.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/depend.internal
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/depend.make
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/executor.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/flags.make
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/httpd.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/jconf.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/jpsock.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/link.txt
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/minethd.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/progress.make
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/socket.cpp.o
        ./xmr-stak-cpu/CMakeFiles/xmr-stak-cpu.dir/webdesign.cpp.o
        ./xmr-stak-cpu/CMakeLists.txt
        ./xmr-stak-cpu/FREEBSDCOMPILE.md
        ./xmr-stak-cpu/LICENSE
        ./xmr-stak-cpu/LINUXCOMPILE.md
        ./xmr-stak-cpu/Makefile
        ./xmr-stak-cpu/README.md
        ./xmr-stak-cpu/WINCOMPILE.md
        ./xmr-stak-cpu/autoAdjust.hpp
        ./xmr-stak-cpu/autoAdjustHwloc.hpp
        ./xmr-stak-cpu/bin
        ./xmr-stak-cpu/bin/config.txt
        ./xmr-stak-cpu/bin/config.txt.old
        ./xmr-stak-cpu/bin/xmr-stak-cpu
        ./xmr-stak-cpu/cli-miner.cpp
        ./xmr-stak-cpu/cmake_install.cmake
        ./xmr-stak-cpu/config.txt
        ./xmr-stak-cpu/console.cpp
        ./xmr-stak-cpu/console.h
        ./xmr-stak-cpu/crypto
        ./xmr-stak-cpu/crypto/c_blake256.c
        ./xmr-stak-cpu/crypto/c_blake256.h
        ./xmr-stak-cpu/crypto/c_groestl.c
        ./xmr-stak-cpu/crypto/c_groestl.h
        ./xmr-stak-cpu/crypto/c_jh.c
        ./xmr-stak-cpu/crypto/c_jh.h
        ./xmr-stak-cpu/crypto/c_keccak.c
        ./xmr-stak-cpu/crypto/c_keccak.h
        ./xmr-stak-cpu/crypto/c_skein.c
        ./xmr-stak-cpu/crypto/c_skein.h
        ./xmr-stak-cpu/crypto/cryptonight.h
        ./xmr-stak-cpu/crypto/cryptonight_aesni.h
        ./xmr-stak-cpu/crypto/cryptonight_common.cpp
        ./xmr-stak-cpu/crypto/groestl_tables.h
        ./xmr-stak-cpu/crypto/hash.h
        ./xmr-stak-cpu/crypto/int-util.h
        ./xmr-stak-cpu/crypto/skein_port.h
        ./xmr-stak-cpu/crypto/soft_aes.c
        ./xmr-stak-cpu/donate-level.h
        ./xmr-stak-cpu/executor.cpp
        ./xmr-stak-cpu/executor.h
        ./xmr-stak-cpu/httpd.cpp
        ./xmr-stak-cpu/httpd.h
        ./xmr-stak-cpu/hwlocMemory.hpp
        ./xmr-stak-cpu/install_manifest.txt
        ./xmr-stak-cpu/jconf.cpp
        ./xmr-stak-cpu/jconf.h
        ./xmr-stak-cpu/jext.h
        ./xmr-stak-cpu/jpsock.cpp
        ./xmr-stak-cpu/jpsock.h
        ./xmr-stak-cpu/libxmr-stak-c.a
        ./xmr-stak-cpu/minethd.cpp
        ./xmr-stak-cpu/minethd.h
        ./xmr-stak-cpu/msgstruct.h
        ./xmr-stak-cpu/rapidjson
        ./xmr-stak-cpu/rapidjson/allocators.h
        ./xmr-stak-cpu/rapidjson/document.h
        ./xmr-stak-cpu/rapidjson/encodedstream.h
        ./xmr-stak-cpu/rapidjson/encodings.h
        ./xmr-stak-cpu/rapidjson/error
        ./xmr-stak-cpu/rapidjson/error/en.h
        ./xmr-stak-cpu/rapidjson/error/error.h
        ./xmr-stak-cpu/rapidjson/filereadstream.h
        ./xmr-stak-cpu/rapidjson/filewritestream.h
        ./xmr-stak-cpu/rapidjson/fwd.h
        ./xmr-stak-cpu/rapidjson/internal
        ./xmr-stak-cpu/rapidjson/internal/biginteger.h
        ./xmr-stak-cpu/rapidjson/internal/diyfp.h
        ./xmr-stak-cpu/rapidjson/internal/dtoa.h
        ./xmr-stak-cpu/rapidjson/internal/ieee754.h
        ./xmr-stak-cpu/rapidjson/internal/itoa.h
        ./xmr-stak-cpu/rapidjson/internal/meta.h
        ./xmr-stak-cpu/rapidjson/internal/pow10.h
        ./xmr-stak-cpu/rapidjson/internal/regex.h
        ./xmr-stak-cpu/rapidjson/internal/stack.h
        ./xmr-stak-cpu/rapidjson/internal/strfunc.h
        ./xmr-stak-cpu/rapidjson/internal/strtod.h
        ./xmr-stak-cpu/rapidjson/internal/swap.h
        ./xmr-stak-cpu/rapidjson/istreamwrapper.h
        ./xmr-stak-cpu/rapidjson/memorybuffer.h
        ./xmr-stak-cpu/rapidjson/memorystream.h
        ./xmr-stak-cpu/rapidjson/msinttypes
        ./xmr-stak-cpu/rapidjson/msinttypes/inttypes.h
        ./xmr-stak-cpu/rapidjson/msinttypes/stdint.h
        ./xmr-stak-cpu/rapidjson/ostreamwrapper.h
        ./xmr-stak-cpu/rapidjson/pointer.h
        ./xmr-stak-cpu/rapidjson/prettywriter.h
        ./xmr-stak-cpu/rapidjson/rapidjson.h
        ./xmr-stak-cpu/rapidjson/reader.h
        ./xmr-stak-cpu/rapidjson/schema.h
        ./xmr-stak-cpu/rapidjson/stream.h
        ./xmr-stak-cpu/rapidjson/stringbuffer.h
        ./xmr-stak-cpu/rapidjson/writer.h
        ./xmr-stak-cpu/socket.cpp
        ./xmr-stak-cpu/socket.h
        ./xmr-stak-cpu/socks.h
        ./xmr-stak-cpu/thdq.hpp
        ./xmr-stak-cpu/version.h
        ./xmr-stak-cpu/webdesign.cpp
        ./xmr-stak-cpu/webdesign.h
        ./xmr-stak-cpu/xmr-stak-cpu.cbp


