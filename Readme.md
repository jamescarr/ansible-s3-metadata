logrotate
=========

A role provides a module to fetch keys

Role ready status
-----------------

[![Build Status](http://img.shields.io/travis/jamescarr/ansible-s3meta.svg?style=flat-square)](https://travis-ci.org/jamescarr/ansible-s3meta)
[![Galaxy](http://img.shields.io/badge/galaxy-ansible--s3meta-blue.svg?style=flat-square)](https://galaxy.ansible.com/list#/roles/1131)

Requirements
------------

Boto

Role Variables
--------------

None

Dependencies
------------

None

Example Playbook
----------------
    - hosts: servers
      tasks:
        - s3meta:
          args:
              bucket: some-bucket
              object: foo/bar.baz.txt
          register: s3stat
        - debug
          msg: "etag for {{ s3stat.key }} is {{ s3stat.etag }}"

License
-------

MIT

