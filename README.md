# Maintenance Ansible
collection of maintenance roles(updates, cron jobs etc...)
***

## Roles

### yum
  - tags = updates,security

### apt
  - tags = updates

### windows
  - tags = updates
  - variables
  ```
  # automatically reboot if needed(timeout set to 60min)
  windows_reboot: yes

# CMD
# https://docs.ansible.com/ansible/latest/user_guide/windows_winrm.html
  export OBJC_DISABLE_INITIALIZE_FORK_SAFETY=YES # for macos
ansible all -i 192.168.2.43, -m setup -c winrm -e ansible_winrm_server_cert_validation=ignore -u Administrator -k
  ```


## Setup
- [pipenv](https://github.com/pypa/pipenv)

```
pipenv sync
pipenv shell
```

## Testing
- [molecule](https://github.com/ansible/molecule)

```
# run tests
cd roles/<role>
molecule test

# initialize existing role
cd roles/<role>
molecule init scenario -r <role> -d docker
```
