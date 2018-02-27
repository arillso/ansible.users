# Ansible Role: users

[![Build Status](https://travis-ci.org/arillso/ansible.users.svg?branch=master)](https://travis-ci.org/arillso/ansible.users) [![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://sbaerlo.ch/er/licence) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-users-blue.svg)](https://galaxy.ansible.com/arillso/users)

## Description

This is an Ansible role which users and user's authorized keys manages on Linux and Windows.

## Installation

```bash
ansible-galaxy install arillso.users
```

## Requirements

None

## Role Variables

| Variable             | Default     | Comments (type)                                   |
| :---                 | :---        | :---                                              |
| users | [] | list of users to add, See defaults |
| users_host_vars | [] | list of users to add by host vars, See users |
| users_group_vars | [] | list of users to add by group vars,  See users |
| users_home | /home |  users home directory |
| users_home_mode | "0755" | default user's home directory permissions |
| users_ssh_key_type | rsa | default user's ssh key type |
| users_ssh_key_bits | 2048 | default user's ssh key bits |
| users_authorized_keys_exclusive | no |  default user's setting for authorized keys exclusive |

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
     - arillso.users
```

## Changelog

### 1.3

* add support for users on group and host vars layer
* add support no log when password or key then aktive no log

### 1.2

* fix lint
* new strucktur

### 1.1

* add windows support

### 1.0

* Initial release

## Author

* [Simon Bärlocher](https://sbaerlocher.ch)
* We Are Interactive

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2017, Simon Bärlocher