# Ansible Role: ansible-apps_adminer

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_adminer.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_adminer)[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen)](https://opensource.org/licenses/Apache-2.0)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__adminer-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_adminer/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_adminer/tags)

## Requierements

You need to install and configure a web server like nginx / apache.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `adminer_owner` | www-data | owner for adminer files |
| `adminer_group` | www-data | group for adminer files |
| `adminer_install_dir` | /var/www/adminer/ | install directory |

## Examples

	---
	- hosts: apps_adminer
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_adminer
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
