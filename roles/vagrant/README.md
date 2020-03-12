# Ansible Role: Vagrant

## Description

This role installs Hashicorps Vagrant on Windows and Linux.

## Role Variables

### vagrant_version

Here you can specify the version to be installed.
By default, the role itself searches for the latest version.

```yml
vagrant_version: '{{ current_version }}'
```

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.virtualization.vagrant
```
