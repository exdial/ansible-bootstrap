# Ansible-bootstrap

## Coding guidelines

- use [semantic versioning](https:://semver.org)
- use `ansible-galaxy init {{ rolename }} -p roles/{{ rolename }}` for new role
- use [snake_case](https://en.wikipedia.org/wiki/Snake_case) for naming variables

## Directories structure

- `.gitignore`
- `README.md`
- defaults/
  - all variables should have default value, defined in `defauls/main.yml`
  - if variable don't have default value, use *omit* instruction
  - name of the variable should have name of the role, using snake_case, e.g. `nginx_listen`
- `handlers/`
  - handlers names should use snake_case
- `meta/`
  - author
  - description
  - company
  - min_ansible_version
  - platforms
- `tasks/`
  - the code should be compact (80 chars), or use YAML multiline (`>`)
  - use includes, if code length more than 2 screens
- `templates/`
  - use `# {{ ansible_managed }}`
- `tests/`
- vars/
  - delete if useless

## Ansible installation

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

## Vagrant installation

```
https://www.vagrantup.com/downloads.html
```

## Create role

```
ansible-galaxy init {{ rolename }} -p roles/{{ rolename }}
```
