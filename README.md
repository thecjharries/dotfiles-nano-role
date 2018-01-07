# `dotfiles-nano-role`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-nano-role.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-nano-role)

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
- src: git+https://github.com/thecjharries/dotfiles-common-software-role.git
- src: git+https://github.com/thecjharries/dotfiles-package-installer-role.git
- src: git+https://github.com/thecjharries/dotfiles-repo-installer-role.git
- src: git+https://github.com/thecjharries/dotfiles-generic-template-role.git
- src: git+https://github.com/thecjharries/dotfiles-git-role.git
```

## Example Playbook

```yml
---
- hosts: all

  roles:
    - role: "dotfiles-nano-role"
```

## License

ISC
