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

## Configuration in Cluster
For security reasons, secrets must be created manually in the cluster. Required secrets:

kubectl create secret generic wifi-monitor-ypf-secrets -n myapp \
  --from-literal=PORT=3000 \
  --from-literal=UNIFI_USERNAME=username \
  --from-literal=UNIFI_PASSWORD=your_password \
  --from-literal=UNIFI_SITE=default \
  --from-literal=UNIFI_URL=https://<IP NETWORK CONTROLLER>:8443/api

- wifi-monitor-master-secrets
- wifi-monitor-axion-secrets
- wifi-monitor-alamos-secrets
- wifi-monitor-ypf-secrets

Contact the system administrator for the proper secret values and creation procedure.