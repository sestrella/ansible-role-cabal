# Ansible Role: Cabal

![CI](https://github.com/sestrella/ansible-role-cabal/workflows/CI/badge.svg)

Installs [Haskell Cabal](https://www.haskell.org/cabal/). Inspired by Jeff
Geerling's [Ruby role](https://github.com/geerlingguy/ansible-role-ruby)

## Requirements

None.


## Role Variables

Available variables are listed below, along with default values (see
defaults/main.yml):

```yml
workspace: "{{ ansible_user_dir }}"
```

The location where temporary files will be downloaded in preparation for Cabal
installation.

```yml
cabal_version: 3.2.0.0
```

The version of Cabal that will be installed.

```yml
cabal_download_url: https://downloads.haskell.org/~cabal/cabal-install-3.2.0.0/cabal-install-3.2.0.0-x86_64-unknown-linux.tar.xz
```

The URL from which Cabal will be downloaded.

```yml
cabal_install_dir: /usr/local/bin
```

The installation directory where `cabal` is going to be copied.

## Dependencies

None.

## Example Playbook
----------------

```yml
- hosts: servers
  roles:
    - sestrella.cabal
```

## License

MIT

## Author Information

Sebastián Estrella
