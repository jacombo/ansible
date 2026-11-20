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

```
sudo ansible-playbook playbook.yml -e "swap_file_size_gb=8 vm_swappiness=20"
sudo ansible-playbook playbook.yml -e '{"swap_file_size_gb": 8}'
```