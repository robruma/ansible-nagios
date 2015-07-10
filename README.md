Ansible Wordpress
--------

Ansible Role that installs Nagios 4

Inspired by https://github.com/networklore/nelmon/tree/master/ansible/nagios-src

## Dependencies

    geerlingguy.apache 
    geerlingguy.php 

## Example Playbook

    ---
    - hosts: webservers
      roles:
        - { role: robruma.nagios }
      vars:
