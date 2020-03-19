# Ansible Role: packer

## Description

This role installs Hashicorps Packer on Windows and Linux.

## Role Variables

### packer_version

Here you can specify the version to be installed.
By default, the role itself searches for the latest version.

```yml
packer_version: '{{ current_version }}'
```

### packer_path

This is the path where packer should be installed.
By default it is installed under the following path.

Linux: /usr/local/bin
Windows: C:\\Program Files\\HashiCorp\\Packer\\bin

```yml
packer_path: '{{ __packer_path }}'
```

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.virtualization.packer
```
