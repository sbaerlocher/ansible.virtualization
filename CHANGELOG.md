# Changelog

This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)
and [human-readable changelog](https://keepachangelog.com/en/1.0.0/).

## master

## 0.0.8

### Fixed

- Fixes mount_path in virtualbox_guest_additions.
- Fixes #12 virtualbox_extension_pack freeze because of new license hash.

## 0.0.7

### Changed

- Adaptation to the role qemu_guest_agent and virtio so they harmonize with each other.
- Adaptation of the method to determine which windows version it is.

## 0.0.6

### Added

- Adding the Ansible Role qemu_guest_agent.

## 0.0.5

### Added

- Support for Microsoft Windows Server 2019 Essentials in the virtio role.

## 0.0.4

### Fixed

- Remove the path to the license file because license must be exclusive.

## 0.0.3

### Fixed

- Fixed the problem if the version number has more than 1 digit.
- Fixed typo in virtualbox_guest_additions role README.md.

## 0.0.2

### Fixed

- Fixed import of variables from the vars directory.
- Fixed Import warnings,

## 0.0.1

### Added

- Initial develop
