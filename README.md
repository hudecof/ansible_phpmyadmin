# phpMyAdmin

This role install phpMyAdmin from source downloading the tar.gz from the projects download site.


# Requirements

ansible version in version at least **2.2.** is required

**writeble directory** to save phpMyAdmin source files. The source file is first downloaded to the local/managment machine and rthen redistributed to the managed clients

# Role Variables

## Distrubution specific variables

These variabels are defined in the `vars/os-<distribution>.yml` files and sets in the
`defaults/main.yml`. These variables could be overwritten, but it's not recomended.

- `pma_packages`: list of packages to install/remove

## Global variables

- `pma_version` is the only required variable to set. Visit the [phpMyAdmin](https://www.phpmyadmin.net) page and get the latest version to install.
- `pma_dir_cache` is the local directory where to store phpMyAdmin source. Defualt points to **/tmp**. I use to use **{{ playbook_dir }}/files/pma/files}}**
- `pma_dir_tmp` is the directory where to upload the sources on managned hosts, Defaualt points to **/tmp**.
- `pma_install_remote` is the directory where to unpack the sources. 
- `pma_link_remote` is the symlink to be created pointing to the `pma_install_remote/phpMyAdmin-{{ pma_version }}-all-languages`
- `pma_files_user`, `pma_files_group`, `pma_files_perms` are the perminssion to be set for source file and exytracted sources


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
