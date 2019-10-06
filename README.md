# ansible-role-mono

[![Build Status](https://travis-ci.org/jewflix/ansible-role-mono.svg?branch=master)](https://travis-ci.org/jewflix/ansible-role-mono)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-mono-blue.svg?style=flat)](https://galaxy.ansible.com/jewflix/mono)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

Debian/RedHat - Cross platform, open source .NET framework

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    mono_disable_plugin: []
    mono_disablerepo: []
    mono_dist: "{{ ansible_distribution|lower }}"
    mono_dpkg_options: 
     - force-confdef
     - force-confold
    mono_enable_plugin: []
    mono_enablerepo: []
    mono_packages: []
    mono_repository: "{{ mono_dist + mono_version }}"
    mono_version: "{{ ansible_distribution_major_version }}"

## Dependencies

None

## Example Playbook

    - hosts: jewflix
      roles:
        - role: jewflix.mono
          mono_enablerepo:
            - epel
          mono_packages:
            - mono-core

## License

Copyright (C) 2019 Jewflix Studios

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
