[![role](https://img.shields.io/ansible/role/55573)](https://galaxy.ansible.com/trallnag/poetry)
[![quality](https://img.shields.io/ansible/quality/55573)](https://galaxy.ansible.com/trallnag/poetry)
[![downloads](https://img.shields.io/ansible/role/d/55573?label=downloads)](https://galaxy.ansible.com/trallnag/poetry)

# Ansible Role for Python Poetry

Ansible role that installs [Python Poetry][python-poetry] on Linux.

[python-poetry]: https://github.com/python-poetry/poetry

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/poetry).

## Content

* Installs Python Poetry via the official installer script.
* Adds init block to `~/.bashrc`.

## Role Variables

```yaml
poetry_version:
  default: 1.1.7
  type: raw
  required: false
  description: >-
    Poetry version to install. Will be passed together with the `--version`
    flag to the poetry installer. Check at <https://github.com/python-poetry/poetry>.
```

## Example Playbook

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  vars:
    rolespec_validate: true
  roles:
    - name: trallnag.poetry
      vars:
        poetry_version: 1.1.7
```

## Special Requirements

* Python must be installed and available via `python3`.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag
