# Ansible-bootstrap

Use:
- ansible for configuration management
- vagrant for testing
- ansible-galaxy for init new role

## Workflow recommendations

### Roles location
- Shared roles should be placed in `git.lo/ansible`
- Project-oriented roles should be placed in `git.lo/ansible-projectname`
- Community roles should be downloaded

### Versioning
See [semver.org](https:://semver.org).

### Variables naming
Use [snake_case](https://en.wikipedia.org/wiki/Snake_case).

### Coding style
- .gitignore
- fill README.md
- repository contents
  - defaults/
    - all variables should have default value in defauls/main.yml
    - if variable have no default value, use `omit`
    - name variable must contain role name in snake_case, e.g. `nginx_listen`
  - handlers/
    - handler names should be in snake_case
  - meta/
    - author
    - description
    - company
    - min_ansible_version
    - platforms
  - tasks/
    - the code should be compact (80 chars), or use YAML multiline (`>`)
    - use includes, if code length more than 2 screens
  - templates/
    - use `# {{ ansible_managed }}`
  - tests/
  - vars/
    - delete, if unuse

## Ansible installation

### On Linux

```
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

### On OSX

```
$ brew update
$ brew install ansible
```

## Vagrant installation

```
https://www.vagrantup.com/downloads.html
```

## Create role

```
ansible-galaxy init {{ rolename }} -p roles/{{ rolename }}
```
