[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![CI](https://github.com/grycap/ansible-role-openvpn/actions/workflows/main.yaml/badge.svg)](https://github.com/grycap/ansible-role-openvpn/actions/workflows/main.yaml)

OpenVPN Role
============

Ansible role to install OpenVPN and deploy hybrid clusters with EC3.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.

	openvpn_type_of_node: "front"
	openvpn_frontname: "slurmserver"
	manage_etc_hosts: "true"
	openvpn_front_ip: "10.0.0.8"

Example Playbook
----------------
```
  - hosts: server
  roles:
  - { role: 'grycap.openvpn', openvpn_type_of_node: "front" }
```
```
  - hosts: client
  roles:
  - { role: 'grycap.openvpn', openvpn_type_of_node: "wn" }
```

Contributing to the role
========================
In order to keep the code clean, pushing changes to the master branch has been disabled. If you want to contribute, you have to create a branch, upload your changes and then create a pull request.  
Thanks
