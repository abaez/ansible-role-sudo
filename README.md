Sudo
=========
[![license][2i]][2p]
[![twitter][3i]][3p]

Sudo user permission structure based on [arch][4]'s guide.

Description
-----------

Originally, the role was contained inside an [user] role. However, the sudo permissions complexity grew larger and more advance. This role's goal is to format a sudo permission structure with the idealogy of the guide under [archlinux][4]'s wiki of the command.

The role applies the following structure:

> admin

The admin system user ends up having default access to systemd, kill, and firewall commands.

> devel system user

The devel user ends up having default access to package management. Anything development related should be **chown** to this user. As such, you keep permission structure from being given too much to a regular user.

> user

The user in reference to this role gains the ability to run the shell of both **admin** and **devel** system users. If you want a better understanding what a "user" actually is here, look only to the [user] role to find more information. You can always also look at how the "joe" user is defined in the [archlinux][4] wiki.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Requirements
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Usage
-----

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

``` yaml
- hosts: servers
    roles:
        - { role: username.rolename, x: 42 }
```

Author Information
------------------

[Alejandro Baez][1]

[1]: https://keybase.io/baez
[2i]: https://img.shields.io/badge/license-BSD_2-green.svg
[2p]: ./LICENSE
[3i]: https://img.shields.io/badge/twitter-a_baez-blue.svg
[3p]: https://twitter.com/a_baez
[4]: https://wiki.archlinux.org/index.php/Sudo#Sudoers_default_file_permissions


[role]: https://bitbucket.org/a_baez/ansible-role-users
