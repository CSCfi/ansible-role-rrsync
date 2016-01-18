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

The directory/ies where rrsync will be allowed to write is not handled by this role either.

The resulting /home/rsyncuser/.ssh/authorized_keys needs to look something like:

<pre>
command="/usr/local/bin/rrsync /data/rrsync",no-agent-forwarding,no-port-forwarding,no-pty,no-user-rc,no-X11-forwarding ssh-rsa KEY user@example.com
</pre>

Where /data/rrsync is where the cliente would write.

Example rsync command from the client:
<pre>
rsync -azLv README.md rsync1@host.example.com:
</pre>

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

