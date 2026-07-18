# Wireguard
To make life easier I opted to use the Proxmox VE helper script for wireguard which asked me some questions instead of manually setting it up.

The script downloaded wireguard in a debian 13 Linux container and WGDashboard for ease of use, i.e., adding new peers.

The wireguard runs on IP 192.168.1.144 on port 51820. I stupidly port forwarded the IP of the proxmox server itself and was having issues as expected. I realized this and fixed the mistake.

I had to delete my original wireguard config and regenerate it because I accidentally exposed the private key. However, doing this deleted the PostUp and PostDown fields in the configuration file. I didn't really know what these did, so I just google searched what these fields would usually be. 
- For PostUp: `iptables -A FORWARD -i %i -j ACCEPT; iptables -A FORWARD -o %i -j ACCEPT; iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE`
- For PostDown: `iptables -D FORWARD -i %i -j ACCEPT; iptables -D FORWARD -o %i -j ACCEPT; iptables -t nat -D POSTROUTING -o eth0 -j MASQUERADE`
Note: I really don't know what these are doing, maybe I'll learn later.
