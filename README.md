![Home Assistant Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Home_Assistant_Logo.svg/240px-Home_Assistant_Logo.svg.png)

# Home Assistant Configuration

![Build Status](https://travis-ci.org/joe-scalise/HomeAssistantConfig.svg?branch=master) [![Build Status](https://dev.azure.com/joescalise/HomeAssistant/_apis/build/status/joe-scalise.HomeAssistantConfig?branchName=local-changes)](https://dev.azure.com/joescalise/HomeAssistant/_build/latest?definitionId=1?branchName=local-changes)

This is a backup of my Home Assistant configuration.

### System Highlights and Containers Used

* [homeassistant/home-assistant](https://hub.docker.com/r/homeassistant/home-assistant/) - Home Assistant
* [Traefik](https://hub.docker.com/r/_/traefik/) - reverse proxy and certificates
* UniFi Security Gateway takes care of updating DNS dynamically
* [Ouroborus](https://hub.docker.com/r/pyouroboros/ouroboros) takes care of updating images
* [healthchecks.io](https://healthchecks.io/) takes care of service pings and emails me when something is down
* [Gotify](https://hub.docker.com/r/gotify/server) for mobile notifications via healthchecks.io.
* [Syncthing](https://hub.docker.com/r/linuxserver/syncthing/) - this is how I choose to modify configuration files remotely
* GitHub for configuration backups, [this script] is used to backup the host
* Travis CI/Azure DevOps provides automatic builds/test for repository changes

### My Tips

* Run Home Assistant in Docker and skip all the other ways of installing/hosting, save yourself headaches.
* Home Assistant Integrations can be fun and addictive at first, but, will ultimately be a constant source of failures and issues.  Stick with the basics.  Lights, presense, smart-home devices like thermostats...

### System

Ubuntu Server, Docker Swarm, 1 on-prem node (old HP laptop) ~~2 nodes in Azure via site-to-site VPN~~ (too costly, one node swarm for now).  Home Assistant does not run in Swarm due to the fact that you cannot map in the Z-Wave USB device.

### Devices

| Qty   | Name                                                  | Link |
| ----- | ----------------------------------------------------- | ---- |
| 10 | GE Z-Wave Wireless Switches (12722, 12723, 14291, 14294) |  |
| 1 | GE Z-Wave Plus Smart Lighting & Appliance Control Outdoor Module |  |
| 1 | Aeotec Z-Stick Gen5 Z-Wave Plus USB |  |
| 1 | Ubiquiti Unifi Security Gateway (USG) |  |
| 1 | Ubiquiti UniFi Switch 8 60W (US-8-60W) |  |
| 2 | Ubiquiti Unifi 802.11ac Dual-Radio PRO Access Point (UAP-AC-PRO-US)|  |
| 1 | Ubiquiti Unifi Cloud Key - Remote Control Device (UC-CK)|  |
| 1 | Synology 2 bay NAS DiskStation DS218j |  |
| 3 | Amazon Fire TV  |  |
| 3 | Ethernet Adapter for Amazon Fire TV Devices |  |
| 1 | Roku Ultra  |  |
| 2 | Haiku Home Lights | [(Haiku Home)](https://www.haikuhome.com/) |
| 2 | Haiku Home L Series 52" Smart Ceiling Fan w/ Wi-Fi |  |
| 1 | ecobee3 Wi-Fi Thermostat  |  |
| 8 | ecobee Room Sensors (temperature, motion) |  |
| 2 | Dahua IPC-HFW4300S V2 IP Security Cameras |  |
| 1 | Ubiquiti UniFi Video G3 Flex Indoor/Outdoor PoE Camera (UVC-G3-FLEX) |  |
| 5 | Ubiquiti UniFi Video Camera G3 (UVC-G3-AF) |  |
