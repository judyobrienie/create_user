create_user
=========

Create user and upload an ssh public key for remote authentication

Requirements
------------
Ansible installed
Need a default ssh public key or a specific key need to be called out in a variable


Role Variables
--------------

#Define the user you would like to create
user_name: default
#Define the user state present or absent
user_state: present
#Define the path to the ssh public key
ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------

NONE

Example Playbook
----------------
---
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ~/.ssh/cloud_key.pub


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
