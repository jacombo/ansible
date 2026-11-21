## Install and configure DevOps Ubuntu box

### Install Ansible
```
sudo apt install ansible -y
```

### How to run playbook
```
sudo ansible-playbook playbook.yml
```

#### Override swap size (optional)
To customize the swap file size from the command line, pass `swap_file_size_gb` using `-e`:
```bash
sudo ansible-playbook playbook.yml -e "swap_file_size_gb=8"
```

#### Passing Multiple Variables
```
sudo ansible-playbook playbook.yml -e "swap_file_size_gb=8 vm_swappiness=20"
```
#### JSON Syntax
```
sudo ansible-playbook playbook.yml -e '{"swap_file_size_gb": 8}'
```

#### Enable/Disable Docker installation (optional)
Install Docker:
```bash
sudo ansible-playbook playbook.yml -e "install_docker=true"
```

#### Enable/Disable Stremio installation (optional)
Install Stremio:
```bash
sudo ansible-playbook playbook.yml -e "install_stremio=true"
```

#### Enable/Disable Google Chrome installation (optional)
Install Google Chrome:
```bash
sudo ansible-playbook playbook.yml -e "install_chrome=true"
```
