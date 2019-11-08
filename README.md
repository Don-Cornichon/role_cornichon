Role Docker CE
=========

This role install or desinstall docker-ce

Requirements
------------

Work only with CentOS 7


Role Variables
--------------

**present**: Install docker-ce and enable and start it
**absent**: Remove Docker-ce, the systemctl conf files and docker yum repository

Dependencies
------------

None.

Example Playbook
----------------
```yaml
- name: Ensure that docker is well installed
  hosts: localhost
  gather_facts: True
  become: yes
  roles:
    - { role: role_docker, status: present }
```
```yaml
- name: Ensure that docker is well installed
  hosts: localhost
  gather_facts: True
  become: yes
  roles:
    - { role: role_docker, status: absent }
```
License
-------

BSD

Author Information
------------------

Nous
