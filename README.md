# OwnCloud over VPN

### Used Docker images
 - [OwnCloud](https://hub.docker.com/_/owncloud/)
 - [IPSec VPN Server](https://hub.docker.com/r/hwdsl2/ipsec-vpn-server/)

# Install

This only works on Linux server.

 1. Change the preshared key, user, and password.
 2. Copy the docker-compose.yml file to the host.
 3. Enable the required kernel module on the host: "sudo modprobe af_key"
 4. Use "docker-compose up -d" to start the system.

# Usage

 1. Connect to the VPN.
 2. In your browser, type the OwnCloud's ip: "172.16.238.11"
 
# Usage in Docker Swarm

You only have to change the "vpn" network's driver to overlay.

VPN's original GitHub [repo](https://github.com/hwdsl2/docker-ipsec-vpn-server) could be useful for better understanding and troubleshooting.