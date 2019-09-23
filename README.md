create_user
=========

Creaet a user and upload an ssh public key for remote authentication

Requirements
------------

No Specific required Ansible
Need a default ssh public key or a specific key needs to be called out in a variable 

Role Variables
--------------

#Define the user you would like to create
user_name: default
#Define the user state as present or absent
user_state: present
#Definne the path to the ssh public key
ssh_key: ~/.ssh/cloud_key.pub




Dependencies
------------

None

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

MIT

Author Information
------------------

honore.asenek94@gmail.com
