# Docker Installation with Ansible

Automated Docker installation on Debian servers using Ansible.

## Requirements
- Ansible
- WSL (Windows Subsystem for Linux)
- SSH access to target servers

## Configuration (ANSIBLE)
Create a `.env` file with your server credentials:
```yaml
SSH_USER: "user"
SSH_PASSWORD: "password"
ROOT_PASSWORD: "root_password"
SERVER1_IP: "192.168.x.x"
# ... more servers

## Configuration (Docker - Image: brclucas/wifimonitor)
Create a `.env` file in your local servers with your server UNIFI credentials:
```yaml
PORT=3000
UNIFI_USERNAME=XXX
UNIFI_PASSWORD=XXX
UNIFI_SITE=default
UNIFI_URL=https://XXX:XXX.XXX.XXX:8443/api