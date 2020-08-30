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

### virtio_driver_directory

Determines which Windows version the Hosts system has to install the correct driver version.

```yml
virtio_driver_directory: >-
  {% if 'Windows Server 2019' in ansible_distribution -%}
    {% set virt_dir = '2k19' %}
  {% elif 'Windows Server 2016' in ansible_distribution -%}
    {% set virt_dir = '2k16' %}
  {% elif 'Windows Server 2012 R2' in ansible_distribution -%}
    {% set virt_dir = '2k12R2' %}
  {% elif 'Windows Server 2008 R2' in ansible_distribution -%}
    {% set virt_dir = '2k8R2' %}
  {% elif 'Windows 10' in ansible_distribution -%}
    {% set virt_dir = 'w10' %}
  {% else -%}
    {% set virt_dir = 'w10' %}
  {%- endif %}{{ virt_dir }}
```

### virtio_block_always

Allows to execute the alway part in the block.

```yml
virtio_block_always: true
```

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.virtualization.virtio
```
