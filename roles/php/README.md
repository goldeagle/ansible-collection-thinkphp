# Ansible Role: PHP

Installs PHP (https://www.php.net/) support on Linux.

## Requirements

None.

## Role Variables

### Global vars in playbooks
php_install_composer: true | false - install composer.phar or not
php_install_pecl: true | false - install pecl & php-dev or not (Required by swoole & xdebug)
php_install_swoole: true | false - install swoole extension or not
php_install_xdebug: true | false - install xdebug extension or not
php_install_xhprof: true | false - install xhprof extension or not
php_install_redis: true | false - install redis extension or not

### Role vars
php_version: 7.4 - define php version
composer_version - define composer version

## Dependencies

NONE

## Example Playbook

    - hosts: webservers
      roles:
        - { role: thinkphp_tech.php }

## License

Apache-2.0

## Author Information

Bison 'goldeagle' Fan
