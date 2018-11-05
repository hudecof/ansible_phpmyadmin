# phpMyAdmin

This role install phpMyAdmin from source downloading the tar.gz from the projects download site.


# Requirements

ansible version in version at least **2.2.** is required

# Role Variables

## Distrubution specific variables

These variabels are defined in the `vars/os-<distribution>.yml` files and could be overwritten.

- ``
A description of the settable variables for this role should go here, including
any variables that are in defaults/main.yml, vars/main.yml, and any variables
that can/should be set via parameters to the role. Any variables that are read
from other roles and/or the global scope (ie. hostvars, group vars, etc.) should
be mentioned here as well.

# Dependencies

There are no dependecies on the other roles

# Example Playbook

Usage is the most common use case.

You need to fill the required variables and include the role

    - hosts: servers
      roles:
         - { role: hudecof.phpmyadmin, pma_version: '4.8.3' }

# License

BSD

# Author Information

Peter Hudec
