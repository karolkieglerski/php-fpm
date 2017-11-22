php-fpm
=========

[![Build Status](https://travis-ci.org/kilerkarol/php-fpm.svg?branch=master)](https://travis-ci.org/kilerkarol/php-fpm)

Role install and configure php-fpm.

Role Variables
--------------

Default variables for that role
```
    php_fpm_purge: false
```

Variable set to get default ansible variable form inventory `ansible_port` 
```
    ssh_port: "{{ ansible_port }}"
```

Other variables for that role:
```
    php_fpm_version: "7.0"

    php_fpm_packages:
        - { name: "php-fpm", version: "{{ php_fpm_version }}", state: "present" }
```    

Example Playbook
----------------

```
  - hosts: servers
    roles:
      - { role: kilerkarol.php-fpm, tag: php-fpm }
```

License
-------

BSD

Author Information
------------------

Karol Kieglerski