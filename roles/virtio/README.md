# Ansible Role: virtio

## Description

This Ansible role installs the VirtIO driver and updates it also for new releases under Windows.

## Role Variables

### virtio_version

here you can specify the version to be installed.
By default, the role itself searches for the latest version.

```yml
virtio_version: '{{ current_version }}'
```

### virtio_win_ovirt

Variable to check if it is a virtual machine on an Ovirt Cluster.

```yml
virtio_win_ovirt: false
```

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.virtualization.virtio
```
