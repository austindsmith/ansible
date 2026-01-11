# Ansible

Made a separate repo for my Ansible files.

## Resources
https://galaxy.ansible.com/ui/standalone/roles/
https://github.com/k3s-io/k3s-ansible

## Installing k3s
```yaml
ansible-playbook playbooks/applications/k3s.yml -i inventories/k3s.yml
```
You may need to add
```yaml
ansible_ssh_private_key_file: ssh/key/path
```
to k3s.yml depending on how your server is configured.

## Vault
Run
```bash
chmod +x ansible-vault-pass-client.sh
```

## Requirements
Install collections and roles by adding to `requirements.yml` and then running
```yaml
ansible-galaxy install -r requirements.yml
```