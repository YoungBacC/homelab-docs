# Docker
I put docker in it's own Ubuntu Server Virtual Machine (VM) since many people suggested this over a LXC. This is because an LXC shares the proxmox OS but a VM will not, so it will be more isolated.

I plan to run a few services in their own docker containers: the *arr services like Radarr, and qbittorrent. 

Since I know absolutely nothing about docker, in order to get docker up and running I am following the guide linked [here](https://www.wundertech.net/how-to-run-docker-in-proxmox-on-a-vm/)

The docker server is running at IP: 192.168.1.42.

I set up a portrainer container in docker to handle all docker containers visually via a WebUI.

I set up qbittorrent with gluetun using docker-compose so that all torrent traffic will go through my protonvpn before getting to my server.