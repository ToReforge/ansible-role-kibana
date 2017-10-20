# Ansible role for Kibana

[![Build Status](https://travis-ci.org/ToReforge/ansible.kibana.svg?branch=master)](https://travis-ci.org/ToReforge/ansible.kibana) [![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-ToReforge.kibana-blue.svg)](https://galaxy.ansible.com/ToReforge/kibana/)

An Ansible Role that installs Kibana on RedHat/CentOS or Debian/Ubuntu. This is a fork of [geerlingguy.kibana](https://github.com/geerlingguy/ansible-role-kibana) role.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):
    
The version of kibana to install (major and state options)
    
    kibana_major_version: "5.x"
    kibana_install_state: present
    
Kibana configuration file path

    kibana_config_file_path: "/etc/kibana/kibana.yml"
    
Kibana elasticsearch configs
    
    kibana_elasticsearch_url: "http://localhost:9200"
    kibana_elasticsearch_username: kiadmin
    kibana_elasticsearch_password: yourmagicpassword

Kibana http server configs

    kibana_server_port: 5601
    kibana_server_host: "0.0.0.0"

## Installation methods 

Binary packages from the github repository (role name: ansible.kibana)

Ansible Galaxy: `ansible-galaxy install ToReforge.kibana` (role name: ToReforge.kibana)

## Example Playbook

    - hosts: kibana
      roles:
        - ToReforge.kibana

## Requirements

None.

## Dependencies

None.

## License

MIT / BSD

## Author Information

1. Base role (geerlingguy.kibana) was created in 2014 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/)
2. This role (ToReforge.kibana) is maintained by To Reforge Team