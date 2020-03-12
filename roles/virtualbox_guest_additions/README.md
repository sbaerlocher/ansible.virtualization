# Ansible Role: virtualbox_guest_additions

## Description

Ansible role that installs virtualbox extension pack.

## Role Variables

### virtualbox_guest_additions_version

Here you can specify the version to be installed.
By default, the role itself searches for the latest version.

```yml
virtualbox_guest_additions_version: '{{ current_version }}'
```

### virtualbox_guest_additions_download_url

URL to download virtualbox guest additions.

```yml
virtualbox_guest_additions_download_url: 'https://download.virtualbox.org/virtualbox/{{ virtualbox_guest_additions_version }}/VBoxGuestAdditions_{{ virtualbox_guest_additions_version }}.iso'
```

### virtualbox_guest_additions_iso_file

Path to temporarily store the virtualbox guest additions.
Windows: '{{ ansible_env.TEMP }}\VBoxGuestAdditions\_{{ virtualbox_guest_additions_version }}.iso'

```yml
virtualbox_guest_additions_iso_file: '{{ __virtualbox_guest_additions_iso_dest }}'
```

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.virtualization.virtualbox_extension_pack
```
