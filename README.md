Ninja-LWRF-Energy
=================

A Ninjablock driver to interface with the Lightwave RF Energy Monitor, via UDP packets to the JSJS Designs WiFi link. 

The driver can be configured via the ninjablock drivers menu, the first time you use your ninja block with the wifi link, it will be necessary to register the ninja on the wifilink box. This can be done by pressing the register button in the LWRF-Energy driver configuration, then pressing the 'Yes' button on the wifi link box.


Currently only the following features are supported,
* Power sockets
* On/Off light switches
* The energy monitor

The Driver -> Settings menu for the LWRF-Energy allows you to parse your configuration information from the Lightwave RF website.

Alternatively o register light switches/sockets currently requires editing index.js, to add another device cut and paste this

self.emit('register', new Device("Light", "R3D5"));

and change the R and D numbers to match the room and device on the LWRF Wifi Link box.



Todo
=======


* Add support for 433Mhz Lightwave RF devices without needing to use udp via the wifi box.
* Tidy up the code.
