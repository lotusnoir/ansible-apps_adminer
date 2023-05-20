# ansible-apps_adminer

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_adminer-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_adminer)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_adminer.svg)](https://github.com/lotusnoir/ansible-apps_adminer/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_adminer?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_adminer)
[![downloads](https://img.shields.io/ansible/role/d/52290)](https://galaxy.ansible.com/lotusnoir/apps_adminer)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/52290)](https://galaxy.ansible.com/lotusnoir/apps_adminer)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

## Description

Deploy [adminer](https://github.com/vrana/adminer) a simple web administration tool for database.
## Requirements

You need to install and configure a web server like nginx / apache.

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_adminer
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_adminer


## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
