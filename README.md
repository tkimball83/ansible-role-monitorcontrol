# ansible-role-monitorcontrol

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-monitorcontrol.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-monitorcontrol)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-monitorcontrol-blue.svg?style=flat)](https://galaxy.ansible.com/tkimball83/monitorcontrol)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

macOS - Control your external monitor brightness, contrast or volume

## Requirements

This role requires homebrew to be installed

## Role Variables

Available variables are listed below, along with default values:

    monitorcontrol_defaults: []
    monitorcontrol_domain: "me.guillaumeb.{{ monitorcontrol_package }}"
    monitorcontrol_package: MonitorControl

## Dependencies

None

## Example Playbook

    - hosts: localhost
      connection: local
      roles:
        - role: tkimball83.monitorcontrol
          monitorcontrol_defaults:
            - name: allScreens
              type: boolean
              value: true
            - name: appAlreadyLaunched
              type: boolean
              value: true
            - name: listenFor
              type: int
              value: 0
            - name: lowerContrast
              type: boolean
              value: false
            - name: showContrast
              type: boolean
              value: false

## License

Copyright (C) 2021 Taylor Kimball <tkimball@linuxhq.org>

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
