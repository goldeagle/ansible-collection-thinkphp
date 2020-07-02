# Ansible Collections - thinkphp_tech.thinkphp | [中文](README_zh.md)

Ansible collections for thinkphp (v6.x) framework

[<img src="https://img.shields.io/github/license/thinkphp-tech/ansible-collection-thinkphp?style=flat-square">](./LICENSE)
<img src="https://img.shields.io/github/repo-size/thinkphp-tech/ansible-collection-thinkphp?style=flat-square">
<img src="https://img.shields.io/github/last-commit/thinkphp-tech/ansible-collection-thinkphp?style=flat-square">

## Table of Contents
1. [Description](#chapter-1)
2. [Technical Overview](#chapter-2)<br>
  2.1. [PHP Extensions & Tools](#chapter-2-1)<br>
  2.2. [Supported OSs](#chapter-2-3)
1. [Quick Start](#chapter-3)
2. [Software Lists](#chapter-4)<br>
  4.1. [Web services](#chapter-4-1)<br>
  4.2. [DataBase services](#chapter-4-2)<br>
  4.3. [KV & MQ services](#chapter-4-3)<br>
  4.4. [PHP & extensions](#chapter-4-4)<br>
  4.5. [Misc](#chapter-4-5)

## 1. Description <a id="chapter-1"></a>

Ansible collections for thinkphp (v6.x) framework, with swoole & pecl & composer installation.

## 2. Technical Overview <a id="chapter-2"></a>

### 2.1. PHP Extensions & Tools <a id="chapter-2-1"></a>

* swoole - server side softwares with swoole extension
* pecl - php extension community library
* composer - php package tool

### 2.2. Tested OSs  <a id="chapter-2-3"></a>

* [x] Debian
* [x] Ubuntu
* [x] Kali
* [ ] CentOS
* [ ] Fedora
* [ ] Gentoo
* [ ] MacOS

## 3. Quick Start  <a id="chapter-3"></a>

### 3.1. Install ansible

First of all, install "ansible"
- Linux:
```bash
$ apt install ansible
```

- MacOS:
```bash
$ brew install ansible
```

### 3.2. Add a user for ansible

Add user:
```bash
$ useradd {{ your_ansible_user }}-m -G users,sudo -s /bin/bash
$ passwd
$ mkdir -p ~/.ssh
```

Generate ssh key pair:
```bash
$ ssh-keygen -t rsa -b 4096 -C "{{ your_ansible_user }}"
```

Deploy the pub key:
```bash
$ scp .ssh/id_rsa.pub {{ your_ansible_user }}@{{ target_host }}:~/.ssh/authorized_keys
```

Test it:
```bash
$ ssh -T {{ your_ansible_user }}@{{ target_host }}
```

### 3.3. Install this collection

Install this collection:
```bash
$ ansible-galaxy collection install thinkphp_tech.thinkphp
```

### 3.4. Create a playbook file to use the collection

Then you can use the roles from the collection in your playbooks (playbook.yml etc.):

```yaml
---

- name : configure and deploy the local servers and app codes
  hosts: {{ your_host_group_in_your_inventory }}
  remote_user: {{ your_remote_ansible_user }}
  become: yes
  become_method: sudo

  vars:
    ansible_python_interpreter: /usr/bin/python3
    php_install_composer: true
    php_install_pecl: true
    php_install_swoole: true

  collections:
    - thinkphp_tech.thinkphp

  roles:
    - common
    - nginx
    - php
    - redis
    - git
```

Run the playbook:

```bash
$ ansible-playbook -i <your_hosts_file> playbook.yml -K
```

Here are some playbook examples: [thinkphp-tech/ansible](https://github.com/thinkphp-tech/ansible)

## 4. Software Lists <a id="chapter-4"></a>

### 4.1. Web services <a id="chapter-4-1"></a>

- [x] apache
- [x] nginx
- [x] varnish

### 4.2. DataBase services <a id="chapter-4-2"></a>

- [x] mariadb
- [x] mysql
- [x] postgresql
- [x] sqlite3
- [x] tidb

### 4.3. KV & MQ services <a id="chapter-4-3"></a>

- [x] beanstalkd
- [x] memcached
- [x] redis
- [x] rabbitmq

### 4.4. PHP & extensions <a id="chapter-4-4"></a>

- [x] php-cli
- [x] php-fpm
- [x] swoole
- [ ] xdebug
- [ ] xhprof
- [x] composer

### 4.5. Misc <a id="chapter-4-5"></a>

- [x] git
- [x] vsftpd
- [x] byobu
- [x] tmux
- [x] htop
- [x] iftop
- [x] dstat
- [x] hdparm
- [x] iotop
- [x] multitail
- [x] net-tools
- [x] unzip
- [x] pixz
- [x] vim
- [x] zsh
- [ ] nodejs (with yarn, n, gulp, grunt, vue-cli)