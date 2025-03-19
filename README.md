# Docker Installation with Ansible

Automated Docker installation on Debian servers using Ansible.

## Requirements
- Ansible
- WSL (Windows Subsystem for Linux)
- SSH access to target servers

## Configuration
Create a `.env` file with your server credentials:
```yaml
SSH_USER: "user"
SSH_PASSWORD: "password"
ROOT_PASSWORD: "root_password"
SERVER1_IP: "192.168.x.x"
# ... more servers