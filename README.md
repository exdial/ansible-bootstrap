# Ansible-bootstrap

## Installation

### Linux

```
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

### OSX

```
$ brew update
$ brew install ansible
```

## Create role

```
ansible-galaxy init {{ rolename }} -p roles/{{ rolename }}
```

## Coding guidelines

- use [semantic versioning](https:://semver.org) for role versioning
- use `ansible-galaxy init {{ rolename }} -p roles/{{ rolename }}` for creating the new role
- use [snake_case](https://en.wikipedia.org/wiki/Snake_case) for naming variables
- all variables should have the default value, defined in `defauls/main.yml`
- if variable don't have default value, use *omit* instruction
- variables names should have name of the role in [snake_case](https://en.wikipedia.org/wiki/Snake_case) format, e.g. `nginx_listen`
- follow [snake_case](https://en.wikipedia.org/wiki/Snake_case) format for naming handlers
- must have fields in the `meta/`: *author*, *description*, *min_ansible_version*, *platforms*
- try to fit in 80 chars or use YAML multiline notation `>`
- use includes, if the code length more than 2 screens
- use `# {{ ansible_managed }}` at the top of the templates
- drop `vars/` if you don't use it
