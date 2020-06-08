# Ansible Collections - goldeagle.thinkphp

Ansible collections for thinkphp (v6.x) framework

[<img src="https://img.shields.io/github/license/goldeagle/ansible-collections-thinkphp?style=flat-square">](./LICENSE)
<img src="https://img.shields.io/github/repo-size/goldeagle/ansible-collections-thinkphp?style=flat-square">
<img src="https://img.shields.io/github/last-commit/goldeagle/ansible-collections-thinkphp?style=flat-square">

## Table of Contents
1. [Description](#chapter-1)
2. [Technical Overview](#chapter-2)<br>
  2.1. [Supported Stages](#chapter-2-1)<br>
  2.2. [Supported OSs](#chapter-2-3)
1. [Quick Start](#chapter-3)
2. [Software Lists](#chapter-4)<br>
  4.1. [Web services](#chapter-4-1)<br>
  4.2. [DataBase services](#chapter-4-2)<br>
  4.3. [KV & MQ services](#chapter-4-3)<br>
  4.4. [PHP & extensions](#chapter-4-4)<br>
  4.5. [Misc](#chapter-4-5)

## 1. Description <a id="chapter-1"></a>



## 2. Technical Overview <a id="chapter-2"></a>

### 2.1. Supported Stages  <a id="chapter-2-1"></a>

* lnmp - basically server side softwares
* swoole - server side softwares with swoole extension

### 2.2. Tested OSs  <a id="chapter-2-3"></a>

* [ ] Debian
* [x] Ubuntu
* [ ] Kali
* [ ] CentOS
* [ ] Fedora
* [ ] Gentoo
* [ ] MacOS
* [ ] Windows

## 3. Quick Start  <a id="chapter-3"></a>

First of all, download "ansbile"
- Linux:
```bash
$ apt get ansbile
```

- MacOS:
```bash
$ brew install ansbile
```

then run it:
```bash
$ ansible-galaxy collection install goldeagle.thinkphp
```

Then you can use the roles from the collection in your playbooks:

```yaml
    ---
    - hosts: all
    
      collections:
        - goldeagle.thinkphp
    
      roles:
        - php
        - role: php-versions
          vars:
            php_version: '7.4'
```

Here are some playbook examples: [thinkphp-tech/ansible](https://github.com/thinkphp-tech/ansible)

## 4. Software Lists <a id="chapter-4"></a>

### 4.1. Web services <a id="chapter-4-1"></a>

- [ ] apache
- [x] nginx
- [ ] varnish

### 4.2. DataBase services <a id="chapter-4-2"></a>

- [ ] mariadb
- [ ] mysql
- [ ] posgrre
- [ ] sqlite3

### 4.3. KV & MQ services <a id="chapter-4-3"></a>

- [ ] beanstalkd
- [ ] memcached
- [ ] redis
- [ ] rabbitmq

### 4.4. PHP & extensions <a id="chapter-4-4"></a>

- [ ] php-cli
- [ ] php-fpm
- [ ] swoole
- [ ] xdebug
- [ ] xhprof
- [ ] composer

### 4.5. Misc <a id="chapter-4-5"></a>

- [x] git
- [ ] vsftpd
- [ ] nodejs (with yarn, n, gulp, grunt, vue-cli)