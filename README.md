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
* Enables tab completion for Bash.

## Role Variables

```yaml
poetry_version:
  default: 1.1.7
  type: raw
  required: false
  description: >-
    Poetry version to install. Will be passed together with the `--version`
    flag to the poetry installer. Check at <https://github.com/python-poetry/poetry>.

poetry_python_path:
  default: python
  type: raw
  required: false
  description: >-
    Python executable that should be used for installation of Poetry.
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
        poetry_python_path: python
```

## Special Requirements

* Passwordless sudo must be working. Required for activating tab completion for
  Bash. Could be refactored if need arises.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag
