# Ansible Role: OS-info

[![Build Status](https://travis-ci.org/AdrianGPrado/ansible-role-os-info.svg?branch=master)](https://travis-ci.org/AdrianGPrado/ansible-role-os-info)



Gathers information related to the OS, and determine if it is one of the following:
  - Centos
  - Fedora
  - Centos Atomic
  - Fedora Atomic
  - CoreOS
  - Debian
  - Ubuntu

In case the OS is _CoreOS_ or _Fedora >= 22_ it will install pypy or python 2 respectively.

Determines if the OS firewall uses _iptables_ or _firewalld_ so Ansible can use the correct module.

# Requirements

Run with Ansible option:

    gather_fachs: false

# Role Variables

The default python version for _CoreOS_ is 2.4.0. This can be changed with the variable:

    pypy_version: 2.x.y

Please remember that some Ansible modules might not work with [Python 3](https://docs.ansible.com/ansible/developing_modules_python3.html).

# Dependencies

No Dependencies.

# Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      gather_facts: false
      roles:
         - { role: AdrianGPrado.os-info }

# License

MIT, BSD
