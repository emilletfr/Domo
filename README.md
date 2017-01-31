# My Domo
Describes my HomeKit compliant Home Automation System from Wifi Modules to Server
<br><br>
![](https://docs.google.com/uc?id=0BxOSr4OUvNOfMWEwOHRkcnNvcU0)
<br>
## Wifi Modules
Role
- Get informations from sensors (indoor temperature/humidity, bed occupancy)
- Command actuators (boiler pomp, boiler heater, open/close rollers shutters)

Hardware part is composed of NodeMcu module, Temperature/Humidity sensor, Relays, PCB, USB power supply, Casing.
<br>
Firmware part for NodeMcu module is written in LUA
## Local Server
Role
- Emulate iOS HomeKit API
- Compute data from sensors, services (Sunrise time, Sunset time, Outdoor temperature), HomeKit Service
- Command actuators in consequence

Local server is a x86-64 system which runs Ubuntu with Docker installed and... that's all! 
Docker's magic operate in such a way that the rest of stack components are docker images.
### Vapor Stack
Docker container that runs Ubuntu/Swift image and Vapor powered Server image.
### Portainer Stack
Docker container that runs Portainer in order to ease Docker management.
### Homebridge Stack
Container that runs (in one image) : Debian, Node.js, Homebridge and homebridge-httpeverything plugin.


