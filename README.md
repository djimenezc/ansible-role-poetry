[![role](https://img.shields.io/ansible/role/55570)](https://galaxy.ansible.com/trallnag/poetry)
[![quality](https://img.shields.io/ansible/quality/55570)](https://galaxy.ansible.com/trallnag/poetry)
[![downloads](https://img.shields.io/ansible/role/d/55570?label=downloads)](https://galaxy.ansible.com/trallnag/poetry)

# Ansible Role for Python Poetry

Ansible role that installs Python Poetry on Linux.

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/poetry).

## Role Variables

```yaml
poetry_version:
  type: raw
  required: false
  default: 1.1.7
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
