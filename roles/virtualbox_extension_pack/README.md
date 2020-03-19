# Ansible Role: virtualbox_extension_pack

## Description

Ansible role that installs virtualbox extension pack.

## Role Variables

### virtualbox_extension_pack_version

Here you can specify the version to be installed.
By default, the role itself searches for the latest version.

```yml
virtualbox_extension_pack_version: '{{ current_version }}'
```

### virtualbox_extension_pack_url

URL to download virtualbox extension pack.

```yml
virtualbox_extension_pack_url: 'https://download.virtualbox.org/virtualbox/{{ current_version }}/Oracle_VM_VirtualBox_Extension_Pack-{{ current_version }}.vbox-extpack'
```

### virtualbox_extension_pack_dest

Path to temporarily store the virtualbox extension pack.
Linux: '/tmp/Oracle_VM_VirtualBox_Extension_Pack-{{ current_version }}.vbox-extpack'

```yml
virtualbox_extension_pack_dest: '{{ __virtualbox_extension_pack_dest }}'
```

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.virtualization.virtualbox_extension_pack
```
