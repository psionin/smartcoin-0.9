![Logo](http://smartcoin.cc/images/smartcoin2-196x196.png)

* [website](http://smartcoin.cc)
* [explorer](http://smartchain.cc)
* [bitcointalk](https://bitcointalk.org/index.php?topic=675821.0)
* [subreddit](https://www.reddit.com/r/Smartcoin_smc/)
* [wallet-win32](https://github.com/psionin/smartcoin/releases/download/0.9.1/smartcoin-0.9.1.zip)

SmartCoin Attributes
--------------------
X11 | DGW3 | 2 minute blocks | 30 million supply | version stable since 2015


License
-------
Copyright © 2009-2015 Bitcoin, Litecoin, and SmartCoin Developers. SmartCoin is released under the terms of the [MIT license](http://opensource.org/licenses/MIT).


Source Code
-----------
The master branch has the latest stable release code for Linux servers running smartcoind. See 'msvc' branch for building the wallet in Visual Studio.


Build Instructions
------------------

Note: this version by default works best on Debian 8, with boost library version 1.55, bdb version 4.8, and openssl version 1.0.0; to build on a different system, you would have to make sure to use the right versions of these dependencies.

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
