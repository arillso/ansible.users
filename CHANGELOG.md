# Changelog

This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)
and [human-readable changelog](https://keepachangelog.com/en/1.0.0/).

## 1.4.6

### Fixed

- add nolog option

## 1.4.5

### Fixed

- add check username length

## 1.4.4

### Fixed

- fixed password expired default
- fixed Linux User default

## 1.4.3

### Fixed

- line error in windows.yml

## 1.4.2

### Fixed

- fixed password expired default

## 1.4.1

### Changed

- update min ansible version to 2.8
- moved changelog from readme
- travis file has been updated
- Documentation has been improved
- change var `users_host_vars` to `users_list_host`
- change var `users_group_vars` to `users_list_group`

### Added

- molecule testing

## 1.4.0

### Removed

- remove become in Windows

## 1.3.0

### Added

- add support for users on group and host vars layer
- add support no log when password or key then aktive no log

## 1.2.0

### Fixed

- fix lint

### Added

- new strucktur

## 1.1

### Added

- add windows support

## 1.0.0

### Added

- Initial release
