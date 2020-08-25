# Ansible Role: qemu_guest_agent

## Description

Ansible role for installing Qemu Guest Agent on RHEL/CentOS and Debian/Ubuntu or Windows.

If you are using an older version than 0.1.149 of Virtio, then use the 1.1.3 role.

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.virtualization.qemu-guest-agent
```
