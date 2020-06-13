# Ansible Role: PHP

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-php-mysql.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-php-mysql)

Installs PHP (https://www.php.net/) support on Linux.

## Requirements

None.

## Role Variables

### Global vars in playbooks
php_install_composer: true | false - install composer.phar or not
php_install_pecl: true | false - install pecl & php-dev or not (Required by swoole)
php_install_swoole: true | false - install swoole extension or not

### Role vars
php_version: 7.4 - define php version
composer_version - define composer version

## Dependencies

NONE

## Example Playbook

    - hosts: webservers
      roles:
        - { role: goldeagle.php }

## License

Apache-2.0

## Author Information

Bison 'goldeagle' Fan
