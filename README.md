# My Domo
Describes my HomeKit compliant Home Automation System from Wifi Modules to Server
<br><br>
![](https://docs.google.com/uc?id=0BxOSr4OUvNOfMWEwOHRkcnNvcU0)
<br>
## Wifi Modules
Wifi Modules aim to 
- Command actuators (boiler pomp, boiler heater, open/close rollers shutters)
- Get informations from sensors (indoor temperature/humidity, bed occupancy)

Hardware part is composed of NodeMcu module, Temperature/Humidity sensor, Relays, PCB, USB power supply, Casing.
<br>
Firmware part for NodeMcu module is written in LUA
## Local Server
Local Server aim to 
- Compute data from sensors/services (Sunrise/Sunset Time, Outdoor temperature), command actuators
- Relay actions/datas from/to HomeKit

Local server is a x86-64 system which runs Ubuntu with Docker installed and... that's all! 
Docker's magic operate in such a way that the rest of stack components are docker images.
### Vapor Stack
Docker container that runs Ubuntu image, Swift image and Vapor image.
### Portainer Stack
Docker container that runs Portainer in order to ease Docker management.
### Homebridge Stack
Container that runs in one image : Debian, Node.js, Homebridge and homebridge-httpeverything plugin.


