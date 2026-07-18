# Pi-Hole
I've seen online people using pi-hole for network wide adblocking. But it also works as a DNS server. So pairing that with Nginx will work well.

I set up network wide adblocking through my router settings by setting the DNS server to be the ip address of the pi-hole server.

Each domain I would like to use locally, I am pointing to my nginx proxy manager (NPM) server which will take care of ports. 