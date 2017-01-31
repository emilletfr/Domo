# My Domo 🏠
HomeKit compliant Home Automation System from WiFi Modules to Local Server
<br><br>
![](https://docs.google.com/uc?id=0BxOSr4OUvNOfMWEwOHRkcnNvcU0)
<br>
## Wifi Modules
Role
- Retrieve informations such as indoor ambiant temperature, humidity, bed occupancy
- Command actuators such as boiler pomp, boiler heater, open/close rollers shutters

Hardware part is composed of [NodeMcu](http://nodemcu.com/index_en.html) module, Temperature/Humidity sensor, Relays, PCB, USB power supply, Casing.
<br>
Firmware part for NodeMcu module is written in LUA
## Local Server
Role
- Emulate iOS HomeKit API
- Compute data from WiFi modules, services (Sunrise time, Sunset time, Outdoor temperature), HomeKit service
- Command actuators in consequence

Infrastructure is a x86-64 architecture system which runs Ubuntu with [Docker](https://www.docker.com) installed and... that's all! 
Docker's magic operate in such a way that the rest of stack components are Docker images.
### Vapor Stack
Retrieve/Compute/Send datas from/to Wi-Fi modules, services, homebridge interface.<br>
Container images and sources: [Ubuntu/Swift image](https://hub.docker.com/r/swiftdocker/swift/), Vapor powered Server image
### Portainer Stack
Ease Docker management with a useful graphic user interface.<br>
Container installation guide: [Portainer](http://portainer.io).
### Homebridge Stack
Emulate iOS Homekit API, declare needed HomeKit accessories/services<br>
Container image and sources: Debian/Node.js/Homebridge/homebridge-httpeverything.


