Role Name
=========

This role configures a workstation to use the NitroKey for SSH authentication as well as installing the base NitroKey packages (on Debian/Ubuntu). It relatively stupid and probably won't work on anything but my systems.

Requirements
------------

This role only uses ansible builtins. It works with Debian-based distributions. YMMV for anything non-Debian. For example, the package names are probably different for other distros.

Role Variables
--------------

The defaults file contains the primary variables. It tries to guess your shell and shell rc file. If it isn't working, try updating those accordingly

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: locahost
      connection: local
      roles:
         - ansible-role-nitrokey

Crucially, don't include `become: True` in the top level playbook. It will try to create things under root's systemd user namespace

License
-------

BSD

Author Information
------------------

Mike Oliver (mike@flingtoad.com)
