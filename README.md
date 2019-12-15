# Ansible Role: users

[![Build Status](https://img.shields.io/travis/arillso/ansible.users.svg?branch=master&style=popout-square)](https://travis-ci.org/arillso/ansible.users) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](https://sbaerlo.ch/licence) [![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-users-blue.svg?style=popout-square)](https://galaxy.ansible.com/arillso/users) [![Ansible Role](https://img.shields.io/ansible/role/d/21607.svg?style=popout-square)](https://galaxy.ansible.com/arillso/users)

## Description

This is an Ansible role which users and user's authorized keys manages on Linux and Windows.

## Installation

```bash
ansible-galaxy install arillso.users
```

## Requirements

None

## Role Variables

### Users

list of users to add

```yml
users: []
```

```yml
 list of users to add by host vars
users_list_host: []
```

list of users to add by group vars

```yml
users_list_group: []
```

#### Example

```yml
 users:
   - username: foobar              (required)
     name: Foo Bar
     uid: 1000
     group: staff
     password: xxxxx               (a hash created with: mkpasswd)
     groups: ["adm", "www-data"]
     append: no                    (only append groups, leave others)
     home_mode: "0750"
     home_create: yes
     home: /path/to/user/home
     system: no
     authorized_keys: []
     authorized_keys_exclusive: yes
     ssh_key_type: rsa
     ssh_key_bits: 2048
     ssh_key_password: ""
     ssh_key_generate: no
     ssh_key: "xxx"
     shell: /bin/bash
     update_password: always

```

```yml
users:
  - username: foobar              (required)
    name: Foo Bar
    description: User
    password: xxxxx
    groups: ['adm', 'www-data']
    hide: true
```

users home directory

```yml
users_home: /home
```

default user's primary group for users

```yml
users_group:
```

default user's secondary groups

```yml
users_groups: []
```

default user's home directory permissions

```yml
users_home_mode: '0755'
```

default user's ssh key type

```yml
users_ssh_key_type: rsa
```

default user's ssh key bits

```yml
users_ssh_key_bits: 2048
```

default user's setting for authorized keys exclusive

```yml
users_authorized_keys_exclusive: 'no'
```

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
    - arillso.users
```

## Author

- [Simon Bärlocher](https://sbaerlocher.ch)

## Inspiration

- [We Are Interactive](https://github.com/weareinteractive/ansible-users)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2020, Arillso
