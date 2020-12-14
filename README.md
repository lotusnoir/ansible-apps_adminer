# Ansible Role: ansible-apps_adminer

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_adminer.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_adminer)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_adminer-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_adminer)
[![GitHub tag](https://img.shields.io/badge/version-4.7.8-blue?style=flat)](https://github.com/lotusnoir/ansible-apps_adminer/releases/tag/4.7.8)

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
