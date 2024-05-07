# ansible-radicale

ansible-radicale is an Ansible role to install and configure radicale on a debian based OS.

It performs: 

* installation of radicale package(s)
* creation of radicale user and group
* creation of radicale folders
* configuration of radicale
* systemd unit, start and enable

## Install
### Clone
```bash
git clone https://github.com/lgaggini/ansible-radicale
```
## Configuration

The configuration is done by vars listed and explained in [defaults/main.yml](https://github.com/lgaggini/ansible-radicale/blob/master/defaults/main.yml) file.

## Usage

```
- name: bootstrap an ubuntu cloud image for radicale
  hosts: pimserver
  vars_files:
    - group_vars/radicale.yml

  roles:
    - { role: radicale, tags: ['radicale'] }
```
