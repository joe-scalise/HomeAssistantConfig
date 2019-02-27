# Home Assistant Configuration

![Build Status](https://travis-ci.org/joe-scalise/HomeAssistantConfig.svg?branch=master) [![Build Status](https://dev.azure.com/joescalise/HomeAssistant/_apis/build/status/joe-scalise.HomeAssistantConfig?branchName=local-changes)](https://dev.azure.com/joescalise/HomeAssistant/_build/latest?definitionId=1?branchName=local-changes)

This is a backup of my Home Assistant configuration.  Started on Raspberry Pi with HASS.IO but it never worked.  Moved to Docker Compose on Ubuntu Server

### Highlights of the System Setup

* Traefik takes care of getting a wildcard SSL
* UniFi Security Gateway takes care of updating DNS dynamically
* Canonical Livepatch takes care of updating the server, mostly without reboots
* Docker Compose `restart: always` takes care of restarting containers
* [Watchtower](https://github.com/v2tec/watchtower) takes care of updating running container's images
* [healthchecks.io](https://healthchecks.io/) takes care of service pings and emails me when something is down
* Github takes care of configuration backup (not automatically)
* Travis CI provides automatic builds/test for repository changes

### Containers (related to Home Assistant):

* [homeassistant/home-assistant](https://hub.docker.com/r/homeassistant/home-assistant/) - Home Assistant
* [traefik](https://hub.docker.com/r/_/traefik/) - Traefik
* [portainer/portainer](https://hub.docker.com/r/portainer/portainer/) - Portainer
* [linuxserver/syncthing](https://hub.docker.com/r/linuxserver/syncthing/) - Syncthing
* [v2tec/watchtower](https://github.com/v2tec/watchtower) - Watchtower

* *TODO* node-red, Influx w/ Grafana


### System:
Ubuntu Server, Docker Swarm, 1 on-prem node (old HP laptop) 2 nodes in Azure via site-to-site VPN.  Home Assistant does not run in Swarm due to the fact that I cannot map in the Z-Wave USB device.

### Devices:

| Qty   | Name                                                  | Link |
| ----- | ----------------------------------------------------- | ---- |
| 10 | GE Z-Wave Wireless Switches (12722, 12723, 14291, 14294) | [(Amazon)](https://amzn.to/2C6WGNI) |
| 1 | GE Z-Wave Plus Smart Lighting & Appliance Control Outdoor Module | [(Amazon)](https://amzn.to/2QNSkDs) |
| 1 | Aeotec Z-Stick Gen5 Z-Wave Plus USB | [(Amazon)](https://amzn.to/2UD2vd7) |
| 1 | Ubiquiti Unifi Security Gateway (USG) | [(Amazon)](https://amzn.to/2ry1HJp) |
| 1 | Ubiquiti UniFi Switch 8 60W (US-8-60W) | [(Amazon)](https://amzn.to/2C8KNqL) |
| 2 | Ubiquiti Unifi 802.11ac Dual-Radio PRO Access Point (UAP-AC-PRO-US)| [(Amazon)](https://amzn.to/2C70HBQ) |
| 1 | Ubiquiti Unifi Cloud Key - Remote Control Device (UC-CK)| [(Amazon)](https://amzn.to/2SJkIUu) |
| 1 | Synology 2 bay NAS DiskStation DS218j | [(Amazon)](https://amzn.to/2UDEiDG) |
| 3 | Amazon Fire TV w/ Ethernet Adapters  | [(Amazon)](https://amzn.to/2QR7yaM) |
| 3 | Ethernet Adapter for Amazon Fire TV Devices | [(Amazon)](https://amzn.to/2PzMeSm) |
| 2 | Haiku Home Lights | [(Haiku Home)](https://www.haikuhome.com/) |
| 2 | Haiku Home L Series 52" Smart Ceiling Fan w/ Wi-Fi | [(Amazon)](https://amzn.to/2EstSSb) |
| 1 | ecobee3 Wi-Fi Thermostat  | [(Amazon)](https://amzn.to/2EerzBv) |
| 6 | ecobee Room Sensors (temperature, motion) | [(Amazon)](https://amzn.to/2Ei1eCI) |
| 2 | Dahua IPC-HFW4300S V2 IP Security Cameras | [(Amazon)](https://amzn.to/2UELI9J) |
| 1 | Ubiquiti UniFi Video G3 Flex Indoor/Outdoor PoE Camera (UVC-G3-FLEX) | [(Amazon)](https://amzn.to/2LfgYaK) |
| 5 | Ubiquiti UniFi Video Camera G3 (UVC-G3-AF) | [(Amazon)](https://amzn.to/2SIgvjZ) |

### To-Do
* https://automatic.com/pro/
* https://opengarage.io/
* https://eightsleep.com/
