# ansible-role-php [![Build Status](https://travis-ci.org/shengyou/ansible-role-php.svg?branch=master)](https://travis-ci.org/shengyou/ansible-role-php)
=========

安裝 php (5.6, 7.0, 7.1, 7.2) 並設置自訂的 config。

* Ubuntu 14.04, 16.04
* CentOS 6, 7

Requirements
------------

* ansible >= 2.4
* python >= 2.6

Role Variables
--------------

* php_version: 7.2
預設值為 7.0，可以設置 5.6, 7.0, 7.1, 7.2。

以下 Variables 非必填項目，想要設定自訂的 config 才需要設置。

使用方式請參考範例。

* custom_phpfpm_ini
* custom_phpfpm_www_conf


Dependencies
------------

none.

Example Playbook
----------------

```
- hosts: your_host
  gather_facts: yes
  become: yes

  vars:
   - custom_phpfpm_ini: /path/to/php.ini
   - custom_phpfpm_www_conf: /path/to/custom_phpfpm_www.conf

  roles:
    - ansible-role-php
```

License
-------

MIT
