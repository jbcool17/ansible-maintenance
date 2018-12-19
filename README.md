# Maintenance Ansible
collection of maintenance roles(updates, cron jobs etc...)
***

## Roles
- yum
  - tags
    - updates
    - security
- apt
  - tags
    - updates
    - security


## Setup
- [pipenv](https://github.com/pypa/pipenv)

```
pipenv sync
pipenv shell
```

## Testing
- [molecule](https://github.com/ansible/molecule)

```
cd roles/<roles>
molecule test
```
