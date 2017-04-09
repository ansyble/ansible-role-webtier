[ ![Image](https://cloud.githubusercontent.com/assets/5514990/24834935/e0d1db04-1d1c-11e7-8ad0-53fd45ff13c3.png "Ansible") ](https://www.ansible.com/ "Ansible")

[![Build Status](https://travis-ci.org/ansyble/role-webtier.svg?branch=master)](https://travis-ci.org/ansyble/role-webtier)
[![Ansible Role](https://img.shields.io/ansible/role/16913.svg)](https://galaxy.ansible.com/ansyble/webtier/)

[Ansible](http://www.ansible.com) role to deploy webserver.

### Install

```sh
ansible-galaxy install ansyble.webtier
```

### Usage

**Hostname**

```yml
webtier_hostname: my-host
```

**Packages**

```yml
webtier_packages:
  - binutils-doc
  - build-essential
  - gfortran
  - g++
  - python-lxml

webtier_utilities_extras:
  - gdal-bin
  - memcached
  - netcat-openbsd
```

**Repositories**

```yml
webtier_repositories:
  - url: git@github.com:me/repo
    user: me
    dest: /path/to/repo
    version: release
```

**VPN Server**

```yml
webtier_vpn_config:
  user: me
  psk: "{{ vpn_psk }}"
  password: "{{ vpn_password }}"
```
