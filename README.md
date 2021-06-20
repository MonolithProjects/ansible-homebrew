# Homebrew for Linux (MVP)

[![Galaxy Quality](https://img.shields.io/ansible/quality/00000?style=flat&logo=ansible)](https://galaxy.ansible.com/monolithprojects/homebrew)
[![Role version](https://img.shields.io/github/v/release/MonolithProjects/ansible-homebrew)](https://galaxy.ansible.com/monolithprojects/homebrew)
[![Role downloads](https://img.shields.io/ansible/role/d/00000)](https://galaxy.ansible.com/monolithprojects/homebrew)
[![GitHub Actions](https://github.com/MonolithProjects/ansible-homebrew/workflows/molecule%20test/badge.svg?branch=main)](https://github.com/MonolithProjects/ansible-homebrew/actions)
[![License](https://img.shields.io/github/license/MonolithProjects/ansible-homebrew)](https://github.com/MonolithProjects/ansible-homebrew/blob/main/LICENSE)

This role will install Homebrew for Linux system and install formulae using it.

## Requirements

* System must have access to the GitHub.

## Supported CPU architecture:

* AMD64, x86_64
## Tested on:

* CentOS/RHEL 7,8
* Debian 9,10
* Fedora 35
* Ubuntu 18,20

## Role Variables

This is a copy from `defaults/main.yml`

```yaml

```

## Example Playbook

In this example ...

```yaml
---
- name: Install Homebrew and aws-vault using homebrew
  hosts: all
  user: ansible
  become: yes
  vars:
    brew_formulae:
      - aws-vault
  roles:
    - role: monolithprojects.homebrew
```

## License

MIT

## Author Information

Created in 2021 by Michal Muransky
