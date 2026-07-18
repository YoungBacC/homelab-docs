# Nginx Proxy Manager
I have seen this service used online to simplify routing to different services. I would rather not memorize a bunch of IPs and their port numbers. With this just remember a domain and a subdomain. This is a bit overkill for the moment since this would likely be very useful if deploying public applications on one server. For now everything will be private to my local network.

The NPM service is running on IP 192.168.1.130 on port 81.

I set this service to run on a static IP.

For each domain in pihole, I have created a proxy host which points the domain to the correct server and port number for the service.

As a side note the rockhaven.local does not work as a domain. I assume this is because I set the hostname to be rockhaven.local when setting up the proxmox server.