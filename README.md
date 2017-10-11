# Ansible Role: users

## Description

This is an Ansible role which users and user's authorized keys manages.

## Installation

```
$ ansible-galaxy install sbaerlocher.users
```

## Requirements

None

## Role Variables

| Variable             | Default     | Comments (type)                                   |
| :---                 | :---        | :---                                              |
| users | [] | list of users to add |
| users_home | /home |  users home directory |
| users_home_mode | "0755" | default user's home directory permissions |
| users_ssh_key_type | rsa | default user's ssh key type |
| users_ssh_key_bits | 2048 | default user's ssh key bits |
| users_authorized_keys_exclusive | no |  default user's setting for authorized keys exclusive |
| users_remove | [] | list of users to be removed |

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
     - sbaerlocher.users
```

## Changelog

### 1.0

* Initial release

## Author

* [Simon Bärlocher](https://sbaerlocher.ch)
* We Are Interactive
 
## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2017, Simon Bärlocher