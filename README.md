NFK Server Launcher
==============

Console Launcher for NFK dedicated server ([Need For Kill](http://needforkill.ru)).

![](http://habrastorage.org/storage2/62a/fa1/3eb/62afa13ebd5c19015dc48aa48501bc84.png)


## Features
* Console interface (native for dedicated)
* Autorestart NFK server when it crashed
* Set processor affinity and priority to NFK server process
* Easy to install as a windows service
* Autoupdate NFK server files ([how it works?](https://github.com/HarpyWar/nfk-service-launcher/wiki/%D0%90%D0%B2%D1%82%D0%BE%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5))

### Requirements
* [.NET Framework 3.5](http://www.microsoft.com/en-us/download/details.aspx?id=21) (but it can be compiled with version >=2.0)



### Config

There are custom parameters can be defined in `nfkservice.xml`:
* `Title` - console title (it also used for windows service description)
* `ServerExeFile` - path to server.dat (nfk dedicated server executable)
* `ExeParameters` - parameters to start nfk server
* `LogFile` - realtime.log from nfk server
* `ProcessorAffinity` - set [processor affinity](http://bit.ly/ZWkGpM) mask to the server process (hex value)
* `ProcessorPriority` - set [processor priority](http://bit.ly/Urr7Rn) to the server process (numeric value 0-5)
* `ServiceName` - windows service name, used on install/uninstall event only
* `AutoUpdate` - enable/disable autoupdate
* `AutoUpdateUrl` - url to xml file that contain information with latest server version and files to update

Config file name must match exe file name. For example: `launcher.exe` and `launcher.xml`.

if config file doesn't exist, then default values are used.



### Installation as a windows service

Just run launcher with one of the parameters:

* `/install` or `/i` - install new service
* `/uninstall` or `/u` - uninstall exist service

For example: `nfkservice.exe /i`

*Note: Administrator rights are required.*

### Control using external scripts

* `sc stop NFK` - stop service
* `sc stop NFK` - start service
* `sc query NFK` - get service state

### [Installation on Linux](https://github.com/NeedForKillTheGame/nfk-service-launcher/wiki/NFK-server-on-Linux)

<br />

## Web Interface to control servers

* [Web API](https://github.com/HarpyWar/nfk-service-launcher/wiki/Web%20API)

[![](http://habrastorage.org/storage2/72a/c7c/bf4/72ac7cbf4a7cc64e3ea4673f12af5d43.jpg)](http://habrastorage.org/storage2/cb6/905/907/cb69059075cdc573a61dbdb67fc50722.png)
[![](http://habrastorage.org/storage2/11f/66c/508/11f66c508178ff0509aeeab2efa241d2.jpg)](http://habrastorage.org/storage2/1c3/32f/2c0/1c332f2c04642362ea9b2607356d9f29.png)
[![](http://habrastorage.org/storage2/edd/9fb/d1e/edd9fbd1e1afa6072ceb469cb8cbc16a.jpg)](http://habrastorage.org/storage2/215/25f/751/21525f75109b38dad7ebf5ff9e5da53f.png)
