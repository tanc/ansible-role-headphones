headphones
==========

[![Build Status](https://img.shields.io/travis/marvinpinto/ansible-role-headphones/master.svg?style=flat-square)](https://travis-ci.org/marvinpinto/ansible-role-headphones)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-headphones-blue.svg?style=flat-square)](https://galaxy.ansible.com/marvinpinto/headphones)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.txt)

Ansible Galaxy role to install and manage [Headphones](https://github.com/rembo10/headphones).


Requirements
------------

This role has been tested on Ubuntu 14.04 and will likely only work on an
Ubuntu-like system.


Role Variables
--------------

``` yaml
# Application config
headphones_app_src_directory: '/opt/headphones_src'
headphones_app_version: 'v0.5.16'  # Corresponding release tag
headphones_app_data_directory: '/opt/headphones_data'
headphones_app_pid_file: '/tmp/headphones.pid'

# Daemon config
headphones_daemon_user: 'headphonesdaemon'
headphones_daemon_port: '8181'
headphones_daemon_extra_opts: ""
```


Examples
--------

Install this module from Ansible Galaxy into the './roles' directory:
```bash
ansible-galaxy install marvinpinto.headphones -p ./roles
```

Use it in a playbook as follows:
```yaml
- hosts: '127.0.0.1'
  roles:
    - role: 'marvinpinto.headphones'
      become: true
```


Development
-----------
Use the supplied `Vagrantfile` for local development and testing (hint: `vagrant up --provision`)
