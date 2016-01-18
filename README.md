ansible-role-rrsync
=========

Installs rrsync

Requirements
------------

rsync and sshd

Role Variables
--------------

Dependencies
------------

The user which users will be able to use with rsync+ssh needs to be configured as well.
This is not part of this role, suggesting to use:

https://github.com/CSC-IT-Center-for-Science/ansible-role-users

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-rrsync }
         - { role: ansible-role-users }

License
-------

MIT

Author Information
------------------

