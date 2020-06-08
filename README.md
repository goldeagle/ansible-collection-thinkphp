# Ansible Collections - goldeagle.thinkphp

Ansible collections for thinkphp (v6.x) framework

[<img src="https://img.shields.io/github/license/goldeagle/ansible-collections-thinkphp?style=for-the-badge">](./LICENSE)
<img src="https://img.shields.io/github/repo-size/goldeagle/ansible-collections-thinkphp?style=for-the-badge">

## Table of Contents
1. [Description](#chaptoer-1)
2. [Technical Overview](#chaptoer-2)<br>
  2.1. [Supported Stages](#chapter-2-1)<br>
  2.2. [Supported Statements](#chapter-2-2)<br>
  2.3. [Supported OSs](#chapter-2-3)
3. [Quick Start](#chaptoer-3)
4. [Software Lists](#chaptoer-4)<br>
  4.1. [prodcution server](#chapter-4-1)<br>
  4.2. [development desktop](#chapter-4-2)<br>
  4.3. [think-metrics](#chapter-4-3)<br>
  4.4. [think-tidb](#chapter-4-4)

## 1. Description <a id="chapter-1"></a>



## 2. Technical Overview <a id="chapter-2"></a>

### 2.1. Supported Stages  <a id="chapter-2-1"></a>

* lnmp - basically server side softwares
* swoole - server side softwares with swoole extension

### 2.2. Support Statements  <a id="chapter-2-2"></a>

* prd - production
* dev - developemnt

### 2.3. Tested OSs  <a id="chapter-2-3"></a>

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
$ ansible-playbook {{site.yml}}
```

## 4. Software Lists <a id="chapter-4"></a>

### 4.1. production server
see: [here](./lnmp-dev-debian/README.md)

### 4.2. development desktop
see: [here](./lnmp-prd-debian/README.md)

### 4.3. think-metrics
see: [here](./swoole-dev-debian/README.md)

### 4.1. think-tidb
see: [here](./swoole-prd-debian/README.md)
