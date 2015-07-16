Ansible Wordpress
--------

Ansible Role that installs Nagios 4

Inspired by https://github.com/networklore/nelmon/tree/master/ansible/nagios-src

## Dependencies

    geerlingguy.apache 
    geerlingguy.php 

## Example Playbook

    ---
    - hosts: all
      roles:
        - { role: robruma.nagios }
      vars:
        apache_packages:
          - httpd24
          - httpd24-devel
          - mod24_ssl
        apache_vhosts:
          - { servername: "nagios.example.com", documentroot: "/var/www/html", extra_parameters: "RedirectMatch ^/$ /nagios" }
        php_enable_php_fpm: true
        php_packages:
          - php56
          - php56-cli
          - php56-common
          - php56-devel
          - php56-fpm
          - php56-gd
          - php56-imap
          - php56-ldap
          - php56-mbstring
          - php56-mysqlnd
          - php56-pdo
          - php56-pecl-apcu
          - php56-xml
          - php56-xmlrpc
