# My Domo
HomeKit compliant Home Automation System from Wifi Modules to Server
<br><br>
![](https://docs.google.com/uc?id=0BxOSr4OUvNOfV3hVN3VzejZxbFk)
<br>
## Wifi Modules
Wifi Modules aim to 
- Command actuators (boiler pomp, boiler heater, open/close rollers shutters)
- Get informations from sensors (indoor temperature/humidity, bed occupancy)

Hardware part is composed of NodeMcu module, Temperature/Humidity sensor, Relays, PCB, USB power supply, Casing.
<br>
Firmware part for NodeMcu module is written in LUA
## Local Server
Local server is a x86-64 system. It runs Ubuntu with Docker installed. The rest of stack components are docker images
### Vapor Stack
Container that stacks Ubuntu, Swift and Vapor Server 
### Portainer Stack
Container 
### Homebridge Stack
Container that stacks Debian, Node.js, Homebridge and homebridge-httpeverything plugin


