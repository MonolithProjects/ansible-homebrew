# Homebrew for Linux

[![Galaxy Quality](https://img.shields.io/ansible/quality/55459?style=flat&logo=ansible)](https://galaxy.ansible.com/monolithprojects/homebrew)
[![Role version](https://img.shields.io/github/v/release/MonolithProjects/ansible-homebrew)](https://galaxy.ansible.com/monolithprojects/homebrew)
[![Role downloads](https://img.shields.io/ansible/role/d/55459)](https://galaxy.ansible.com/monolithprojects/homebrew)
[![GitHub Actions](https://github.com/MonolithProjects/ansible-homebrew/workflows/molecule%20test/badge.svg)](https://github.com/MonolithProjects/ansible-homebrew/actions)
[![License](https://img.shields.io/github/license/MonolithProjects/ansible-homebrew)](https://github.com/MonolithProjects/ansible-homebrew/blob/main/LICENSE)

This Ansible Role will install Homebrew for Linux system and install formulae using it.

## Requirements

* System must have access to the GitHub.

## Supported Linux Shells:

- bash
- fish
- zsh

## Supported CPU architectures:

* AMD64, x86_64

## Tested on:

* CentOS/RHEL 8
* Debian 10,11
* Fedora 35
* Rocky Linux 8
* Ubuntu 18,20

## Role Variables

This is a copy from `defaults/main.yml`

```yaml
# Homebrew packages to be installed
brew_formulae: []

# Homebrew git repo
homebrew_git_repo: "https://github.com/Homebrew/brew"

# Homebrew release (default is the master github repo)
homebrew_release: "master"

# Homebrew user
homebrew_user: "{{ lookup('env', 'USER') }}"
```

## Example Playbook

In this example ...

```yaml
---
- name: Install Homebrew and aws-vault using homebrew
  hosts: all
  user: mike
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
