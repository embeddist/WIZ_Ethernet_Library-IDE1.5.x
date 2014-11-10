WIZ Ethernet Library
========
The Ethernet library lets you connect to the Internet or a local network.  

## Supported devices
* ioShield, WIZ550io (used in W5500)
* W5200 Ethernet Shield, WIZ820io (used in W5200)
* Ethernet Shield (used in W5100)

## Hardware
* [ioShield](http://wizwiki.net/wiki/doku.php?id=osh:ioshield-a:start "ioShield-A")
* [W5200 Ethernet Shield](https://github.com/Wiznet/W5200-Ethernet-Shield "W5200 Ethernet Shield")  
* [Ethernet Shield](http://arduino.cc/en/Main/ArduinoEthernetShield "Ethernet Shield")  

## Software
#### Install WIZ Ethernet library  
Download all files and overwrite onto the"Arduino\libraries\Ethernet" folder in your project in sketch.
- Ethernet folder has two folers, examples and src folers.

#### Select device(shield)  
Uncomment device(shiel) you want to use.  
```cpp
//Arduino\libraries\Ethernet\utility\w5100.h
#ifndef	W5100_H_INCLUDED
#define	W5100_H_INCLUDED

#include <avr/pgmspace.h>
#include <SPI.h>

typedef uint8_t SOCKET;
//#define W5100_ETHERNET_SHIELD
//#define W5200_ETHERNET_SHIELD
#define W5500_ETHERNET_SHIELD
```

#### WIZ550io (if you use, ioShield-A/K/L)
* WIZ550io has a unique real MAC address.
* [WIZ550io](http://wizwiki.net/wiki/doku.php?id=products:wiz550io:start "WIZ550io")
* It configures the network setting which has included MAC address automatically.
* Uncomment WIZ550io with MACADDRESS to user unique real MAC address. 
```cpp
//Arduino\libraries\Ethernet\utility\w5100.h
#if defined(W5500_ETHERNET_SHIELD)
#define WIZ550io_WITH_MACADDRESS // Use assigned MAC address of WIZ550io
#include "utility/w5500.h"
#endif
```

## Using the WIZ Ethernet library and evaluate existing Ethernet example.
All other steps are the same as the steps from the Arduino Ethernet Shield. 
You can use examples in ./Ethernet/examples folder for the Arduino IDE 1.5.7, go to Files->Examples->Ethernet, open any example, then copy it to your sketch file and change configuration values properly.
After that, you can check if it is work well. For example, if you choose 'WebServer', you should change IP Address first and compile and download it. Then you can access web server page through your web browser of your PC or something.

## Revision History
Initial Release : 15 Jul. 2014
