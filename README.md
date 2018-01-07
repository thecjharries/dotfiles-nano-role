# `dotfiles-role-nano`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-role-nano.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-role-nano)
[![GitHub release](https://img.shields.io/github/release/thecjharries/dotfiles-role-nano.svg)](https://github.com/thecjharries/dotfiles-role-nano)

## Requirements

Fedora 27 is recommended.

## Role Variables

Defaults are below.

```yml
---
owning_user: "{{ ansible_user }}"
owning_group: "{{ ansible_user }}"
root_dir: "/home/{{ ansible_user }}"
config_dir: "{{ root_dir }}/.config"
```

Additionally, these `vars` are set:

```yml
---
need_packages:
  - nano
```

## Dependencies

```yml
---
- src: git+https://github.com/thecjharries/dotfiles-role-common-software.git
- src: git+https://github.com/thecjharries/dotfiles-role-package-installer.git
- src: git+https://github.com/thecjharries/dotfiles-role-repo-installer.git
- src: git+https://github.com/thecjharries/dotfiles-role-generic-template.git
- src: git+https://github.com/thecjharries/dotfiles-role-git.git
```

## Example Playbook

```yml
---
- hosts: all

  roles:
    - role: "dotfiles-role-nano"
```

## License

ISC
