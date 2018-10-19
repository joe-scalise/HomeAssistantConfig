# Home Assistant Configuration

![Build Status](https://travis-ci.org/joe-scalise/HomeAssistantConfig.svg?branch=master)

This is a backup of my Home Assistant configuration.  I recently moved it all from a Raspberry Pi to Docker.  I have not had any stability issues since - I was constantly chasing some issue or another on the Raspberry Pi/HASS.IO which led me down this path.

I use Docker Compose, and Traefik as a reverse proxy.  

### Highlights of the System Setup

* Traefik takes care of getting a wildcard SSL
* UniFi Security Gateway takes care of updating DNS dynamically
* Canonical Livepatch takes care of updating the server, mostly without reboots
* Docker Compose `restart: always` takes care of restarting containers
* [Watchtower](https://github.com/v2tec/watchtower) takes care of updating running container's images
* [healthchecks.io](https://healthchecks.io/) takes care of service pings and emails me when something is down
* Github takes care of configuration backup (not automatically)
* Travis CI provides automatic builds/test for repository changes

### Containers:

* [homeassistant/home-assistant](https://hub.docker.com/r/homeassistant/home-assistant/) - Home Assistant
* []() - Traefik
* []() - Portainer
* []() - Syncthing
* [v2tec/watchtower](https://github.com/v2tec/watchtower) - Watchtower

Home Assistant is open source software for home automation.  This repo serves as a backup of my configuration.

### System:
- old HP laptop
- Aeotec ZW090 Z-Stick Gen5 US
- Ubiquiti UniFi networking gear
- Synology NAS
- ~~Raspberry Pi 3 running HASS.IO~~
- ~~Waveshare Official Raspberry Pi Power Supply~~
- ~~SanDisk Ultra 64GB MicroSDXC Class 10 UHS Memory Card~~

### Devices:

| Qty   | Name                                                  | Link |
| ----- | ----------------------------------------------------- | ---- |
| 6 | GE Z-Wave Wireless Switches (12722, 12723, 14291, 14294) | [(Amazon)](https://www.amazon.com/gp/product/B01M1AHC3R/) |
| 3 | Amazon Fire TV (3rd Gen) w/ Ethernet Adapters  | |
| 2 | Haiku Home Lights | |
| 2 | Haiku Home Fans | |
| 1 | ecobee3 Wi-Fi Thermostat  | |
| 6 | ecobee Room Sensors (temperature, motion) | |
| 2 | Dahua IPC-HFW4300S V2 IP Security Cameras | |

### To-Do
* https://automatic.com/pro/
* https://opengarage.io/
* https://eightsleep.com/
