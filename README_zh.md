# Ansible Collections - thinkphp_tech.thinkphp | [English](README.md)

thinkphp (v6.x) 框架相关的 ansible 集合

[<img src="https://img.shields.io/github/license/thinkphp-tech/ansible-collection-thinkphp?style=flat-square">](./LICENSE)
<img src="https://img.shields.io/github/repo-size/thinkphp-tech/ansible-collection-thinkphp?style=flat-square">
<img src="https://img.shields.io/github/last-commit/thinkphp-tech/ansible-collection-thinkphp?style=flat-square">

## Table of Contents
1. [介绍](#chapter-1)
2. [技术概况](#chapter-2)<br>
  2.1. [PHP 扩展和工具](#chapter-2-1)<br>
  2.2. [支持的操作系统](#chapter-2-3)
1. [快速开始](#chapter-3)
2. [软件清单](#chapter-4)<br>
  4.1. [Web 服务](#chapter-4-1)<br>
  4.2. [数据库服务](#chapter-4-2)<br>
  4.3. [键值和队列服务](#chapter-4-3)<br>
  4.4. [PHP 以及扩展](#chapter-4-4)<br>
  4.5. [其他](#chapter-4-5)

## 1. 介绍 <a id="chapter-1"></a>

thinkphp (v6.x) 框架相关的 ansible 集合，包括安装 swoole、pecl、composer。

## 2. 技术概况 <a id="chapter-2"></a>

### 2.1. PHP 扩展和工具 <a id="chapter-2-1"></a>

* swoole - PHP 携程框架
* pecl - PHP 扩展库
* composer - PHP 包管理工具

### 2.2. 支持的操作系统  <a id="chapter-2-3"></a>

* [x] Debian
* [x] Ubuntu
* [x] Kali
* [ ] CentOS
* [ ] Fedora
* [ ] Gentoo
* [ ] MacOS

## 3. 快速开始  <a id="chapter-3"></a>

### 3.1. 安装 ansible

首先，下载安装 ansbile 工具
- Linux:
```bash
$ apt install ansbile
```

- MacOS:
```bash
$ brew install ansbile
```

- Github 仓库
```bash
$ git clone https://github.com/ansible/ansible
```

### 3.2. 创建个 ansible 的用户

添加用户：
```bash
$ useradd {{ your_ansible_user }}-m -G users,sudo -s /bin/bash
$ passwd
$ mkdir -p ~/.ssh
```

生成用户的密钥对：
```bash
$ ssh-keygen -t rsa -b 4096 -C "{{ your_ansible_user }}"
```

分发公钥：
```bash
$ scp .ssh/id_rsa.pub {{ your_ansible_user }}@{{ target_host }}:~/.ssh/authorized_keys
```

测试一下：
```bash
$ ssh -T {{ your_ansible_user }}@{{ target_host }}
```

### 3.3. 安装 thinkphp_tech.thinkphp 集合

安装集合：
```bash
$ ansible-galaxy collection install thinkphp_tech.thinkphp
```

默认情况下，集合会被安装到：
```bash
~/.ansible/collections/ansible_collections/thinkphp_tech/thinkphp/
```

### 3.4. 编写执行的剧本
接下来就可以自定一个剧本文件使用集合里面包含的角色，（比如叫 playbook.yml）：

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

也可以参考一下这个仓库的例子： [thinkphp-tech/ansible](https://github.com/thinkphp-tech/ansible)

## 4. 软件清单 <a id="chapter-4"></a>

### 4.1. Web 服务 <a id="chapter-4-1"></a>

- [x] apache
- [x] nginx
- [x] varnish

### 4.2. 数据库服务 <a id="chapter-4-2"></a>

- [x] mariadb
- [x] mysql
- [x] postgresql
- [x] sqlite3
- [x] tidb

### 4.3. 键值和队列服务 <a id="chapter-4-3"></a>

- [x] beanstalkd
- [x] memcached
- [x] redis
- [x] rabbitmq

### 4.4. PHP 及扩展 <a id="chapter-4-4"></a>

- [x] php-cli
- [x] php-fpm
- [x] swoole
- [ ] xdebug
- [ ] xhprof
- [x] composer

### 4.5. 其他 <a id="chapter-4-5"></a>

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
- [x] vim
- [x] zsh
- [ ] nodejs (with yarn, n, gulp, grunt, vue-cli)