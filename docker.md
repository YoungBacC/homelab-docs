# Docker
I put docker in it's own Ubuntu Server Virtual Machine (VM) since many people suggested this over a LXC. This is because an LXC shares the proxmox OS but a VM will not, so it will be more isolated.

I plan to run a few services in their own docker containers: the *arr services like Radarr and qbittorrent. 

To get docker up and running I am following the guide linked [[https://www.wundertech.net/how-to-run-docker-in-proxmox-on-a-vm/|here]]