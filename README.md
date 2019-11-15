![Home Assistant Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Home_Assistant_Logo.svg/240px-Home_Assistant_Logo.svg.png)

# Home Assistant Configuration

![Build Status](https://travis-ci.org/joe-scalise/HomeAssistantConfig.svg?branch=master) [![Build Status](https://img.shields.io/azure-devops/build/joescalise/af5372e7-8c15-4d17-8dbd-3effb1bf0fc2/1?style=for-the-badge)](https://dev.azure.com/joescalise/HomeAssistant)

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

### Tips

* Run Home Assistant in Docker and skip all the other ways of installing/hosting - save yourself headaches!
* Home Assistant Integrations can be fun and addictive at first, but, will ultimately be a constant source of failures and issues.  Stick with the basics.  Lights, presense, smart-home devices like thermostats...

### System

Ubuntu Server, Docker Swarm, 1 on-prem node (old HP laptop) ~~2 nodes in Azure via site-to-site VPN~~ (too costly, one node swarm for now).  Home Assistant does not run in Swarm due to the fact that you cannot map in the Z-Wave USB device.

### Devices

| Qty   | Name                                                  | Link |
| ----- | ----------------------------------------------------- | ---- |
| 10 | GE Z-Wave Wireless Switches (12722, 12723, 14291, 14294) | [Amazon](https://amzn.to/2XmCIb2) |
| 1 | GE Z-Wave Plus Smart Lighting & Appliance Control Outdoor Module | [Amazon](https://amzn.to/32Nk1yf) |
| 1 | Aeotec Z-Stick Gen5 Z-Wave Plus USB | [Amazon](https://amzn.to/32NZ5qS) |
| 1 | Ubiquiti Unifi Security Gateway (USG) | [Amazon](https://amzn.to/2CM7HUd) |
| 1 | Ubiquiti UniFi Switch 8 60W (US-8-60W) | [Amazon](https://amzn.to/374BpSp) |
| 2 | Ubiquiti Unifi 802.11ac Dual-Radio PRO Access Point (UAP-AC-PRO-US)| [Amazon](https://amzn.to/2KkbsnZ) |
| 1 | Ubiquiti Unifi Cloud Key - Remote Control Device (UC-CK)| [Amazon](https://amzn.to/2CIQBqz) |
| 1 | Synology 2 bay NAS DiskStation DS218j | [Amazon](https://amzn.to/2KhXxiv) |
| 3 | Amazon Fire TV  | [Amazon](https://amzn.to/33RzoH6) |
| 3 | Ethernet Adapter for Amazon Fire TV Devices | [Amazon](https://amzn.to/2pitaB5) |
| 1 | Roku Ultra  | [Amazon](https://amzn.to/2QqCgXw) |
| 2 | Haiku Home Lights | [Haiku Home](https://www.haikuhome.com/) |
| 2 | Haiku Home L Series 52" Smart Ceiling Fan w/ Wi-Fi | [Amazon](https://amzn.to/2rLd3Nr) |
| 1 | ecobee3 Wi-Fi Thermostat | [Amazon](https://amzn.to/2Oh3Gwo) |
| 8 | ecobee Room Sensors (temperature, motion) | [Amazon](https://amzn.to/2CKC4dQ) |
| 2 | Dahua IPC-HFW4300S V2 IP Security Cameras | [Amazon](https://amzn.to/2rLJBqz) |
| 1 | Ubiquiti UniFi Video G3 Flex Indoor/Outdoor PoE Camera (UVC-G3-FLEX) | [Amazon](https://amzn.to/2NKBCm2) |
| 5 | Ubiquiti UniFi Video Camera G3 (UVC-G3-AF) | [Amazon](https://amzn.to/33MdTaI) |
| 3 | Ubiquiti UniFi Video G3-Micro Wireless Camera (UVC-G3-MICRO)| [Amazon](https://amzn.to/357a2Fl) |
