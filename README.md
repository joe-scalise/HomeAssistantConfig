# Home Assistant Configuration

![Build Status](https://travis-ci.org/joe-scalise/HomeAssistantConfig.svg?branch=master)

This is a backup of my Home Assistant configuration.  I recently moved it all from a Raspberry Pi to Docker.  I have not had any stability issues since - I was constantly chasing some issue or another on the Raspberry Pi/HASS.IO which led me down this path.

I use Docker Compose, and Traefik as a reverse proxy.  Traefik takes care of getting a wildcard SSL too.

### Containers:

* [homeassistant/home-assistant](https://hub.docker.com/r/homeassistant/home-assistant/) - Home Assistant

Home Assistant is open source software for home automation.  This repo serves as a backup of my configuration.

#### System:
- old HP laptop
- Aeotec ZW090 Z-Stick Gen5 US
- Ubiquiti UniFi networking gear
- Synology NAS
- ~~Raspberry Pi 3 running HASS.IO~~
- ~~Waveshare Official Raspberry Pi Power Supply~~
- ~~SanDisk Ultra 64GB MicroSDXC Class 10 UHS Memory Card~~

#### Devices:

| Qty   | Name                                                  | Link |
| ----- | ----------------------------------------------------- | ---- |
| 6 | GE Z-Wave Wireless Switches (12722, 12723, 14291, 14294) | [(Amazon)](https://www.amazon.com/gp/product/B01M1AHC3R/) |
| 3 | Amazon Fire TV (3rd Gen) w/ Ethernet Adapters  | |
| 2 | Haiku Home Lights | |
| 2 | Haiku Home Fans | |
| 1 | ecobee3 Wi-Fi Thermostat  | |
| 6 | ecobee Room Sensors (temperature, motion) | |
| 2 | Dahua IPC-HFW4300S V2 IP Security Cameras | |
