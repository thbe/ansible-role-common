# Ansible Role thbe-common

[![Molecule](https://github.com/thbe/ansible-role-common/actions/workflows/molecule.yml/badge.svg)](https://github.com/thbe/ansible-role-common/actions/workflows/molecule.yml)

This role creates a common directory structure that is used by all other roles from "thbe" Ansible Galaxy namespace.

## Requirements

This role does not have any requirements.

## Role Variables

* **role_directory** - This variable contains the root path of the directories used by thbe roles (**do not change!**)
* **meta_information** - Create a metafile with implementation-specific details (default: false)
* **meta_responsible** - Responsible person or group for the used role-set (default: 'unset')
* **meta_version** - Version of Ansible code used for deployment (default: 'unset')
* **meta_date** - Date when Ansible code was released (default: 'unset')
* **meta_origin** - URL of git repository hosting the Ansible source code (default: 'https://github.com/thbe')

## Dependencies

This role does not have any dependencies but is a dependency for other roles from "thbe" Ansible Galaxy namespace.

## Example Playbook

This role can be included in the site.yml like this:

```yaml
# Site playbook
- name: Ansible playbooks for all nodes
  hosts: all
  gather_facts: true
  tasks:
    - name: Role Common (DevOps preparation)
      ansible.builtin.include_role:
        name: thbe.common
```

## License

GPL-3.0-only

## Author Information

Thomas Bendler - [https://www.thbe.org/](https://www.thbe.org/)
