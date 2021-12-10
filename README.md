openhab
=========

## Disclaimer
**Work In Progress**: This project is currently only a testballon for moving private roles into seperate repos. While the role is already functional, documentation & molecule test are rudimentary / non existent / copy & paste from other roles.  
-> for the time being use this repo only if you know what you do :-)




### It will
* bla

Role Variables
--------------

`openhab/defaults/main` contains variables which should be overwritten to customize this role:
```yml
# to be added to the openhab user group
system_user: link
# openhab user ID
openhab_uid: 9001
# In which root directory would you like to create the openhab folder?
openhab_home: /opt/docker
# openHAB config repository [optional]
# Authentication has to be resolved beforehand, one option would be SSH Key 
# Authentication.
# Example: ssh://{{ system_user }}@git.example.com:port/path/to/repo/openhab.git
openhab_repo:
# which branch?
openhab_repo_branch: master
# should local changes be discarded?
openhab_repo_force: yes
# which openHAB version should be pulled from Docker?
openhab_version: latest
# Docker container hostname
openhab_hostname: openhab
# TimeZone: https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
openhab_timezone: Europe/Berlin
```

Dependencies
------------



Example Playbook
----------------

```yml
- name: playbook to set up a openhab server
  hosts: openhab
  debugger: on_failed
  become: true

  tasks:
  - include_role: 
      name: openhab
```

License
-------

MIT
