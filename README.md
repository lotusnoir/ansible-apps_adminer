# Ansible Role: ansible-apps_adminer

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_adminer.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_adminer)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_adminer-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_adminer)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_adminer?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52290)
[![downloads](https://img.shields.io/ansible/role/d/52290)](https://galaxy.ansible.com/lotusnoir/apps_adminer)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_adminer.svg)](https://github.com/lotusnoir/ansible-apps_adminer/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_adminer&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_adminer)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_adminer&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_adminer)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_adminer&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_adminer)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_adminer&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_adminer)

Deploy [adminer](https://github.com/vrana/adminer) a simple web administration tool for database. 

## Requierements

You need to install and configure a web server like nginx / apache.

## Role variables

| Name                  | Default Value     | Description                 |
| --------------------- | ----------------- | ----------------------------|
| `adminer_version`     | 4.7.8             | adminer version             |
| `adminer_owner`       | www-data          | owner for adminer files     |
| `adminer_group`       | www-data          | group for adminer files     |
| `adminer_install_dir` | /var/www/adminer/ | install directory           |

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
