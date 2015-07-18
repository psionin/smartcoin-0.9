![SMC Logo](http://i60.tinypic.com/nvxreo.png)
<h5> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [smartcoin.cc](http://smartcoin.cc) &nbsp;&nbsp; [bitcointalk](https://bitcointalk.org/index.php?topic=675821.0) &nbsp;&nbsp; [explorer](http://smartchain.cc) &nbsp;&nbsp; [wallet-win32](https://github.com/psionin/smartcoin/releases/download/0.9.1/smartcoin-0.9.1.zip)<h5>
<br>

SmartCoin Attributes
--------------------
PoW Algorithm: X11  
Block Interval: 2 minutes  
Difficulty Retarget: DarkGravityWave  
Block Subsidy: 16 SMC  
Total Coin Supply: ~24.5 million coins


License
-------
Copyright © 2009-2015 Bitcoin, Litecoin, and SmartCoin Developers. SmartCoin is released under the terms of the [MIT license](http://opensource.org/licenses/MIT).


Source Code
-----------
The master branch should have the latest stable release code.


Build Instructions
------------------
###### Linux (Ubuntu)  
To build on Linux, first make sure you have the necessary dependencies
```
apt-get update && apt-get upgrade
apt-get install ntp git build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev libqrencode-dev libminiupnpc-dev
```
Get the daemon source code
```
git clone https://github.com/psionin/smartcoin
```
Then go into the directory
```
cd smartcoin
```
Change permissions for a leveldb build file
```
chmod 755 src/leveldb/build_detect_platform  
```
Compile and move smartcoind
```
cd src && make -f makefile.unix USE_UPNP=1 USE_IPV6=1
strip smartcoind
mv smartcoind ..
```
