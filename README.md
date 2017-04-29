![SMC Logo](http://i66.tinypic.com/219crqr.png)
<h5> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [smartcoin.cc](http://smartcoin.cc) &nbsp;&nbsp; [bitcointalk](https://bitcointalk.org/index.php?topic=675821.0) &nbsp;&nbsp; [explorer](http://smartchain.cc) &nbsp;&nbsp; [wallet-win32](https://github.com/psionin/smartcoin/releases/download/0.9.1/smartcoin-0.9.1.zip)<h5>
<br>

SmartCoin Attributes
--------------------
X11 | DGW3 | 2 minute blocks | 24.5 mn total | 16 SMC / block


License
-------
Copyright © 2009-2015 Bitcoin, Litecoin, and SmartCoin Developers. SmartCoin is released under the terms of the [MIT license](http://opensource.org/licenses/MIT).


Source Code
-----------
The master branch has the latest stable release code for Linux servers running smartcoind. See 'msvc' branch for building the wallet in Visual Studio.


Build Instructions
------------------
###### Linux (Ubuntu/Debian)  
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
cd src && make -f makefile.unix
strip smartcoind
mv smartcoind ..
```
