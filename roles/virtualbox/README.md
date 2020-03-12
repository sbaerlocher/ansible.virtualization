# Ansible Role: virtualbox

## Description

Role for installing and configuring VirtualBox software.

## Role Variables

### virtualbox_version

here you can specify the version to be installed.
By default, the role itself searches for the latest version.

```yml
virtualbox_version: '{{ current_version }}'
```

### virtualbox_repository

Repository url from where virualbox can be installed.

```yml
virtualbox_repository: 'https://download.virtualbox.org/virtualbox'
```

### virtualbox_packages

Version of Virtualbox that is to be installed.
By default, it chooses the latest version.

```yml
virtualbox_packages: 'virtualbox-{{ virtualbox_version[:-2] }}'
```

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.virtualization.virtualbox
```
