# Docker network access through VPN

This is my personal system. I use this for a low-end virtual machine.
The purpuse is simple: a cheap and (relatively) secure Docker-Compose to store my own files and developments.

### What is included?
 - VPN server to access the inner Docker network and containers
 - OwnCloud for file storage
 - Gitea as Git server
 - Portainer for Docker WebUI
 
### Ideal for:
 - Low capacity VMs
 - A template for VPN protected containers

# Install

This only works on Linux server.

 1. Change the environment variables of the vpn and gitea-db to some secure. 
 2. Copy the docker-compose.yml file to the host.
 3. Enable the required kernel module on the host: "sudo modprobe af_key"
 4. Use "docker-compose up -d" to start the system.

# Usage
 
 1. Setup the VPN connection: [IPSec VPN tutorial](https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/docs/clients.md)
 2. Connect to the VPN.
 3. In your browser, type the ip of required service.
 
# Usage in Docker Swarm

You only have to change the "vpn" network's driver to overlay.

VPN's original GitHub [repo](https://github.com/hwdsl2/docker-ipsec-vpn-server) could be useful for better understanding and troubleshooting.